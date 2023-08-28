<template>
    <div class="header">
        <div class="logo">
            <h5>R2 Laundry</h5>
        </div>
        <ul>
            <li>Home</li>
            <li>Laundry Package</li>
            <li>Product</li>
            <li>Contact</li>
            <li>About Us</li>
        </ul>
        <div class="menu-toggle">
            <input type="checkbox" />
            <span></span>
            <span></span>
            <span></span>
        </div>
    </div>
</template>

<style>
    .header{
        display: flex;
        background-color:#4DC4FF;
        width: 100%;
        justify-content: space-between;
        padding : 20px 0;
        align-items: center;
        overflow-x:hidden ;
    }
    .logo{
        font-weight: bold;
        color: white;
        font-size: 24px;
        margin-left:50px;
    }
    .header ul{
        display: flex;
        justify-content: space-between;
        color:#daf1fd;
        list-style: none;
        width:44%;
        margin-right:50px;
    }
    .header ul li a{
        text-decoration: none;
    }

    .menu-toggle{
        position: relative;
        display: none;
        flex-direction: column;
        justify-content: space-between;
        height: 24px;
        margin-right: 20px;
        
    }
    .menu-toggle span{
        display: block;
        width: 28px;
        height: 4px;
        background-color: white;
        border-radius: 3px;
        transition: all 0.5s;
    }
    
    .menu-toggle input{
        position: absolute;
        width: 40px;
        height: 28px;
        left:-10px;
        top:-5px;
        z-index: 2;
        opacity: 0;
    }
    .menu-toggle span:nth-child(2){
        transform-origin: 0 0;
    }
    .menu-toggle span:nth-child(4){
        transform-origin: 0 100%;
    }

    .menu-toggle input:checked ~ span:nth-child(2){
        transform: rotate(45deg) translate(1px,1px);
    }
    .menu-toggle input:checked ~ span:nth-child(3){
        transform: scale(0) ;
        opacity: 0;
    }
    .menu-toggle input:checked ~ span:nth-child(4){
        transform: rotate(-45deg) translate(0px,0px); 
    }
    /* Responsive */

    /* Tablet */
    @media screen and (max-width:780px){
        .header ul{
            width: 60%;
        }    
    }
    @media screen and (max-width:625px){
        .menu-toggle{
            display:flex;
        }
        .header ul{
            margin: 0;
            background-color: #4DC4FF;
            position: absolute;
            top: 0;
            right: 0;
            flex-direction: column;
            justify-content: space-evenly;
            align-items: center;
            width: 80%;
            height: 100vh;
            z-index: -1;
            transform: translateX(100%);
        }
   
        
    }
    .header ul li:hover{
        color:white;
        cursor: pointer;
    }
</style>
<script>


</script>





