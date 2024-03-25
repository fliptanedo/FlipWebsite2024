---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

sections:
  - block: flip.avatar
    id: about
    content:
      title: 
      username: admin
      text:
      blurb: |-
        Flip is the first Filipino-American professor of particle physics. He runs a [Physical Science book club](https://sites.google.com/ucr.edu/physci-book-club/) (Phy-Sci) at his local independent book store. He enjoys swimming, basketball, and speculative fiction.
# 
  - block: flip.CV
    id: CV
    cv_pdf: ./files/Tanedo.pdf
    content: 
        title: Curriculum Vitae
        text: Flip Tanedo is an associate professor of theoretical physics at the University of California, Riverside. His research seeks to discover how dark matter fits into our fundamental understanding of nature.
        group_logo: ./img/logo/UCRHEP_2022.png
    awards:
      - thing: NSF CAREER Award
        link: https://beta.nsf.gov/funding/opportunities/faculty-early-career-development-program-career
        dates: 2021 - 2026
      - thing: UCR Junior Excellence in Teaching Award
        link: https://academyteachers.ucr.edu/awards/jet
        dates: 2021
      - thing: Hellman Fellow
        link: http://www.hellmanfellows.org
        dates: 2020 - 2021
      - thing: UCR Commitment to Graduate Diversity Award
        link: https://insideucr.ucr.edu/awards/2020/06/24/four-professors-honored-senate-faculty-awards
        dates: 2020
      - thing: UCI Chancellor's Advance Postdoctoral Fellow
        link: https://inclusion.uci.edu/funding-programs/postdoctoral-fellowship-programs/#capfp
        dates: 2014 - 2015  
      - thing: Paul & Daisy Soros Fellowship
        link: https://www.pdsoros.org
        dates: 2010 - 2012  
      - thing: NSF Graduate Research Fellow
        link: https://www.nsfgrfp.org
        dates: 2006 - 2011  
      - thing: Marshall Scholarship
        link: https://www.marshallscholarship.org
        dates: 2006 - 2008
    interests:
      - interest: Dark Matter
      - interest: Quantum field theory
      - interest: Phenomenology
      - interest: Astro/Cosmo-Particle
    education:
      - course: PhD in Physics
        course_short: PhD
        institution: Cornell University
        institution_short: Cornell
        year: 2013
        logo: /logo/icon_Co.png
      - course: MSc in Physics
        course_short: MSc
        institution: Durham University/IPPP
        institution_short: Durham IPPP
        year: 2008
        logo: /logo/icon_D.png
      - course: MASt in Mathematics
        course_short: MASt
        institution: Cambridge University
        institution_short: Cambridge
        year: 2007
        logo: /logo/icon_Ca.png
      - course: BS in Physics & Mathematics
        course_short: BS
        institution: Stanford University
        institution_short: Stanford
        year: 2008
        logo: /logo/icon_S.png
    service:
      - thing: Fall Physics Colloquium Chair 
      - thing: Website Committee 
      - thing: '[CNAS Equity Advisor](https://diversity.ucr.edu/equity-advisors)'
      - thing: Climate Committee
      - thing: '[Phy Sci Book Club
      Moderator](https://www.cellardoorbookstore.com/book-clubs)'
      - thing: '[POWUR faculty adviser](https://sites.google.com/view/ucr-powur/)'
      - thing: '[APS IDEA UCR lead](https://www.aps.org/programs/innovation/fund/idea.cfm)'
      - thing: '[Snowmass TF/CF Liaison](https://www.aps.org/units/dpf/snowmass-2021.cfm)'
# 
  - block: markdown
    id: research
    content:
      title: Research 
      subtitle:  
      text: |-
        I am a theoretical particle physicist. My main focus has been the search for an fundamental theory of **dark matter**. I specialize in quantum field theories with holographic hidden sectors. These models of dark sectors inform our experimental program to discover new physics. 

          Find more about my current work on [Inspire {{< icon name="inspire" pack="ai" >}}](https://inspirehep.net/literature?sort=mostrecent&size=25&page=1&q=tanedo)
    design:
      columns: '2'
#
  - block: slider
    id: research-slider
    design:
      slide_height: '300px; background-position:center; background-repeat: no-repeat; background-size: cover'
      is_fullscreen: false 
      loop: true
      interval: 3500
    content: 
      title: test
      text: 
      slides:
      - title: 
        content: Find my papers on InspireHEP
        align: center
        background:
          position: right
          # color: '#666'
          brightness: 0.7
          media: research/carousel_chalkboard.jpg
        link:
          icon: atom
          icon_pack: fas
          text: Join Us
          url: https://inspirehep.net/authors/1049892
      - title: ML
        content: Machine Learning High-Dimensional Theory Spaces
        align: left
        background:
          position: left
          # color: '#666'
          brightness: 0.7
          media: research/carousel_ml.jpg
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 2103.06957
          url: https://arxiv.org/abs/2103.06957
        credit: '[@fabioha via Unsplash](https://unsplash.com/photos/oyXis2kALVg)'
      - title: Dark Z
        content: at linear colliders
        align: right
        background:
          position: left
          # color: '#666'
          brightness: 0.7
          media: research/carousel_ILC.jpg
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 2205.10304
          url: https://arxiv.org/abs/2205.10304
        credit: '[@Umberto via Unsplash](https://unsplash.com/photos/  FewHpO4VC9Y)'
      - title: Conformal DM
        content: Continuum Mediated Self-Interactions
        align: left
        background:
          position: left
          # color: '#666'
          brightness: 0.7
          media: research/carousel_sidm.jpg
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 2102.05674
          url: https://arxiv.org/abs/2102.05674
        credit: '[Adrien Olichon via Pexels](https://www.pexels.com/photo/black-sand-dunes-2387793/)'
      - title: AdS
        content: Continuum Soft Bombs
        align: left
        background:
          position: left
          brightness: 0.7
          media: research/carousel_softbomb.jpg
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 2002.12335
          url: https://arxiv.org/abs/2002.12335
        credit: '[Jessica Lewis via Pexels](https://www.pexels.com/photo/  close-up-photo-of-dandelion-1118427/)'
      - title: DM Capture
        content: on relativistic targets
        align: right
        background:
          position: left
          brightness: 0.7
          media: research/carousel_neutronstar.png  # path relative to   `assets/
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 2004.09539
          url: https://arxiv.org/abs/2004.09539
        credit: '[FNS via Pexels](https://www.pexels.com/photo/  stars-during-nighttime-127577/)'
      - title: Symmetry Breaking
        content: vector self-interacting dark matter
        align: left
        background:
          position: left
          brightness: 0.7
          media: research/carousel_fiberbundle.jpg  # path relative to   `assets/
        link:
          icon: graduation-cap
          icon_pack: fas
          text: 1907.10217
          url: https://arxiv.org/abs/1907.10217
        credit: '[@anyctophile via Unsplash ("fiber bundle"   😄)](https://unsplash.com/photos/8uTqI_KpC_Q)'
# 
  - block: flip.teaching
    id: teaching
    content: 
      title: Teaching
      blurb: |-
        How to [request a letter of recommendation](./post/recs/).
    class:
      - name: Math Methods
        number: P17
        session: Spr 2023
        photo: P017-2021.png
        website: 'https://sites.google.com/ucr.edu/physics017/'
      - name: Math Methods
        number: P231
        session: Fall 2022
        photo: P231-2017.png
        website: 'https://sites.google.com/ucr.edu/p231/'
      - name: Math Methods
        number: P17
        session: Spr 2022
        photo: P017-2021.png
        website: 'https://sites.google.com/ucr.edu/physics017/'
      - name: Particle Physics
        number: P165
        session: Spr 2022
        photo: P165-2018.png
        website: 'https://sites.google.com/ucr.edu/p165/'
      - name: Poetry for Physicists
        number: H018
        session: Fall 2021
        photo: H018-2019.png
        website: 'https://sites.google.com/ucr.edu/poetryforphysicists/'
      - name: Math Methods
        number: P231
        session: Fall 2021
        photo: P231-2017.png
        website: 'https://sites.google.com/ucr.edu/p231/'
      - name: General Physics
        number: P40B
        session: Win 2021
        photo: P40B-2020.png
        website: 'https://sites.google.com/ucr.edu/physics40b/home'
      - name: Math Methods
        number: P231
        session: Fall 2020
        photo: P231-2017.png
        website: 'https://sites.google.com/ucr.edu/p231/'
    oldclass:
      - name: General Physics
        number: P40B
        session: Spr 2020
        photo: P40B-2020.png
        website: 'https://sites.google.com/ucr.edu/physics40b-s20/home'
      - name: Quantum Field Theory
        number: P230B
        session: Win 2020
        photo: P230B-2020.png
        website: 'https://sites.google.com/ucr.edu/p230b/'
      - name: Particle Physics
        number: P165
        session: Win 2020
        photo: P165-2018.png
        website: 'https://sites.google.com/ucr.edu/p165/'
      - name: Poetry for Physicists
        number: H018
        session: Fall 2019
        photo: H018-2019.png
        website: 'https://sites.google.com/ucr.edu/poetryforphysicists/'
      - name: Math Methods
        number: P231
        session: Fall 2019
        photo: P231-2017.png
        website: 'https://sites.google.com/ucr.edu/p231/'
      - name: Group Theory
        number: P262
        session: Win 2019
        photo: P262-2019.png
        website: 'https://tanedo.github.io/Physics262-2019/'
      - name: Math Methods
        number: P231
        session: Fall 2018
        photo: P231-2017.png
        website: 'https://tanedo.github.io/Physics231-2018/'
      - name: Computational Physics
        number: P177
        session: Spr 2018
        photo: P177-2018.png
        website: 'https://github.com/Physics177-2018'
      - name: Particle Physics
        number: P165
        session: Win 2018
        photo: P165-2018.png
        website: 'https://github.com/Tanedo/Physics165-2018'
    olderclass:
      - name: Math Methods
        number: P231
        session: Fall 2017
        photo: P231-2017.png
        website: 'https://github.com/Tanedo/P231-2017'
      - name: Computational Physics
        number: P177
        session: Spr 2017
        photo: P177-2017.png
        website: 'https://github.com/Physics177-2017'
      - name: General Relativity
        number: P208
        session: Win 2017
        photo: P208-2017.png
        website: 'https://github.com/Tanedo/Physics208-2017'
      - name: Math Methods
        number: P231
        session: Fall 2016
        photo: P231-2016.png
        website: 'https://github.com/Tanedo/P231-2016'
      - name: Advanced Mechanics
        number: P3318
        session: Spring 2013
        photo: P3318-2013.png
        website: 'https://github.com/Tanedo/P3318-2013'
      - name: Advanced E&M
        number: P3327
        session: Fall 2012
        photo: P3327-2012.png
        website: 'https://github.com/Tanedo/P3327-2012'
      - name: Basic Particles
        number: Pxx
        session: Summer 2012
        photo: Particle4UG.png
        website: 'https://github.com/Tanedo/BasicParticlePhysics'
      - name: Quantum Field Theory
        number: P7561
        session: Fall 2011
        photo: P7651-2011.png
        website: 'https://github.com/Tanedo/P7651-2011'
      - name: Electrodynamics II
        number: P121
        session: Spring 2006
        photo: P121-2006.png
        website: 'https://github.com/Tanedo/P121-2006'
# 
  - block: flip.students
    id: students
    content:
      title: Team
      subtitle: Tanedo Group
      text: |-
        I am part of the [UCR particle theory](https://theory.ucr.edu) group. I also work with some of the theory faculty in the [UCR astro group](https://astro.ucr.edu).

        {{% callout note %}}
        I am not currently taking new Ph.D students. <small>Prospective UCR students should reach out to discuss expectations of studentship.</small>
        {{% /callout %}}

        UCR undergraduates seeking mentoring in particle physics (e.g. through [NMC](https://www.aps.org/programs/minorities/nmc/) or [CL](https://www.cientificolatino.com)) may [contact me](#contact). I welcome invitations for potential postdocs eligible for the [UC PPFP](https://ppfp.ucop.edu/info/) fellowship, NSF MPS ASCEND fellowship, or a [UC-MEXUS](https://alianzamx.universityofcalifornia.edu/research-and-innovation/uc-mexus-conacyt-doctoral-fellow-program/) fellowship.
    mygroup:
      students:
        - name: Matt Lugatiman †
          start: '2022'
          position: Undergrad
          photo: template_matt.jpg
          website: 'https://www.linkedin.com/in/matthew-lugatiman-883820233/'
        - name: Rob Clemenson §
          start: '2022'
          position: Grad
          photo: template_rob.jpg
          website: 'https://cosmicconundra.com/'
        - name: Nathan Kang ‡
          start: '2022'
          position: HS
          photo: template_nathan.jpg
        - name: Yash Aggarwal *
          start: '2019'
          position: Grad
          photo: template_yash.jpg
          website: 'https://orcid.org/0000-0002-3862-0622%20'
        - name: Adam Green
          position: Grad
          start: '2018'
          photo: template_agreen-2.jpg
          website: 'https://github.com/agree019'
        - name: Kuntal Pal*
          position: Grad
          start: '2018'
          photo: template_kuntal.jpg
          website: 
      oldstudents:
        - name: Lexi Costantino
          start: '2018'
          position: Grad
          photo: template_lexi.jpg
          website: 
        - name: Ian Chaffey
          start: '2017'
          end: '2022'
          position: Grad
          photo: template_ian.jpg
          website: 'http://theory.ucr.edu/group.html'
        - name: Aniket Joglekar ◊
          position: Postdoc
          start: '2017'
          end: '2020'
          photo: template_aniket.jpg
          website: 'http://theory.ucr.edu/group.html'
        - name: Cecelia Ngo †
          start: '2021'
          end: '2022'
          position: UG
          photo: portrait.jpg
        - name: Sagada Penano †§
          position: Undergrad (Stanford)
          start: '2020'
          end: '2021'
          photo: template_sagada.jpg
          website: 'https://profiles.stanford.edu/sagada-penano'
        - name: Anagha Satish ‡§
          position: HS
          start: '2020'
          end: '2021'
          photo: template_anagha.jpg
          website: ''
        - name: Sergio Garcia
          start: '2018'
          end: '19'
          position: NMC Mentee
          photo: template_sergio.jpg
          website: 'http://theory.ucr.edu/group.html'
        - name: Corey Kownacki *
          position: Grad
          start: '2017'
          end: '18'
          photo: template_corey.jpg
          website: 'http://theory.ucr.edu/group.html'
        - name: Syris Norelli
          start: '2017'
          end: '18'
          position: UG
          role: Chancellor's Research Fellow
          photo: template_syris.jpg
          website: 'http://theory.ucr.edu/group.html'
        - name: Adam Green
          position: UG
          start: '2016'
          end: '18'
          role: Honors thesis
          photo: template_agreen-2.jpg
          website: 'https://github.com/agree019'
        - name: Kamran Vaziri
          start: '2016'
          end: '17'
          position: MS
          role: Masters Student
          photo: template_kamran.jpg
          website: 'http://theory.ucr.edu/group.html'
    design:
      columns: '2'
# 
  # - block: flip.some
  #   id: public
  #   content:
  #     title: Public
  #     subtitle: (Social) Media
  #     text: |-
  #       {{< twitter fliptanedo >}}
  #     currentpress: |-
  #       * [*Ologies* Podcast](https://www.alieward.com/ologies/scotohylology), 2/8/23
  #       * [*Pollica Summer Workshop, LA7*](https://www.youtube.com/watch?v=ZEgfN_5KErI) 6/11/2022
  #       * [Fourteen UC Riverside professors receive NSF CAREER Awards](https://insideucr.ucr.edu/awards/2021/08/23/fourteen-uc-riverside-professors-receive-nsf-career-awards), Holly Olber, *Inside UCR* 8/23/2021
  #     olderpress: |-
  #       * [*Get to know 10 early-career theorists*](https://www.symmetrymagazine.org/article/get-to-know-10-early-career-theorists), Emily Ayshford, *Symmetry Magazine*, 7/16/19
  #       * [*UCR Magazine*](https://medium.com/ucr-magazine/flip-tanedo-assistant-professor-physics-and-astronomy-b98c51bfa405) 11/21/2018
  #       * [*Science Friday*]((https://www.sciencefriday.com/segments/dark-matter-eludes-particle-physicists/)) [[SciFri Bio](https://www.sciencefriday.com/person/flip-tanedo/)] 06/08/2018
  #       * [Interview with Space.com](https://www.facebook.com/spacecom/videos/space-com-talks-%27nova-wonders:/10155409335906466/) 05/30/18
  #       * [*NOVA Wonders*](https://www.pbs.org/video/nova-wonders-whats-the-universe-made-of-2eyoyw/) 04/04/18
  #       * [Panel Discussion at Harvey Mudd](https://ucrtoday.ucr.edu/53202) 04/30/2018
  #       * [Generation: First [pdf]](./files/clippings/UCRMag_Win_2018_v13_n01.pdf) UCR Magazine, Win. 2018 <!-- (Vol 13, No. 1) -->
  #       * [*Science News*](https://www.sciencenews.org/article/hard-times-theorists-post-higgs-world), 2013
  #   design:
  #     columns: '2'
# 
  - block: flip.portfolio
    id: design
    content:
      title: Design
      subtitle: Portfolio
      text: 
    portfolio:
      - description: '2018'
        title: Ambigram
        photo: AmbigramFlip.png
        website: ambigram
      - description: '2016'
        title: SoCal BSM
        photo: SoCalBSM.png
        website: socalbsm
      - description: '2016'
        title: UCR HEP
        photo: UCRHEP.png
        website: ucrhep
      - description: '2022'
        title: Physics For Ukraine
        photo: PhysicsUkraine.png
        website: ukraine
      - description: '2022'
        title: Snowmass
        photo: snowmasstf.png
        website: snowmass
      - description: '2022'
        title: Business Card
        photo: businesscard.png
        website: businesscard
      - description: '2015'
        title: Particle Bites
        photo: particlebites.png
        website: particlebites
      - description: '2017'
        title: Tinker Feynman
        photo: tinkerfeyn.png
        website: tinker
      - description: '2006'
        title: Stanford SPS
        photo: stanfordphysics.png
        website: stanfordphysics
      - description: '2009'
        title: TASI 09
        photo: TASI.png
        website: tasi
      - description: '2020'
        title: Failed Allies
        photo: failedallies.png
        website: failedallies 
    design:
      columns: '2'
#
  - block: slider
    id: photo-slider
    design:
      slide_height: '300px; background-position:center; background-repeat: no-repeat; background-size: cover'
      is_fullscreen: false 
      loop: true
      interval: 3500
    content:
      slides:
        - title: ACP
          content: Aspen Center for Physics 2019
          credit: w/ Nirmal, Rohana, and Gopi
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/Aspen19.jpg
    
        - title: UCR
          content: theory group lunch 2019
          credit: 
          align: left
          background:
            position: center
            brightness: 0.7
            media: photos/group19.jpg
    
        - title: phy-sci
          content: book club @ Cellar Door
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/physci.jpg
          link:
            icon: book
            icon_pack: fas
            text: phy-sci
            url: https://sites.google.com/ucr.edu/physci-book-club/
    
        - title: 
          content: 
          credit: with Sylvain, Hai-Bo, Brian
          align: left
          background:
            position: center
            brightness: 0.7
            media: photos/saltedpig.jpg
    
        - title: Tanedo
          content: group photo 2019
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/tanedogroup19.jpg
    
        - title: 
          content: 
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/swim.jpg
    
        - title: 
          content: 
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/office.jpg
    
        - title: 
          content: 
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/apple.jpg
    
        - title: 
          content: 
          credit: 
          align: right
          background:
            position: center
            brightness: 0.7
            media: photos/flip_5.jpg
#
  - block: flip.contact
    id: contact
    content:
      title: Contact
      subtitle:
      text: |-
        Please allow a reasonable amount of time before I follow up.
      # Contact (add or remove contact options as necessary)
      # email: test@example.org
      email1: flip.tanedo # using cryptedmail
      email2: ucr # using cryptedmail
      email3: edu # using cryptedmail
      phone: x 26168
      # appointment_url: 'https://calendly.com'
      appointment_blurb: 'Collaborators may book appointments through Calendly'
      appointment_blurb2: 'Contact Flip for the Calendly link'
      address:
        street: 900 University Ave.
        city: Riverside
        region: CA
        postcode: '29521'
        country: United States
        country_code: US
      directions: Physics Building, Room 3054
      office_hours: Office hours by appointment
        # - 'Monday 10:00 to 13:00'
        # - 'Wednesday 09:00 to 10:00'
      # contact_links:
      #   - icon: twitter
      #     icon_pack: fab
      #     name: DM Me
      #     link: 'https://twitter.com/Twitter'
      #   - icon: skype
      #     icon_pack: fab
      #     name: Skype Me
      #     link: 'skype:echo123?call'
      #   - icon: video
      #     icon_pack: fas
      #     name: Zoom Me
      #     link: 'https://zoom.com'
      # Automatically link email and phone or display as text?
      autolink: false
    design:
      columns: '2'
#
  # - block: flip.sponsors
  #   id: sponsors
  #   content:
  #     text: 
  #   departmentlogo: logo_UCRPA.png
  #   sponsorintro: Special thanks to
  #   sponsors:
  #     - sponsor: bob
  #       logo: logo_DOE.png
  #       logowidth: 1116
  #     - sponsor: bob
  #       logo: logo_NSF.png
  #       logowidth: 200
  #     - sponsor: bob
  #       logo: logo_Hellman.png
  #       logowidth: 541
  #   sponsorwidth: 28.57
  #   design:
  #     columns: '1'
---
