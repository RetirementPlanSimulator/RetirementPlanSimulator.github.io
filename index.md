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

<p> The purpose of yRetirement Plan Simulator (RPS) is to pressure test the survivability of financial plans for retirement by running the following simulations:</p>

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
     <input type="number" name="you_retire_age" value="65" min="20" max="99"> 

     <label for="you_retire_end_age">Retire End Age:</label>  
     <input type="number" name="you_retire_end_age" value="94" min="20" max="99">

     <label for="you_socsec_age">Soc Sec Start Age:</label> 	
     <input type="number" name="you_socsec_age" value="70" min="62" max="70">

     <label for="you_socsec_amt">Annual Soc Sec:</label> 	
     <input type="number" name="you_socsec_amt" value=0 min="0" max="100000"     >
    
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

<script type="text/javascript">
 function getprev(form) 
  { 
   form.spo_cur_age.value = localStorage.getItem("SimpSim_spo_cur_age");
   form.spo_cur_age.value = localStorage.getItem("SimpSim_spo_cur_age");
   form.you_cur_age.value = localStorage.getItem("SimpSim_you_cur_age");
   form.spo_pension_begin_age.value = localStorage.getItem("SimpSim_spo_pension_begin_age");
   form.spo_pension_inf_pct.value = localStorage.getItem("SimpSim_spo_pension_inf_pct");
   form.spo_pension_survivor_pct.value = localStorage.getItem("SimpSim_spo_pension_survivor_pct");
   form.spo_retire_age.value = localStorage.getItem("SimpSim_spo_retire_age");
   form.spo_socsec_age.value = localStorage.getItem("SimpSim_spo_socsec_age");
   form.you_pension_begin_age.value = localStorage.getItem("SimpSim_you_pension_begin_age");
   form.you_pension_inf_pct.value = localStorage.getItem("SimpSim_you_pension_inf_pct");
   form.you_pension_survivor_pct.value = localStorage.getItem("SimpSim_you_pension_survivor_pct");
   form.you_retire_age.value = localStorage.getItem("SimpSim_you_retire_age");
   form.you_socsec_age.value = localStorage.getItem("SimpSim_you_socsec_age");
   form.brkrg_start_bal_amt.value = localStorage.getItem("SimpSim_brkrg_start_bal_amt");
   form.brkrg_cost_basis_amt.value = localStorage.getItem("SimpSim_brkrg_cost_basis_amt");

   form.gogo_budget_amt.value = localStorage.getItem("SimpSim_gogo_budget_amt");
   form.slowgo_budget_amt.value = localStorage.getItem("SimpSim_slowgo_budget_amt");
   form.nogo_budget_amt.value = localStorage.getItem("SimpSim_nogo_budget_amt");
   form.last3_budget_amt.value = localStorage.getItem("SimpSim_last3_budget_amt");
   form.mortgage_budget_amt.value = localStorage.getItem("SimpSim_mortgage_budget_amt");
   form.mortgage_end_age.value = localStorage.getItem("SimpSim_mortgage_end_age");

   form.spo_ira_start_bal_amt.value = localStorage.getItem("SimpSim_spo_ira_start_bal_amt");
   form.spo_pension_amt.value = localStorage.getItem("SimpSim_spo_pension_amt");
   form.spo_socsec_amt.value = localStorage.getItem("SimpSim_spo_socsec_amt");
   form.you_ira_start_bal_amt.value = localStorage.getItem("SimpSim_you_ira_start_bal_amt");
   form.you_pension_amt.value = localStorage.getItem("SimpSim_you_pension_amt");
   form.you_socsec_amt.value = localStorage.getItem("SimpSim_you_socsec_amt");
   form.stock_pct.value = localStorage.getItem("SimpSim_stock_pct");
   form.bonus_pct.value = localStorage.getItem("SimpSim_bonus_pct");
   form.spo_retire_end_age.value = localStorage.getItem("SimpSim_spo_retire_end_age");
   form.you_retire_end_age.value = localStorage.getItem("SimpSim_you_retire_end_age");
   form.roth_start_bal_amt.value = localStorage.getItem("SimpSim_roth_start_bal_amt");
   form.roth_conv_pct.value = localStorage.getItem("SimpSim_roth_conv_pct");

   form.you_ira_ann_dep_amt.value = localStorage.getItem("SimpSim_you_ira_ann_dep_amt");
   form.spo_ira_ann_dep_amt.value = localStorage.getItem("SimpSim_spo_ira_ann_dep_amt");
   form.brkrg_ann_dep_amt.value = localStorage.getItem("SimpSim_brkrg_ann_dep_amt");
   form.roth_ann_dep_amt.value = localStorage.getItem("SimpSim_roth_ann_dep_amt");

   form.baseline_stock_return_pct.value = localStorage.getItem("SimpSim_baseline_stock_return_pct");
   form.baseline_bond_return_pct.value = localStorage.getItem("SimpSim_baseline_bond_return_pct");

  }  
</script>

<script type="text/javascript">
 function calcdraw(form, fDownload_Results) {

      error_message = '';
      error_message1 = '<p> Ooops.  Errors found on input</p>';

      if (form.you_cur_age.value > 99) 
          {error_message = error_message + "<p> Your Current Age must be between 20 and 99. </p> ";  }
  
      if (form.you_cur_age.value < 20) 
        {error_message = error_message + "<p> Your Current Age must be between 20 and 99. </p> "; }

      if (form.you_retire_age.value > 99) 
        {error_message = error_message + "<p> Your Retire Age must be between 20 and 99. </p>"; }
  
      if (form.you_retire_age.value < 20) 
        {error_message = error_message + "<p> Your Retire Age must be between 20 and 99. </p>"; }

      if (form.you_retire_end_age.value > 99) 
        {error_message = error_message + "<p> Your Retire End Age must be between 70 and 99. </p> "; }
  
      if (form.you_retire_end_age.value < 70) 
        {error_message = error_message + "<p> Your Retire End Age must be between 70 and 99. </p>"; }

      if (form.you_socsec_age.value < 62) 
        {error_message = error_message + "<p> Your Social Security Start Age must be between 62 and 70. </p> "; }

      if (form.you_socsec_age.value > 70) 
        {error_message = error_message + "<p> Your Social Security Start Age must be between 62 and 70. </p>"; }

      if (form.you_socsec_amt.value > 100000) 
          {error_message = error_message + "<p> Your Social Security Amount must be betwen 0 and 100000. </p>"; }
      
      if (form.you_socsec_amt.value < 0) 
          {error_message = error_message + "<p> Your Social Security Amount must be between 0 and 100000. </p> "; }

      if (form.you_ira_start_bal_amt.value < 0) 
          {error_message = error_message + "<p> Your IRA Amount must be between 0 and 1000000000. </p> "; }

      if (form.you_ira_start_bal_amt.value > 1000000000) 
         {error_message = error_message + "<p> Your IRA Amount must be between 0 and 1000000000.  </p>"; }

      if (form.you_ira_ann_dep_amt.value < 0) 
         {error_message = error_message + "<p> Your Annual IRA Deposit must be between 0 and 1000000. </p>"; }

      if (form.you_ira_ann_dep_amt.value > 1000000) 
         {error_message = error_message + "<p> Your Annual IRA Deposit must be between 0 and 1000000. </p>"; }

      if (form.you_pension_amt.value < 0) 
         {error_message = error_message + "<p> Your Pension must be between 0 and 1000000.  </p>"; }

      if (form.you_pension_amt.value > 1000000) 
         {error_message = error_message + "<p> Your Pension must be between 0 and 1000000.  </p>"; }

      if (form.you_pension_begin_age.value < 0) 
         {error_message = error_message + "<p> Your Pension Begin Age must be between 0 and 99. </p>"; }

      if (form.you_pension_begin_age.value > 99) 
         {error_message = error_message + "<p> Your Pension Begin Age must be between 0 and 99.  </p>"; }

      if (form.you_pension_inf_pct.value < 0) 
         {error_message = error_message + "<p> Your Pension Inflation Adjustment must be between 0 and 10.  </p>"; }

      if (form.you_pension_inf_pct.value > 10) 
         {error_message = error_message + "<p> Your Pension Inflation Adjustment must be between 0 and 10.  </p>"; }

      if (form.you_pension_survivor_pct.value < 0) 
         {error_message = error_message + "<p> Your Pension Survivor Percent must be between 0 and 100.  </p>"; }

      if (form.you_pension_survivor_pct.value > 100) 
         {error_message = error_message + "<p> Your Pension Survivor Percent must be between 0 and 100.  </p>"; }

      if (form.spo_cur_age.value > 0)
          {error_message = edit_spouse_form(form, error_message);}

      if (form.spo_cur_age.value == 0)
          {error_message = edit_spouse_form2(form, error_message);}

       if (form.brkrg_start_bal_amt.value < 0) 
         {error_message = error_message + "<p> Brokerage Balance must be between 0 and 1000000000.  </p>"; }
      
       if (form.brkrg_start_bal_amt.value > 1000000000) 
         {error_message = error_message + "<p> Brokerage Balance must be between 0 and 1000000000.  </p>"; }
      
       if (form.brkrg_cost_basis_amt.value < 0) 
         {error_message = error_message + "<p> Brokerage Cost Basis must be between 0 and 1000000000.  </p>"; }
      
       if (form.brkrg_cost_basis_amt.value > 1000000000) 
         {error_message = error_message + "<p> Brokerage Cost Basis must be between 0 and 1000000000.  </p>"; }
      
       if (form.brkrg_ann_dep_amt.value < 0) 
         {error_message = error_message + "<p> Brokerage Annual Deposit must be between 0 and 1000000000.  </p>"; }
      
       if (form.brkrg_ann_dep_amt.value > 1000000000) 
         {error_message = error_message + "<p> Brokerage Annual Deposit must be between 0 and 1000000000.  </p>"; }
      
       if (form.roth_start_bal_amt.value < 0) 
         {error_message = error_message + "<p> Roth Start Balance must be between 0 and 1000000000.  </p>"; }
      
       if (form.roth_start_bal_amt.value > 1000000000) 
         {error_message = error_message + "<p> Roth Start Balance must be between 0 and 1000000000.  </p>"; }
      
       if (form.roth_ann_dep_amt.value < 0) 
         {error_message = error_message + "<p> Roth Annual Deposit must be between 0 and 1000000000.  </p>"; }
      
       if (form.roth_ann_dep_amt.value > 1000000000) 
         {error_message = error_message + "<p> Roth Annual Deposit must be between 0 and 1000000000.  </p>"; }
      
       if (form.gogo_budget_amt.value < 0) 
         {error_message = error_message + "<p> Go Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.gogo_budget_amt.value > 1000000000) 
         {error_message = error_message + "<p> Go Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.slowgo_budget_amt.value < 0) 
         {error_message = error_message + "<p> Slow Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.slowgo_budget_amt.value > 1000000000) 
         {error_message = error_message + "<p> Slow Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.nogo_budget_amt.value < 0) 
         {error_message = error_message + "<p> No Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.nogo_budget_amt.value > 1000000000) 
         {error_message = error_message + "<p> No Go Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.last3_budget_amt.value < 0) 
         {error_message = error_message + "<p> Last 3 Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.last3_budget_amt.value > 1000000000) 
         {error_message = error_message + "<p> Last 3 Budget must be between 0 and 1000000000.  </p>"; }
     
       if (form.mortgage_budget_amt.value < 0) 
         {error_message = error_message + "<p> Mortgage Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.mortgage_budget_amt.value > 1000000000) 
         {error_message = error_message + "<p> Mortgage Budget must be between 0 and 1000000000.  </p>"; }
      
       if (form.mortgage_end_age.value < 0) 
         {error_message = error_message + "<p> Mortgage End Age must be between 0 and 99.  </p>"; }
      
       if (form.mortgage_end_age.value > 99) 
         {error_message = error_message + "<p> Mortgage End Age must be between 0 and 99.  </p>"; }
      
       if (form.stock_pct.value < 0) 
         {error_message = error_message + "<p> Stock Pct must be between 0 and 100.  </p>"; }
      
       if (form.stock_pct.value > 100) 
         {error_message = error_message + "<p> Stock Pct must be between 0 and 100.  </p>"; }
      
       if (form.bonus_pct.value < 0) 
         {error_message = error_message + "<p> Bonus Pct must be between 0 and 100.  </p>"; }
      
       if (form.bonus_pct.value > 100) 
         {error_message = error_message + "<p> Bonus Pct must be between 0 and 100.  </p>"; }
      
       if (form.baseline_stock_return_pct.value < 0) 
         {error_message = error_message + "<p> Baseline Stock Return Pct must be between 0 and 10.  </p>"; }
      
       if (form.baseline_stock_return_pct.value > 10) 
         {error_message = error_message + "<p> Baseline Stock Return Pct must be between 0 and 10.  </p>"; }
      
       if (form.baseline_bond_return_pct.value < 0) 
         {error_message = error_message + "<p> Baseline Bond Return Pct must be between 0 and 10.  </p>"; }
      
       if (form.baseline_bond_return_pct.value > 10) 
         {error_message = error_message + "<p> Baseline Bond Return Pct must be between 0 and 10.  </p>"; }
      
      if (error_message == '')
         {process_form(form,fDownload_Results)};
      
      if (error_message != '')
         {
           document.getElementById("showresults").innerHTML = error_message1 + error_message;
           window.scrollTo(0, 200);
         }
 
  }  
</script>


<script type="text/javascript">
 function edit_spouse_form (form, error_message) {

      if (form.spo_cur_age.value > 99) 
          {error_message = error_message + "<p> Spouse Current Age must be between 20 and 99. </p> ";  }
  
      if (form.spo_cur_age.value < 20) 
        {error_message = error_message + "<p> Spouse Current Age must be between 20 and 99. </p> "; }
      
      if (form.spo_retire_age.value > 99) 
        {error_message = error_message + "<p> Spouse Retire Age must be between 20 and 99. </p>"; }
  
      if (form.spo_retire_age.value < 20) 
        {error_message = error_message + "<p> Spouse Retire Age must be between 20 and 99. </p>"; }

      if (form.spo_retire_end_age.value > 99) 
        {error_message = error_message + "<p> Spouse Retire End Age must be between 70 and 99. </p> "; }
  
      if (form.spo_retire_end_age.value < 70) 
        {error_message = error_message + "<p> Spouse Retire End Age must be between 70 and 99. </p>"; }

      if (form.spo_socsec_age.value < 62) 
         {error_message = error_message + "<p> Spouse Social Security Start Age must be between 62 and 70. </p> "; }

      if (form.spo_socsec_age.value > 70) 
        {error_message = error_message + "<p> Spouse Social Security Start Age must be between 62 and 70. </p>"; }

      if (form.spo_socsec_amt.value > 100000) 
          {error_message = error_message + "<p> Spouse Social Security Amount must be betwen 0 and 100000. </p>"; }
      
      if (form.spo_socsec_amt.value < 0) 
          {error_message = error_message + "<p> Spouse Social Security Amount must be between 0 and 100000. </p> "; }

      if (form.spo_ira_start_bal_amt.value < 0) 
          {error_message = error_message + "<p> Spouse IRA Amount must be between 0 and 1000000000. </p> "; }

      if (form.spo_ira_start_bal_amt.value > 1000000000) 
         {error_message = error_message + "<p> Spouse IRA Amount must be between 0 and 1000000000.  </p>"; }

      if (form.spo_ira_ann_dep_amt.value < 0) 
         {error_message = error_message + "<p> Spouse Annual IRA Deposit must be between 0 and 1000000. </p>"; }

      if (form.spo_ira_ann_dep_amt.value > 1000000) 
         {error_message = error_message + "<p> Spouse Annual IRA Deposit must be between 0 and 1000000. </p>"; }

      if (form.spo_pension_amt.value < 0) 
         {error_message = error_message + "<p> Spouse Pension must be between 0 and 1000000.  </p>"; }

      if (form.spo_pension_amt.value > 1000000) 
         {error_message = error_message + "<p> Spouse Pension must be between 0 and 1000000.  </p>"; }

      if (form.spo_pension_begin_age.value < 0) 
         {error_message = error_message + "<p> Spouse Pension Begin Age must be between 0 and 99. </p>"; }

      if (form.spo_pension_begin_age.value > 99) 
         {error_message = error_message + "<p> Spouse Pension Begin Age must be between 0 and 99.  </p>"; }

      if (form.spo_pension_inf_pct.value < 0) 
         {error_message = error_message + "<p> Spouse Pension Inflation Adjustment must be between 0 and 10.  </p>"; }

      if (form.spo_pension_inf_pct.value > 10) 
         {error_message = error_message + "<p> Spouse Pension Inflation Adjustment must be between 0 and 10.  </p>"; }

      if (form.spo_pension_survivor_pct.value < 0) 
         {error_message = error_message + "<p> Spouse Pension Survivor Percent must be between 0 and 100.  </p>"; }

      if (form.spo_pension_survivor_pct.value > 100) 
         {error_message = error_message + "<p> Spouse Pension Survivor Percent must be between 0 and 100.  </p>"; }

      
       return error_message; 
  }  

</script>
          
<script type="text/javascript">
 function edit_spouse_form2 (form, error_message) {

      if (form.spo_retire_age.value != 0) 
        {error_message = error_message + "<p> Spouse Retire Age entered - Spouse Current Age must be between 20 and 99. </p>"; }
  
      if (form.spo_retire_end_age.value != 0) 
        {error_message = error_message + "<p> Spouse Retire End entered - Spouse Current Age must be between 20 and 99. </p> "; }
  
     if (form.spo_socsec_age.value != 0) 
         {error_message = error_message + "<p> Spouse Social Security Age entered - Spouse Current Age must be between 20 and 99.  </p> "; }

     if (form.spo_socsec_amt.value != 0) 
          {error_message = error_message + "<p> Spouse Social Security Amount entered - Spouse Current Age must be between 20 and 99.   </p>"; }
      
      if (form.spo_ira_start_bal_amt.value != 0) 
          {error_message = error_message + "<p> Spouse IRA Amount entered - Spouse Current Age must be between 20 and 99.    </p> "; }

      if (form.spo_ira_ann_dep_amt.value != 0) 
         {error_message = error_message + "<p> Spouse Annual IRA Deposit entered - Spouse Current Age must be between 20 and 99.  </p>"; }

      if (form.spo_pension_amt.value != 0) 
         {error_message = error_message + "<p> Spouse Pension Spouse Annual IRA Deposit entered - Spouse Current Age must be between 20 and 99. </p>"; }

      if (form.spo_pension_begin_age.value != 0) 
         {error_message = error_message + "<p> Spouse Pension Begin Age entered - Spouse Current Age must be between 20 and 99. </p>"; }

      if (form.spo_pension_inf_pct.value != 0) 
         {error_message = error_message + "<p> Spouse Pension Inflation Adjustment entered - Spouse Current Age must be between 20 and 99. </p>"; }

      if (form.spo_pension_survivor_pct.value != 0) 
         {error_message = error_message + "<p> Spouse Pension Survivor Percent entered - Spouse Current Age must be between 20 and 99. </p>"; }

       return error_message; 
  }  
</script>

<script type="text/javascript">
 function process_form(form, fDownload_Results) {

   localStorage.setItem("SimpSim_spo_cur_age", form.spo_cur_age.value);
   localStorage.setItem("SimpSim_you_cur_age", form.you_cur_age.value);
   localStorage.setItem("SimpSim_spo_pension_begin_age", form.spo_pension_begin_age.value);
   localStorage.setItem("SimpSim_spo_pension_inf_pct", form.spo_pension_inf_pct.value);
   localStorage.setItem("SimpSim_spo_pension_survivor_pct", form.spo_pension_survivor_pct.value);
   localStorage.setItem("SimpSim_spo_retire_age", form.spo_retire_age.value);
   localStorage.setItem("SimpSim_spo_socsec_age", form.spo_socsec_age.value);
   localStorage.setItem("SimpSim_you_pension_begin_age", form.you_pension_begin_age.value);
   localStorage.setItem("SimpSim_you_pension_inf_pct", form.you_pension_inf_pct.value);
   localStorage.setItem("SimpSim_you_pension_survivor_pct", form.you_pension_survivor_pct.value);
   localStorage.setItem("SimpSim_you_retire_age", form.you_retire_age.value);
   localStorage.setItem("SimpSim_you_socsec_age", form.you_socsec_age.value);
   localStorage.setItem("SimpSim_brkrg_start_bal_amt", form.brkrg_start_bal_amt.value);
   localStorage.setItem("SimpSim_brkrg_cost_basis_amt", form.brkrg_cost_basis_amt.value);
   localStorage.setItem("SimpSim_gogo_budget_amt", form.gogo_budget_amt.value);
   localStorage.setItem("SimpSim_slowgo_budget_amt", form.slowgo_budget_amt.value);
   localStorage.setItem("SimpSim_nogo_budget_amt", form.nogo_budget_amt.value);

   localStorage.setItem("SimpSim_last3_budget_amt", form.last3_budget_amt.value);
   localStorage.setItem("SimpSim_mortgage_budget_amt", form.mortgage_budget_amt.value);
   localStorage.setItem("SimpSim_mortgage_end_age", form.mortgage_end_age.value);

   localStorage.setItem("SimpSim_spo_ira_start_bal_amt", form.spo_ira_start_bal_amt.value);
   localStorage.setItem("SimpSim_spo_pension_amt", form.spo_pension_amt.value);
   localStorage.setItem("SimpSim_spo_socsec_amt", form.spo_socsec_amt.value);
   localStorage.setItem("SimpSim_you_ira_start_bal_amt", form.you_ira_start_bal_amt.value);
   localStorage.setItem("SimpSim_you_pension_amt", form.you_pension_amt.value);
   localStorage.setItem("SimpSim_you_socsec_amt", form.you_socsec_amt.value);
   localStorage.setItem("SimpSim_bonus_pct", form.bonus_pct.value);
   localStorage.setItem("SimpSim_stock_pct", form.stock_pct.value);
   localStorage.setItem("SimpSim_spo_retire_end_age", form.spo_retire_end_age.value);
   localStorage.setItem("SimpSim_you_retire_end_age", form.you_retire_end_age.value);
   localStorage.setItem("SimpSim_roth_start_bal_amt", form.roth_start_bal_amt.value);
   localStorage.setItem("SimpSim_roth_conv_pct", form.roth_conv_pct.value);

   localStorage.setItem("SimpSim_you_ira_ann_dep_amt", form.you_ira_ann_dep_amt.value);
   localStorage.setItem("SimpSim_spo_ira_ann_dep_amt", form.spo_ira_ann_dep_amt.value);
   localStorage.setItem("SimpSim_brkrg_ann_dep_amt", form.brkrg_ann_dep_amt.value);
   localStorage.setItem("SimpSim_roth_ann_dep_amt", form.roth_ann_dep_amt.value);

   localStorage.setItem("SimpSim_baseline_stock_return_pct", form.baseline_stock_return_pct.value);
   localStorage.setItem("SimpSim_baseline_bond_return_pct", form.baseline_bond_return_pct.value);

    var fRateLen     = ratehistory.length;    

    var simulation_scenario = new Array( );
    var scenario_summary = new Array( );

    var fCurrent_Year = getcurrentyear();

    var fRowNbr      = 0;
    var fStock_Pct    = form.stock_pct.value / 100;
    var fBonus_Pct   = form.bonus_pct.value / 100;

    fBaseline_Stock_Return_Pct = form.baseline_stock_return_pct.value / 100;
    fBaseline_Bond_Return_Pct = form.baseline_bond_return_pct.value / 100;

    var fYou_Current_Age           = form.you_cur_age.value * 1;
    var fYou_Retire_Age            = form.you_retire_age.value * 1;

    var fSpo_Current_Age           = form.spo_cur_age.value * 1;
    var fSpo_Retire_Age            = form.spo_retire_age.value * 1;

    var fFrm_You_Retire_End_Age                  = form.you_retire_end_age.value * 1;
    var fFrm_Spo_Retire_End_Age               = form.spo_retire_end_age.value * 1;

    var fFrm_You_IRA_Start_Bal_Amt           = form.you_ira_start_bal_amt.value * 1;
    var fFrm_Spo_IRA_Start_Bal_Amt           = form.spo_ira_start_bal_amt.value * 1;
    var fFrm_Brkrg_Start_Bal_Amt             = form.brkrg_start_bal_amt.value * 1;
    var fFrm_Brkrg_Cost_Basis_Amt            = form.brkrg_cost_basis_amt.value * 1;
    var fFrm_Roth_Start_Bal_Amt              = form.roth_start_bal_amt.value * 1;
    var fFrm_Roth_Conv_Pct                   = form.roth_conv_pct.value;

    fFrm_You_IRA_Ann_Dep_Amt                 = form.you_ira_ann_dep_amt.value * 1;
    fFrm_Spo_IRA_Ann_Dep_Amt                 = form.spo_ira_ann_dep_amt.value * 1;
    fFrm_Brkrg_Ann_Dep_Amt                   = form.brkrg_ann_dep_amt.value * 1;
    fFrm_Roth_Ann_Dep_Amt                    = form.roth_ann_dep_amt.value * 1;

    var fFrm_You_Pension_Amt                 = form.you_pension_amt.value * 1;
    var fFrm_You_Pension_Begin_Age           = form.you_pension_begin_age.value * 1;
    var fFrm_You_Pension_Inf_Pct             = form.you_pension_inf_pct.value / 100;
    var fFrm_You_Pension_Survivor_Pct        = form.you_pension_survivor_pct.value /100;

    var fFrm_Spo_Pension_Amt                 = form.spo_pension_amt.value * 1;
    var fFrm_Spo_Pension_Begin_Age           = form.spo_pension_begin_age.value * 1;
    var fFrm_Spo_Pension_Inf_Pct             = form.spo_pension_inf_pct.value / 100;
    var fFrm_Spo_Pension_Survivor_Pct        = form.spo_pension_survivor_pct.value / 100;
 	
    fYou_Nbr_Years = fFrm_You_Retire_End_Age - fYou_Current_Age;
    fSpouse_Nbr_Years = fFrm_Spo_Retire_End_Age - fSpo_Current_Age;	

    fNbr_Years = fYou_Nbr_Years;
    
    if (fSpouse_Nbr_Years > fYou_Nbr_Years) 
            {fNbr_Years = fSpouse_Nbr_Years;}   

    fYou_Remain_Years = fFrm_You_Retire_End_Age - fYou_Current_Age;
    fSpo_Remain_Years = fFrm_Spo_Retire_End_Age - fSpo_Current_Age; 

    fLast_Alive = "you";
    fLast3_Start_Age = fFrm_You_Retire_End_Age - 2;
    if (fSpo_Remain_Years > fYou_Remain_Years) 
         {fLast_Alive = "spouse";
          fLast3_Start_Age = fFrm_Spo_Retire_End_Age - 2;
         }
             
    var fScenario_Nbr = 0;
    var fFailure_Nbr  = 0; 
    var fSurvive_Cnt = 0;
    
    baseline =  {year : 0, age_runout : 000, years_remain: 0, end_bal : 0};   
    sim_summary = {bl : baseline}; 

    fMax_Year = (fCurrent_Year - fNbr_Years + 10);
      
for (var x=0; ratehistory[x].year <= fMax_Year ; x++)
  {
  
//******************************************************************************************
//*** Year 1 simulation will be the baseline plan.  Real simulations will start with year 1871.
//*** Reset inflation adjusted variables back to starting for first year in scenario.
//********************************************************************************************
    if (ratehistory[x].year > 1 && ratehistory[x].year < 1871) {continue;} 

//    fProcess = "no";                                                        
//    if (ratehistory[x].year == 1) {fProcess = "yes";}
//    if (ratehistory[x].year == 1937) {fProcess = "yes";}
//    if (fProcess == "no") {continue;}
                                                              
    var fInfAdj_You_SocSec_Amt   = form.you_socsec_amt.value;
    var fInfAdj_Spo_SocSec_Amt   = form.spo_socsec_amt.value;

    fInfAdj_GoGo_Budget_Amt = form.gogo_budget_amt.value * 1;
    fInfAdj_SlowGo_Budget_Amt = form.slowgo_budget_amt.value * 1;
    fInfAdj_NoGo_Budget_Amt = form.nogo_budget_amt.value * 1;
    fInfAdj_Last3_Budget_Amt = form.last3_budget_amt.value * 1;
      
    fMortgage_Budget_Amt = form.mortgage_budget_amt.value * 1;
    fMortgage_End_Age = form.mortgage_end_age.value * 1;

    var fInfAdj_You_Pension_Amt     = fFrm_You_Pension_Amt;
    var fInfAdj_Spo_Pension_Amt     = fFrm_Spo_Pension_Amt;

    fYou_IRA_Beg_Bal_Amt   = fFrm_You_IRA_Start_Bal_Amt;
    fYou_IRA_Stock_Amt = Math.round(fYou_IRA_Beg_Bal_Amt * fStock_Pct);
    fYou_IRA_Bond_Amt = fYou_IRA_Beg_Bal_Amt - fYou_IRA_Stock_Amt;
    
    fSpo_IRA_Beg_Bal_Amt   = fFrm_Spo_IRA_Start_Bal_Amt;
    fSpo_IRA_Stock_Amt = Math.round(fSpo_IRA_Beg_Bal_Amt * fStock_Pct);
    fSpo_IRA_Bond_Amt = fSpo_IRA_Beg_Bal_Amt - fSpo_IRA_Stock_Amt;
    
    var fBrkrg_Beg_Bal_Amt        = fFrm_Brkrg_Start_Bal_Amt;
    var fBrkrg_Beg_Cost_Basis_Amt = fFrm_Brkrg_Cost_Basis_Amt;
    fBrkrg_Stock_Amt = Math.round(fBrkrg_Beg_Bal_Amt * fStock_Pct);
    fBrkrg_Bond_Amt = fBrkrg_Beg_Bal_Amt - fBrkrg_Stock_Amt;

    var fRoth_Beg_Bal_Amt      = fFrm_Roth_Start_Bal_Amt;
    fRoth_Stock_Amt = Math.round(fRoth_Beg_Bal_Amt * fStock_Pct);
    fRoth_Bond_Amt = fRoth_Beg_Bal_Amt - fRoth_Stock_Amt;

    fYou_Age  = fYou_Current_Age;
    fSpo_Age  = fSpo_Current_Age; 

    var fYearCnt        = 0;
    fScenario_Nbr++;

    oTax_Results = {taxable_income    : 0,
                    taxable_income_pre : 0,
                    inc_tax_amt       : 0,
                    senior_deduct_nbr : 0,
                    senior_deduct_amt : 0,
                    std_deduct_amt    : 0,
                    top_pct           : 0,
                    top_amt           : 0};
  
   oCapgains_Tax_Results = {taxable_income    : 0,
                            tax_amt           : 0};                 


   var fIRA_Distribution_Amt = 0;
   var fPension_Amt = 0;
   var fSocSec_Taxable_Amt = 0;
   var fSocSec_Taxable_Pct = 0;            
   var fAdjusted_Gross_Amt = 0;
   var fExemptions = 0; 
   var fStd_Deduct_Amt = 0;
   var fSenior_Deduct_Nbr = 0;
   var fSenior_Deduct_Amt = 0;                   
   var fTaxable_Income = 0;
   var fInc_Tax_Amt = 0;
   var fCapGains_Tax_Amt = 0;
   var fBas_End_Bal = 0;
   var fBonus_Amt = 0;
   var fBonus_Running_Total = 0;
   var fInfAdj_Budget_Running_Total = 0;

   

//*************************************************************************************************
//* reset inflation adjusted variables for first year in a scenario.  
//*************************************************************************************************
    infadj_std_deduct_married = stddeductmarried;
    infadj_std_deduct_single = stddeductsingle;
    infadj_senior_deduct_amt = senior_deduct_amt;

    for (ri=0; ri < TaxTableMarriedLen; ri++) 
     infadj_taxtable_married[ri] =       
        {from : taxtablemarried[ri].from, 
         thru : taxtablemarried[ri].thru};

    for (ri=0; ri < TaxTableSingleLen; ri++) 
     infadj_taxtable_single[ri] =       
        {from : taxtablesingle[ri].from, 
         thru : taxtablesingle[ri].thru};

    for (ri=0; ri < capgains_taxtable_len; ri++) 
      infadj_capgains_taxtable[ri] =       
        {from : capgains_taxtable[ri].from, 
         thru : capgains_taxtable[ri].thru};   
    
//***************************************************************************       *
//*
//* The below loop performs one time for each year in a scenario until 
//* until end of retirement or run out of money.
//*
//***************************************************************************
    for (var i=x; i <= x+fNbr_Years; i++)
       
      {
          fYearCnt = fYearCnt + 1; 

          fYou_SocSec_Amt = 0;
          fSpo_SocSec_Amt = 0;

         if (fYou_Age >= form.you_socsec_age.value)     
             {fYou_SocSec_Amt = fInfAdj_You_SocSec_Amt;}
          
         if(fSpo_Current_Age > 0)
              {if (fSpo_Age >= form.spo_socsec_age.value) 
                 {fSpo_SocSec_Amt = fInfAdj_Spo_SocSec_Amt;}}
              
//****************************************************************************************************
//* if you've passed away, spouse gets greater of your social security or spouse social security.
//* same holds true for spouse
//*****************************************************************************************************     
          if (fYou_Age > fFrm_You_Retire_End_Age) 
             {fYou_SocSec_Amt = 0;
              fSpo_SocSec_Amt = Math.max(fInfAdj_You_SocSec_Amt, fInfAdj_Spo_SocSec_Amt);}

          if (fSpo_Current_Age > 0)         
             {if (fSpo_Age > fFrm_Spo_Retire_End_Age) 
               {fSpo_SocSec_Amt = 0;
                fYou_SocSec_Amt = Math.max(fInfAdj_You_SocSec_Amt, fInfAdj_Spo_SocSec_Amt);}}

//****************************************************************************************************
//* if simulation includes a spouse and if one has passed away mid scenario, budget will be reduced to 75%
//*****************************************************************************************************     
          fBudget_Adj_Pct = cBudget_Full * 1;  
          if (fSpo_Current_Age > 0 && fSpo_Age > fFrm_Spo_Retire_End_Age) {fBudget_Adj_Pct = cBudget_Single_Adj * 1;}
          if (fYou_Age > fFrm_You_Retire_End_Age) {fBudget_Adj_Pct = cBudget_Single_Adj * 1;}

//********************************************************************************************************
//* determine if pension applies
//******************************************************************************************************

          var fUse_You_Pension_Amt = 0; 
          if (fFrm_You_Pension_Begin_Age > 0 && fYou_Age >= fFrm_You_Pension_Begin_Age) 
               {fUse_You_Pension_Amt = fInfAdj_You_Pension_Amt;
                if (fYou_Age > fFrm_You_Retire_End_Age)              
                    { fUse_You_Pension_Amt = 
                      Math.round(fUse_You_Pension_Amt * fFrm_You_Pension_Survivor_Pct);}                
               }

          var fUse_Spo_Pension_Amt = 0; 
          if (fFrm_Spo_Pension_Begin_Age > 0 && fSpo_Age >= fFrm_Spo_Pension_Begin_Age) 
               {fUse_Spo_Pension_Amt = fInfAdj_Spo_Pension_Amt;
                if (fSpo_Age > fFrm_Spo_Retire_End_Age)              
                    { fUse_Spo_Pension_Amt = 
                      Math.round(fUse_Spo_Pension_Amt * fFrm_Spo_Pension_Survivor_Pct);}                
               }

//*******************************************************************************************************************
//* start drawing down when both you and spouse have retired.
//* if drawing down, determine if go-go, slow-go, or no-go budget is being used
//* Total need to draw = Budget + Bonus + Income Tax + Capital gains tax - social security - pension
//********************************************************************************************************************
         fInfAdj_Budget_Amt = 0;
         fTotal_Need_Amt = 0;
         fUse_Mortgage_Budget_Amt = 0;        

        if (fYou_Age >= fYou_Retire_Age || (fSpo_Current_Age > 0 && fSpo_Age >= fSpo_Retire_Age))
             {
               if (fYou_Age <= fMortgage_End_Age) {fUse_Mortgage_Budget_Amt = fMortgage_Budget_Amt;}
               
               fInfAdj_Budget_Amt = fInfAdj_GoGo_Budget_Amt;
               if (fYou_Age >= 75) {fInfAdj_Budget_Amt = fInfAdj_SlowGo_Budget_Amt;}
               if (fYou_Age >= 85) {fInfAdj_Budget_Amt = fInfAdj_NoGo_Budget_Amt;}
               if (fLast_Alive == "you" && fYou_Age >= fLast3_Start_Age) {fInfAdj_Budget_Amt = fInfAdj_Last3_Budget_Amt;}
               if (fLast_Alive == "spouse" && fSpo_Age >= fLast3_Start_Age) {fInfAdj_Budget_Amt = fInfAdj_Last3_Budget_Amt;}
               
               fInfAdj_Budget_Amt = Math.round(fInfAdj_Budget_Amt * fBudget_Adj_Pct);  // make adjustment if one if deceased
               fTotal_Need_Amt = fInfAdj_Budget_Amt + fUse_Mortgage_Budget_Amt + fBonus_Amt + fInc_Tax_Amt + fCapGains_Tax_Amt 
                                 - fYou_SocSec_Amt - fSpo_SocSec_Amt 
                                 - fUse_You_Pension_Amt - fUse_Spo_Pension_Amt;
            }
//***********************************************************
//* determine # exemptions for tax purposes
//***********************************************************
          fExemptions = 1;

          fYou_Years_Deceased = 0;
          if (fYou_Age > fFrm_You_Retire_End_Age) {fYou_Years_Deceased = fYou_Age - fFrm_You_Retire_End_Age;}

          fSpo_Years_Deceased = 0;
          if (fSpo_Age > fFrm_Spo_Retire_End_Age) {fSpo_Years_Deceased = fSpo_Age - fFrm_Spo_Retire_End_Age;}

          if (fYou_Years_Deceased < 2 && fSpo_Years_Deceased <2 && fSpo_Current_Age > 0)
              {fExemptions++;}
                   
          fPension_Amt = fUse_You_Pension_Amt + fUse_Spo_Pension_Amt;
          fSocSec_Total_Amt = fYou_SocSec_Amt + fSpo_SocSec_Amt;
 
//***************************************************************************
//* determine how much to draw from each account 
//****************************************************************************
                   
          fRemain_Need_Amt = fTotal_Need_Amt;

          fYou_RMD_Draw_Amt = calc_rmd(fYou_Age, fYou_IRA_Beg_Bal_Amt);  // you RMD
          fYou_IRA_End_Bal_Amt1 = fYou_IRA_Beg_Bal_Amt - fYou_RMD_Draw_Amt;     
          
          fSpo_RMD_Draw_Amt = calc_rmd(fSpo_Age, fSpo_IRA_Beg_Bal_Amt);  // spouse RMD
          fSpo_IRA_End_Bal_Amt1 = fSpo_IRA_Beg_Bal_Amt - fSpo_RMD_Draw_Amt;
      
          fRemain_Need_Amt = fRemain_Need_Amt - fYou_RMD_Draw_Amt - fSpo_RMD_Draw_Amt;   
        
          fBrkrg_Draw_Amt1 = Math.min(fRemain_Need_Amt, fBrkrg_Beg_Bal_Amt);
          fBrkrg_End_Bal_Amt1 = fBrkrg_Beg_Bal_Amt - fBrkrg_Draw_Amt1;        
          fRemain_Need_Amt = fRemain_Need_Amt - fBrkrg_Draw_Amt1;

          fYou_IRA_Addl_Draw_Amt = Math.min(fRemain_Need_Amt, fYou_IRA_End_Bal_Amt1);
          fYou_IRA_End_Bal_Amt1 = fYou_IRA_End_Bal_Amt1 - fYou_IRA_Addl_Draw_Amt; 
          fRemain_Need_Amt = fRemain_Need_Amt - fYou_IRA_Addl_Draw_Amt;    
                   
          fSpo_IRA_Addl_Draw_Amt = Math.min(fRemain_Need_Amt, fSpo_IRA_End_Bal_Amt1);
          fSpo_IRA_End_Bal_Amt1 = fSpo_IRA_End_Bal_Amt1 - fSpo_IRA_Addl_Draw_Amt;
          fRemain_Need_Amt = fRemain_Need_Amt - fSpo_IRA_Addl_Draw_Amt;
                   
          fRoth_Draw_Amt1 = Math.min(fRemain_Need_Amt, fRoth_Beg_Bal_Amt);
          fRoth_End_Bal_Amt1 = fRoth_Beg_Bal_Amt - fRoth_Draw_Amt1;           
          fRemain_Need_Amt = fRemain_Need_Amt - fRoth_Draw_Amt1;    
                   
//***************************************************************************
//* see if roth conversion viable.  
//***************************************************************************                   

          fMax_Taxable_Income = 0;
          if (fExemptions ==2)
             {      
              if (fFrm_Roth_Conv_Pct == 10) fMax_Taxable_Income = infadj_taxtable_married[0].thru;   
              if (fFrm_Roth_Conv_Pct == 12) fMax_Taxable_Income = infadj_taxtable_married[1].thru;
             }
        
           if (fExemptions ==1)
             {      
              if (fFrm_Roth_Conv_Pct == 10) fMax_Taxable_Income = infadj_taxtable_single[0].thru;   
              if (fFrm_Roth_Conv_Pct == 12) fMax_Taxable_Income = infadj_taxtable_single[1].thru;
             }
        
                   
//**********************************************************************
//* preliminary calculate taxes to help determine if roth conversion viable
//**********************************************************************
                   
          fIRA_Distribution_Amt = fYou_RMD_Draw_Amt + fYou_IRA_Addl_Draw_Amt + fSpo_RMD_Draw_Amt + fSpo_IRA_Addl_Draw_Amt;
                   
          fIncome_Less_SS = fIRA_Distribution_Amt + fPension_Amt;

          fSocSec_Taxable_Amt = calc_socsec_taxable_func(fIncome_Less_SS, fSocSec_Total_Amt, fExemptions);                 
          fSocSec_Taxable_Pct = 0;
          if (fSocSec_Total_Amt > 0) {fSocSec_Taxable_Pct = Math.round((fSocSec_Taxable_Amt / fSocSec_Total_Amt)*100);}

          fAdjusted_Gross_Amt = fIncome_Less_SS + fSocSec_Taxable_Amt;

          oTax_Results =          calc_income_tax(fAdjusted_Gross_Amt, fExemptions, fYou_Age, fSpo_Age);
          
          fRoth_Conv_Amt = fMax_Taxable_Income - oTax_Results.taxable_income_pre;
        
          fYou_Roth_Conv_Amt = 0;
          fSpo_Roth_Conv_Amt = 0;
                   
          if (fFrm_Roth_Conv_Pct != 'none' && fRemain_Need_Amt == 0 && fRoth_Conv_Amt > 0 && fInfAdj_Budget_Amt > 0)
             {
              fYou_Roth_Conv_Amt = Math.min(fRoth_Conv_Amt, fYou_IRA_End_Bal_Amt1);
              fYou_IRA_Addl_Draw_Amt = fYou_IRA_Addl_Draw_Amt + fYou_Roth_Conv_Amt;
              fYou_IRA_End_Bal_Amt1 = fYou_IRA_End_Bal_Amt1 - fYou_Roth_Conv_Amt;       
              fRoth_Draw_Amt1 = fRoth_Draw_Amt1 - fYou_Roth_Conv_Amt;       
              fRoth_End_Bal_Amt1 = fRoth_End_Bal_Amt1 + fYou_Roth_Conv_Amt;
                   
              fRoth_Conv_Amt = fRoth_Conv_Amt - fYou_Roth_Conv_Amt;
              
              fSpo_Roth_Conv_Amt = Math.min(fRoth_Conv_Amt, fSpo_IRA_End_Bal_Amt1);
              fSpo_IRA_Addl_Draw_Amt = fSpo_IRA_Addl_Draw_Amt + fSpo_Roth_Conv_Amt;
              fSpo_IRA_End_Bal_Amt1 = fSpo_IRA_End_Bal_Amt1 - fSpo_Roth_Conv_Amt;
              fRoth_Draw_Amt1 = fRoth_Draw_Amt1 - fSpo_Roth_Conv_Amt;       
              fRoth_End_Bal_Amt1 = fRoth_End_Bal_Amt1 + fSpo_Roth_Conv_Amt;
            }

//**********************************************************************
//* final tax calculation.  taxes will be included in the budget for next year.
//**********************************************************************
                   
          fIRA_Distribution_Amt = fYou_RMD_Draw_Amt + fYou_IRA_Addl_Draw_Amt + fSpo_RMD_Draw_Amt + fSpo_IRA_Addl_Draw_Amt;
                   
          fIncome_Less_SS = fIRA_Distribution_Amt + fPension_Amt;

          fSocSec_Taxable_Amt = calc_socsec_taxable_func(fIncome_Less_SS, fSocSec_Total_Amt, fExemptions);                 
          fSocSec_Taxable_Pct = 0;
          if (fSocSec_Total_Amt > 0) {fSocSec_Taxable_Pct = Math.round((fSocSec_Taxable_Amt / fSocSec_Total_Amt)*100);}

          fAdjusted_Gross_Amt = fIncome_Less_SS + fSocSec_Taxable_Amt;

          oTax_Results =          calc_income_tax(fAdjusted_Gross_Amt, fExemptions, fYou_Age, fSpo_Age);
                   
          fCurYr_Taxable_Income = oTax_Results.taxable_income;
          fCurYr_Inc_Tax_Amt = oTax_Results.inc_tax_amt;

          fSenior_Deduct_Nbr = oTax_Results.senior_deduct_nbr; 
          fSenior_Deduct_Amt = oTax_Results.senior_deduct_amt;
          fStd_Deduct_Amt    = oTax_Results.std_deduct_amt;

//**************************************************************************************************************************************             
//*   adjust cost basis if updating brokerage balance       
//************************************************************************************************************************************       
         
          fBrkrg_Adj_Cost_Basis_Amt = 0;

          if (fBrkrg_Beg_Bal_Amt != 0 && fBrkrg_Draw_Amt1 > 0) 
             {fBrkrg_Adj_Cost_Basis_Amt = (Math.round((fBrkrg_Draw_Amt1 / fBrkrg_Beg_Bal_Amt) * 
                                           fBrkrg_Beg_Cost_Basis_Amt))*-1;}
          if (fBrkrg_Draw_Amt1 < 0) 
             {fBrkrg_Adj_Cost_Basis_Amt = fBrkrg_Draw_Amt1 * -1;}
          
           
//*************************************************************************************
//* calculate capital gains tax
//************************************************************************************
          
          fCapgains_Amt = 0;
          fCurYr_CapGains_Tax_Amt = 0;
          if (fBrkrg_Draw_Amt1 > 0) 
             {fCapgains_Amt = fBrkrg_Draw_Amt1 + fBrkrg_Adj_Cost_Basis_Amt;    
              oCapgains_Tax_Results = calc_capgains_tax(fAdjusted_Gross_Amt, 
                                                        fStd_Deduct_Amt + fSenior_Deduct_Amt, 
                                                        fCapgains_Amt, 
                                                        fExemptions);
              fCurYr_CapGains_Tax_Amt = oCapgains_Tax_Results.tax_amt
             }
               
 
//**************************************************************************************************************************************             
//* calculate gains, add deposits, and rebalance
//************************************************************************************************************************************       
          fYou_IRA_Ann_Dep_Amt = 0;
          fSpo_IRA_Ann_Dep_Amt = 0;
          fBrkrg_Ann_Dep_Amt = 0;
          fRoth_Ann_Dep_Amt = 0;

          if(fYou_Age < fYou_Retire_Age) {fYou_IRA_Ann_Dep_Amt = fFrm_You_IRA_Ann_Dep_Amt;}
          if(fSpo_Age < fSpo_Retire_Age) {fSpo_IRA_Ann_Dep_Amt = fFrm_Spo_IRA_Ann_Dep_Amt;}
          if(fYou_Age < fYou_Retire_Age) {fBrkrg_Ann_Dep_Amt = fFrm_Brkrg_Ann_Dep_Amt;}
          if(fYou_Age < fYou_Retire_Age) {fRoth_Ann_Dep_Amt = fFrm_Roth_Ann_Dep_Amt;}
                                  
//***********************************************************************************************************************    
//* 1) withdraw from account - done earlier, 2) reallocate 3) calculate gain 4) add deposit and gains 5) reallocate again
//* 
//* if testing year 1 (baseline plan), baseline rates can be overriden by user.
//***********************************************************************************************************************
    
          if (ratehistory[x].year == 1) 
               {
                ratehistory[i].stockret = fBaseline_Stock_Return_Pct;
                ratehistory[i].bondret = fBaseline_Bond_Return_Pct;
               }
    
    
          fYou_IRA_Stock_Amt = Math.round(fYou_IRA_End_Bal_Amt1 * fStock_Pct);
          fYou_IRA_Bond_Amt = fYou_IRA_End_Bal_Amt1 - fYou_IRA_Stock_Amt;
          fYou_IRA_Gain_Stock_Amt = Math.round(fYou_IRA_Stock_Amt * ratehistory[i].stockret);
          fYou_IRA_Gain_Bond_Amt  = Math.round(fYou_IRA_Bond_Amt * ratehistory[i].bondret);
          fYou_IRA_End_Bal_Amt2 = fYou_IRA_End_Bal_Amt1 + fYou_IRA_Gain_Stock_Amt + fYou_IRA_Gain_Bond_Amt
                                + fYou_IRA_Ann_Dep_Amt;
          fYou_IRA_Stock_Amt = Math.round(fYou_IRA_End_Bal_Amt2 * fStock_Pct);
          fYou_IRA_Bond_Amt = fYou_IRA_End_Bal_Amt2 - fYou_IRA_Stock_Amt;
                                   
          fSpo_IRA_Stock_Amt = Math.round(fSpo_IRA_End_Bal_Amt1 * fStock_Pct);
          fSpo_IRA_Bond_Amt = fSpo_IRA_End_Bal_Amt1 - fSpo_IRA_Stock_Amt;      
          fSpo_IRA_Gain_Stock_Amt = Math.round(fSpo_IRA_Stock_Amt * ratehistory[i].stockret);
          fSpo_IRA_Gain_Bond_Amt  = Math.round(fSpo_IRA_Bond_Amt * ratehistory[i].bondret);
          fSpo_IRA_End_Bal_Amt2 = fSpo_IRA_End_Bal_Amt1 + fSpo_IRA_Gain_Stock_Amt + fSpo_IRA_Gain_Bond_Amt
                                + fSpo_IRA_Ann_Dep_Amt;
          fSpo_IRA_Stock_Amt = Math.round(fSpo_IRA_End_Bal_Amt2 * fStock_Pct);
          fSpo_IRA_Bond_Amt = fSpo_IRA_End_Bal_Amt2 - fSpo_IRA_Stock_Amt;
      
          fBrkrg_Stock_Amt = Math.round(fBrkrg_End_Bal_Amt1 * fStock_Pct);
          fBrkrg_Bond_Amt = fBrkrg_End_Bal_Amt1 - fBrkrg_Stock_Amt;
          fBrkrg_Gain_Stock_Amt = Math.round(fBrkrg_Stock_Amt * ratehistory[i].stockret);
          fBrkrg_Gain_Bond_Amt  = Math.round(fBrkrg_Bond_Amt * ratehistory[i].bondret);
          fBrkrg_End_Bal_Amt2 = fBrkrg_End_Bal_Amt1 + fBrkrg_Gain_Stock_Amt + fBrkrg_Gain_Bond_Amt
                                + fBrkrg_Ann_Dep_Amt;
          fBrkrg_Stock_Amt = Math.round(fBrkrg_End_Bal_Amt2 * fStock_Pct);
          fBrkrg_Bond_Amt = fBrkrg_End_Bal_Amt2 - fBrkrg_Stock_Amt;
          
          fBrkrg_End_Cost_Basis_Amt = fBrkrg_Beg_Cost_Basis_Amt + fBrkrg_Adj_Cost_Basis_Amt + fBrkrg_Ann_Dep_Amt;                                
                                        
          fRoth_Stock_Amt = Math.round(fRoth_End_Bal_Amt1 * fStock_Pct);
          fRoth_Bond_Amt = fRoth_End_Bal_Amt1 - fRoth_Stock_Amt;      
          fRoth_Gain_Stock_Amt = Math.round(fRoth_Stock_Amt * ratehistory[i].stockret);
          fRoth_Gain_Bond_Amt  = Math.round(fRoth_Bond_Amt * ratehistory[i].bondret);
          fRoth_End_Bal_Amt2 = fRoth_End_Bal_Amt1 + fRoth_Gain_Stock_Amt + fRoth_Gain_Bond_Amt
                                + fRoth_Ann_Dep_Amt;
          fRoth_Stock_Amt = Math.round(fRoth_End_Bal_Amt2 * fStock_Pct);
          fRoth_Bond_Amt = fRoth_End_Bal_Amt2 - fRoth_Stock_Amt;
                
          fBeg_Bal = fYou_IRA_Beg_Bal_Amt + fSpo_IRA_Beg_Bal_Amt + fBrkrg_Beg_Bal_Amt + fRoth_Beg_Bal_Amt;
          fEnd_Bal = fYou_IRA_End_Bal_Amt2 + fSpo_IRA_End_Bal_Amt2 + fBrkrg_End_Bal_Amt2 + fRoth_End_Bal_Amt2;

          fTotal_Draw_Amt = fYou_RMD_Draw_Amt + fYou_IRA_Addl_Draw_Amt + fSpo_RMD_Draw_Amt + fSpo_IRA_Addl_Draw_Amt +
                            fBrkrg_Draw_Amt1 + fRoth_Draw_Amt1;
                                        
          fTotal_Ann_Dep_Amt = fYou_IRA_Ann_Dep_Amt + fSpo_IRA_Ann_Dep_Amt +
                            fBrkrg_Ann_Dep_Amt + fRoth_Ann_Dep_Amt;

          fTotal_Gain_Amt = fYou_IRA_Gain_Stock_Amt + fYou_IRA_Gain_Bond_Amt + 
                            fSpo_IRA_Gain_Stock_Amt + fSpo_IRA_Gain_Bond_Amt +
                            fBrkrg_Gain_Stock_Amt + fBrkrg_Gain_Bond_Amt + 
                            fRoth_Gain_Stock_Amt + fRoth_Gain_Bond_Amt;  
       
          fBas_End_Bal = 0;
          fBas_Diff = 0;
          if (ratehistory[x].year > 1) 
            {fBas_End_Bal = simulation_scenario[fYearCnt-1].end_bal
             if (fEnd_Bal > fBas_End_Bal)
                {fBas_Diff = fEnd_Bal - fBas_End_Bal;}
            }

          fBonus_Running_Total = fBonus_Running_Total + fBonus_Amt;
          fInfAdj_Budget_Running_Total = fInfAdj_Budget_Running_Total + fInfAdj_Budget_Amt + fUse_Mortgage_Budget_Amt;
        
//**********************************************************************************
//* compute a score for the scenario.  used to determine best, worst and median scenarios
//***********************************************************************************
          fScore_Age = (fYou_Age * 1000000000000) 
          
          fScore_Survived = 0;            
          if (fEnd_Bal > 0 ) {fScore_Survived = 1000000000;}
          
          fScore_Bonus = 0;
          if (fInfAdj_Budget_Running_Total > 0) {fScore_Bonus = Math.round((fBonus_Running_Total / fInfAdj_Budget_Running_Total) * 1000000);}
                   
          fScore_Years_Remain = 0;
          if (fInfAdj_Budget_Amt > 0) {fScore_Years_Remain = Math.round(fEnd_Bal / fInfAdj_Budget_Amt) * 1000;}
                     
          fScenario_Score =  fScore_Age + fScore_Survived + fScore_Bonus + fScore_Years_Remain;   
                            
//**************************************************************************************
//* save scenario / year calculation results
//**************************************************************************************
          simulation_scenario[fRowNbr] = 
                       {scenario_year :ratehistory[x].year,
                        year:    ratehistory[i].year,
                        you_age: fYou_Age,
                        spouse_age: fSpo_Age,
                        scenario_nbr: fScenario_Nbr,
                        yearcnt: fYearCnt,
                        budgetadj : fBudget_Adj_Pct,
                        infadj_budget_amt : fInfAdj_Budget_Amt,
                        infadj_budget_running_total : fInfAdj_Budget_Running_Total,
                        mortgage_budget_amt : fUse_Mortgage_Budget_Amt,

                        you_pension_amt : fUse_You_Pension_Amt,
                        spo_pension_amt : fUse_Spo_Pension_Amt,
                         
                        exemptions: fExemptions, 
                    
                        inc_tax_amt : fInc_Tax_Amt, 
                        capgains_tax_amt : fCapGains_Tax_Amt,
                        
                        curyr_inc_tax_amt : fCurYr_Inc_Tax_Amt,
                        curyr_taxable_income : fCurYr_Taxable_Income, 
                        
                        curyr_capgains_amt : fCapgains_Amt,
    
                        curyr_capgains_tax_amt : fCurYr_CapGains_Tax_Amt,
                    
                        you_socsec_amt: fYou_SocSec_Amt,
                        spo_socsec_amt: fSpo_SocSec_Amt,

                        total_need_amt      : fTotal_Need_Amt,
                        remain_need_amt     : fRemain_Need_Amt,

                        you_ira_beg_bal_amt   : fYou_IRA_Beg_Bal_Amt,
                        you_rmd_draw_amt      : fYou_RMD_Draw_Amt,
                        you_ira_addl_draw_amt : fYou_IRA_Addl_Draw_Amt,
                        you_ira_gain_amt      : fYou_IRA_Gain_Stock_Amt + fYou_IRA_Gain_Bond_Amt,
                        you_ira_ann_dep_amt   : fYou_IRA_Ann_Dep_Amt,
                        you_ira_end_bal_amt   : fYou_IRA_End_Bal_Amt2,

                        spo_ira_beg_bal_amt   : fSpo_IRA_Beg_Bal_Amt,
                        spo_rmd_draw_amt      : fSpo_RMD_Draw_Amt,
                        spo_ira_addl_draw_amt : fSpo_IRA_Addl_Draw_Amt,
                        spo_ira_gain_amt      : fSpo_IRA_Gain_Stock_Amt + fSpo_IRA_Gain_Bond_Amt,
                        spo_ira_ann_dep_amt   : fSpo_IRA_Ann_Dep_Amt,
                        spo_ira_end_bal_amt   : fSpo_IRA_End_Bal_Amt2,

                        brkrg_beg_bal_amt  : fBrkrg_Beg_Bal_Amt,
                        brkrg_draw_amt1    : fBrkrg_Draw_Amt1,
                        brkrg_gain_amt     : fBrkrg_Gain_Stock_Amt + fBrkrg_Gain_Bond_Amt,
                        brkrg_ann_dep_amt   : fBrkrg_Ann_Dep_Amt,
                        brkrg_end_bal_amt  : fBrkrg_End_Bal_Amt2,
    
                        brkrg_beg_cost_basis_amt : fBrkrg_Beg_Cost_Basis_Amt,
                        brkrg_adj_cost_basis_amt : fBrkrg_Adj_Cost_Basis_Amt,
                        brkrg_end_cost_basis_amt : fBrkrg_End_Cost_Basis_Amt,
          
                        roth_beg_bal_amt  : fRoth_Beg_Bal_Amt,
                        roth_draw_amt1    : fRoth_Draw_Amt1,
                        roth_gain_amt     : fRoth_Gain_Stock_Amt + fRoth_Gain_Bond_Amt,
                        roth_ann_dep_amt   : fRoth_Ann_Dep_Amt,
                        roth_end_bal_amt  : fRoth_End_Bal_Amt2,

                        beg_bal            : fBeg_Bal,  
                        total_draw_amt    : fTotal_Draw_Amt,
                        total_gain_amt    : fTotal_Gain_Amt,
                        total_ann_dep_amt : fTotal_Ann_Dep_Amt,
                        end_bal            : fEnd_Bal,
                        bas_end_bal        : fBas_End_Bal,
                        bonus_amt          : fBonus_Amt,
                        bonus_running_total : fBonus_Running_Total, 
    
                        you_roth_conv_amt : fYou_Roth_Conv_Amt,
                        spo_roth_conv_amt : fSpo_Roth_Conv_Amt,

                        scenario_score      : fScenario_Score,

                        stockret:  ratehistory[i].stockret,
                        bondret:   ratehistory[i].bondret,
                        infrate: ratehistory[i].infrate,

                        
                        ira_distribution_amt: fIRA_Distribution_Amt,
                        pension_amt         : fPension_Amt,
                        socsec_taxable_amt  : fSocSec_Taxable_Amt,
                        socsec_taxable_pct  : fSocSec_Taxable_Pct,            
                        adjusted_gross_amt  : fAdjusted_Gross_Amt,
                        std_deduct_nbr      : fExemptions, 
                        std_deduct_amt      : fStd_Deduct_Amt,
                        senior_deduct_nbr  : fSenior_Deduct_Nbr,
                        senior_deduct_amt   : fSenior_Deduct_Amt,                   
                        
                        stddeductmarried : infadj_std_deduct_married,
                        stddeductsingle  : infadj_std_deduct_single,
                        taxtablemarried0 : infadj_taxtable_married[0].thru,
                        taxtablemarried1 : infadj_taxtable_married[1].thru,
                        taxtablemarried2 : infadj_taxtable_married[2].thru,
                        taxtablemarried3 : infadj_taxtable_married[3].thru,
                        taxtablemarried4 : infadj_taxtable_married[4].thru,
                        taxtablemarried5 : infadj_taxtable_married[5].thru,
                        taxtablemarried6 : infadj_taxtable_married[6].thru,
                        taxtablesingle0 : infadj_taxtable_single[0].thru,
                        taxtablesingle1 : infadj_taxtable_single[1].thru,
                        taxtablesingle2 : infadj_taxtable_single[2].thru,
                        taxtablesingle3 : infadj_taxtable_single[3].thru,
                        taxtablesingle4 : infadj_taxtable_single[4].thru,
                        taxtablesingle5 : infadj_taxtable_single[5].thru,
                        taxtablesingle6 : infadj_taxtable_single[6].thru,
                        captaxtable0_file_status : infadj_capgains_taxtable[0].file_status,
                        captaxtable0_thru : infadj_capgains_taxtable[0].thru,
                        captaxtable1_file_status : infadj_capgains_taxtable[1].file_status,
                        captaxtable1_thru : infadj_capgains_taxtable[1].thru,
                        captaxtable2_file_status : infadj_capgains_taxtable[2].file_status,
                        captaxtable2_thru : infadj_capgains_taxtable[2].thru,
                        captaxtable3_file_status : infadj_capgains_taxtable[3].file_status,
                        captaxtable3_thru : infadj_capgains_taxtable[3].thru,
                        captaxtable4_file_status : infadj_capgains_taxtable[4].file_status,
                        captaxtable4_thru : infadj_capgains_taxtable[4].thru,
                        captaxtable5_file_status : infadj_capgains_taxtable[5].file_status,
                        captaxtable5_thru : infadj_capgains_taxtable[5].thru,
                        
                       };

//**********************************************************************************
//* current yr taxes will be included in budget for next year.
//**********************************************************************************

         fInc_Tax_Amt = fCurYr_Inc_Tax_Amt;
         fCapGains_Tax_Amt = fCurYr_CapGains_Tax_Amt;                   
                   
//*************************************************************************************
//* calculate bonus amount
//************************************************************************************
                   
           if (fTotal_Need_Amt > 0) {fBonus_Amt = Math.round(fBas_Diff * fBonus_Pct);}
   
//************************************************************************
//* inflation adjustments : social security, budget, pension, tax tables 
//************************************************************************

          fInfAdj_You_SocSec_Amt  = Math.round(fInfAdj_You_SocSec_Amt * (1+ratehistory[i].infrate));
          fInfAdj_Spo_SocSec_Amt  = Math.round(fInfAdj_Spo_SocSec_Amt * (1+ratehistory[i].infrate));

          fInfAdj_GoGo_Budget_Amt = Math.round(fInfAdj_GoGo_Budget_Amt  * (1+ratehistory[i].infrate));
          fInfAdj_SlowGo_Budget_Amt = Math.round(fInfAdj_SlowGo_Budget_Amt  * (1+ratehistory[i].infrate));
          fInfAdj_NoGo_Budget_Amt = Math.round(fInfAdj_NoGo_Budget_Amt  * (1+ratehistory[i].infrate));
          fInfAdj_Last3_Budget_Amt = Math.round(fInfAdj_Last3_Budget_Amt  * (1+ratehistory[i].infrate));

          if (fFrm_You_Pension_Begin_Age > 0 && fYou_Age >= fFrm_You_Pension_Begin_Age)  
               {fInfAdj_You_Pension_Amt = Math.round(fInfAdj_You_Pension_Amt * (1+fFrm_You_Pension_Inf_Pct));}

          if (fFrm_Spo_Pension_Begin_Age > 0 && fSpo_Age >= fFrm_Spo_Pension_Begin_Age)
             {fInfAdj_Spo_Pension_Amt = Math.round(fInfAdj_Spo_Pension_Amt * (1+fFrm_Spo_Pension_Inf_Pct));}
       
          infadj_tax_variables_func(ratehistory[i].infrate);          

//************************************************************************
//* set beginning balances for next year from ending balance in current year 
//************************************************************************          
          fYou_IRA_Beg_Bal_Amt = fYou_IRA_End_Bal_Amt2;
          fSpo_IRA_Beg_Bal_Amt = fSpo_IRA_End_Bal_Amt2;
          fBrkrg_Beg_Bal_Amt = fBrkrg_End_Bal_Amt2;
          fBrkrg_Beg_Cost_Basis_Amt = fBrkrg_End_Cost_Basis_Amt;
          fRoth_Beg_Bal_Amt = fRoth_End_Bal_Amt2;
                   
          fRowNbr++;
          fYou_Age++;
          if (fSpo_Current_Age > 0) {fSpo_Age++};

//***********************************************************************************************
//* if total ending balance for this scneario is 0, finish this scenario and go to next scenario
//************************************************************************************************
          if (fEnd_Bal <= 0)
            {
               scenario_summary[fScenario_Nbr-1] = simulation_scenario[fRowNbr-1];
               fFailure_Nbr = fFailure_Nbr + 1;
               break;
            } 
        
      }
//***********************************************************************************************
//* if falls out of inside loop, means scenario got to end without running out of money.  
//************************************************************************************************
         fSurvive_Cnt++;
         scenario_summary[fScenario_Nbr-1] = simulation_scenario[fRowNbr-1];   
   }  

//***********************************************************************************************
//* if falls out of outside loop, means all scenarios simulated - now time to report results.
//************************************************************************************************
    
    var today = new Date();
    var date = today.getFullYear()+'-'+(today.getMonth()+1)+'-'+today.getDate();
    var time = today.getHours() + ":" + today.getMinutes() + ":" + today.getSeconds();
    var dateTime = date+' '+time;

    var fSuccessNbr = fScenario_Nbr - fFailure_Nbr;
    var fSuccessRate = Math.round((fSuccessNbr / fScenario_Nbr) * 100);

    var TableResults = "<h3> RPS Simulation Results - " + dateTime + "</h3>";

    TableResults = TableResults + fScenario_Nbr + " scenarios simulated ";  
    TableResults = TableResults + " of which " + fSuccessNbr + " passed for a success rate of ";
    TableResults = TableResults + fSuccessRate + "%.  Scenario test is considered successful if ending balance is greater than zero at the end of the scenario simulation. </p>";   

//    TableResults = TableResults + "<p> For your baseline plan, ";
//    TableResults = TableResults + "your money would have lasted until your age ";
//    TableResults = TableResults + scenario_summary[0].you_age + " and you would have had ";
//    TableResults = TableResults + addcomma(scenario_summary[0].end_bal) + " total remaining balance. </p>";

//*****************************************************************************************
//* sort scenario summary results worst to best
//****************************************************************************************    
    scenario_summary.sort(function(a, b){return a.scenario_score - b.scenario_score});

    fMedian_Scenario = Math.round(fScenario_Nbr / 2);
    if (scenario_summary[fMedian_Scenario].scenario_year == 1) {fMedian_Scenario++;}

    fWorst_Case_Scenario = 0;
    if (scenario_summary[fWorst_Case_Scenario].scenario_year == 1) {fWorst_Case_Scenario++;}
    
    fBest_Case_Scenario = fScenario_Nbr - 1; 
    if (scenario_summary[fBest_Case_Scenario].scenario_year == 1) {fMedian_Scenario--;}

    fWorst_Year=scenario_summary[fWorst_Case_Scenario].scenario_year;
    fBest_Year=scenario_summary[fBest_Case_Scenario].scenario_year;
    fMedian_Year=scenario_summary[fMedian_Scenario].scenario_year;


//    TableResults = TableResults + "<p> Worst case scenario is if you would have retired in ";
//    TableResults = TableResults + scenario_summary[fWorst_Case_Scenario].scenario_year + " - your money would have lasted until your age ";
//    TableResults = TableResults + scenario_summary[fWorst_Case_Scenario].you_age + " and you would have had ";
//    TableResults = TableResults + addcomma(scenario_summary[fWorst_Case_Scenario].end_bal) + " remaining balance in your accounts. </p>";

//    TableResults = TableResults + "<p> Best case scenario is if you would have retired in ";
//    TableResults = TableResults + scenario_summary[fBest_Case_Scenario].scenario_year + " - your money would have lasted until your age ";
//    TableResults = TableResults + scenario_summary[fBest_Case_Scenario].you_age + " and you would have had ";
//    TableResults = TableResults + addcomma(scenario_summary[fBest_Case_Scenario].end_bal) + " remaining balance in your accounts. </p>";

//   TableResults = TableResults + "<p> Median scenario is if you would have retired in ";
//    TableResults = TableResults + scenario_summary[fMedian_Scenario].scenario_year + " - your money would have lasted until your age ";
//    TableResults = TableResults + scenario_summary[fMedian_Scenario].you_age + " and you would have had ";/
//    TableResults = TableResults + addcomma(scenario_summary[fMedian_Scenario].end_bal) + " remaining balance in your accounts. </p>";
 
        
    fMost_Recent_Year = fCurrent_Year - fNbr_Years - 1;                       
    TableResults = showscenarioresults(TableResults, scenario_summary, fFrm_You_Retire_End_Age, fNbr_Years,fWorst_Year,fBest_Year,fMedian_Year, fMost_Recent_Year);

    if (fDownload_Results == "YES")
         {download_simulation_result_summary(scenario_summary, fFrm_You_Retire_End_Age, fNbr_Years); }
       
    TableResults = showdetails(TableResults,simulation_scenario, 1);

    TableResults = showdetails(TableResults,simulation_scenario, fWorst_Year);
 
    TableResults = showdetails(TableResults,simulation_scenario, fMedian_Year);
  
    TableResults = showdetails(TableResults,simulation_scenario, fBest_Year);

    document.getElementById("showresults").innerHTML = " ";
    
//    window.scrollTo(0, 700);
    
   if (fDownload_Results == "YES")
        {download_simulation_result_detail(simulation_scenario); }
     
   openWin(TableResults);   
    
 }
</script>

<script>

function openWin(TableResults) {
try {
  myWindow.close();
 }
  catch (err)
      {   }
  myWindow = window.open("", "myWindow", "_blank", "toolbar=yes,scrollbars=yes,resizable=yes,top=500,left=500,width=400,height=400");
  myWindow.document.write(TableResults);
}

function closeWin() {
  myWindow.close();
}
</script>          
          
          
                   
<script type="text/javascript"> 
    function showdetails(TableResults, simulation_scenario, fYear) {
 

      var fsimulation_scenarioLen = simulation_scenario.length;

//      TableResults = TableResults + '<table class="center"; style="width:100%">';
      TableResults = TableResults + '<table class="center">';

      TableResults = TableResults + 
      "<style> table, th, td {border: 1px solid black; border-collapse: separate; padding: 20x; } </style>";

      fCaption =  '<caption style="text-align:left"> <h3> Simulation using Baseline Rates </h3></caption>';
      
      if (fYear != 1) 
	  {fCaption = '<caption style="text-align:left"> <h3> Simulation using rates starting in ' + fYear + '</h3></caption>';}
      
      TableResults = TableResults + fCaption;
        
    
       TableResults = TableResults + "<tr> " + 
                          '<th colspan="3" style="background-color:#66ff66">Age</th> ' +
                          '<th colspan="5" style="background-color:#e6ecff">Spend Plan</th> ' +
                          '<th colspan="4" style="background-color:#ff66ff">Total Income</th> ' +
                          '<th colspan="1"> </th> ' +
                          '<th colspan="4" style="background-color:#666699">Withdraw Strategy </th> ' +
                          '<th colspan="5" style="background-color:#E18973">Summary Account Activity</th> ' +
                          '<th colspan="4"> </th> ' +
                          '<th colspan="6" style="background-color:#33C0FF">You IRA Account Activity</th> ' +
                          '<th colspan="6" style="background-color:#D833FF">Spouse IRA Account Activity</th> ' +
                          '<th colspan="8" style="background-color:#33FF95">Brokerage Account Activity</th> ' +
                          '<th colspan="7" style="background-color:#FF9A33">Roth Account Activity</th> ' +
                          '<th colspan="11" style="background-color:#5F9EA0">Federal Income Tax Calculations</th> ' +
                          '<th colspan="14" style="background-color:#5F9EA0">Federal Tax Brackets</th> ' +
                          '<th colspan="9" style="background-color:#999966">Capital Gains Tax Calculation</th> ' +
                          '<th colspan="6" style="background-color:#999966">Capital Gains Tax Brackets</th> ' +
                          " </tr> " ;
                         
      
      TableResults = TableResults + "<tr> " + 
                         '<th style="background-color:#66ff66">Year</th> ' +
                         '<th style="background-color:#66ff66">You</th> ' +
                         '<th style="background-color:#66ff66">Spouse</th> ' +
                         '<th style="background-color:#e6ecff">Budget</th> ' +
                         '<th style="background-color:#e6ecff">Mortgage</th> ' +
                         '<th style="background-color:#e6ecff">Bonus</th> ' +
                         
                         '<th style="background-color:#e6ecff">Inc Tax</th> ' + 
                         '<th style="background-color:#e6ecff">Cap Gains Tax</th> ' + 
                         '<th style="background-color:#ff66ff">You Soc Sec</th> ' +
                         '<th style="background-color:#ff66ff">Spouse Soc Sec</th> ' +
                         '<th style="background-color:#ff66ff">You Pension</th> ' +
                         '<th style="background-color:#ff66ff">Spouse Pension</th> ' +
                         '<th>Withdraw From Savings</th> ' +
          
                          '<th style="background-color:#666699">You IRA</th> ' +
                          '<th style="background-color:#666699">Spouse IRA</th> ' +
                          '<th style="background-color:#666699">Brokerage</th> ' +
                          '<th style="background-color:#666699">Roth HSA</th> ' +
          
          
// summary account info          
                         '<th style="background-color:#E18973">Beg Bal</th> ' +
                         '<th style="background-color:#E18973">Withdraw</th> ' +
                         '<th style="background-color:#E18973">Gain (Loss)</th> ' +
                         '<th style="background-color:#E18973">Deposit</th> ' +
                         '<th style="background-color:#E18973">End Bal</th> ' +
          
                         '<th style="background-color:#FFFF99">Baseline</th> ' +
	                 "<th>Stock Ret</th> " + 
                         "<th>Bond Ret</th> " +      
                         "<th>Inf Rate</th> " +

// you ira info
                         '<th style="background-color:#33C0FF">Beg Bal </th> ' +
                         '<th style="background-color:#33C0FF">Draw RMD </th> ' +
                         '<th style="background-color:#33C0FF">Draw Addl </th> ' +
                         '<th style="background-color:#33C0FF">Gain / Loss</th> ' +
                         '<th style="background-color:#33C0FF">Deposit </th> ' +
                         '<th style="background-color:#33C0FF">End Bal </th> ' +
// Spouse IRA activity
                         '<th style="background-color:#D833FF">Beg Bal </th> ' +
                         '<th style="background-color:#D833FF">Draw RMD </th> ' +
                         '<th style="background-color:#D833FF">Draw Addl </th> ' +
                         '<th style="background-color:#D833FF">Gain / Loss</th> ' +
                         '<th style="background-color:#D833FF">Deposit </th> ' +
                         '<th style="background-color:#D833FF">End Bal </th> ' +
// brokerage account activity          
                         '<th style="background-color:#33FF95">Beg Bal </th> ' +
                         '<th style="background-color:#33FF95">Draw / Deposit</th> ' +
                         '<th style="background-color:#33FF95">Gain / Loss</th> ' +
                         '<th style="background-color:#33FF95">Deposit </th> ' +
                         '<th style="background-color:#33FF95">End Bal </th> ' +

                         '<th style="background-color:#E6FFE6">Beg Cost Basis </th> ' +
                         '<th style="background-color:#E6FFE6">Adj Cost Basis </th> ' +
                         '<th style="background-color:#E6FFE6">End Cost Basis </th> ' +
// Roth account activity                        
                         '<th style="background-color:#FF9A33">Beg Bal </th> ' +
                         '<th style="background-color:#FF9A33">Draw / Deposit </th> ' +
                         '<th style="background-color:#FF9A33">Gain / Loss</th> ' +
                         '<th style="background-color:#FF9A33">Deposit </th> ' +
                         '<th style="background-color:#FF9A33">End Bal </th> ' +
                         '<th style="background-color:#fff0e6">Conv You </th> ' +
                         '<th style="background-color:#fff0e6">Conv Spouse </th> ' +
                                     
// income tax calcultion 
                         '<th style="background-color:#5F9EA0">IRA Draw</th> ' +
                         '<th style="background-color:#5F9EA0">Pension</th> ' +
                         '<th style="background-color:#5F9EA0">SS Taxable Amt </th> ' +
                         '<th style="background-color:#5F9EA0">SS Taxable Pct </th> ' +
                         '<th style="background-color:#5F9EA0">Adjusted Gross </th> ' +
                         '<th style="background-color:#5F9EA0">Std Deduct Nbr </th> ' +
                         '<th style="background-color:#5F9EA0">Std Deduct Amt </th> ' +
                         '<th style="background-color:#5F9EA0">Sr Deduct Nbr </th> ' +
                         '<th style="background-color:#5F9EA0">Sr Deduct Amt </th> ' +
                         '<th style="background-color:#5F9EA0">Taxable Income</th> ' +
                         '<th style="background-color:#5F9EA0">Est Tax</th> ' +   

  
                         "<th>Tax Married 10%</th> " +
                         "<th>Tax Married 12%</th> " +
                         "<th>Tax Married 22%</th> " +
                         "<th>Tax Married 24%</th> " +
                         "<th>Tax Married 32%</th> " +
                         "<th>Tax Married 35%</th> " + 
                         "<th>Tax Married 37%</th> " +
                         "<th>Tax Single 10%</th> " +
                         "<th>Tax Single 12%</th> " +
                         "<th>Tax Single 22%</th> " +
                         "<th>Tax Single 24%</th> " +
                         "<th>Tax Single 32%</th> " +
                         "<th>Tax Single 35%</th> " +
                         "<th>Tax Single 37%</th> " +
// capital gains tax calculation
          
                         '<th style="background-color:#999966">Adj Gross</th> ' + 
                         '<th style="background-color:#999966">Std Ded Nbr</th> ' + 
                         '<th style="background-color:#999966">Std Ded Amt</th> ' + 
                         '<th style="background-color:#999966">Sr Ded Nbr</th> ' + 
                         '<th style="background-color:#999966">Sr Ded Amt</th> ' + 
                         '<th style="background-color:#999966">Brkg Withdraw</th> ' + 
                         '<th style="background-color:#999966">Adj Cost Basis</th> ' + 
                         '<th style="background-color:#999966">Cap Gains</th> ' + 
                         '<th style="background-color:#999966">Cap Gains Tax</th> ' +  
                         
                         "<th>Tax Married 0%</th> " +
                         "<th>Tax Married 15%</th> " +
                         "<th>Tax Married 20%</th> " +

                         "<th>Tax Single 0%</th> " +
                         "<th>Tax Single 15%</th> " +
                         "<th>Tax Single 20%</th> " +
          
                         " </tr> " ;
     
      for (var i=0; i<fsimulation_scenarioLen; i++)
       
      {
         if (simulation_scenario[i].scenario_year == fYear)
          {
           fStockColor = setcolor(simulation_scenario[i].stockret);
           fGainColor = setcolor(simulation_scenario[i].total_gain_amt);
           fRoth_Background_Color = setbackgroundcolor(simulation_scenario[i].roth_draw_amt1);  
              
           fYou_IRA_Draw_Amt = simulation_scenario[i].you_rmd_draw_amt + simulation_scenario[i].you_ira_addl_draw_amt;
           fSpo_IRA_Draw_Amt = simulation_scenario[i].spo_rmd_draw_amt + simulation_scenario[i].spo_ira_addl_draw_amt;
              
                         
           TableResults = TableResults + "<tr>" +  
           '<td align = "right"> ' + simulation_scenario[i].year  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].you_age  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].spouse_age  + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].infadj_budget_amt)  + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].mortgage_budget_amt)  + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].bonus_amt)  + " </td> " +
           
           '<td align = "right"> ' + simulation_scenario[i].inc_tax_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].capgains_tax_amt  + " </td> " +           


           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_socsec_amt)  + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_socsec_amt)  + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_pension_amt)  + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_pension_amt)  + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].total_need_amt)   + " </td> " +
               
           '<td align = "right"> ' + addcomma(fYou_IRA_Draw_Amt * -1)+"</td> " +       
           '<td align = "right"> ' + addcomma(fSpo_IRA_Draw_Amt * -1)+"</td> " +       
           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_draw_amt1 * -1)+"</td> " +      
           '<td ' + fRoth_Background_Color + '> ' + addcomma(simulation_scenario[i].roth_draw_amt1 * -1)+"</td> " +      
                  
           '<td align = "right"> ' + addcomma(simulation_scenario[i].beg_bal)   + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].total_draw_amt * -1)   + " </td> " +
           '<td ' + fGainColor + ' align = "right"> ' + addcomma(simulation_scenario[i].total_gain_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].total_ann_dep_amt)   + " </td> " +    
           '<td align = "right"> ' + addcomma(simulation_scenario[i].end_bal)   + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].bas_end_bal)   + " </td> " +
             
           '<td ' + fStockColor + ' align = "right"> ' + (Math.round(simulation_scenario[i].stockret * 10000)/100) + "%"+ " </td> " +
           '<td align = "right"> ' + (Math.round(simulation_scenario[i].bondret * 10000)/100)  + "%"+ " </td> " +
           '<td align = "right"> ' + (Math.round(simulation_scenario[i].infrate * 10000)/100)  + "%"+ " </td> " +


           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_ira_beg_bal_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_rmd_draw_amt * -1) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_ira_addl_draw_amt * -1) + " </td> " +
           '<td ' + fGainColor + ' align = "right"> ' + addcomma(simulation_scenario[i].you_ira_gain_amt) + " </td> " +
            '<td align = "right"> ' + addcomma(simulation_scenario[i].you_ira_ann_dep_amt) + " </td> " +      
           '<td align = "right"> ' + addcomma(simulation_scenario[i].you_ira_end_bal_amt) + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_ira_beg_bal_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_rmd_draw_amt * -1) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_ira_addl_draw_amt * -1) + " </td> " +
           '<td ' + fGainColor + ' align = "right"> ' + addcomma(simulation_scenario[i].spo_ira_gain_amt) + " </td> " +
            '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_ira_ann_dep_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_ira_end_bal_amt) + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_beg_bal_amt) + " </]td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_draw_amt1 * -1) + " </td> " +
           '<td ' + fGainColor + ' align = "right"> ' + addcomma(simulation_scenario[i].brkrg_gain_amt) + " </td> " +
            '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_ann_dep_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_end_bal_amt) + " </td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_beg_cost_basis_amt) + " </]td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_adj_cost_basis_amt) + " </]td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].brkrg_end_cost_basis_amt) + " </]td> " +

           '<td align = "right"> ' + addcomma(simulation_scenario[i].roth_beg_bal_amt)    + " </]td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].roth_draw_amt1 * -1)      + " </td> " +
           '<td ' + fGainColor + ' align = "right"> ' + addcomma(simulation_scenario[i].roth_gain_amt)       + " </td> " +
            '<td align = "right"> ' + addcomma(simulation_scenario[i].roth_ann_dep_amt) + " </td> " +   
           '<td align = "right"> ' + addcomma(simulation_scenario[i].roth_end_bal_amt)    + " </td> " +
            '<td align = "right"> ' + addcomma(simulation_scenario[i].you_roth_conv_amt) + " </td> " +
           '<td align = "right"> ' + addcomma(simulation_scenario[i].spo_roth_conv_amt) + " </td> " +
          
           '<td align = "right"> ' + simulation_scenario[i].ira_distribution_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].pension_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].socsec_taxable_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].socsec_taxable_pct  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].adjusted_gross_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].std_deduct_nbr  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].std_deduct_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].senior_deduct_nbr  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].senior_deduct_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].curyr_taxable_income  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].curyr_inc_tax_amt  + " </td> " +

           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried0    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried1    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried2    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried3    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried4    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablemarried5    + " </td> " +
           '<td align = "right"> ' + 'unlimited'    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle0    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle1    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle2    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle3    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle4    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].taxtablesingle5    + " </td> " +
           '<td align = "right"> ' + 'unlimited'    + " </td> " +
            
           '<td align = "right"> ' + simulation_scenario[i].adjusted_gross_amt    + " </td> " +    
           '<td align = "right"> ' + simulation_scenario[i].std_deduct_nbr  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].std_deduct_amt  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].senior_deduct_nbr  + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].senior_deduct_amt  + " </td> " +
           '<td align = "right"> ' + (simulation_scenario[i].brkrg_draw_amt1 * -1) + " </td> " +       
           '<td align = "right"> ' + simulation_scenario[i].brkrg_adj_cost_basis_amt + " </]td> " +
           '<td align = "right"> ' + simulation_scenario[i].curyr_capgains_amt + " </]td> " +
           '<td align = "right"> ' + simulation_scenario[i].curyr_capgains_tax_amt + " </]td> " +
    
           '<td align = "right"> ' + simulation_scenario[i].captaxtable0_thru    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].captaxtable1_thru    + " </td> " +
           '<td align = "right"> ' + 'unlimited'   + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].captaxtable3_thru    + " </td> " +
           '<td align = "right"> ' + simulation_scenario[i].captaxtable4_thru    + " </td> " +
           '<td align = "right"> ' + 'unlimited'    + " </td> " +

           " </tr>" ;


          }
       }      

      TableResults = TableResults + "</table>";
       
      return TableResults;
 }
</script>

<script type="text/javascript">
 function showscenarioresults(TableResults, scenario_summary, fFrm_You_Retire_End_Age, fNbr_Years,fWorst_Year, fBest_Year, fMedian_Year,fMost_Recent_Year) {

      scenario_summary.sort(function(a, b){return a.scenario_year - b.scenario_year});      

      fscenario_summary_len = scenario_summary.length;

      TableResults = TableResults + '<table class="center"; style="width:75%">';

      TableResults = TableResults + 
      "<style> table, th, td {border: 1px solid black; border-collapse: collapse; } </style>";

      TableResults = TableResults + 
         "<caption><h3>Simulation Hightlights</h3></caption>";
   
      TableResults = TableResults + "<tr> " + 
                    '<th style="background-color:#e0e0eb">Simulated Scenario</th> ' +
                    '<th style="background-color:#e0e0eb">Scenario Status</th> ' +
                    '<th style="background-color:#e0e0eb">Simulation Result</th> ' +
                    '<th style="background-color:#e0e0eb">Budget Spent</th> ' +
                    '<th style="background-color:#e0e0eb">Bonus Earned</th> ' +
                    '<th style="background-color:#e0e0eb">Avg Bonus </th> ' +
                    '<th style="background-color:#e0e0eb">Last Year Withdraw </th> ' +
                    '<th style="background-color:#e0e0eb">End Bal </th> ' +
                    '<th style="background-color:#e0e0eb">Years Remain </th> ' +
                    " </tr> " ;
     
      for (var i=0; i<fscenario_summary_len; i++)
       
      {
           fScenario_Status = "Success";
           fShow = "N";
           if (scenario_summary[i].end_bal == 0) {fScenario_Status = "Failed Case"; fShow = "Y";}
           if (scenario_summary[i].scenario_year == fWorst_Year) {fScenario_Status = "Worst Case"; fShow="Y";}
           if (scenario_summary[i].scenario_year == fBest_Year) {fScenario_Status = "Best Case"; fShow="Y";}
           if (scenario_summary[i].scenario_year == fMedian_Year) {fScenario_Status = "Median Case"; fShow="Y";}
           if (scenario_summary[i].scenario_year == 1) {fScenario_Status = "Baseline Plan"; fShow="Y";}
           if (scenario_summary[i].scenario_year == fMost_Recent_Year) {fScenario_Status = "Recent Case"; fShow="Y";}
           
           if (fShow == "Y")
            {   
              fYears_Remain = Math.round(scenario_summary[i].end_bal / scenario_summary[i].infadj_budget_amt); 
              fBackGround = 'style="background-color:#ffffff">'; // default white 
              if (scenario_summary[i].end_bal == 0) 
               {fBackGround = 'style="background-color:#ffff00">'};  // set to yellow "background-color:#FF0000"

              fScenarioRange = scenario_summary[i].scenario_year + " thru " + (scenario_summary[i].scenario_year + fNbr_Years);
              if (scenario_summary[i].scenario_year == 1) {fScenarioRange = "Baseline";}
           
              fResult = "Success!" 
              if (scenario_summary[i].end_bal == 0) {fResult = "Savings exhausted in " + (scenario_summary[i].year);}

              TableResults = TableResults + "<tr " +  fBackGround + 
           
              '<td align = "center"> ' + fScenarioRange  + " </td> " +
              '<td align = "center"> ' + fScenario_Status  + " </td> " +
              
              '<td align = "center"> ' + fResult  + " </td> " +
              '<td align = "center"> '  + addcomma(scenario_summary[i].infadj_budget_running_total) + "</td> " +
              '<td align = "center"> '  + addcomma(scenario_summary[i].bonus_running_total) + "</td> " +
              '<td align = "center"> '  + Math.round((scenario_summary[i].bonus_running_total /
                                                   scenario_summary[i].infadj_budget_running_total)*100) + "%"      
                                                     + "</td> " +  
              '<td align = "center"> '  + addcomma(scenario_summary[i].infadj_budget_amt) + "</td> " +
              '<td align = "center"> '  + addcomma(scenario_summary[i].end_bal) + "</td> " +
              '<td align = "center"> ' + fYears_Remain  + " </td> " +
              " </tr>" ;
            }

       }      

      TableResults = TableResults + "</table>";
       
      return TableResults;
 }	
</script>
    
<script type="text/javascript">
 function download_simulation_result_summary(scenario_summary, fFrm_You_Retire_End_Age, fNbr_Years) {

     scenario_summary.sort(function(a, b){return a.scenario_year - b.scenario_year});      

     fscenario_summary_len = scenario_summary.length;

     csv = "Scenario Year, Simulation Result, Budget Spent, Bonus Earned, Avg Bonus, Last Year Budget, End Bal, Years Remain, Score \r\n";   
     
     for (var i=0; i<fscenario_summary_len; i++)
       
      {
           fScenario_Status = "Success";
             
           fYears_Remain = Math.round(scenario_summary[i].end_bal / scenario_summary[i].infadj_budget_amt); 
           fAvg_Bonus = Math.round((scenario_summary[i].bonus_running_total / scenario_summary[i].infadj_budget_running_total)*100);
           
              fScenarioRange = scenario_summary[i].scenario_year + " thru " + (scenario_summary[i].scenario_year + fNbr_Years);
              if (scenario_summary[i].scenario_year == 1) {fScenarioRange = "Baseline";}
           
              fResult = "Success!" 
              if (scenario_summary[i].end_bal == 0) {fResult = "Savings exhausted in " + (scenario_summary[i].year);}
            
              csv = csv + fScenarioRange + "," + 
                    fResult + "," + scenario_summary[i].infadj_budget_running_total + 
                  "," + scenario_summary[i].bonus_running_total + 
                  "," + fAvg_Bonus + "%" + 
                  "," + scenario_summary[i].infadj_budget_amt + 
                  "," + scenario_summary[i].end_bal + 
                  "," + fYears_Remain  +
                  "," + scenario_summary[i].scenario_score + 
                  " \r\n" ;
    
       } 
     
     fileName = "RPS_sim_result_smry";
     let csvData = new Blob([csv], { type: 'text/csv' });  
     let csvUrl = URL.createObjectURL(csvData);
 
     let hiddenElement = document.createElement('a');
     hiddenElement.href = csvUrl;
     hiddenElement.target = '_blank';
     hiddenElement.download = fileName + '.csv';
     hiddenElement.click();

     
 }	
</script>    

<script type="text/javascript"> 
    function download_simulation_result_detail(simulation_scenario) {
 
      csv =  ",,Age,,Spend Plan,,,,,Total Income,,,,,Withdraw Strategy,,,,Summary Account Activity,,,,,,,,," + 
               "You IRA Account Activity,,,,,,Spouse IRA Account Activity,,,,,,Brokerage Account Activity,,,,,,,," + 
               "Roth Account Activity,,,,,,,Federal Income Tax Calculations,,,,,,,,,,," + 
               "Federal Tax Brackets,,,,,,,,,,,,,,Capital Gains Tax Calculation,,,,,,,,," + 
               "Capital Gains Tax Brackets,,,,,," + 
               " \r\n" ;
                         
      csv = csv +  
               "Scenario, Year, You, Spouse, Budget, Mortgage,Bonus, Inc Tax, Cap Gains Tax, You Soc Sec, " +
               "Spouse Soc Sec, You Pension, Spouse Pension, Withdraw From Savings, You IRA, Spouse IRA," +
               "Brokerage, Roth HSA, Beg Bal, Withdraw, Gain(Loss), Deposit, End Bal, " +
               "Baseline, Stock Ret, Bond Ret, Inf Rate," +
               "Beg Bal, Draw RMD ,Draw Addl, Gain / Loss, Deposit, End Bal," +
               "Beg Bal, Draw RMD, Draw Addl, Gain / Loss, Deposit, End Bal," +
               "Beg Bal, Draw / Deposit, Gain / Loss, Deposit, End Bal," +
               "Beg Cost Basis, Adj Cost Basis, End Cost Basis," +
               "Beg Bal , Draw / Deposit, Gain / Loss, Deposit, End Bal, Conv You, Conv Spouse," +
               "IRA Draw, Pension, SS Taxable Amt, SS Taxable Pct, Adjusted Gross, Std Deduct Nbr, Std Deduct Amt," +
               "Sr Deduct Nbr, Sr Deduct Amt, Taxable Income, Est Tax," +   
               "Tax Married 10% , Tax Married 12%, Tax Married 22%, Tax Married 24%, " +
               "Tax Married 32%, Tax Married 35% , Tax Married 37% , Tax Single 10%, " +
               "Tax Single 12% , Tax Single 22% , Tax Single 24%, Tax Single 32%, " +
               "Tax Single 35% , Tax Single 37%, Adj Gross, Std Ded Nbr, Std Ded Amt, " + 
               "Sr Ded Nbr , Sr Ded Amt, Brkg Withdraw, Adj Cost Basis, Cap Gains, Cap Gains Tax, " +  
               "Tax Married 0%, Tax Married 15%, Tax Married 20%, Tax Single 0%, Tax Single 15%, Tax Single 20%, " +
               " \r\n";     

       var fsimulation_scenarioLen = simulation_scenario.length;
        
for (var i=0; i<fsimulation_scenarioLen; i++)
   
  {
         
     fYou_IRA_Draw_Amt = simulation_scenario[i].you_rmd_draw_amt + simulation_scenario[i].you_ira_addl_draw_amt;
     fSpo_IRA_Draw_Amt = simulation_scenario[i].spo_rmd_draw_amt + simulation_scenario[i].spo_ira_addl_draw_amt;
     
     csv = csv + simulation_scenario[i].scenario_year + 
       "," + simulation_scenario[i].year + "," + simulation_scenario[i].you_age + "," + simulation_scenario[i].spouse_age +
       "," + simulation_scenario[i].infadj_budget_amt + "," + simulation_scenario[i].mortgage_budget_amt + "," + simulation_scenario[i].bonus_amt +
       "," + simulation_scenario[i].inc_tax_amt + "," +  simulation_scenario[i].capgains_tax_amt + "," +  simulation_scenario[i].you_socsec_amt +
       "," + simulation_scenario[i].spo_socsec_amt + "," + simulation_scenario[i].you_pension_amt + "," +  simulation_scenario[i].spo_pension_amt +
       "," + simulation_scenario[i].total_need_amt + "," + (fYou_IRA_Draw_Amt * -1) + "," + (fSpo_IRA_Draw_Amt * -1) + "," + (simulation_scenario[i].brkrg_draw_amt1 * -1) +  
       "," + (simulation_scenario[i].roth_draw_amt1 * -1) + "," +  simulation_scenario[i].beg_bal + "," +  (simulation_scenario[i].total_draw_amt * -1)  +
       "," + simulation_scenario[i].total_gain_amt + "," +  simulation_scenario[i].total_ann_dep_amt  + "," +  simulation_scenario[i].end_bal  +
       "," + simulation_scenario[i].bas_end_bal  + "," +  (Math.round(simulation_scenario[i].stockret * 10000)/100) + "%" + 
       "," + (Math.round(simulation_scenario[i].bondret * 10000)/100) + "%" + "," +  (Math.round(simulation_scenario[i].infrate * 10000)/100) + "%" +
       "," + simulation_scenario[i].you_ira_beg_bal_amt + "," +  (simulation_scenario[i].you_rmd_draw_amt * -1) + "," + (simulation_scenario[i].you_ira_addl_draw_amt * -1) +
       "," + simulation_scenario[i].you_ira_gain_amt + "," +  simulation_scenario[i].you_ira_ann_dep_amt + "," +  simulation_scenario[i].you_ira_end_bal_amt +
       "," + simulation_scenario[i].spo_ira_beg_bal_amt + "," +  (simulation_scenario[i].spo_rmd_draw_amt * -1) + "," +  (simulation_scenario[i].spo_ira_addl_draw_amt * -1) +
       "," + simulation_scenario[i].spo_ira_gain_amt +  "," +  simulation_scenario[i].spo_ira_ann_dep_amt + "," +  simulation_scenario[i].spo_ira_end_bal_amt +
       "," + simulation_scenario[i].brkrg_beg_bal_amt + "," +  (simulation_scenario[i].brkrg_draw_amt1 * -1) + "," +  simulation_scenario[i].brkrg_gain_amt +
       "," + simulation_scenario[i].brkrg_ann_dep_amt + "," +  simulation_scenario[i].brkrg_end_bal_amt + "," +  simulation_scenario[i].brkrg_beg_cost_basis_amt + 
       "," +  simulation_scenario[i].brkrg_adj_cost_basis_amt + "," +  simulation_scenario[i].brkrg_end_cost_basis_amt + "," +  simulation_scenario[i].roth_beg_bal_amt  + 
       "," +  (simulation_scenario[i].roth_draw_amt1 * -1)  + "," +  simulation_scenario[i].roth_gain_amt + "," +  simulation_scenario[i].roth_ann_dep_amt +  
       "," +  simulation_scenario[i].roth_end_bal_amt  + "," +  simulation_scenario[i].you_roth_conv_amt + "," +  simulation_scenario[i].spo_roth_conv_amt +
       "," +  simulation_scenario[i].ira_distribution_amt + "," +  simulation_scenario[i].pension_amt + "," +  simulation_scenario[i].socsec_taxable_amt +
       "," +  simulation_scenario[i].socsec_taxable_pct + "," +  simulation_scenario[i].adjusted_gross_amt + "," +  simulation_scenario[i].std_deduct_nbr +
       "," +  simulation_scenario[i].std_deduct_amt + "," +  simulation_scenario[i].senior_deduct_nbr + "," +  simulation_scenario[i].senior_deduct_amt +
       "," +  simulation_scenario[i].curyr_taxable_income + "," +  simulation_scenario[i].curyr_inc_tax_amt + "," +  simulation_scenario[i].taxtablemarried0  +
       "," +  simulation_scenario[i].taxtablemarried1  + "," +  simulation_scenario[i].taxtablemarried2 + "," +  simulation_scenario[i].taxtablemarried3  +
       "," +  simulation_scenario[i].taxtablemarried4  + "," +  simulation_scenario[i].taxtablemarried5  +  "," +  "unlimited"  +
       "," +  simulation_scenario[i].taxtablesingle0  + "," +  simulation_scenario[i].taxtablesingle1  + "," +  simulation_scenario[i].taxtablesingle2  +
       "," +  simulation_scenario[i].taxtablesingle3  + "," +  simulation_scenario[i].taxtablesingle4  + "," +  simulation_scenario[i].taxtablesingle5  +
       "," +  "unlimited"  + "," +  simulation_scenario[i].adjusted_gross_amt  + "," +  simulation_scenario[i].std_deduct_nbr + "," +  simulation_scenario[i].std_deduct_amt +
       "," +  simulation_scenario[i].senior_deduct_nbr + "," +  simulation_scenario[i].senior_deduct_amt + "," +  (simulation_scenario[i].brkrg_draw_amt1 * -1) +   
       "," +  simulation_scenario[i].brkrg_adj_cost_basis_amt + "," +  simulation_scenario[i].curyr_capgains_amt + "," +  simulation_scenario[i].curyr_capgains_tax_amt + 
       "," +  simulation_scenario[i].captaxtable0_thru  + "," +  simulation_scenario[i].captaxtable1_thru  + "," +  "unlimited"  +
       "," +  simulation_scenario[i].captaxtable3_thru  + "," +  simulation_scenario[i].captaxtable4_thru  + "," +  "unlimited"  +
      " \r\n"; 

   }
        
        
     fileName = "RPS_sim_result_dtl";
     let csvData = new Blob([csv], { type: 'text/csv' });  
     let csvUrl = URL.createObjectURL(csvData);
 
     let hiddenElement = document.createElement('a');
     hiddenElement.href = csvUrl;
     hiddenElement.target = '_blank';
     hiddenElement.download = fileName + '.csv';
     hiddenElement.click();

     
 }	
</script> 
    
    
<script type="text/javascript">
 function downloadrates () {

                csv = "col1,, col3,, col5 \r\n";
                csv = csv + "col1,col2,col3,col4,col5"
                fileName = "RPS_scenario_result_summary";   
            let csvData = new Blob([csv], { type: 'text/csv' });  
            let csvUrl = URL.createObjectURL(csvData);
 
            let hiddenElement = document.createElement('a');
            hiddenElement.href = csvUrl;
            hiddenElement.target = '_blank';
            hiddenElement.download = fileName + '.csv';
            hiddenElement.click();
       }
</script>

<script type="text/javascript">
 function setcolor (fInput) {

    fColor='style="color:black;"';   
    if (fInput < 0)
      {fColor = 'style="color:red;"';}
 
    return fColor;
       }
</script>

<script type="text/javascript">
 function setbackgroundcolor (fInput) {

    fBackground_Color=' align = "right" ';   
    if (fInput < 0)
      {fBackground_Color = ' style="background-color:#e6ffee" align = "right" ';}
 
    return fBackground_Color;
       }
</script>
    
<script type="text/javascript">
 function addcomma (fInput) {
	
    fWithComma = fInput.toLocaleString(); 
    return fWithComma;

       }
</script>

<script>
function getcurrentyear() {
  var d = new Date();
  var n = d.getFullYear();
  return n;
}
</script>



<script>
function infadj_tax_variables_func(infrate) {
// ************************************ -- >
// adjst tax variables by inflation rate -- >
// ************************************* -- >    
   infadj_std_deduct_married = Math.round(infadj_std_deduct_married * (1+infrate));
   infadj_std_deduct_single  = Math.round(infadj_std_deduct_single * (1+infrate));
   infadj_senior_deduct_amt  = Math.round(infadj_senior_deduct_amt * (1+infrate));

   infadj_from = 0;
   for (ri=0; ri < TaxTableMarriedLen; ri++)
    {infadj_taxtable_married[ri].from = infadj_from; 
     infadj_taxtable_married[ri].thru = Math.round(infadj_taxtable_married[ri].thru*(1+infrate));
     infadj_from = infadj_taxtable_married[ri].thru + 1;    
    }

  infadj_from = 0;
  for (ri=0; ri < TaxTableSingleLen; ri++)
    {infadj_taxtable_single[ri].from = infadj_from;
     infadj_taxtable_single[ri].thru = Math.round(infadj_taxtable_single[ri].thru*(1+infrate));
     infadj_from = infadj_taxtable_single[ri].thru + 1;
    }

  lFile_Status = "single";
  infadj_from = 0;
  for (ri=0; ri < capgains_taxtable_len; ri++)
    {if (capgains_taxtable[ri].file_status == lFile_Status)
        {infadj_capgains_taxtable[ri].from = infadj_from;
         infadj_capgains_taxtable[ri].thru = Math.round(infadj_capgains_taxtable[ri].thru*(1+infrate));
         infadj_from = infadj_capgains_taxtable[ri].thru + 1;
        }
    }

  lFile_Status = "married";
  infadj_from = 0;
  for (ri=0; ri < capgains_taxtable_len; ri++)
    {if (capgains_taxtable[ri].file_status == lFile_Status)
        {infadj_capgains_taxtable[ri].from = infadj_from;
         infadj_capgains_taxtable[ri].thru = Math.round(infadj_capgains_taxtable[ri].thru*(1+infrate));
         infadj_from = infadj_capgains_taxtable[ri].thru + 1;
        }
    } 

  return; 
}
</script>


<script>
function calc_rmd(fAge, fIRA_Bal_Amt) {

  var fRMD_Amt = 0;
  
  if(fAge < 70) {return fRMD_Amt};
  if(fAge > 114) {return fRMD_Amt};

  if (fIRA_Bal_Amt <= 0) {return fRMD_Amt};

  var ri = fAge - 70;

  var fFactor = rmdtable[ri].factor * 1;
  
  fRMD_Amt = Math.round(fIRA_Bal_Amt / fFactor);
 
  return fRMD_Amt;

}
</script>
 

<script>
function calc_socsec_taxable_func(fAdjusted_Gross_Amt, fSocSec_Amt, fExemptions) {

   var line1_amt = fSocSec_Amt; 
   var line2_amt = Math.round(line1_amt * .50);
   var line3_amt = fAdjusted_Gross_Amt;
   var line4_amt = 0;
   var line5_amt = line2_amt + line3_amt + line4_amt;
   var line6_amt = 0;
   var line7_amt = line5_amt - line6_amt;
   var line8_amt = 25000;
   if (fExemptions==2) {line8_amt=32000};
   var line9_amt = line7_amt - line8_amt;
   if (line9_amt < 0) {line9_amt = 0};
   var line10_amt = 9000;
   if (fExemptions==2) {line10_amt = 12000};
   var line11_amt = line9_amt - line10_amt;
   if (line11_amt < 0) {line11_amt = 0};
   var line12_amt = Math.min(line9_amt, line10_amt);
   var line13_amt = Math.round(line12_amt * .50);
   var line14_amt = Math.min(line2_amt, line13_amt);
   var line15_amt = Math.round(line11_amt * .85);
   var line16_amt = line14_amt + line15_amt;
   var line17_amt = Math.round(line1_amt * .85);
   var line18_amt = Math.min(line16_amt, line17_amt);

   var fSocSec_Taxable_Amt = line18_amt;
   
   return fSocSec_Taxable_Amt;

}
</script>   



<script>
function calc_income_tax(fAdjusted_Gross_Amt, fExemptions, fYou_Age, fSpo_Age) {
//****************************************************************
//* calculate income tax function
//****************************************************************
   
   var fThru=0;
   var fTax_Amt=0;
   var fSenior_Deduct_Nbr = 0;
   var fUsed_Std_Deduct_Amt = 0;
   var fTaxable_Income_Pre = 0;
   var fTaxable_Income = 0;    

   if (fYou_Age >= 65) {fSenior_Deduct_Nbr++;}
   if (fSpo_Age >=65) {fSenior_Deduct_Nbr++};
   
   fSenior_Deduct_Nbr = Math.min(fSenior_Deduct_Nbr, fExemptions);
  
   fSenior_Deduct_Amt = infadj_senior_deduct_amt * fSenior_Deduct_Nbr;

   if (fExemptions == 1)
     {
       fUsed_Std_Deduct_Amt = infadj_std_deduct_single;
       fTaxable_Income_Pre = fAdjusted_Gross_Amt - infadj_std_deduct_single - infadj_senior_deduct_amt;
       fTaxable_Income = Math.max(0,fTaxable_Income_Pre);
       for (ri=0; ri < TaxTableSingleLen; ri++)
        {fThru = Math.min(fTaxable_Income, infadj_taxtable_single[ri].thru);
         fTax_Amt = fTax_Amt + Math.round((fThru - infadj_taxtable_single[ri].from) * taxtablesingle[ri].pct);
         if (fThru == fTaxable_Income) 
              {   fTax_Top_Pct = taxtablesingle[ri].pct;
                  fTax_Top_Amt = taxtablesingle[ri].thru;
                  break;
              }
        } 
    }

   if (fExemptions != 1)
     {
       fUsed_Std_Deduct_Amt = infadj_std_deduct_married;
       fTaxable_Income_Pre = fAdjusted_Gross_Amt - infadj_std_deduct_married - fSenior_Deduct_Amt;
       fTaxable_Income = Math.max(0,fTaxable_Income_Pre);
       if (fTaxable_Income < 0) {fTaxable_Income = 0};
       for (ri=0; ri < TaxTableMarriedLen; ri++)
        {fThru = Math.min(fTaxable_Income, infadj_taxtable_married[ri].thru);
         fTax_Amt = fTax_Amt + Math.round((fThru - infadj_taxtable_married[ri].from) * taxtablemarried[ri].pct);
         if (fThru == fTaxable_Income)
         {
            fTax_Top_Pct = taxtablemarried[ri].pct;
            fTax_Top_Amt = taxtablemarried[ri].thru;
            break;
         }
        } 
    }

    oTax_Results = {taxable_income    : fTaxable_Income,
                    taxable_income_pre : fTaxable_Income_Pre,
                    inc_tax_amt       : fTax_Amt,
                    senior_deduct_nbr : fSenior_Deduct_Nbr,
                    senior_deduct_amt : fSenior_Deduct_Amt,
                    std_deduct_amt    : fUsed_Std_Deduct_Amt,
                    top_pct           : fTax_Top_Pct,
                    top_amt           : fTax_Top_Amt};
  
    return oTax_Results  
  
}
</script>

<script>
function calc_capgains_tax(fAdjusted_Gross_Amt, fDeductions_Amt, fCapgains_Amt, fExemptions) {
//****************************************************************
//* calculate capital gains tax
//****************************************************************
   
   var fThru=0;
   var fTax_Amt=0;
  
   fFile_Status = "married";
   if (fExemptions == 1) {lFile_Status = "single";}

   fTaxable_Income = fAdjusted_Gross_Amt -fDeductions_Amt + fCapgains_Amt;       
  
   if (fTaxable_Income < 0)  {fTaxable_Income = 0;}
  
   for (ri=0; ri < capgains_taxtable_len; ri++)
        {
         if (fFile_Status == capgains_taxtable[ri].file_status) 
         
           {fThru = Math.min(fTaxable_Income, infadj_capgains_taxtable[ri].thru);
            fTax_Amt = fTax_Amt + Math.round((fThru - infadj_capgains_taxtable[ri].from) * capgains_taxtable[ri].pct);
            if (fThru == fTaxable_Income) {break;}
           }
        } 

    oCapgains_Tax_Results = {total_income    : fTaxable_Income,
                             tax_amt         : fTax_Amt};

    return oCapgains_Tax_Results;  
  
}
</script>

<script type="text/javascript">

//********************
//* constants
//********************

var myWindow;

var socsec_taxable_pct = .85;
var cBudget_Single_Adj = .75;
var cBudget_Full = 1;
 
var stddeductmarried = 24800;
var stddeductsingle = 12400;
var infadj_std_deduct_married = 0;
var infadj_std_deduct_single = 0;

var senior_deduct_amt = 1300;
var infadj_senior_deduct_amt = 0;

var taxtablemarried = new Array( );
taxtablemarried[0] = {pct:.10, from:0, thru:19750};
taxtablemarried[1] = {pct:.12, from:19751, thru:80250};
taxtablemarried[2] = {pct:.22, from:80251, thru:171050};
taxtablemarried[3] = {pct:.24, from:171051, thru:326600};
taxtablemarried[4] = {pct:.32, from:326601, thru:414700};
taxtablemarried[5] = {pct:.35, from:414701, thru:622050};
taxtablemarried[6] = {pct:.37, from:622051, thru:9999999999};
var TaxTableMarriedLen = taxtablemarried.length;

var taxtablesingle = new Array( );
taxtablesingle[0] = {pct:.10, from:0, thru:9875};
taxtablesingle[1] = {pct:.12, from:9876, thru:40125};
taxtablesingle[2] = {pct:.22, from:40126, thru:85525};
taxtablesingle[3] = {pct:.24, from:85526, thru:163300};
taxtablesingle[4] = {pct:.32, from:163301, thru:207350};
taxtablesingle[5] = {pct:.35, from:207351, thru:518400};
taxtablesingle[6] = {pct:.37, from:518401, thru:9999999999};
var TaxTableSingleLen = taxtablesingle.length;

var infadj_taxtable_married = new Array();
var infadj_taxtable_single = new Array();

var capgains_taxtable = new Array( );
capgains_taxtable[0] = {file_status: "married", pct:.0,  from:0, thru: 80000};
capgains_taxtable[1] = {file_status: "married", pct:.15, from:80001, thru: 496600};
capgains_taxtable[2] = {file_status: "married", pct:.20, from:496601, thru: 999999999};
capgains_taxtable[3] = {file_status: "single", pct:.0, from:0, thru: 40000};
capgains_taxtable[4] = {file_status: "single", pct:.15, from:40001, thru: 441450};
capgains_taxtable[5] = {file_status: "single", pct:.20, from:441451, thru: 999999999};
var infadj_capgains_taxtable = new Array();
var capgains_taxtable_len = capgains_taxtable.length;

var rmdtable = new Array( );
rmdtable[0]={age:70,factor:27.4};
rmdtable[1]={age:71,factor:26.5};
rmdtable[2]={age:72,factor:25.6};
rmdtable[3]={age:73,factor:24.7};
rmdtable[4]={age:74,factor:23.8};
rmdtable[5]={age:75,factor:22.9};
rmdtable[6]={age:76,factor:22};
rmdtable[7]={age:77,factor:21.2};
rmdtable[8]={age:78,factor:20.3};
rmdtable[9]={age:79,factor:19.5};
rmdtable[10]={age:80,factor:18.7};
rmdtable[11]={age:81,factor:17.9};
rmdtable[12]={age:82,factor:17.1};
rmdtable[13]={age:83,factor:16.3};
rmdtable[14]={age:84,factor:15.5};
rmdtable[15]={age:85,factor:14.8};
rmdtable[16]={age:86,factor:14.1};
rmdtable[17]={age:87,factor:13.4};
rmdtable[18]={age:88,factor:12.7};
rmdtable[19]={age:89,factor:12};
rmdtable[20]={age:90,factor:11.4};
rmdtable[21]={age:91,factor:10.8};
rmdtable[22]={age:92,factor:10.2};
rmdtable[23]={age:93,factor:9.6};
rmdtable[24]={age:94,factor:9.1};
rmdtable[25]={age:95,factor:8.6};1
rmdtable[26]={age:96,factor:8.1};
rmdtable[27]={age:97,factor:7.6};
rmdtable[28]={age:98,factor:7.1};
rmdtable[29]={age:99,factor:6.7};
rmdtable[30]={age:100,factor:6.3};
rmdtable[31]={age:101,factor:5.9};
rmdtable[32]={age:102,factor:5.5};
rmdtable[33]={age:103,factor:5.2};
rmdtable[34]={age:104,factor:4.9};
rmdtable[35]={age:105,factor:4.5};
rmdtable[36]={age:106,factor:4.2};
rmdtable[37]={age:107,factor:3.9};
rmdtable[38]={age:108,factor:3.7};
rmdtable[39]={age:109,factor:3.4};
rmdtable[40]={age:110,factor:3.1};
rmdtable[41]={age:111,factor:2.9};
rmdtable[42]={age:112,factor:2.6};
rmdtable[43]={age:113,factor:2.4};
rmdtable[44]={age:114,factor:2.1};

var ratehistory = new Array( );
ratehistory[0]={year:1,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[1]={year:2,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[2]={year:3,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[3]={year:4,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[4]={year:5,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[5]={year:6,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[6]={year:7,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[7]={year:8,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[8]={year:9,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[9]={year:10,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[10]={year:11,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[11]={year:12,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[12]={year:13,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[13]={year:14,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[14]={year:15,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[15]={year:16,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[16]={year:17,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[17]={year:18,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[18]={year:19,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[19]={year:20,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[20]={year:21,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[21]={year:22,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[22]={year:23,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[23]={year:24,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[24]={year:25,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[25]={year:26,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[26]={year:27,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[27]={year:28,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[28]={year:29,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[29]={year:30,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[30]={year:31,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[31]={year:32,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[32]={year:33,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[33]={year:34,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[34]={year:35,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[35]={year:36,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[36]={year:37,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[37]={year:38,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[38]={year:39,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[39]={year:40,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[40]={year:41,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[41]={year:42,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[42]={year:43,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[43]={year:44,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[44]={year:45,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[45]={year:46,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[46]={year:47,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[47]={year:48,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[48]={year:49,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[49]={year:50,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[50]={year:51,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[51]={year:52,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[52]={year:53,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[53]={year:54,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[54]={year:55,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[55]={year:56,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[56]={year:57,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[57]={year:58,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[58]={year:59,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[59]={year:60,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[60]={year:61,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[61]={year:62,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[62]={year:63,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[63]={year:64,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[64]={year:65,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[65]={year:66,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[66]={year:67,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[67]={year:68,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[68]={year:69,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[69]={year:70,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[70]={year:71,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[71]={year:72,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[72]={year:73,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[73]={year:74,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[74]={year:75,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[75]={year:76,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[76]={year:77,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[77]={year:78,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[78]={year:79,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[79]={year:80,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[80]={year:81,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[81]={year:82,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[82]={year:83,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[83]={year:84,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[84]={year:85,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[85]={year:86,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[86]={year:87,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[87]={year:88,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[88]={year:89,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[89]={year:90,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[90]={year:91,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[91]={year:92,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[92]={year:93,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[93]={year:94,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[94]={year:95,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[95]={year:96,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[96]={year:97,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[97]={year:98,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[98]={year:99,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[99]={year:1871,stockret:0.1532,bondret:0.0251,stret:0.001,infrate:0.0153};
ratehistory[100]={year:1872,stockret:0.1132,bondret:0.0397,stret:0.001,infrate:0.0226};
ratehistory[101]={year:1873,stockret:-0.0235,bondret:0.0623,stret:0.001,infrate:-0.0441};
ratehistory[102]={year:1874,stockret:0.0451,bondret:0.0828,stret:0.001,infrate:-0.0692};
ratehistory[103]={year:1875,stockret:0.0485,bondret:0.0867,stret:0.001,infrate:-0.0579};
ratehistory[104]={year:1876,stockret:-0.1368,bondret:0.0593,stret:0.001,infrate:0.0088};
ratehistory[105]={year:1877,stockret:-0.031,bondret:0.0535,stret:0.001,infrate:-0.1565};
ratehistory[106]={year:1878,stockret:0.1569,bondret:0.0529,stret:0.001,infrate:-0.1031};
ratehistory[107]={year:1879,stockret:0.4832,bondret:0.0574,stret:0.001,infrate:0.2069};
ratehistory[108]={year:1880,stockret:0.2622,bondret:0.0646,stret:0.001,infrate:-0.0571};
ratehistory[109]={year:1881,stockret:0.0081,bondret:0.0453,stret:0.001,infrate:0.0808};
ratehistory[110]={year:1882,stockret:0.0355,bondret:0.0364,stret:0.001,infrate:-0.0187};
ratehistory[111]={year:1883,stockret:-0.0516,bondret:0.0373,stret:0.001,infrate:-0.0762};
ratehistory[112]={year:1884,stockret:-0.1216,bondret:0.0437,stret:0.001,infrate:-0.1031};
ratehistory[113]={year:1885,stockret:0.283,bondret:0.0469,stret:0.001,infrate:-0.0345};
ratehistory[114]={year:1886,stockret:0.1154,bondret:0.0244,stret:0.001,infrate:0};
ratehistory[115]={year:1887,stockret:-0.0036,bondret:0.0239,stret:0.001,infrate:0.0476};
ratehistory[116]={year:1888,stockret:0.0301,bondret:0.0516,stret:0.001,infrate:-0.0455};
ratehistory[117]={year:1889,stockret:0.0687,bondret:0.0385,stret:0.001,infrate:-0.0476};
ratehistory[118]={year:1890,stockret:-0.0595,bondret:0.0206,stret:0.001,infrate:0.025};
ratehistory[119]={year:1891,stockret:0.1839,bondret:0.0365,stret:0.001,infrate:-0.061};
ratehistory[120]={year:1892,stockret:0.0617,bondret:0.0259,stret:0.001,infrate:0.0779};
ratehistory[121]={year:1893,stockret:-0.1854,bondret:0.0403,stret:0.001,infrate:-0.1325};
ratehistory[122]={year:1894,stockret:0.0324,bondret:0.0548,stret:0.001,infrate:-0.0417};
ratehistory[123]={year:1895,stockret:0.0494,bondret:0.0267,stret:0.001,infrate:0.0145};
ratehistory[124]={year:1896,stockret:0.0304,bondret:0.0496,stret:0.001,infrate:-0.0286};
ratehistory[125]={year:1897,stockret:0.1991,bondret:0.0339,stret:0.001,infrate:0.0294};
ratehistory[126]={year:1898,stockret:0.2869,bondret:0.0522,stret:0.001,infrate:0.0143};
ratehistory[127]={year:1899,stockret:0.0378,bondret:0.0295,stret:0.001,infrate:0.169};
ratehistory[128]={year:1900,stockret:0.2082,bondret:0.035,stret:0.001,infrate:-0.0241};
ratehistory[129]={year:1901,stockret:0.1938,bondret:0.0259,stret:0.001,infrate:0.0247};
ratehistory[130]={year:1902,stockret:0.0825,bondret:0.0229,stret:0.001,infrate:0.0964};
ratehistory[131]={year:1903,stockret:-0.169,bondret:0.0253,stret:0.001,infrate:-0.044};
ratehistory[132]={year:1904,stockret:0.3084,bondret:0.0279,stret:0.001,infrate:0.023};
ratehistory[133]={year:1905,stockret:0.21,bondret:0.0381,stret:0.001,infrate:0};
ratehistory[134]={year:1906,stockret:0.0091,bondret:0.018,stret:0.001,infrate:0.0449};
ratehistory[135]={year:1907,stockret:-0.2374,bondret:0.0214,stret:0.001,infrate:-0.0215};
ratehistory[136]={year:1908,stockret:0.381,bondret:0.0454,stret:0.001,infrate:0.033};
ratehistory[137]={year:1909,stockret:0.1611,bondret:0.0283,stret:0.001,infrate:0.1064};
ratehistory[138]={year:1910,stockret:-0.0337,bondret:0.0336,stret:0.001,infrate:-0.0673};
ratehistory[139]={year:1911,stockret:0.0345,bondret:0.0376,stret:0.001,infrate:-0.0103};
ratehistory[140]={year:1912,stockret:0.0724,bondret:0.0103,stret:0.001,infrate:0.0729};
ratehistory[141]={year:1913,stockret:-0.0484,bondret:0.0619,stret:0.001,infrate:0.0204};
ratehistory[142]={year:1914,stockret:-0.0562,bondret:0.0386,stret:0.001,infrate:0.01};
ratehistory[143]={year:1915,stockret:0.3048,bondret:0.0555,stret:0.001,infrate:0.0297};
ratehistory[144]={year:1916,stockret:0.0857,bondret:0.0299,stret:0.001,infrate:0.125};
ratehistory[145]={year:1917,stockret:-0.1745,bondret:0.0184,stret:0.001,infrate:0.1966};
ratehistory[146]={year:1918,stockret:0.1678,bondret:0.0486,stret:0.001,infrate:0.1786};
ratehistory[147]={year:1919,stockret:0.1924,bondret:0.0146,stret:0.001,infrate:0.1697};
ratehistory[148]={year:1920,stockret:-0.137,bondret:0.0391,stret:0.001,infrate:-0.0155};
ratehistory[149]={year:1921,stockret:0.0914,bondret:0.1049,stret:0.001,infrate:-0.1105};
ratehistory[150]={year:1922,stockret:0.289,bondret:0.0449,stret:0.001,infrate:-0.0059};
ratehistory[151]={year:1923,stockret:0.0517,bondret:0.0646,stret:0.001,infrate:0.0298};
ratehistory[152]={year:1924,stockret:0.2605,bondret:0.0571,stret:0.001,infrate:0};
ratehistory[153]={year:1925,stockret:0.2524,bondret:0.0531,stret:0.001,infrate:0.0347};
ratehistory[154]={year:1926,stockret:0.1138,bondret:0.0627,stret:0.001,infrate:-0.0223};
ratehistory[155]={year:1927,stockret:0.3507,bondret:0.0369,stret:0.001,infrate:-0.0114};
ratehistory[156]={year:1928,stockret:0.3943,bondret:0.0146,stret:0.001,infrate:-0.0116};
ratehistory[157]={year:1929,stockret:-0.1037,bondret:0.0566,stret:0.001,infrate:0};
ratehistory[158]={year:1930,stockret:-0.2741,bondret:0.0319,stret:0.001,infrate:-0.0702};
ratehistory[159]={year:1931,stockret:-0.4277,bondret:0.0231,stret:0.001,infrate:-0.1006};
ratehistory[160]={year:1932,stockret:-0.0638,bondret:0.0107,stret:0.001,infrate:-0.0979};
ratehistory[161]={year:1933,stockret:0.5853,bondret:0.0096,stret:0.001,infrate:0.0233};
ratehistory[162]={year:1934,stockret:0.0327,bondret:0.0032,stret:0.001,infrate:0.0303};
ratehistory[163]={year:1935,stockret:0.4637,bondret:0.0018,stret:0.001,infrate:0.0147};
ratehistory[164]={year:1936,stockret:0.3313,bondret:0.0017,stret:0.001,infrate:0.0217};
ratehistory[165]={year:1937,stockret:-0.3415,bondret:0.003,stret:0.001,infrate:0.0286};
ratehistory[166]={year:1938,stockret:0.3093,bondret:0.0008,stret:0.001,infrate:-0.0278};
ratehistory[167]={year:1939,stockret:0.0041,bondret:0.0004,stret:0.001,infrate:0};
ratehistory[168]={year:1940,stockret:-0.0781,bondret:0.0003,stret:0.001,infrate:0.0071};
ratehistory[169]={year:1941,stockret:-0.1083,bondret:0.0008,stret:0.001,infrate:0.0993};
ratehistory[170]={year:1942,stockret:0.1687,bondret:0.0034,stret:0.001,infrate:0.0903};
ratehistory[171]={year:1943,stockret:0.2794,bondret:0.0038,stret:0.001,infrate:0.0296};
ratehistory[172]={year:1944,stockret:0.2245,bondret:0.0038,stret:0.001,infrate:0.023};
ratehistory[173]={year:1945,stockret:0.3931,bondret:0.0038,stret:0.001,infrate:0.0225};
ratehistory[174]={year:1946,stockret:-0.0562,bondret:0.0038,stret:0.001,infrate:0.1813};
ratehistory[175]={year:1947,stockret:0.0388,bondret:0.0057,stret:0.001,infrate:0.0884};
ratehistory[176]={year:1948,stockret:0.0196,bondret:0.0102,stret:0.001,infrate:0.0299};
ratehistory[177]={year:1949,stockret:0.2089,bondret:0.011,stret:0.001,infrate:-0.0207};
ratehistory[178]={year:1950,stockret:0.3002,bondret:0.0117,stret:0.001,infrate:0.0593};
ratehistory[179]={year:1951,stockret:0.2275,bondret:0.0148,stret:0.001,infrate:0.06};
ratehistory[180]={year:1952,stockret:0.1438,bondret:0.0167,stret:0.001,infrate:0.0075};
ratehistory[181]={year:1953,stockret:0.0046,bondret:0.0189,stret:0.001,infrate:0.0075};
ratehistory[182]={year:1954,stockret:0.5072,bondret:0.0096,stret:0.001,infrate:-0.0074};
ratehistory[183]={year:1955,stockret:0.2643,bondret:0.0166,stret:0.001,infrate:0.0037};
ratehistory[184]={year:1956,stockret:0.0829,bondret:0.0256,stret:0.001,infrate:0.0299};
ratehistory[185]={year:1957,stockret:-0.0974,bondret:0.0323,stret:0.001,infrate:0.029};
ratehistory[186]={year:1958,stockret:0.4644,bondret:0.0178,stret:0.001,infrate:0.0176};
ratehistory[187]={year:1959,stockret:0.1399,bondret:0.0326,stret:0.001,infrate:0.0173};
ratehistory[188]={year:1960,stockret:0.0182,bondret:0.0305,stret:0.001,infrate:0.0136};
ratehistory[189]={year:1961,stockret:0.2657,bondret:0.0227,stret:0.001,infrate:0.0067};
ratehistory[190]={year:1962,stockret:-0.0872,bondret:0.0278,stret:0.001,infrate:0.0133};
ratehistory[191]={year:1963,stockret:0.2138,bondret:0.0311,stret:0.001,infrate:0.0164};
ratehistory[192]={year:1964,stockret:0.1635,bondret:0.0351,stret:0.001,infrate:0.0097};
ratehistory[193]={year:1965,stockret:0.1429,bondret:0.039,stret:0.0476,infrate:0.0192};
ratehistory[194]={year:1966,stockret:-0.0866,bondret:0.0484,stret:0.0531,infrate:0.0346};
ratehistory[195]={year:1967,stockret:0.272,bondret:0.0433,stret:0.0474,infrate:0.0304};
ratehistory[196]={year:1968,stockret:0.1441,bondret:0.0526,stret:0.0567,infrate:0.0472};
ratehistory[197]={year:1969,stockret:-0.106,bondret:0.0656,stret:0.0712,infrate:0.062};
ratehistory[198]={year:1970,stockret:0,bondret:0.0669,stret:0.0744,infrate:0.0557};
ratehistory[199]={year:1971,stockret:0.1615,bondret:0.0454,stret:0.0479,infrate:0.0327};
ratehistory[200]={year:1972,stockret:0.1684,bondret:0.0395,stret:0.0439,infrate:0.0341};
ratehistory[201]={year:1973,stockret:-0.1806,bondret:0.0673,stret:0.0929,infrate:0.0871};
ratehistory[202]={year:1974,stockret:-0.2704,bondret:0.0778,stret:0.1033,infrate:0.1234};
ratehistory[203]={year:1975,stockret:0.3875,bondret:0.0599,stret:0.0614,infrate:0.0694};
ratehistory[204]={year:1976,stockret:0.2676,bondret:0.156,stret:0.0508,infrate:0.0486};
ratehistory[205]={year:1977,stockret:-0.0426,bondret:0.03,stret:0.0547,infrate:0.067};
ratehistory[206]={year:1978,stockret:0.0749,bondret:0.014,stret:0.0787,infrate:0.0902};
ratehistory[207]={year:1979,stockret:0.2262,bondret:0.019,stret:0.1101,infrate:0.1329};
ratehistory[208]={year:1980,stockret:0.3281,bondret:0.027,stret:0.1287,infrate:0.1252};
ratehistory[209]={year:1981,stockret:-0.0365,bondret:0.063,stret:0.1594,infrate:0.0892};
ratehistory[210]={year:1982,stockret:0.21,bondret:0.326,stret:0.1204,infrate:0.0383};
ratehistory[211]={year:1983,stockret:0.2198,bondret:0.084,stret:0.0896,infrate:0.0379};
ratehistory[212]={year:1984,stockret:0.0451,bondret:0.1515,stret:0.102,infrate:0.0395};
ratehistory[213]={year:1985,stockret:0.3217,bondret:0.2211,stret:0.0796,infrate:0.038};
ratehistory[214]={year:1986,stockret:0.1619,bondret:0.1526,stret:0.0661,infrate:0.011};
ratehistory[215]={year:1987,stockret:0.0167,bondret:0.0276,stret:0.0675,infrate:0.0443};
ratehistory[216]={year:1988,stockret:0.1803,bondret:0.0789,stret:0.0759,infrate:0.0442};
ratehistory[217]={year:1989,stockret:0.2886,bondret:0.1453,stret:0.0911,infrate:0.0465};
ratehistory[218]={year:1990,stockret:-0.0596,bondret:0.0896,stret:0.0815,infrate:0.0611};
ratehistory[219]={year:1991,stockret:0.3467,bondret:0.16,stret:0.0582,infrate:0.0306};
ratehistory[220]={year:1992,stockret:0.098,bondret:0.074,stret:0.0364,infrate:0.029};
ratehistory[221]={year:1993,stockret:0.1062,bondret:0.0975,stret:0.0311,infrate:0.0275};
ratehistory[222]={year:1994,stockret:-0.0017,bondret:-0.0292,stret:0.0438,infrate:0.0267};
ratehistory[223]={year:1995,stockret:0.3579,bondret:0.2001,stret:0.0587,infrate:0.0254};
ratehistory[224]={year:1996,stockret:0.2096,bondret:0.0813,stret:0.0535,infrate:0.0332};
ratehistory[225]={year:1997,stockret:0.3099,bondret:0.0943,stret:0.0554,infrate:0.017};
ratehistory[226]={year:1998,stockret:0.2326,bondret:0.0557,stret:0.0549,infrate:0.0161};
ratehistory[227]={year:1999,stockret:0.2381,bondret:0.026,stret:0.0519,infrate:0.0268};
ratehistory[228]={year:2000,stockret:-0.1057,bondret:0.0742,stret:0.0635,infrate:0.0339};
ratehistory[229]={year:2001,stockret:-0.1097,bondret:0.0732,stret:0.0384,infrate:0.0155};
ratehistory[230]={year:2002,stockret:-0.2096,bondret:0.096,stret:0.0172,infrate:0.0238};
ratehistory[231]={year:2003,stockret:0.3135,bondret:0.1195,stret:0.0115,infrate:0.0188};
ratehistory[232]={year:2004,stockret:0.1252,bondret:0.068,stret:0.0145,infrate:0.0326};
ratehistory[233]={year:2005,stockret:0.0598,bondret:0.0252,stret:0.0334,infrate:0.0342};
ratehistory[234]={year:2006,stockret:0.1551,bondret:0.0591,stret:0.0506,infrate:0.0254};
ratehistory[235]={year:2007,stockret:0.0549,bondret:0.0532,stret:0.0523,infrate:0.0408};
ratehistory[236]={year:2008,stockret:-0.3704,bondret:-0.036,stret:0.0273,infrate:0.0009};
ratehistory[237]={year:2009,stockret:0.287,bondret:0.1904,stret:0.003,infrate:0.0272};
ratehistory[238]={year:2010,stockret:0.1709,bondret:0.0792,stret:0.0024,infrate:0.015};
ratehistory[239]={year:2011,stockret:0.0096,bondret:0.0612,stret:0.002,infrate:0.0296};
ratehistory[240]={year:2012,stockret:0.1625,bondret:0.0736,stret:0.0019,infrate:0.0174};
ratehistory[241]={year:2013,stockret:0.3335,bondret:-0.0101,stret:0.0017,infrate:0.015};
ratehistory[242]={year:2014,stockret:0.1243,bondret:0.0475,stret:0.001,infrate:0.0076};
ratehistory[243]={year:2015,stockret:0.0029,bondret:-0.0065,stret:0.001,infrate:0.0073};
ratehistory[244]={year:2016,stockret:0.1253,bondret:0.0551,stret:0.001,infrate:0.021};
ratehistory[245]={year:2017,stockret:0.2105,bondret:0.0564,stret:0.01,infrate:0.021};
ratehistory[246]={year:2018,stockret:-0.0528,bondret:-0.0134,stret:0.02,infrate:0.019};
ratehistory[247]={year:2019,stockret:0.3092,bondret:0.0976,stret:0.0175,infrate:0.0171};
ratehistory[248]={year:2020,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[249]={year:2021,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[250]={year:2022,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[251]={year:2023,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[252]={year:2024,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[253]={year:2025,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[254]={year:2026,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[255]={year:2027,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[256]={year:2028,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[257]={year:2029,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[258]={year:2030,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[259]={year:2031,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[260]={year:2032,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[261]={year:2033,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[262]={year:2034,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[263]={year:2035,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[264]={year:2036,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[265]={year:2037,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[266]={year:2038,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[267]={year:2039,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[268]={year:2040,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[269]={year:2041,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[270]={year:2042,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[271]={year:2043,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[272]={year:2044,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[273]={year:2045,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[274]={year:2046,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[275]={year:2047,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[276]={year:2048,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[277]={year:2049,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[278]={year:2050,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[279]={year:2051,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[280]={year:2052,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[281]={year:2053,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[282]={year:2054,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[283]={year:2055,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[284]={year:2056,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[285]={year:2057,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[286]={year:2058,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.0225};
ratehistory[287]={year:2059,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[288]={year:2060,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[289]={year:2061,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[290]={year:2062,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[291]={year:2063,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[292]={year:2064,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[293]={year:2065,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[294]={year:2066,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[295]={year:2067,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[296]={year:2068,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[297]={year:2069,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[298]={year:2070,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[299]={year:2071,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[300]={year:2072,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[301]={year:2073,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[302]={year:2074,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[303]={year:2075,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[304]={year:2076,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[305]={year:2077,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[306]={year:2078,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[307]={year:2079,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[308]={year:2080,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[309]={year:2081,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[310]={year:2082,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[311]={year:2083,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[312]={year:2084,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[313]={year:2085,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[314]={year:2086,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[315]={year:2087,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[316]={year:2088,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[317]={year:2089,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[318]={year:2090,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[319]={year:2091,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[320]={year:2092,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[321]={year:2093,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[322]={year:2094,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[323]={year:2095,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[324]={year:2096,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[325]={year:2097,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[326]={year:2098,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[327]={year:2099,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[328]={year:2100,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[329]={year:2101,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[330]={year:2102,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[331]={year:2103,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[332]={year:2104,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[333]={year:2105,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[334]={year:2106,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[335]={year:2107,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[336]={year:2108,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[337]={year:2109,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[338]={year:2110,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[339]={year:2111,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[340]={year:2112,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[341]={year:2113,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[342]={year:2114,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[343]={year:2115,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[344]={year:2116,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[345]={year:2117,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[346]={year:2118,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[347]={year:2119,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[348]={year:2120,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[349]={year:2121,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[350]={year:2122,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[351]={year:2123,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[352]={year:2124,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[353]={year:2125,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[354]={year:2126,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[355]={year:2127,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[356]={year:2128,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[357]={year:2129,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[358]={year:2130,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[359]={year:2131,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[360]={year:2132,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[361]={year:2133,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[362]={year:2134,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[363]={year:2135,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[364]={year:2136,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[365]={year:2137,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[366]={year:2138,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[367]={year:2139,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[368]={year:2140,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[369]={year:2141,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[370]={year:2142,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[371]={year:2143,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[372]={year:2144,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[373]={year:2145,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[374]={year:2146,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[375]={year:2147,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[376]={year:2148,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[377]={year:2149,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[378]={year:2150,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[379]={year:2151,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[380]={year:2152,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[381]={year:2153,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[382]={year:2154,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[383]={year:2155,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[384]={year:2156,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[385]={year:2157,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[386]={year:2158,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[387]={year:2159,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[388]={year:2160,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[389]={year:2161,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[390]={year:2162,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[391]={year:2163,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[392]={year:2164,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[393]={year:2165,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[394]={year:2166,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[395]={year:2167,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
ratehistory[396]={year:2168,stockret:0.06,bondret:0.03,stret:0.02,infrate:0.02};
</div>
</form>

</html>
