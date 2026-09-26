---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-09-26
type: landing

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me
      greeting: "Hi, I'm"
      show_status: true
      show_scroll_indicator: true
      typewriter:
        enable: true
        prefix: "I specialize in"
        strings:
          - "quantitative finance"
          - "stochastic modeling"
          - "derivatives pricing"
          - "AI process optimization"
        type_speed: 70
        delete_speed: 40
        pause_time: 2500
      cta_buttons:
        - text: View My Work
          url: "#projects"
          icon: arrow-down
        - text: Get In Touch
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]
  
  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      items:
        - title: Corporate & Investment Banking Intern (CIB)
          company: NTT DATA Europe & Latam
          location: Oviedo, Spain
          date_start: '2026-01-01'
          date_end: '2026-06-30'
          description: |
            
            * Designed and implemented an AI-driven process optimization solution for Banco Santander's Confirming area (€300,000 budget).
            * Engineered automated data pipelines (Python, FastAPI, Pandas) and integrated graph databases to optimize Global Transaction Banking workflows.
            * Automated trading operations and financial reconciliation pipelines using n8n orchestration and NLP, drastically reducing manual intervention.
            * Modeled and monitored credit risk parameters, supporting quantitative infrastructure for Tier-1 financial entities.
        - title: Advanced Mathematics & Physics Tutor
          company: Freelance
          location: Asturias, Spain
          date_start: '2021-09-01'
          date_end: '2023-06-30'
          description: |
            
            * Instructed students in Multivariable Optimization, Differential Calculus, and Finite Difference Methods.
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Education Timeline
  - block: resume-experience
    id: education
    content:
      title: Education
      date_format: Jan 2006
      items:
        - title: Master in Financial Engineering & Innovation (MEFI)
          company: UPM/BME
          location: Madrid, Spain
          date_start: '2026-09-01'
          date_end: '2027-12-31'
          description: |
            
            * Awarded 50% Excellence Scholarship. Focus on Quantitative Finance, Portfolio Risk Optimization, and Statistical Arbitrage.
        - title: Double Degree in Mathematics and Physics
          company: University of Oviedo
          location: Oviedo, Spain
          date_start: '2021-09-01'
          date_end: '2026-06-30'
          description: |
            
            * GPA: 9.5/10 (Ranked 2nd in class). Awarded 11 Honors in core quantitative subjects, including Probability, PDEs, Optimization, and Finite Differences.
            * Pre-University Metric: EBAU Score of 13.7/14 (Ranked Top 10 in Asturias).
        - title: Erasmus+ (Computer Science & AI Exchange Program)
          company: University of Split
          location: Split, Croatia
          date_start: '2024-09-01'
          date_end: '2025-06-30'
          description: |
            
            * Specialized in advanced Deep Learning architectures (CNNs, LSTMs) and AI algorithms.
    design:
      columns: '1'
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Filterable Portfolio
  - block: portfolio
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my recent quantitative and ML work"
      count: 0
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Machine Learning
          tag: ML
        - name: Quantitative
          tag: Quant
      default_button_index: 0
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Visual Tech Stack
  - block: tech-stack
    id: skills
    content:
      title: "Tech Stack & Skills"
      subtitle: "Tools and technologies I use"
      categories:
        - name: Languages
          items:
            - name: Python
              icon: devicon/python
            - name: SQL
              icon: devicon/sqldeveloper
            - name: R
              icon: devicon/r
            - name: MATLAB
              icon: devicon/matlab
        - name: ML & Data
          items:
            - name: PyTorch
              icon: devicon/pytorch
            - name: TensorFlow
              icon: devicon/tensorflow
            - name: Pandas
              icon: devicon/pandas
            - name: Scikit-learn
              icon: devicon/scikitlearn
        - name: Tools & Backend
          items:
            - name: Docker
              icon: devicon/docker
            - name: FastAPI
              icon: devicon/fastapi
            - name: Git
              icon: devicon/git
            - name: LaTeX
              icon: devicon/latex
    design:
      style: grid
      show_levels: false
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's discuss quantitative finance and AI"
      text: |-
        I'm currently available for opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
      email: anxoherrera@gmail.com
      autolink: true
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # CTA Card
  - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm actively looking for roles in **Quantitative Finance**, **Data Science**, and **Financial Engineering**.
        
        Let's connect and discuss how I can bring value to your team.
      button:
        text: 'Download Resume'
        url: uploads/resume.pdf
        new_tab: true
    design:
      card:
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
