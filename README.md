welcome
=======


	pollutantmean <- function(directory,pollutant,id) {

    new = paste("C:/Projects/R/",directory,sep="")
    files=list.files(new,full.names=TRUE)
    data=data.frame()

	for(i in id){
	data=rbind(data,read.csv(files[i]))
  	}

	ifelse(pollutant=="nitrate",mean(data$nitrate,na.rm=TRUE), 
                                  mean(data$sulfate,na.rm=TRUE))

	}
