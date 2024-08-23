# Portfolio
## Overview
This is a portfolio website to show who Chris Apps is, and provide work-related information. It also has a contact page.
## Components
### Header
The header has a basic logo area at the very top, and the logo sits to the far left. Underneath that is the navbar with two items: home and contact. Each item has a hover and active animation. There are no media queries that affect the header.
```
<header>
    <div class="header-logo"><a href="index.html"><img src="images/sitelogo.png" alt="site logo"></a><h1>Who is Chris Apps?</h1></div>

    <!-- nav bar -->
    <nav>
        <div class="home"><a href="index.html">HOME</a></div>
        <div class="about"><a href="html/contact.html">CONTACT</a></div>
    </nav>
</header>
```
### Footer
The footer functions similarly to the header where it takes up the full width and sits at the very bottom. It contains two social media links (Instagram and Linkedin), and the suburb and postcode where Chris lives. The social media logos are not currently linked to actual sites.
```
<footer>
    <div class="linkedin-logo"><a href="https://www.linkedin.com/in/chrisapps/" target="_blank"><i class="fa-brands fa-linkedin"></i></a></div>
    <div class="instagram-logo"><a href="https://www.instagram.com/appsc_" target="_blank"><i class="fa-brands fa-instagram"></i></a></div>
    <div class="contact">chris.e.apps@gmail.com</div>
</footer>
```
### Main - Home Page
The main area has a simple 4 container design:
* A picture of Chris and a page title
* An introduction feature card - this is a brief intro to who Chris is
* A work-related skill feature card, listing Chris' professional skills
* A work history skill feature card, listing Chris' work history
* "Back to Top" anchor link at the bottom

A media query hides the anchor link on wide screens as the viewport height isn't tall enough to require it. It modifies it at the point where all three feature containers are aligned horizontally.
```
<main>
    <!-- top feature image -->
    <div class="feature main-img"><img src="images/selfportrait.JPG" alt="picture of chris"><h3>Chris Apps</h3></div>
            
    <!-- introduction area -->        
    <article class="feature one">
        <section class="intro title">INTRODUCTION</section>
        <section class="intro graphic"><img src="images/intro-graphic.jpeg" alt="guy in home office with musical equipment and tech"></section>
        <section class="intro text"><p>Hi, I’m Chris, but you can call me Appsy! I’m from the sunny Gold Coast, where I work remotely as a Training Operations Manager and Instructional Designer for an RTO.<br><br> 
        When I’m not busy shaping the future of education, you’ll find me jamming on my guitar or producing music in my studio. I’m here to explore a side gig that might just lead to an exciting career change. 
        <br><br>
        And here’s a fun fact about me: despite all my adventures, I’ve never broken a bone! I’m working from my trusty Mac and ready to bring my talents to the next level.</p>
        </section>
    </article>
    
    <!-- work-related skills area -->
    <article class="feature two"><section class="work-skills title">WORK-RELATED SKILLS</section>
        <section class="work-skills graphic"><img src="images/skills-graphic.jpeg" alt="classroom focusing on technology"></section>
        <section class="work-skills text"><p>I have a strong background in training operations, project management, and instructional design. Over the years, I’ve honed my skills in leading teams, managing accredited programs, and implementing innovative learning solutions. I excel at driving organisational success through strategic planning and effective collaboration across departments. My expertise spans compliance, end-to-end learning design, and integrating technology and AI into training programs, all aimed at boosting operational efficiency and enhancing student satisfaction. Whether I’m pioneering new systems or optimising existing processes, I’m committed to delivering high-impact results that elevate both teams and organisations.</p>
        </section>
    </article>
    
    <!-- work history area -->
    <article class="feature three"><section class="work-history title">WORK HISTORY</section>
        <section class="work-history graphic"><img src="images/history-graphic.jpeg" alt="jet flying low over desert"></section>
        <section class="work-history text">
            <ul>
                <li><span class="work-title">Training Operations Manager</span> (Oct 2023 - Present)</li>
                <li><span class="work-title">Massage Training Manager</span> (Nov 2022 - Oct 2023)</li>
                <li><span class="work-title">Program Coordinator</span> (May 2021 - Nov 2022)</li>
                <li><span class="work-title">Master Coach</span> (Apr 2019 - May 2021)</li>
                <li><span class="work-title">Trainer and Assessor</span> (Jul 2015 - Apr 2019)</li>
                <li><span class="work-title">Personal Trainer & Remedial Therapist</span> (Aug 2014 - May 2021)</li>
                <li><span class="work-title">Logistics Coordinator</span> (Aug 2013 - Jan 2015)</li>
                <li><span class="work-title">Procurement Officer</span> (Nov 2008 - Aug 2013)</li>
                <li><span class="work-title">Aircraft Technician</span> (Jun 2002 - Jun 2008)</li>
                
            </ul>
        </section>
    </article>
    <p id="bottomAnchor"><a href="index.html">Back To Top</a></p>
</main>
```
```
@media screen and (min-width: 1545px) {
      
    main a {
        display: none;
    }

}
```
### Main - Contact Page
The contact page has a simple 4 input field form: name, email, mobile and message. All except the email fields are required. There is a form title and submit button, that doesn't currently work. There is a media query to prevent the form from expanding continually with the viewport, and it will lock width when the viewport gets to 768px.
```
<!-- contact form -->
<main>
    <form>
        <div class="form-title">
            CONTACT FORM
        </div>

        <!-- form labels and inputs-->
        <label for="nameInput">Name (required)</label>
        <input type="text" id="nameInput" required>

        <label for="emailInput">Email (required)</label>
        <input type="email" id="emailInput" required>

        <label for="mobileInput">Mobile</label>
        <input type="tel" id="mobileInput">

        <label id="messageArea" for="messageInput">Message (required)</label>
        <textarea type="text" id="messageInput" required></textarea>
        
        <div class="btn-div">
            <button type="button">SUBMIT</button>
        </div>
    </form>

</main>
```
```
@media screen and (min-width: 1035px) {
    .one, .two, .three {
        min-height: 620px;
        align-content: flex-start;
    }
}
```
### Other Noteable Features
The main and header sections are grouped into their own div so the main content stays at the top of the main container as the CSS styling uses flex-direction: column; and justify-content: space-between;. This ensure the header and footer stay locked at the top and bottom of the screen respectively:
```
<div class="header-main">
    <!-- footer and main html code -->
</div>
```
