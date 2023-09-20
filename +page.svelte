<script>
	import './styles.css';
    import My_ComputerSrc from '../lib/Icons/35My_Computer.png';
    import My_WebsitesSrc from '../lib/Icons/35My_Websites.png';
    import Contact_MeSrc from '../lib/Icons/25Contact_Me.png';
    import My_BlogSrc from '../lib/Icons/35My_Notes.png';
    import OrangeSrc from '../lib/Icons/25Orange.png';
    let currentDate = new Date();
    let dayNames = ['Sunday', 'Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday'];
    let currentDay = dayNames[currentDate.getDay()];
    let currentTime = currentDate.getHours() + ":" + (currentDate.getMinutes() < 10 ? '0' : '') + currentDate.getMinutes();
    let currentDateString = currentDate.toDateString();
</script>


<div class="icon-container">
    <img src={My_ComputerSrc} alt="Logo" class="icon-image">
    <span>My Computer</span>
</div>

<div class="icon-container">
    <img src={My_WebsitesSrc} alt="Logo" class="icon-image">
    <span>My Websites</span>
</div>

<div class="icon-container">
    <img src={Contact_MeSrc} alt="Logo" class="folder-image">
    <span>Contact Me</span>
</div>

<div class="icon-container">
    <img src={My_BlogSrc} alt="Logo" class="icon-image">
    <span>My Notes</span>
</div>

<div class="bottom-bar">
    <div class="start-box">
        <div class="start-section">
            <img src={OrangeSrc} alt="Start" class="start-icon">
            <span>Start</span>
        </div>
    </div>

    <div class="time-section">
        <span> {currentDateString}, {currentTime}</span>
    </div>
</div>


<style>
    .icon-container {
        display: flex;
        flex-direction: column;
        align-items: center; 
        text-align: center;  
        width: 3%;        
        height: 3%;           
        margin-left: 1%;
        padding: 10px;
    }
    .folder-image {
        width: 105%;        
        height: 105%;       
    }
    .icon-image {
        width: 100%;        
        height: 100%;       
    }
    .icon-container span {
        font-size: 80%;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis; 
        width: 190%;
        padding-top: 10px;
    }
    .bottom-bar {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 50px;
    background-color: hsl(44, 79%, 96%);
    color: #000000;
    display: grid;  /* Change to grid */
    grid-template-columns: auto 1fr; /* First column auto, second column takes up remaining space */
    align-items: center;
    border-radius: 10px;
    border: 2px solid #000; 
    padding-left: 1%;
    gap: 10px;  /* Control the spacing between grid items */
}

.start-section, .time-section {
    display: flex;
    align-items: center;
    margin-right: 2%;
    margin-left: 2%;
}

.time-section {
    justify-content: flex-end;  /* Push content to the right of the column */
    white-space: nowrap;  /* Prevent wrapping to the next line */
}

    .start-icon {
        width: 25px; /* Adjust this as per your needs */
        height: 25px; /* Adjust this as per your needs */
        margin-right: 10%;
        margin-left: 2%;
    }
</style>
