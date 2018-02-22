# Social-Network-Analysis

library("intergraph")
library("sand")

path<- "C:/Users/sharvana/Documents/CSC495/Project/Political Books - Part 1"
setwd(path)

bkEdge <- read.csv("Edges.csv",header = T, sep=',', stringsAsFactors = F)
bkAttr <- read.csv("Attr.csv", header = T, sep = ',',stringsAsFactors = F)


gr <- graph.data.frame(bkEdge,directed = F,vertices = bkAttr)
bkGraph <- graph_from_data_frame(edg.df, directed = FALSE, vertices = nod.df)
plot(bkGraph)

duplicated(bkEdge) == TRUE
duplicated(bkAttr) == TRUE

edg.df[duplicated(bkEdge)]
nod.df[duplicated(bkAttr)]

