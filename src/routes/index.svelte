<script lang="ts">
// @ts-nocheck

//import { text } from "svelte/internal";
import Calendar from '/home/oracle/svelte/yes/src/routes/Calendar.svelte';
//import DatePicker  from "svelte-touch-datepicker";
 //import calendar from "/home/oracle/svelte/yes/src/routes/Calendar.svelte";
  let date = new Date();
  $: _date = date.toLocaleDateString("en-US")



  //import SveltyPicker from 'svelty-picker';
  
  let myDate = '2021-11-11 14:35';

  import MenuSurface from '@smui/menu-surface';
  import Button from '@smui/button';
 
	
	function handleClick () {
		console.log(surface.isOpen());
		if (surface.isOpen()) { // always false
			surface.setOpen(false)
		} else {
			surface.setOpen(true)
		}
	}


  import type { MenuSurfaceComponentDev } from '@smui/menu-surface';
  import Textfield from '@smui/textfield';

  let surface: MenuSurfaceComponentDev;
  let name = '';
  let email = '';
</script>

<style>
    /*.todos {
      width: 50%;
      max-width: 42rem;
      margin: 4rem auto 0 auto;
    }
  
    .new {
      margin: 0 0 0.5rem 0;
    }
  
    .new input {
      font-size: 15px;
      width: 50%;
      padding: 0.5em 1em 0.3em 1em;
      box-sizing: border-box;
          background: rgba(255, 255, 255, 0.05);
          border-radius: 8px;
          text-align: center;
    }*/
  
    /*.todos :global(input) {
      border: 1px solid transparent;
    }
  
    /*.todos :global(input:focus-visible) {
      box-shadow: inset 1px 1px 6px rgba(0, 0, 0, 0.1);
      border: 1px solid #ff3e00 !important;
      outline: none;
    }*/
    /*.container{
    height: 100%;
    width: 100%;
  }
 
  .center {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    font: 20px 'Roboto', sans-serif;
  }*/
  /*.new {
    margin: 0 0 0.5rem 0;
    font-size: 28px;
    width: 100%;
    padding: 0.5em 1em 0.3em 1em;
    box-sizing: border-box;
		background: rgba(255, 255, 255, 0.05);
		border-radius: 8px;
		text-align: center;
  }*/
  </style><!--
<div class="container" >
  <div class="center">
    <p>Date: {_date}</p>
    <DatePicker bind:date />
  </div>
</div>-->
<!--<form class="new">

<SveltyPicker  inputClasses="form-control" format="yyyy-mm-dd hh:ii" bind:value={myDate} placeholder="select" ></SveltyPicker>

</form>
<input type="date"/>-->
<div style="min-width: 100px;">
  <Button on:click={() => surface.setOpen(true)}>Open Menu Surface</Button>
  <MenuSurface bind:this={surface} anchorCorner="BOTTOM_LEFT">
    <div
      style="margin: 1em; display: flex; flex-direction: column; align-items: flex-end;"
    >
      <Textfield bind:value={name} label="Name" />
      <Textfield bind:value={email} label="Email" type="email" />
      <Button style="margin-top: 1em;" on:click={() => surface.setOpen(false)}>
        Submit
      </Button>
    </div>
  </MenuSurface>
</div>






<Calendar/>

<!--<DatePicker dateFormat="d/m/Y" datePickerType="single with calendar"
      
      id="date-picker-calendar-id"
      placeholder="date"
      labelText="Date picker label"
      type="text"
    >
  </DatePicker>-->
  
   
  <!--<script lang="ts">
   
  </script>-->
  <svelte:head>
    <!-- Fonts -->
    <link rel="stylesheet" href="https://fonts.googleapis.com/icon?family=Material+Icons">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Roboto:300,400,500,600,700">
    
    <!-- Material Typography -->
    <link rel="stylesheet" href="https://unpkg.com/@material/typography@13.0.0/dist/mdc.typography.css" />
    
    <!-- SMUI -->
    <link rel="stylesheet" href="https://unpkg.com/svelte-material-ui/bare.css" />
  </svelte:head>

