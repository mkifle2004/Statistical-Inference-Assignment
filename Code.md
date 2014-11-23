For 1000 Sample

> library(ggplot2)
> N<-40
> lambda=0.2
> Simulation_number<-1000
> exp_set<-matrix(rexp(N*Simulation_number, lambda), Simulation_number)
> Theoretical_Mean<-1/lambda
> Row_mean<-apply(exp_set, 1, mean)
> Actual_Mean<-mean(Row_mean)
> Theoretical_SD<-(Theoretical_Mean*(1/sqrt(N)))
> Actual_SD<-sd(Row_mean)
> Theorertical_var<-Theoretical_SD
> Actual_var<-var(Row_mean)
> Row_mean_DF<-data.frame(Row_mean)


> Exp_plot<-ggplot(Row_mean_DF, aes(x=Row_mean))
> Exp_plot<-Exp_plot+geom_histogram(binwidth = lambda,fill="green",color="black",aes(y = ..density..))
> Exp_plot<-Exp_plot + labs(title="Exponential Distribution of 40 samples", x="Mean", y="Density")
> Exp_plot<-Exp_plot + geom_vline(xintercept=Actual_Mean,size=1.0, color="black")
> exp_plot<-Exp_plot + stat_function(fun=dnorm,args=list(mean=Actual_Mean, sd=Actual_SD),color = "blue", size = 1.0)
> Exp_plot<-exp_plot + geom_vline(xintercept=Theoretical_Mean,size=1.0,color="yellow",linetype = "longdash")
> Exp_plot<-Exp_plot + stat_function(fun=dnorm,args=list(mean= Theoretical_Mean, sd=Theoretical_SD),color = "red", size = 1.0)
> Exp_plot


For 2000 Sample

> library(ggplot2)
> N<-40
> lambda=0.2
> Simulation_number<-2000
> exp_set<-matrix(rexp(N*Simulation_number, lambda), Simulation_number)
> Theoretical_Mean<-1/lambda
> Row_mean<-apply(exp_set, 1, mean)
>  Actual_Mean<-mean(Row_mean)
> Theoretical_SD<-(Theoretical_Mean*(1/sqrt(N)))
> Actual_SD<-sd(Row_mean)
> Theorertical_var<-Theoretical_SD
> Actual_var<-var(Row_mean)
> Row_mean_DF<-data.frame(Row_mean)
>  Exp_plot<-ggplot(Row_mean_DF, aes(x=Row_mean))
> Exp_plot<-Exp_plot+geom_histogram(binwidth = lambda,fill="green",color="black",aes(y = ..density..))
> Exp_plot<-Exp_plot + labs(title="Exponential Distribution of 40 samples", x="Mean", y="Density")
> Exp_plot<-Exp_plot + geom_vline(xintercept=Actual_Mean,size=1.0, color="black")
> exp_plot<-Exp_plot + stat_function(fun=dnorm,args=list(mean=Actual_Mean, sd=Actual_SD),color = "blue", size = 1.0)
> Exp_plot<-exp_plot + geom_vline(xintercept=Theoretical_Mean,size=1.0,color="yellow",linetype = "longdash")
> Exp_plot<-Exp_plot + stat_function(fun=dnorm,args=list(mean= Theoretical_Mean, sd=Theoretical_SD),color = "red", size = 1.0)
> Exp_plot
