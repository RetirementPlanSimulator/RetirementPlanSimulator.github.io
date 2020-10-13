<html>
<style>
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 20px;
  text-align: center;
} 
</style>

 <head>
  <title>Back Test Retirement Plan</title>
  <meta http-equiv="Content-Type" content="text/html; charset=windows-1252">
 </head>

<h1 id="myHeader">Retirement Plan Simulator</h1>

<p> The purpose of Retirement Plan Simulator (RPS) is to pressure test the survivability of financial plans for retirement by running the following simulations:</p>

<p>1)	Baseline Simulation: RPS will simulate your retirement plan against a simple smooth annual return rates of 6% for stocks and 3% for bonds, and 2.25% inflation rate. </p>

<p>2)	Historical Simulation: RPS will simulate your retirement plan against actual prior historical market performance and sequence of events.  Annual return rates of the S&P500 index (or total stock market index when available), intermediate bond fund index and inflation rates are used in the simulation.</p>

<p>RPS cannot definitively tell if a plan will survive retirement, but it can provide an increased level of awareness on the range of possibilities that could be experienced during retirement.  If a plan can survive every sequence of events in history (even the worst-case sequence of events), there is an excellent chance the plan will survive future scenarios.</p>  
<p> Before using RPS, please read the <a href="RPS_Disclaimer.html" target="_blank">disclaimer</a>.  More information can be found in the <a href="RPS_User_Guide2.html" target="_blank"> user guide </a>.  Hope you find this tool useful.  Please <a href="mailto:home@josephenagy.com"> email me </a> with comments and suggestions. </p>

<form onsubmit=" ">
<div align="left">
<p> If you have used RPS on this computer before: 
<input type="button" value="Get Your Previously Processed Plan" onclick="getprev(this.form)">
</p>

<p>
<fieldset>
  <legend> <b> Your Information </b> </legend>
     <label for="you_cur_age">Age: </label> 
     <input id='youcurage' type="number" name="you_cur_age" min="20" max="99"> 

     <label for="you_retire_age">Retire Begin Age:</label> 
     <input type="number" name="you_retire_age", value="65" min="20" max="99"> 

     <label for="you_retire_end_age">Retire End Age:</label>  
     <input type="number" name="you_retire_end_age", value="94" min="20" max="99">

     <label for="you_socsec_age">Soc Sec Start Age:</label> 	
     <input type="number" name="you_socsec_age", value="70" min="62" max="70">

     <label for="you_socsec_amt">Annual Soc Sec:</label> 	
     <input type="number" name="you_socsec_amt", value=0, min="0" max="100000"     >
    
     <label for="you_ira_start_bal_amt">IRA/401K Balance:</label>
     <input type="number" name="you_ira_start_bal_amt" value=0 min="0" max="999999999">

     <label for="you_ira_ann_dep_amt">IRA/401K Annual Deposit:</label>
     <input type="number" name="you_ira_ann_dep_amt" value=0 min="0" max="999999">

     <br> 
     <label for="you_pension_amt">Annual Pension:</label> 
     <input type="number" name="you_pension_amt" value=0 min="0" max="999999">

     <label for="you_pension_beg_age">Pension Begin Age:</label> 
     <input type="number" name="you_pension_begin_age" value=0 min="0" max="99"	>

    <label for="you_pension_inf_pct">Annual Pension Inflation Adjustment %:</label> 
    <input type="number" name="you_pension_inf_pct" value=0 min="0" max="10">

    <label for="you_pension_survivor_pct">Pension Survivor %:</label> 
    <input type="number" name="you_pension_survivor_pct" value=0 min="0" max="100">

</fieldset>
<br>
<fieldset>
  <legend><b> Spouse Information </b> </legend>
     <label for="spo_cur_age">Age: </label>
     <input type="number" name="spo_cur_age" value=0 min="20" max="99"> 

     <label for="spo_retire_age">Retire Begin Age:</label> 
     <input type="number" name="spo_retire_age" value=0 min="20" max="99"> 

     <label for="spo_retire_end_age">Retire End Age:</label> 
     <input type="number" name="spo_retire_end_age" value=0 min="20" max="99">
     
     <label for="spo_socsec_age">Soc Sec Start Age:</label>  	
     <input type="number" name="spo_socsec_age" value=0 min="62" max="70">
     
     <label for="spo_socsec_amt">Annual Soc Sec:</label>
     <input type="number" name="spo_socsec_amt" value=0 min="0" max="100000">       

     <label for="spo_ira_start_bal_amt">IRA/401k Balance:</label> 
     <input type="number" name="spo_ira_start_bal_amt" value=0 min="0" max="999999999">

     <label for="spo_ira_ann_dep_amt">IRA/401k Annual Deposit:</label> 
     <input type="number" name="spo_ira_ann_dep_amt" value=0 min="0" max="999999">

     <br>
     <label for="spo_pension_amt">Annual Pension:</label> 
     <input type="number" name="spo_pension_amt" value=0 min="0" max="999999">

     <label for="spo_pension_beg_age">Pension Begin Age:</label> 
     <input type="number" name="spo_pension_begin_age" value=0 min="0" max="99">

    <label for="spo_pension_inf_pct">Annual Pension Inflation Adjustment %:</label> 
    <input type="number" name="spo_pension_inf_pct" value=0 min="0" max="10">

    <label for="spo_pension_survivor_pct">Pension Survivor %:</label>  
    <input type="number" name="spo_pension_survivor_pct" value=0 min="0" max="100">

</fieldset>
<br>
<fieldset>
  <legend><b> Brokerage Account Information </b> </legend>

    <label for="brkrg_start_bal_amt">Current Balance:</label>
    <input type="number" name="brkrg_start_bal_amt" value=0 min="0" max="999999999">

    <label for="brkrg_cost_basis_amt">Cost Basis:</label>
    <input type="number" name="brkrg_cost_basis_amt" value=0 min="0" max="999999999">

     <label for="brkrg_ann_dep_amt">Annual Deposit:</label> 
     <input type="number" name="brkrg_ann_dep_amt" value=0 min="0" max="999999">
</fieldset> 
<br>

<fieldset>
  <legend><b> Roth / HSA Account Information </b> </legend>

    <label for="roth_start_bal_amt">Current Balance:</label> 
    <input type="number" name="roth_start_bal_amt" value=0 min="0" max="999999999">

     <label for="roth_ann_dep_amt">Annual Deposit:</label> 
     <input type="number" name="roth_ann_dep_amt" value=0 min="0" max="999999">

    <label for="roth_conv_pct">Backdoor Conversion Max Tax Bracket:</label>
         <select name="roth_conv_pct" id="roth_conv_pct">
           <option value="none">None</option>
           <option value="0">0%</option>
           <option value="10">10%</option>
           <option value="12">12%</option>
          </select>

</fieldset> 
<br>
<fieldset>
  <legend><b> Annual Budget </b> </legend>
    
    <label for="gogo_budget_amt">Go Go Years (< 75):</label> 
    <input type="number" name="gogo_budget_amt" value=0 min="0" max="999999">

    <label for="slowgo_budget_amt">Slow Go Years (< 85):</label> 
    <input type="number" name="slowgo_budget_amt" value=0 min="0" max="999999">

    <label for="nogo_budget_amt">No Go Years (> 85):</label> 
    <input type="number" name="nogo_budget_amt" value=0 min="0" max="999999">

    <label for="last3_budget_amt">Nursing Home Years (Last 3):</label> 
    <input type="number" name="last3_budget_amt" value=0 min="0" max="9999999">

    <label for="mortgage_budget_amt">Mortgage Amount:</label> 
    <input type="number" name="mortgage_budget_amt" value=0 min="0" max="999999">

    <label for="mortgage_end_age">Age Mortgage Ends:</label> 
    <input type="number" name="mortgage_end_age" value=0 min="0" max="99">

</fieldset> 
<br>
<fieldset>
  <legend><b> Other Information </b> </legend>
    
    <label for="stock_pct">Stock Allocation %:</label> 
    <input type="number" name="stock_pct" value=60 min="0" max="100"                >

    <label for="bonus_pct">Retirement Bonus %:</label>
    <input type="number" name="bonus_pct" value=0 min="0" max="100">

    <label for="baseline_stock_return_pct">Baseline Stock Return %:</label>
    <input type="number" name="baseline_stock_return_pct" value=6 min="0" max="10">

    <label for="baseline_bond_return_pct">Baseline Bond Return %:</label>
    <input type="number" name="baseline_bond_return_pct" value=3 min="0" max="10">


</fieldset> 
<br>
<input type="button" value="Run Simulation" onclick="calcdraw(this.form,'NO')">

<input type="button" value="Download Detail Results" onclick="calcdraw(this.form,'YES')">

<p id="showresults">


</div>
</form>

</html>
