Deuxiéme programmme de rattrapage 
define buffer cermvt for cermvt.

for each  cermvt where
     cermvt.codsoc     = "0000"
     and cermvt.e-codmag     = "7002"
     and cermvt.campagne   = "2016"
     and cermvt.codmag   = "7180"
/*     and substring(cermvt.no-ticket , 1 , 8 )  = substring( cermvt.ticket-trs , 1 , 8 )
*/
     and  cermvt.no-ticket matches  "*000111070*"
     and cermvt.codmvt     = "CeT"
   /*  and cermvt.codmag     <> "ROUL"
     and cermvt.pds-norme  = cermvt.pds-norme
      and cermvt.statut  = cermvt.statut
     
      and cermvt.alpha-1   <> ""
      */
   /* and chrono = 1673 */ 
      /* no-lock
      */
       :
      
      displ  cermvt.codmag format "xxxx"  cermvt.codcer  format "xxxx"
      cermvt.datsai  cermvt.pds-norme  (total)
      
         cermvt.statut
          cermvt.e-codmag format "xxxx"  cermvt.chrono cermvt.chrono-ini cermvt.no-ticket cermvt.ticket-trs cermvt.alpha-1 cermvt.datcre cermvt.opecre cermvt.pds-norm cermvt.statut cermvt.heucre         
           .
           
      /* codsoc = "del-0000" . 
        */
