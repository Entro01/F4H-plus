<script lang="ts">
    import { FaChevronDown } from 'svelte-icons/fa';
    export let items: string[] ;
    export let label:string;
    export let width:string;
    export let value:string;
</script>


<div class="relative h-24 {width} min-w-[200px]">
  <select bind:value class="peer select h-full w-full rounded-[7px] border border-white border-t-transparent bg-transparent px-3 py-2.5 font-sans text-3xl font-normal text-white outline outline-0 transition-all placeholder-shown:border placeholder-shown:border-white placeholder-shown:border-t-white empty:!bg-red-500 focus:border-2 focus:border-white focus:border-t-transparent focus:outline-0 disabled:border-0 disabled:bg-blue-gray-50 ">
    {#each items as item}
    <option class="bg-white text-primary" value={item}>{item}</option>
    {/each}
  </select>
  <div class="absolute top-0 right-0 h-full flex items-center justify-center p-3 pointer-events-none">
<FaChevronDown stroke={2} class="w-6 h-6 text-white" />
  </div>
  <!-- svelte-ignore a11y-label-has-associated-control -->
  <label class="before:content[' '] after:content[' '] pointer-events-none  absolute left-0 -top-3 flex h-full w-full select-none font-normal leading-tight text-white transition-all before:pointer-events-none before:mt-3 before:mr-2 before:box-border before:block before:h-1.5 before:w-2.5 before:rounded-tl-md before:border-t before:border-l before:border-white before:transition-all after:pointer-events-none after:mt-3 after:ml-1 after:box-border  after:block after:h-1.5 after:w-2.5 after:flex-grow after:rounded-tr-md after:border-t after:border-r after:border-white after:transition-all peer-placeholder-shown:text-3xl peer-placeholder-shown:leading-[3.75] peer-placeholder-shown:text-white peer-placeholder-shown:before:border-transparent peer-placeholder-shown:after:border-transparent peer-focus:text-2xl peer-focus:leading-tight peer-focus:text-white peer-focus:before:border-t-2 peer-focus:before:border-l-2 peer-focus:before:border-white peer-focus:after:border-t-2 peer-focus:after:border-r-2 peer-focus:after:border-white peer-disabled:text-transparent peer-disabled:before:border-transparent peer-disabled:after:border-transparent peer-disabled:peer-placeholder-shown:text-white">
    {label}
  </label>
</div>

<!-- <div class="relative h-24 {width} min-w-[200px]">
    <select class="peer h-full w-full rounded-[7px] border border-white border-t-transparent bg-transparent px-3 py-2.5 font-sans text-3xl font-normal text-white outline outline-0 transition-all placeholder-shown:border placeholder-shown:border-white placeholder-shown:border-t-white empty:!bg-red-500 focus:border-2 focus:border-white focus:border-t-transparent focus:outline-0 disabled:border-0 disabled:bg-blue-gray-50">
      {#each items as item}
      <option value={item}>{item}</option>
      {/each}
    </select>
    <div class="absolute top-0 right-0 h-full flex items-center justify-center p-3 pointer-events-none">
      <FontAwesomeIcon icon="chevron-down" class="text-white" />
    </div>
    <label class="before:content[' '] after:content[' '] pointer-events-none  absolute left-0 -top-3 flex h-full w-full select-none font-normal leading-tight text-white transition-all before:pointer-events-none before:mt-3 before:mr-2 before:box-border before:block before:h-1.5 before:w-2.5 before:rounded-tl-md before:border-t before:border-l before:border-white before:transition-all after:pointer-events-none after:mt-3 after:ml-1 after:box-border  after:block after:h-1.5 after:w-2.5 after:flex-grow after:rounded-tr-md after:border-t after:border-r after:border-white after:transition-all peer-placeholder-shown:text-3xl peer-placeholder-shown:leading-[3.75] peer-placeholder-shown:text-white peer-placeholder-shown:before:border-transparent peer-placeholder-shown:after:border-transparent peer-focus:text-2xl peer-focus:leading-tight peer-focus:text-white peer-focus:before:border-t-2 peer-focus:before:border-l-2 peer-focus:before:border-white peer-focus:after:border-t-2 peer-focus:after:border-r-2 peer-focus:after:border-white peer-disabled:text-transparent peer-disabled:before:border-transparent peer-disabled:after:border-transparent peer-disabled:peer-placeholder-shown:text-white">
      {label}
    </label>
  </div> -->

  <style>
    select {
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
  }
  </style>