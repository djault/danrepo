/* contrôle des transferts entrées */ 
for each cermvt where cermvt.codsoc = "0000"
and cermvt.campagne = "2016"
and cermvt.typbon = 3
and cermvt.codmvt = "CET"
 and cermvt.alpha-1 <> ""

and cermvt.codmag = "0658"
 and cermvt.transp = "998"

 :
 displ cermvt.codmag cermvt.codmvt cermvt.datsai cermvt.no-ticket  .
 end.
