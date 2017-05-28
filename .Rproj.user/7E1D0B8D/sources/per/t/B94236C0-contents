mydata <- function  (d1){
  dataF <- data.frame(Temps=integer(),
                     Teau=double(),
                     Tis=double(),
                     Tamb=double(),
                     Tcr=double())
  j <- 0
  for(i in d1$Temps) 
  {
    if (i%%100==0){ 
      tmp <- subset(d1, d1$Temps >= j & d1$Temps <= i)
      new <- c(i, mean(tmp$Teau), mean(tmp$Tis), mean(tmp$Tamb), mean(tmp$Tcr))
      dataF <- rbind(dataF, new)
      j <- i 
      #print(new)
    }
  }
  colnames(dataF) <- c("Temps","Teau","Tis","Tamb","Tcr")
  #head(dataF)
  return (dataF)
}
