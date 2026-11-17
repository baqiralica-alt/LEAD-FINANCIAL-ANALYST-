LEAD FINANCIAL ANALYST		
		
		
Linked 3-Statement Model  •  Driver-Based SaaS Forecast  •  Scenario Analysis  •  Variance Walk  •  Trackers  •  Dashboard		
		
Baqir Ali, CPA  •  MBA Finance  •  FMVA		
		
		
		
Workbook Contents		
01_README	Color codes, conventions, how to use this workbook	
02_Assumptions	Single source of truth for all drivers — scenario toggle lives here	
03_Revenue_Build	SaaS ARR bridge: starting ARR + new logos − churn = ending ARR	
04_Headcount_Build	Headcount by department, comp build, fully-loaded cost	
05_OPEX_Build	SaaS, contractor, marketing, G&A expense build	
06_3_Statement_Model	Linked P&L, Balance Sheet, Cash Flow	
07_Variance_Analysis	Budget vs. actual walk with price/volume/mix decomposition	
08_Headcount_Tracker	Live HC tracker (HRIS / ATS / Budget reconciliation)	
09_PO_Log	Purchase order log with budget check & approval matrix	
10_KPI_Dashboard	Executive dashboard with charts and metrics	
11_Interview_CheatSheet	Top interview Q&A quick reference	
12_Formula_Reference	Excel formulas and their FP&A use cases	
		
		
COLOR CONVENTIONS		
Input cell (hardcoded)	Blue text on light blue fill	
Formula cell	Black text on light grey fill	
Link to another sheet	Green text	
Total / subtotal	Bold dark navy, double underline	

README — How to Use This Workbook	
	
Purpose	This workbook is a study tool for the Lead Financial Analyst interview at Motive. Every tab models a real FP&A workflow with small fictional data so you can study every formula, trace every link, and rebuild the logic from scratch.
	
Fictional Data	All numbers are made up for study. Motive is a SaaS / IoT platform company serving the physical economy (trucking, construction, etc.). Treat the numbers as illustrative only.
	
Starting Point	Always go to the 02_Assumptions tab first. Every driver (revenue, headcount, opex) lives there. Change a number there and watch it cascade through the entire model.
	
Scenario Toggle	The 02_Assumptions tab has a scenario selector (1=Base, 2=Upside, 3=Downside). Change that single cell and the entire model updates.
	
Color Convention	Blue = input (you can change). Black = formula (don't change). Green = link to another sheet. Bold dark navy = total/subtotal.
	
3-Statement Model	Tab 06 has the integrated P&L, Balance Sheet, and Cash Flow. Every formula traces back to assumptions or driver sheets.
	
Variance Walk	Tab 07 decomposes a budget-to-actual variance into price / volume / mix drivers — a classic FP&A interview question.
	
Trackers	Tabs 08 (Headcount) and 09 (PO Log) are operational trackers that feed the model. In real life these live in Google Sheets; here they're in Excel for study.
	
Dashboard	Tab 10 is the executive summary with KPIs and charts — the kind of view the CFO sees monthly.
	
Interview Prep	Tab 11 has top interview Q&A in compressed form. Tab 12 is a formula reference.


ASSUMPTIONS — Single Source of Truth				
				
Scenario Toggle	1 = Base / 2 = Upside / 3 = Downside			
Active Scenario	1			
				
REVENUE DRIVERS				
Driver	Base (1)	Upside (2)	Downside (3)	Active
Starting ARR ($)	$24,000,000	$24,000,000	$24,000,000	$24,000,000
New logos per month	50	65	35	50
Average ARPU per logo ($/month)	$4,000	$4,200	$3,700	$4,000
Gross logo churn rate (annual %)	8.0%	6.0%	12.0%	8.0%
Revenue recognition months per logo (contract term)	12	12	12	12
Net new ARR from expansion (% of starting ARR)	$0	$0	$0	$0
				
HEADCOUNT DRIVERS				
Driver	Base (1)	Upside (2)	Downside (3)	Active
Starting headcount (Engineering)	80	80	80	80
Starting headcount (Sales)	60	60	60	60
Starting headcount (Customer Success)	40	40	40	40
Starting headcount (G&A)	35	35	35	35
Monthly hires (Engineering)	4	6	2	4
Monthly hires (Sales)	5	7	3	5
Monthly hires (Customer Success)	2	3	1	2
Monthly hires (G&A)	1	2	0	1
Monthly attrition rate (all depts)	1.5%	1.0%	2.5%	1.5%
Avg base salary — Engineering ($/month)	$9,500	$9,700	$9,200	$9,500
Avg base salary — Sales ($/month)	$7,000	$7,200	$6,800	$7,000
Avg base salary — Customer Success ($/month)	$6,000	$6,200	$5,800	$6,000
Avg base salary — G&A ($/month)	$6,500	$6,700	$6,300	$6,500
Variable comp load — Sales (% of base)	40.0%	45.0%	30.0%	40.0%
Benefits + payroll tax load (% of total comp)	25.0%	25.0%	25.0%	25.0%
				
OPEX DRIVERS (Non-Comp)				
Driver	Base (1)	Upside (2)	Downside (3)	Active
Hosting (AWS/GCP) — $/active customer/month	$85	$80	$95	$85
SaaS subscriptions — $/employee/month	$350	$350	$350	$350
Marketing spend — $/month	$600,000	$750,000	$400,000	$600,000
Contractor costs — Engineering ($/month)	$180,000	$200,000	$140,000	$180,000
Legal & professional services ($/month)	$120,000	$120,000	$120,000	$120,000
Travel & entertainment ($/month)	$80,000	$90,000	$60,000	$80,000
Office & facilities ($/month)	$60,000	$60,000	$60,000	$60,000
Other G&A ($/month)	$50,000	$50,000	$50,000	$50,000
Annual capex for the year ($)	$1,500,000	$2,000,000	$1,000,000	$1,500,000
Annual D&A from prior capex ($)	$1,200,000	$1,200,000	$1,200,000	$1,200,000
Effective tax rate (%)	25.0%	25.0%	25.0%	25.0%
DSO — days sales outstanding	3500.0%	3000.0%	4500.0%	3500.0%
DPO — days payable outstanding	3000.0%	3000.0%	3000.0%	3000.0%
Interest rate on debt (%)	6.0%	6.0%	6.0%	6.0%
Starting debt balance ($)	$5,000,000	$5,000,000	$5,000,000	$5,000,000
Starting cash balance ($)	$8,000,000	$8,000,000	$8,000,000	$8,000,000
				
				
ROW REFERENCES (used by other tabs)				
Starting ARR	B9:F9			
New logos/month	B10:F10			
ARPU/logo/month	B11:F11			
Gross churn %	B12:F12			
Expansion ARR %	B14:F14			
Starting HC by dept	B18:E21			
Monthly hires by dept	B22:E25			
Attrition rate	B26:F26			
Avg base salary by dept	B27:F30			
Sales variable comp %	B31:F31			
Benefits load %	B32:F32			
Hosting $/customer/month	B36:F36			
SaaS subs $/employee/month	B37:F37			
Marketing $/month	B38:F38			
Contractor cost $/month	B39:F39			
Legal/prof $/month	B40:F40			
T&E $/month	B41:F41			
Office/facilities $/month	B42:F42			
Other G&A $/month	B43:F43			
Annual capex	B44:F44			
Annual D&A	B45:F45			
Tax rate	B46:F46			
DSO	B47:F47			
DPO	B48:F48			
Interest rate	B49:F49			
Starting debt	B50:F50			
Starting cash	B51:F51			

	
Practice	Try this: change the 'new logos per month' on 02_Assumptions from 50 to 35. Trace where it shows up in P&L, BS, CF, and the KPI dashboard.
	
    
