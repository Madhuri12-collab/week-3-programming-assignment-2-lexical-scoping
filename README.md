## Put comments here that give an overall description of what your

## functions do



## Write a short comment describing this function



makeCachematrix <- function(x=matrix()){

inv<-NULL

set<-function(){



x<<-y

inv<<-NULL

}

get<-function(){x}

setInverse<-function(Inverse){inv<<-inverse}

getInverse<-function(){inv}

list(set=set, get=get, setInverse=setInverse, getInverse=getInverse)

}



cacheSolve<-function(x, ...){



inv<- x$getInverse()

if(is.null(inv)){



message("getting cached data")

return(inv)



}

mat<-x$get()

inv<-solve(mat, ...)

x$setInv

erse(inv)

inv

}



