### SOLUTIE INFORMATICA PENTRU ANALIZA PROFILULUI SI COMPORTAMENTULUI BANCAR

# Cuprins 
* [Introducere](#Introducere)  
<a name="Introducere"/>

* [Date](#Date)  
<a name="Date"/>

-----

# Introducere

Conform [Big Data Analytics for Improved Risk Management and Customer Segregation in Banking Applications](https://irojournals.com/iroismac/V3/I3/05.pdf)

> As most of the data generated in internet banking and ATM transactions are unstructured accounting around for 2.5 quintillion bytes useful for fraud detection, risk management, and customer satisfaction, the use of trending Big Data Analytics methodology can be used to tackle the challenges and competition among banks

datele sunt majoritar nestructurate in acest domeniu.

-----

Pentru a putea contura comportamentul clienților și pentru a putea face predicții ar trebui structurate datele nestructurate. Există diferite procese care pot face ca datele să fie structurate. 
De exemplu:
* [ETL](https://www.sciencedirect.com/science/article/pii/S131915781100019X/?imgSel=Y)
> Extraction–transformation–loading (ETL) tools are pieces of software responsible for the extraction of data from several sources, its cleansing, customization, reformatting, integration, and insertion into a data warehouse.
![image](https://user-images.githubusercontent.com/73749739/219964652-f9c5969a-4237-438c-8bd3-b8658a003144.png)

* [ELT](https://www.sciencedirect.com/science/article/pii/S2212017314002424)
> Extract, Load and Transform (ELT), in comparison with ETL, has four following advantages:(1) flexibility in adding new data sources (EL part); (2) aggregation can be applied multiple times on same raw data; (3) Transformation process can be re -adopted, even on legacy data; (4) speed -up process of implementation. It allows firstly extracting and loading data, and then apply on demand transformation according to the business need

![image](https://user-images.githubusercontent.com/73749739/219965199-4989c33d-d193-4b2d-be05-99b54737b60c.png)

* [ELTA](https://www.sciencedirect.com/science/article/pii/S2212017314002424)
> ELTA stands for Extract, Load, Transform and Analyse. The authors define the ELTA term as follows: a process called Extract enables data extraction from the heterogeneous sources in heterogeneous formats (transactional data, machine generated data etc.); process Load provides ability to store data in side storage s ystem; process named Transform provides ability to transform data from raw state (a) on demand and (b) according to the needs of decision making process; Analyse phase makes business users efficiently utilize preprocessed data to understand enterprise behavior through analysis

![image](https://user-images.githubusercontent.com/73749739/219965282-ee66a919-7cc5-487a-baf9-95f8e7dcd730.png)

-----

Băncile folosesc acum datele pentru a anticipa nevoile clienților.
> "in order for the Bank to act on them in a timely manner with an adequate offer of products, services and recommendations"
De exemplu:


**ERSTE**(https://www.erstebank.hr/en/about-us/Information-on-data-processing)
>(i) the creation of special offers of/recommendations for products, services and possibilities of their use (personalized marketing), in order for you to manage your finances more efficiently as the client. For this purpose, the Bank shall process the data based on the product or service usage, such as: the data on the amount, frequency, transaction type and place, bank balance, bank account card usage, and the data on the frequency of visits to the branch office, in order to be able to inform you about the benefits and possibilities of using your bank account, online*2 banking services or a standing order, the possibilities of contracting a saving product etc. The aforementioned data processing may include the creation of your profile based on the analysis of your personal interests, conduct and location. **Such profiling is aimed at anticipating your needs in order for the Bank to act on them in a timely manner with an adequate offer of products, services and recommendations** 

![image](https://user-images.githubusercontent.com/73749739/219967007-f70481fd-d584-4b79-b36d-6db16e8abd8c.png)

-----

Conform [dataideology](https://www.dataideology.com/the-benefits-of-data-warehousing-in-finance/)
>Data warehousing is essential in the financial sector because of the large amount of data that needs to be processed and analyzed. Financial institutions generate a vast amount of data from their day-to-day operations, which can be extremely valuable if used correctly.

Astfel, putem spune ca data warehousin a devenit un standard pentru sectorul financiar

-----

# Date

Prin data warehousing, datele sunt stocate in data marts, reprezentand subseturi mari de date pentru a indeplini anumite nevoi ale unei anumite unitati business sau a unui grup.

Pentru implementarea acestei lucrari, data marts reprezinta tabelele SQL in care informatiile folosite despre clienti sunt grupate astfel:

        
	A. DEMOGRAFICE
* 	VARSTA	-	Varsta clientului
* 	DOMICILIU_ORAS	-	Orasul domiciliului
* 	DOMICILIU_JUDET	-	Judetul domiciliului
* 	DOMICILIU_TARA	-	Tara domiciliului
* 	DOMICILIU_REGIUNE	-	Regiunea domiciliului
* 	DOMICILIU_ZONA	-	Zona domiciliului clientului ( Urban/Rural)
* 	OCUPATIE	-	Ocupatia clientului
* 	EDUCATIE	-	Educatia clientului
* 	GEN	-	Genul clientului
* 	STARE_CIVILA	-	Starea civila a clientului
* 	NATIONALITATE	-	Nationalitatea clientului
* 	CETATENIE	-	Cetatenia clientului
* 	NR_COPII	-	Numarul de copii pe care ii are clientului
* 	VECHIME	-	Vechimea clientului in banca
	
	
	B. VENITURI		
* 	VENIT_SOCIAL	-	Valoare venit din ajutor social 
* 	VENIT_SOCIAL_DATA	-	Data incasarii venitului din ajutor social 
* 	NR_VENIT_SOCIAL		- 	De cate ori a primit venit din ajutor social 
* 	VENIT_PENSIE	-	Valoare venit din pensii 
* 	VENIT_PENSIE_DATA	-	Data incasarii venitului din pensii 
* 	NR_VENIT_PENSIE 	-	De cate ori a primi venit din pensii 
* 	VENIT_SOMAJ	-	Valoare venit din somaj 
* 	VENIT_SOMAJ_DATA	-	Data incasarii venitului din somai 
* 	NR_VENIT_SOMAJ - De cate ori a primit venit din somaj 
* 	VENIT_SALARIU	-	Valoare venit din salariu 
* 	VENIT_SALARIU_DATA	-	Data incasarii venitului din salariu 
* 	NR_VENIT_SALARIU - De cate ori a primit venit din salariu

	C. TRANZACTII		
* 	INCASARE_TOTAL	-	Valoarea totala a incasarii
* 	NR_INCASARE_TOTAL	-	Nr total de incasari
* 	PLATA_TOTAL	-	Valoarea totala a platilor ( Toate iesirile din cont)
* 	NR_PLATA_TOTAL	-	Nr total al platilor
* 	RETRAGERE_ATM	-	Valoarea retragere ATM
* 	NR_RETRAGERE_ATM	-	Nr retrageri ATM
* 	PLATA_EC	-	Valoare plata prin E-commerce
* 	NR_PLATA_EC	-	Nr plati prin E-commerce
* 	TRANSFER_APP	-	Valoare transfer prin aplicatie
* 	NR_TRANSFER_APP	-	Nr transferuri prin aplicatie
* 	PLATA_POS	-	Valoare plata prin POS
* 	NR_PLATA_POS	-	Nr plati prin POS
			
	D.PRODUSE		
* 	CURRNT_TOTAL	-	Valoarea totala din cont curent
* 	NR_CURRNT	-	Nr de conturi curente
* 	CREDIT_NP	-	Valoarea creditului de nevoi personale 
* 	NR_AC_CREDIT_NP	-	Nr produse active de credit de nevoi personale
* 	NR_CREDIT_NP	-	Nr produse total de credit de nevoi personale
* 	CREDIT_CARD	-	Valoarea cardului de credit
* 	NR_AC_CREDIT_CARD	-	Nr produse active card de credit
* 	NR_CREDIT_CARD	-	Nr produse card de credit
* 	DEP_TOTAL	-	Valoarea totala a depozitului
* 	NR_AC_DEP	-	Nr produse active depozite
* 	NR_DEP	-	Nr produse depozite
* 	ASIG_TOTAL	-	Valoarea asigurare
* 	NR_AC_ASIG	-	Nr produse active asigurari
* 	NR_ASIG	-	Nr produse asigurari
* 	INV_TOTAL	-	Valoarea totala investitii
* 	NR_AC_INV	-	Nr produse active investitii
* 	NR_INV	-	Nr produse investitii
* 	REF_TOTAL	-	Valoarea totala refinantare
* 	NR_AC_REFIN	-	Nr produse active refinantare
* 	NR_REFIN	-	Nr produse refinantare
* 	PLAN_EC_TOTAL	-	Valoarea totala plan de economii
* 	NR_AC_PLAN_EC	-	Nr produse active plan de economii
* 	NR_PLAN_EC	-	Nr produse plan de economii
			
	E.SERVICII		
* 	IND_APP_NOTIF	-	Indicator 1/0 daca clientul accepta sa primeasca notificari prin aplicatie
* 	IND_GOOGLE_PAY	-	Indicator 1/0 daca clientul foloseste Google Pay
* 	IND_CASHBACK	-	Indicator 1/0 daca clientul are activat serviciul CashBack
* 	IND_APPLE_PAY	-	Indicator 1/0 daca clientul foloseste Apple Pay
			
			
			
