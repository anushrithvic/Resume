
\documentclass[letterpaper,11pt]{article}


% Dependencies
% NOTE: Some packages (lastpage, hyperref) require second build!
\usepackage[empty]{fullpage}
\usepackage{titlesec}
\usepackage{enumitem}
\usepackage[hidelinks]{hyperref}
\usepackage{fancyhdr}
\usepackage{fontawesome5}
\usepackage{multicol}
\usepackage{bookmark}
\usepackage{lastpage}

% Sans-Serif
%\usepackage[sfdefault]{FiraSans}
%\usepackage[sfdefault]{roboto}
%\usepackage[sfdefault]{noto-sans}
%\usepackage[default]{sourcesanspro}

% Serif
\usepackage{CormorantGaramond}
\usepackage{charter}

% Colors
% Use with \color{Name}
% Can wrap entire heading with {\color{accent} [...] }
\usepackage{xcolor}
\definecolor{accentTitle}{HTML}{0e6e55}
\definecolor{accentText}{HTML}{0e6e55}
\definecolor{accentLine}{HTML}{a16f0b}

% Misc. Options
\pagestyle{fancy}
\fancyhf{}
\fancyfoot{}
\renewcommand{\headrulewidth}{0pt}
\renewcommand{\footrulewidth}{0pt}
\urlstyle{same}

% Adjust Margins
\addtolength{\oddsidemargin}{-0.7in}
\addtolength{\evensidemargin}{-0.5in}
\addtolength{\textwidth}{1.19in}
\addtolength{\topmargin}{-0.7in}
\addtolength{\textheight}{1.4in}

\setlength{\multicolsep}{-3.0pt}
\setlength{\columnsep}{-1pt}
\setlength{\tabcolsep}{0pt}
\setlength{\footskip}{3.7pt}
\raggedbottom
\raggedright

% ATS Readability
\input{glyphtounicode}
\pdfgentounicode=1

%-----------------%
% Custom Commands %
%-----------------%

% Centered title along with subtitle between HR
% Usage: \documentTitle{Name}{Details}
\newcommand{\documentTitle}[2]{
  \begin{center}
    {\Huge\color{accentTitle} #1}
    \vspace{10pt}
    {\color{accentLine} \hrule}
    \vspace{2pt}
    %{\footnotesize\color{accentTitle} #2}
    \footnotesize{#2}
    \vspace{2pt}
    {\color{accentLine} \hrule}
  \end{center}
}

% Create a footer with correct padding
% Usage: \documentFooter{\thepage of X}
\newcommand{\documentFooter}[1]{
  \setlength{\footskip}{10.25pt}
  \fancyfoot[C]{\footnotesize #1}
}

% Simple wrapper to set up page numbering
% Usage: \numberedPages
% WARNING: Must run pdflatex twice!
\newcommand{\numberedPages}{
  \documentFooter{\thepage/\pageref{LastPage}}
}

% Section heading with horizontal rule
% Usage: \section{Title}
\titleformat{\section}{
  \vspace{-5pt}
  \color{accentText}
  \raggedright\large\bfseries
}{}{0em}{}[\color{accentLine}\titlerule]

% Section heading with separator and content on same line
% Usage: \tinysection{Title}
\newcommand{\tinysection}[1]{
  \phantomsection
  \addcontentsline{toc}{section}{#1}
  {\large{\bfseries\color{accentText}#1} {\color{accentLine} \textbar}}
}

% Indented line with arguments left/right aligned in document
% Usage: \heading{Left}{Right}
\newcommand{\heading}[2]{
  \hspace{10pt}#1\hfill#2\\
}

% Adds \textbf to \heading
\newcommand{\headingBf}[2]{
  \heading{\textbf{#1}}{\textbf{#2}}
}

% Adds \textit to \heading
\newcommand{\headingIt}[2]{
  \heading{\textit{#1}}{\textit{#2}}
}

% Template for itemized lists
% Usage: \begin{resume_list} [items] \end{resume_list}
\newenvironment{resume_list}{
  \vspace{-7pt}
  \begin{itemize}[itemsep=-2px, parsep=1pt, leftmargin=30pt]
}{
  \end{itemize}
  %\vspace{-2pt}
}

% Formats an item to use as an itemized title
% Usage: \itemTitle{Title}
\newcommand{\itemTitle}[1]{
  \item[] \underline{#1}\vspace{4pt}
}

% Bullets used in itemized lists
\renewcommand\labelitemi{--}

%% END_FILE: mteck.sty
%%%%%%%%%%%%%%%%%%%%%%


%===================%
% John Doe's Resume %
%===================%

%\numberedPages % NOTE: lastpage requires a second build
%\documentFooter{\thepage of 2} % Does similar without using lastpage
\begin{document}

  %---------%
  % Heading %
  %---------%

  \documentTitle{Anush Rithvic Murugasamy}{
    % Web Version
    %\raisebox{-0.05\height} \faPhone\ [redacted - web copy] ~
    %\raisebox{-0.15\height} \faEnvelope\ [redacted - web copy] ~
    %%
    
      \raisebox{-0.05\height} \faPhone\ +91 9487327918 ~ | ~
    \href{mailto:anushrithvic@gmail.com}{
      \raisebox{-0.15\height} \faEnvelope\ anushrithvic@gmail.com} ~ | ~
    \href{https://www.linkedin.com/in/anush-rithvic-m-87a154307}{
      \raisebox{-0.15\height} \faLinkedin\ linkedin.com/in/anushrithvic} ~ | ~
    \raisebox{-0.15\height} \faMapMarker\ Coimbatore, Tamil Nadu.
    \
  }

  %---------%
  % Summary %
  %---------%

  % Skills %
  %--------%
  \section{Education}

  \headingBf{Bachelor of  Technology in Computer Science and Engineering}{August 2023 - Present}
  \headingIt{Amrita School of Computing, Amrita Vishwa Vidyapeetham}{Coimbatore , India}
  
  \vspace{5pt}

  \headingBf{Shree Sarasswathi Vidhyaah Mandheer }{Schooling}
  \headingIt{An aggregate of 86\% in Standard 12 and 84\% in Standard 10 }{Coimbatore , India}

  %-----------%
  % Education %
  %-----------%

 \section{Skills}

    \begin{itemize}[itemsep=-2px, parsep=1pt, leftmargin=110pt]
      \item[\textbf{Language}] Python , SQL , C , Java , HTML, Dart (Intermediate)
      \item[\textbf{Problem Solving}] Data structures , Algorithms and Logical Thinking. 
      \item[\textbf{Soft Skills}] Project Leadership , Event Management , Time Management and Prioritization
      \item[\textbf{Frameworks \& Tools}] Tkinter, TensorFlow, PyTorch, PyGame, VS Code, PyCharm, Code Blocks, Windows, macOS
      \item[\textbf{Areas of Interest}] App Development, System Design, Competitive Programming . 

      \end{itemize}

  %------------%
  % Experience %
  %------------%

  \section{Projects}

  \headingBf{Billify}{\href{https://github.com/anushrithvic/Billify.git}{\raisebox{-0.15\height} \faGithub\ GitHub}}
  \headingIt{Generates Invoice}{}
  \begin{resume_list}

    \item Developed \textbf{Billify}, a Python-based invoice generation system leveraging \textbf{Tkinter} for a dynamic front-end,\\\textbf{SQL} for structured back-end data management, and \textbf{FPDF} for professional PDF generation.

    \item Optimized the invoice workflow, achieving an \textbf{80\% increase in generation efficiency} and a \textbf{65\% improvement in accuracy} through seamless integration of UI, database operations, and automated reporting.
  \end{resume_list}

\headingBf{Manage Wise}{}
  \headingIt{Software that Manages Tasks}{}
  \begin{resume_list}
    \item Engineered a robust task management system with \textbf{project tracking, employee scheduling, and real-time analytics}, automating \textbf{75\% of repetitive processes} and enhancing \textbf{task tracking accuracy by 50\%}.
    \item Responsive front-end application using \textbf{Python - tkinter} , seamlessly integrating with an \textbf{SQL} - based back-end, optimizing data retrieval, and enhancing user experience and operational efficiency.

  \end{resume_list}  

  \headingBf{Smart Mirror}{\href{https://github.com/anushrithvic/Smart-Mirror.git}
  {\raisebox{-0.15\height} \faGithub\ GitHub}}
  \headingIt{A Mirror that Blends Functionality with Innovation}{}
  \begin{resume_list}
    \item Developed a state-of-the-art \textbf{intelligent mirror} with real-time updates, including \textbf{time, weather, news, personalized to-do lists, and music playback}, integrating \textbf{APIs for live updates} and a \textbf{voice control system} for hands-free operation.
    \item Utilized \textbf{Raspberry Pi} as the primary hardware platform, with \textbf{Python} for the user interface and Storage solutions are met with \textbf{SQL}

  \end{resume_list}

    \headingBf{Classi Fly}{\href{https://github.com/anushrithvic/ClassiFly.git}
    {\raisebox{-0.15\height} \faGithub\ GitHub}}
  \headingIt{A High-Performance Bird Classification Model}{}
  \begin{resume_list}
    \item Deployed an advanced \textbf{machine learning model} capable of accurately classifying bird species, supporting over \textbf{199 distinct bird classes} utilizing the Kaggle dataset.
    \item Leveraged advanced deep learning frameworks, including \textbf{TensorFlow} and \textbf{PyTorch}, for model training, optimization, and deployment using pre-trained models.

  \end{resume_list}
  
  %-----------%
  % Education %
  %-----------%

\section{Achievements and Activities}
\begin{resume_list}
    \item Selected as a \textbf{Core Team Member of ACM Student Chapter '25-26}, contributing to technical event planning, outreach, and community engagement.
    \item 	Developed innovative projects like Smart Mirror and Manage Wise to improve daily and \textbf{workplace efficiency}.
    \item Enthusiastic about technologies like \textbf{ Raspberry Pi, APIs, and machine learning}, applying them to build practical solutions.
    \item  Led a six-member team in \textbf{Smart India Hackathon} and participated in \textbf{Tech Fest 2022} organized by SSVM.
    \item Certified in \textbf{Python and Problem Solving} by HackerRank.
\end{resume_list}

  

\end{document}


