* review structure as compared to midas data or others
** look at xml renderings...

** correct url   -- currently prefix is off. Can I fix that? -edit file

** numbering of nodes - some have numbers. some don't. can I fix that? - do I need this?

* review other structures of inheritance.
** regimens being subclass of parts pr phases
** others?


populate definitions
  - phases onwards.


- populate the induction, intensification, etc. from  AAML with meds and administration.
- is there any way to avoid explosuion of classes with medication adminsitration?

- try to figure out how to best model the ordering of regimens
- remove redundant information?
- continue modeling aaml https://hemonc.org/wiki/Acute_myeloid_leukemia,_pediatric#COG_AAML1031_arm_C_.28FLT3.2FITD.2B.29




DONE
* add names for protocols and regimens
   name property
* haspublication
* publication - has DOI
* look at duration property - subpropoerties hasduration days
  has duration weeks.
* can i find an example of a course with cycles?
* mail jeremy
  dropbox/list of questoins ?
  - definitions
  - troble running code
  - reviewing which is the protocol/course/regimen
  - list of phases?
- treatment context -hasLine, has Phase-
- add a diagnosis - associated with a protocol


add subclasses of medication administration for local
    	       anticancer
	supportive
	

- treatment context -hasLine, has Phase-

If it is intended to be given once, but might be repeated, it is a course. A regimen that occurs in isolation is stand-alone,

-treatmentList hasTreatment someTreatment (exactly1)
 treatmentList hasPhase somePhase (exactly 1)
 protocol has treatment list
model regiment with types of medication adminsistration.
      anticancer
      local
      supportive
      treatment modality `

* regimen
* phase
* protocol  definition
* line definition* phase, line, protocol, regimen relations

- review of definitions of regimen, protocol, line, intent...

  flesh out line

-mail jeremy
      are phasess asoociated with reigmens? Lines? If we downplay protocol, where do phases fit itn ?
        depreate treatment contesxt
  *** notes on open questions
  **heck status in github - commit and backup
  * check haspriortherapy - domain and range?
  * add Line
  
  
  - remove medicaiton administration.
  - put lists in regimen for treatment
  - protocol as ordered list?
-make treatment list refer to these
- add subclasses
- clean names of phases.
- add study protocol with DOI.
https://www.researchgate.net/publication/351037551_A_Practical_Guide_to_Building_OWL_Ontologies_Using_Protege_55_and_Plugins - diagnsois  name and coee? 
clean up definitions


- order phases  https://www.cancerresearchuk.org/about-cancer/acute-lymphoblastic-leukaemia-all/treatment/phases
Should specific phases (Inductino, etc. be individuals? Look at pizza?
       yes. add these
       	  *  	pre-phase/pre-induction    -induction subsequent
		*induction  - consolidation  subsequent
		*consolidation - intensification
		*intensification - maintenance
		*maintenance
		interim_maintenance
		adjuvant   - maintenance
		neoadjuvant -definitive
		definitive -adjuvant
		delayed intensification
		continuation
		salvage
		upfrontinductiontherapy


* work on ordering of phases?
**How do i say that induction may be followed by either intensification or consoolidation?

* add cancer, cns, and locall subytypes of administration to medication administartion
* add these administrations to regiemn
- move away from medication categories - all medications should be in one list. we will use medicationadministration catgories to indicate how each drug is used in a given protocol.
- what about the instances of AAML_1031_ARMC_C , etc.?  - yes. remove these instances
- should we remove the explicit instances of medication administration? yes
- run pellet and look at reasoning errors.a
- remove instances
