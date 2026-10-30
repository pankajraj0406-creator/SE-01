# ShikshaSetu: Deep Research & Product Strategy

## Offline Adaptive Learning App for Government-School Students in India

**Document type:** Hackathon research dossier and product strategy\
**Working project name:** ShikshaSetu\
**Research focus:** India, with an initial government-school deployment
context\
**Status:** Preliminary research and product recommendation\
**Important:** This document distinguishes reported research findings
from proposed product decisions and assumptions requiring validation.

------------------------------------------------------------------------

## 1. Executive Summary

The opportunity is not to build another video-based EdTech platform. It
is to build an **offline-first, competency-based adaptive learning
system** that helps students learn at their actual level, rather than
assuming that every student enrolled in the same grade has mastered the
same concepts.

The proposed product, ShikshaSetu, would:

-   Diagnose students' current understanding.
-   Identify missing prerequisite concepts.
-   Recommend an appropriate next lesson or practice activity.
-   Adapt difficulty and explanations based on performance.
-   Work without continuous internet access.
-   Support regional languages.
-   Maintain separate profiles on shared devices.
-   Give teachers useful insight into individual and classroom-level
    learning gaps.
-   Synchronize progress when connectivity becomes available.

The strongest differentiator is the combination of **genuine adaptive
learning, offline operation, low-cost/shared-device deployment,
local-language content and teacher support**.

An offline app is not automatically adaptive. Downloading videos or PDFs
only solves content access. Adaptive learning requires the system to
estimate what a learner understands and use that information to select
the next useful learning activity.

### Preliminary opportunity assessment

  -----------------------------------------------------------------------
  Dimension                           Preliminary assessment
  ----------------------------------- -----------------------------------
  Social impact                       High potential

  Technical feasibility of a focused  High
  MVP                                 

  Innovation potential                Medium to high

  Offline feasibility                 High with careful architecture

  Institutional deployment complexity High

  Long-term scalability               Promising

  Main risks                          Content quality, teacher adoption,
                                      device access and educational
                                      validation
  -----------------------------------------------------------------------

These are qualitative assessments, not externally measured scores.

------------------------------------------------------------------------

## 2. Problem Definition

Three connected problems sit inside this problem statement.

### 2.1 Learning-level differences

Students in the same grade can have very different levels of
foundational understanding. A student enrolled in Grade 6 may still
struggle with multiplication or division. Giving that student more
advanced Grade 6 exercises may not address the underlying gap.

The system should distinguish:

-   **Enrolled grade:** The student's formal school grade.
-   **Current competency:** What the student can currently demonstrate.
-   **Prerequisite knowledge:** Concepts needed to understand the next
    concept.
-   **Learning progression:** The sequence of concepts the student
    should work through.

The underlying problem is that educational content is often organized by
grade, while effective remediation needs to consider what the student
has actually mastered.

### 2.2 Connectivity and device limitations

The earlier research review cited UDISE+ 2024--25 figures reporting that
63.5% of schools had internet access and 93.6% had electricity.

These are school-level infrastructure figures. They do **not** establish
whether an individual student owns a smartphone, whether devices are
available during learning time, or whether connectivity is reliable
throughout the day.

Product implications:

-   Lessons and assessments must work offline.
-   Progress must be saved locally.
-   Recommendations must be calculated locally.
-   Students should be able to share a device without mixing profiles.
-   Synchronization should be useful but not required for everyday
    learning.

### 2.3 Foundational learning gaps

The ASER 2024 rural report was cited for the following government-school
reading figures:

  Indicator                                        Reported figure
  ---------------------------------------------- -----------------
  Grade 3 students able to read a Grade 2 text               23.4%
  Grade 5 students able to read a Grade 2 text               44.8%

These figures concern rural India and should not be generalized to every
government school, state or student.

### 2.4 Problem statement

> Government-school students may have limited access to individualized,
> curriculum-aligned learning support, particularly where connectivity,
> device availability and teacher time are constrained. Students in the
> same grade may have different foundational learning levels. A useful
> system should diagnose these differences, provide targeted practice
> and explanations, and operate reliably without continuous internet
> access.

------------------------------------------------------------------------

## 3. Existing Government Initiatives and Ecosystem

The proposed app should complement existing public education
infrastructure rather than simply recreate it.

### 3.1 DIKSHA

DIKSHA (Digital Infrastructure for Knowledge Sharing) is India's
national digital education platform. The research review identified
capabilities including:

-   Curriculum-linked resources.
-   QR-code access through textbooks.
-   Downloadable content.
-   Offline content consumption.
-   Courses, quizzes and multilingual resources.

**Strategic implication:** A new app that only downloads videos and
quizzes would have weak differentiation. The stronger opportunity is an
adaptive learning layer that diagnoses knowledge gaps and recommends the
next concept or activity.

Official resources:

-   https://diksha.gov.in/
-   https://diksha.gov.in/help/getting-started/diksha-mobile-app/index.html

### 3.2 Other relevant initiatives

  -----------------------------------------------------------------------
  Initiative              Purpose                 Relevance
  ----------------------- ----------------------- -----------------------
  PM e-VIDYA              Digital, online and     Multi-channel learning
                          broadcast education     context

  NIPUN Bharat            Foundational literacy   Learning-level and
                          and numeracy            competency focus

  National Education      Education reform and    Policy context
  Policy 2020             technology integration  

  NDEAR                   National Digital        Interoperability
                          Education Architecture  context

  Samagra Shiksha         School education        Potential institutional
                          support                 deployment context
  -----------------------------------------------------------------------

Official resources:

-   PM e-VIDYA: https://pmevidya.education.gov.in/
-   NIPUN Bharat: https://nipunbharat.education.gov.in/
-   NEP 2020: https://www.education.gov.in/nep/about-nep
-   NDEAR: https://www.ndear.gov.in/
-   Samagra Shiksha: https://samagra.education.gov.in/

### 3.3 Ecosystem positioning

The proposed product should not claim to replace DIKSHA or national
education systems. It should investigate whether it can provide:

1.  Student-level diagnostic assessment.
2.  Competency and prerequisite mapping.
3.  Local adaptive recommendations.
4.  Offline mastery tracking.
5.  Teacher-facing learning-gap insights.
6.  Interoperable content and data workflows where permitted.

Any integration with government platforms must be verified against their
current technical documentation, access rules and licensing.

------------------------------------------------------------------------

## 4. Academic Research and Evidence

### 4.1 Mindspark: personalized adaptive learning in Rajasthan

The J-PAL evaluation, *Scaling Personalized Adaptive Learning (PAL) for
Math and Language in India*, studied Mindspark in government schools in
Rajasthan.

The cited evaluation covered 80 schools and approximately 6,500 students
over 18 months. The reported effects were:

  Subject                   Reported effect
  ------------- ---------------------------
  Mathematics     +0.22 standard deviations
  Hindi           +0.20 standard deviations

These are standard-deviation effects, not percentage-point improvements.

**What this suggests:** Personalized learning software can be integrated
into government-school settings and can improve learning outcomes under
a suitable implementation model.

Sources: -
https://www.povertyactionlab.org/evaluation/scaling-personalized-adaptive-learning-pal-math-and-language-india -
https://www.nber.org/papers/w34205

### 4.2 Individualization and initially low-performing students

A separate randomized evaluation discussed in the research review
involved 1,528 students in Grades 6--8 across 15 schools in Rajasthan.
It compared personalized and grade-level versions of learning software.

The reported finding highlighted in the review was that initially
low-performing students experienced a positive mathematics effect of
0.22 standard deviations, while average students did not show a
meaningful difference between the versions.

**Product implication:** Changing question difficulty alone is not
enough. Adaptation should identify and address the underlying concept
gaps, especially for students with weak foundational understanding.

Source: - https://www.povertyactionlab.org/ (locate the relevant
Mindspark individualization evaluation and verify the full study details
before citing in a formal submission)

### 4.3 Teaching at the Right Level (TaRL)

Pratham's Teaching at the Right Level approach groups and teaches
children according to their actual learning level rather than their
enrolled grade.

Its central principles include:

1.  Assess actual learning levels.
2.  Group students by current proficiency.
3.  Teach concepts appropriate to those levels.
4.  Reassess regularly.
5.  Move students forward as they progress.

Research in India has found positive effects from well-implemented TaRL
interventions. The research review also noted that implementation
quality matters and that some attempts to integrate the approach into
regular government-school routines faced adoption challenges.

**Product implication:** Digitize and support assessment, practice
recommendations and progress monitoring, but keep teachers involved.

Sources: - https://www.pratham.org/ - https://www.povertyactionlab.org/

### 4.4 Knowledge tracing research

Knowledge tracing attempts to estimate a learner's mastery of a skill
from their responses over time.

Methods worth investigating:

-   Bayesian Knowledge Tracing (BKT).
-   Item Response Theory (IRT).
-   Deep Knowledge Tracing (DKT).
-   Forgetting and spaced-repetition models.

A useful review paper is:

Pelánek, R. (2017). *Bayesian knowledge tracing, logistic models, and
beyond: an overview of learner modeling techniques.*

https://doi.org/10.1007/s11257-017-9193-2

**Recommendation:** Begin with a transparent, rules-based mastery
engine. Consider BKT after collecting enough quality learning data. Use
neural knowledge tracing only if data volume and evaluation justify it.

### 4.5 Freadom personalization research

The earlier research review referenced a 2026 NBER working paper
describing a randomized evaluation involving 7,750 students using the
Freadom English-learning app. It reported increased engagement in
targeted content and across the app, while noting that benefits were
front-loaded and diminished as students exhausted the best available
content matches.

**Product implication:** Recommendation quality alone cannot compensate
for a small or repetitive content library. The system must improve both
recommendations and the quality, variety and coverage of content.

Source: - https://www.nber.org/ (verify the exact working paper record,
title and publication details before formal citation)

### 4.6 Research synthesis

  -----------------------------------------------------------------------
  Research area           Main lesson             Product application
  ----------------------- ----------------------- -----------------------
  Mindspark evaluation    Personalized learning   Adaptive instruction
                          can improve outcomes    

  Individualization       Some low-performing     Targeted remediation
  evaluation              students may benefit    
                          particularly            

  TaRL                    Teach according to      Diagnostic assessment
                          actual proficiency      

  Knowledge tracing       Learner mastery can be  Mastery engine
                          modeled over time       

  Freadom personalization Recommendation benefits Content diversity and
  study                   depend on content       coverage
                          availability            
  -----------------------------------------------------------------------

**Central research conclusion:** The strongest product direction is a
competency-based learning engine, not an AI chatbot that merely explains
textbook chapters.

------------------------------------------------------------------------

## 5. Competitor and Alternative Analysis

### 5.1 DIKSHA

**Type:** Government digital education platform.

Strengths identified in the research:

-   Government ecosystem integration.
-   Curriculum resources.
-   QR-linked textbooks.
-   Downloadable and offline content.
-   Multilingual support.

Potential differentiation:

-   Student-level competency diagnosis.
-   Prerequisite-aware remediation.
-   Local adaptive learning paths.
-   Shared-device profiles and offline mastery tracking.

Website: https://diksha.gov.in/

### 5.2 Mindspark

**Type:** Adaptive learning platform by Educational Initiatives.

Strengths:

-   Personalized instruction.
-   Diagnostic learning.
-   Research evidence from Indian school deployments.

Potential differentiation to investigate:

-   Lightweight offline-first architecture.
-   Shared low-cost Android device support.
-   Local-language-first design.
-   Teacher workflows designed around resource-constrained schools.

Website: https://www.mindspark.in/

### 5.3 Khan Academy

**Type:** Nonprofit educational learning platform.

Strengths:

-   Structured lessons.
-   Practice and explanations.
-   Progress tracking.

Potential differentiation:

-   Stronger local curriculum alignment.
-   Offline-first operation.
-   Government-school classroom workflows.

Website: https://www.khanacademy.org/

### 5.4 ePathshala

**Type:** NCERT digital textbook platform.

Strengths:

-   Digital textbooks.
-   Curriculum resources.

Potential differentiation:

-   Move from content access to adaptive assessment and concept mastery.

Website: https://epathshala.nic.in/

### 5.5 Teaching at the Right Level

**Type:** Pedagogical approach and implementation model.

Strengths:

-   Assessment by actual learning level.
-   Foundational learning focus.
-   Teacher-led remediation.

Potential differentiation:

-   Digital assessment support.
-   Individual practice recommendations.
-   Progress tracking and teacher insights.

Website: https://www.pratham.org/

### 5.6 Comparison matrix

  ------------------------------------------------------------------------------
  Capability        DIKSHA            Mindspark              Proposed product
  ----------------- ----------------- ---------------------- -------------------
  Curriculum        Yes               Yes                    Curated/localized
  content                                                    

  Offline access    Yes               Verify by deployment   Core requirement

  Adaptive          Not its central   Yes                    Core requirement
  instruction       documented                               
                    positioning                              

  Foundational      Assessments       Yes                    Core requirement
  diagnostics       available                                

  Shared-device     Verify deployment Verify deployment      Explicit design
  design            details           details                goal

  Teacher dashboard Existing          Deployment-dependent   Planned
                    ecosystem                                
                    features                                 

  Local-language    Multiple          Product-dependent      Core requirement
  support           languages                                
  ------------------------------------------------------------------------------

This is a preliminary positioning comparison, not a complete feature
audit. A blank or qualified cell is not proof that a competitor lacks a
capability.

------------------------------------------------------------------------

## 6. Lessons from BYJU'S: What Not to Build

### 6.1 Important distinction

BYJU'S financial and corporate crisis should not be simplified into a
claim that video-based learning itself failed. Its crisis involved
business strategy, financial management, governance, aggressive
expansion, acquisitions and sales practices. Corporate failure and
educational product effectiveness are related but distinct questions.

Reporting by Reuters and Indian media has documented financial distress,
governance disputes, delayed financial reporting and aggressive sales
concerns.

Sources to verify and cite in a formal report: -
https://www.reuters.com/ - https://indianexpress.com/

### 6.2 Lessons for our product

  -----------------------------------------------------------------------
  BYJU'S-associated risk or approach  Product lesson
  ----------------------------------- -----------------------------------
  Heavy marketing investment          Product value should drive adoption

  Expensive consumer subscription     Avoid making access depend on
  model                               family purchasing power

  Aggressive sales practices          Do not pressure parents or students

  Rapid expansion and acquisitions    Validate one school and one
                                      curriculum before scaling

  Heavy dependence on digital content Content alone does not guarantee
                                      understanding

  Growth-focused strategy             Measure learning outcomes, not only
                                      downloads

  Expensive operating structure       Keep deployment and maintenance
                                      affordable

  Governance and transparency         Maintain accountable operations and
  concerns                            transparent reporting
  -----------------------------------------------------------------------

The proposed product should not optimize for the number of students who
install it. It should optimize for demonstrated learning improvement.

### 6.3 BYJU'S-style versus proposed product

  --------------------------------------------------------------------------
  Dimension               Content/subscription-led   Proposed model
                          model                      
  ----------------------- -------------------------- -----------------------
  Main objective          Deliver educational        Improve concept mastery
                          content                    

  Learning                Video-led lessons          Interactive, adaptive
                                                     learning

  Student level           Grade-oriented content     Actual competency

  Personalization         Recommendations and        Diagnose gaps and adapt
                          learning paths             instruction

  Internet                Digital delivery           Offline-first

  Devices                 Primarily consumer access  Shared-device support

  Languages               Product-dependent          Local-language-first

  Teachers                Supplementary learning     Active teaching partner

  Assessment              Quizzes and progress       Diagnostic and
                                                     continuous mastery

  Revenue                 Consumer subscriptions and Institutional/public
                          other businesses           deployment options

  Success metric          Commercial growth and      Measurable learning
                          engagement                 improvement
  --------------------------------------------------------------------------

This compares broad product strategies, not every feature BYJU'S has
offered.

------------------------------------------------------------------------

## 7. Recommended Product Changes

### Change 1: Think in learning gaps, not courses

Avoid giving every Grade 6 student the same Grade 6 sequence.

Instead:

1.  Assess prerequisite knowledge.
2.  Identify the concept causing difficulty.
3.  Provide a short remedial explanation.
4.  Give targeted practice.
5.  Reassess.
6.  Move forward when the concept is sufficiently understood.

### Change 2: Build an adaptive engine, not an AI chatbot

Use three layers:

**Layer 1: Diagnostic engine** - Estimates current understanding. -
Identifies likely knowledge gaps. - Tracks performance by concept.

**Layer 2: Learning recommendation engine** - Selects the next
concept. - Selects question difficulty. - Chooses remedial or advanced
practice. - Uses curriculum dependencies.

**Layer 3: Explanation assistant** - Gives hints and alternative
explanations. - Uses the student's language. - Can rely on curated
offline explanations. - May use an AI model as an optional support
layer.

The recommendation engine must work offline. AI should be a supporting
component, not a dependency.

### Change 3: Make content modular

Do not require students to download an entire grade-level course.

Example structure:

``` text
Grade 6
  Mathematics
    Numbers
      Multiplication
      Division
    Fractions
      Introduction
      Equivalent Fractions
      Addition of Fractions
    Geometry
      Basic Shapes
      Angles
```

Each concept package should contain:

-   Short explanation.
-   Illustrated example.
-   Practice questions.
-   Hints.
-   Answer explanations.
-   Concept identifiers.
-   Prerequisite relationships.
-   Language variants.
-   Content version and curriculum metadata.

### Change 4: Support shared devices

A single school tablet should support multiple students:

-   Individual profiles.
-   Separate progress records.
-   PIN or QR-based profile selection, subject to school requirements.
-   Session logout.
-   Offline continuation.
-   Teacher-assigned activities.

### Change 5: Make teachers central

The teacher should be able to see:

-   Students behind in foundational concepts.
-   Topics causing difficulty across the classroom.
-   Students needing individual attention.
-   Lesson completion.
-   Whether remedial activities are helping.

The app supports repetitive assessment and practice. Teachers remain
responsible for instruction, motivation and intervention.

### Change 6: Make offline operation genuine

  -----------------------------------------------------------------------
  Function                            Offline requirement
  ----------------------------------- -----------------------------------
  Open downloaded lessons             Yes

  Take assessments                    Yes

  Evaluate answers                    Yes

  Calculate mastery                   Yes

  Recommend next lesson               Yes

  Save student progress               Yes

  View learning history               Yes

  Change local profile                Yes

  Update central teacher dashboard    Sync when connected

  Download new content                Requires connectivity or approved
                                      transfer method
  -----------------------------------------------------------------------

DIKSHA already supports offline content consumption. Differentiation
must come from adaptive learning and classroom usefulness, not offline
availability alone.

------------------------------------------------------------------------

## 8. Continuous Learning Optimization Loop

The central product architecture should continuously improve the
student's learning path.

1.  **Assess:** Identify current understanding.
2.  **Analyze:** Find knowledge gaps, error patterns and prerequisites.
3.  **Personalize:** Select the next lesson, explanation and difficulty.
4.  **Practice:** Provide targeted activities and feedback.
5.  **Reassess:** Check whether understanding improved.
6.  **Update:** Revise the student's mastery estimate and next learning
    path.

### Learning events to record

With appropriate consent and data minimization:

-   Question attempted.
-   Correct or incorrect response.
-   Concept being tested.
-   Difficulty level.
-   Hints used.
-   Whether the student succeeded after remediation.
-   Performance on later assessments.
-   Content version and language.

### Use learning events to improve the system

  -----------------------------------------------------------------------
  Observation                         Potential improvement
  ----------------------------------- -----------------------------------
  Many students fail the same         Review wording or explanation
  question                            

  Students repeatedly struggle with a Improve prerequisite lesson
  prerequisite                        

  Students answer correctly but fail  Add spaced revision
  later                               

  Students abandon long lessons       Break content into smaller
                                      activities

  One language explanation works      Improve localized content
  better                              

  A question is consistently          Request teacher review
  misunderstood                       
  -----------------------------------------------------------------------

Do not automatically interpret every wrong answer as a knowledge gap. It
may be confusing wording, translation, interface design or an incorrect
answer key.

------------------------------------------------------------------------

## 9. Adaptive Learning Engine

### 9.1 Diagnostic assessment example

Illustrative Grade 6 mathematics assessment:

  Concept            Questions   Correct
  ---------------- ----------- ---------
  Addition                   5         5
  Multiplication             5         4
  Division                   5         2
  Fractions                  5         1

The app identifies division and fractions as possible gaps and
investigates prerequisites.

### 9.2 Concept dependency graph

Illustrative simplified graph:

``` text
Basic arithmetic
  ├── Addition
  └── Multiplication
        |
        v
      Division
        |
        v
     Fractions
        |
        v
Advanced fraction operations
```

Actual prerequisites must be validated by subject experts and aligned to
the selected curriculum.

### 9.3 Initial mastery calculation

A simple MVP formula:

\[ M = 100 `\times `{=tex}`\frac{C}{N}`{=tex} \]

Where:

-   \(C\) = correct answers.
-   \(N\) = attempted questions.

Proposed starting thresholds:

  Mastery score   Suggested action
  --------------- -----------------------------------
  Below 40%       Revisit prerequisites
  40--69%         Guided explanation and practice
  70--84%         Continue with the next concept
  85% or above    Mixed assessment and later review

These are initial product hypotheses, not universal educational
standards. Validate them with teachers and assessment results.

### 9.4 Adaptive learning flow

``` mermaid
flowchart TD
    A[Student opens app] --> B[Diagnostic assessment]
    B --> C[Evaluate concept mastery]
    C --> D{Concept mastered?}
    D -->|No| E[Identify missing prerequisite]
    E --> F[Recommend remedial lesson]
    F --> G[Practice questions]
    D -->|Yes| H[Recommend next concept]
    G --> I[Update mastery]
    H --> I
    I --> J{Need further practice?}
    J -->|Yes| E
    J -->|No| K[Save progress locally]
    K --> L[Continue offline]
    K --> M[Sync when internet returns]
```

### 9.5 Recommended algorithm progression

  -----------------------------------------------------------------------
  Stage                   Approach                Reason
  ----------------------- ----------------------- -----------------------
  MVP                     Rules-based mastery     Transparent,
                          engine                  explainable and easy to
                                                  test

  Later                   Bayesian Knowledge      Estimate skill mastery
                          Tracing                 over time

  Later                   Item Response Theory    Model question
                                                  difficulty and learner
                                                  ability

  Research stage          Deep Knowledge Tracing  Consider only with
                                                  adequate quality data
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 10. Technical Architecture

### 10.1 Offline-first architecture

``` mermaid
flowchart TD
    A[Android learning application] --> B[Local adaptive engine]
    A --> C[Local database]
    B --> C
    C --> D[Queued synchronization events]
    D --> E{Internet available?}
    E -->|No| F[Continue offline]
    F --> D
    E -->|Yes| G[Backend API]
    G --> H[Central database]
    H --> I[Teacher dashboard]
    H --> J[Content management]
    J --> K[Versioned content packages]
    K --> A
```

### 10.2 Recommended technology stack

  -----------------------------------------------------------------------
  Layer                   Suggested technology    Reason
  ----------------------- ----------------------- -----------------------
  Android application     Kotlin + Jetpack        Native Android and
                          Compose                 local device
                                                  integration

  Alternative frontend    React Native            Useful for teams
                                                  stronger in TypeScript

  Local database          SQLite / Room           Local persistence

  Backend                 FastAPI                 Lightweight API and
                                                  Python integration

  Central database        PostgreSQL              Student, school and
                                                  curriculum data

  Adaptive engine         Python or TypeScript    Transparent
                          rules engine            recommendations

  Content                 Compressed HTML,        Small downloadable
                          images, audio and JSON  packages

  Teacher dashboard       Next.js + TypeScript    Classroom analytics

  Synchronization         REST API and queued     Intermittent
                          events                  connectivity

  Optional ML             ONNX Runtime Mobile     Local inference where
                                                  justified
  -----------------------------------------------------------------------

**Recommendation:** Use React Native if the team already knows
JavaScript and TypeScript. Do not add a new framework solely for
appearance.

### 10.3 Core data entities

A practical initial data model:

-   School
-   Teacher
-   Student
-   StudentProfile
-   Subject
-   Grade
-   Competency
-   Prerequisite
-   Lesson
-   Question
-   AssessmentAttempt
-   MasteryRecord
-   ContentPackage
-   SyncEvent

Keep personally identifying information separate from learning analytics
wherever practical.

### 10.4 Synchronization requirements

The synchronization layer should support:

-   Queuing events locally.
-   Retrying after network failure.
-   Idempotent event submission.
-   Content versioning.
-   Conflict handling.
-   Data integrity checks.
-   Secure transport.
-   Minimal data collection.

A student must not lose progress because a network request failed.

------------------------------------------------------------------------

## 11. Content and Dataset Strategy

The largest content dependency is a high-quality dataset mapped to
learning competencies.

### 11.1 Potential sources

  ---------------------------------------------------------------------------------------
  Resource                Potential use           Official source
  ----------------------- ----------------------- ---------------------------------------
  DIKSHA                  Curriculum-linked       https://diksha.gov.in/
                          resources               

  NCERT                   Textbooks and           https://ncert.nic.in/textbook.php
                          curriculum references   

  ePathshala              Digital textbooks       https://epathshala.nic.in/

  NIPUN Bharat            Foundational learning   https://nipunbharat.education.gov.in/
                          goals                   

  ASER                    Learning assessment     https://asercentre.org/
                          evidence                

  OpenStax                Additional educational  https://openstax.org/
                          material                
  ---------------------------------------------------------------------------------------

These sources do not automatically provide unrestricted, ready-to-use
adaptive question APIs. Verify content licensing, download methods,
curriculum versions and permitted redistribution before integration.

### 11.2 Proposed content schema

``` json
{
  "subject": "Mathematics",
  "grade": 6,
  "chapter": "Fractions",
  "concept": "Equivalent Fractions",
  "prerequisites": [
    "Division",
    "Multiplication"
  ],
  "difficulty": "easy",
  "language": "Hindi",
  "lesson": {
    "type": "interactive",
    "content": "..."
  },
  "questions": [
    {
      "question": "Which fraction is equal to 1/2?",
      "options": ["2/4", "1/3", "3/5", "2/3"],
      "answer": "2/4",
      "explanation": "..."
    }
  ]
}
```

### 11.3 MVP content scope

Create approximately 30--50 carefully reviewed questions for one subject
and a small number of connected concepts before attempting a huge
content library.

Each package should include:

-   Lesson text.
-   Compressed images and diagrams.
-   Optional audio.
-   Questions and answer keys.
-   Explanations.
-   Concept IDs.
-   Prerequisites.
-   Language variants.
-   Version metadata.

Avoid large video downloads by default.

------------------------------------------------------------------------

## 12. Product Design and User Experience

### Student dashboard

-   Continue learning.
-   Today's learning goal.
-   Subject selection.
-   Progress.
-   Downloaded lessons.

### Diagnostic assessment

-   Short questions.
-   Clear instructions.
-   Visual explanations.
-   Minimal registration friction.

### Adaptive lesson

-   Appropriate difficulty.
-   Interactive exercises.
-   Feedback after incorrect answers.
-   Hints and additional practice.

### Teacher dashboard

-   Student learning levels.
-   Weak concepts across the classroom.
-   Progress reports.
-   Recommended intervention activities.

### Language strategy

Potential initial languages for a Punjab-focused pilot:

-   Punjabi.
-   Hindi.
-   English.

Localization should involve more than literal translation. Examples and
explanations should be understandable in the student's context.

------------------------------------------------------------------------

## 13. Security, Privacy and Ethics

The application is intended for children. Privacy must be part of the
architecture.

  -----------------------------------------------------------------------
  Risk                                Recommended protection
  ----------------------------------- -----------------------------------
  Children's personal information     Collect minimum necessary
                                      information

  Account misuse                      PIN-based local profiles and access
                                      controls

  Unauthorized teacher access         Role-based authorization

  Synchronization conflicts           Versioned records and conflict
                                      handling

  Incorrect recommendations           Teacher review and transparent
                                      explanations

  Assessment bias                     Test across language and
                                      proficiency groups

  Shared-device exposure              Separate profiles and session
                                      logout

  Data loss                           Local persistence and controlled
                                      synchronization
  -----------------------------------------------------------------------

Investigate India's Digital Personal Data Protection Act, 2023 and
applicable rules and commencement notifications, particularly
requirements concerning children's data.

Official reference: - https://www.meity.gov.in/data-protection-framework

Do not assume that parental consent, school consent or a particular
processing arrangement automatically satisfies every legal requirement.
Obligations depend on deployment details and applicable law.

Additional principles:

-   No advertising targeted at children.
-   No unnecessary location tracking.
-   No sale of student data.
-   No artificial engagement loops.
-   No opaque high-stakes automated decisions.
-   Clear teacher oversight.
-   Defined retention and deletion policies.

------------------------------------------------------------------------

## 14. Business and Deployment Model

A consumer subscription model is not recommended as the primary
approach.

The likely customer and deployment partners are institutions rather than
individual children or parents.

### Potential deployment structure

``` text
Government / Education Department
             |
             v
        Government Schools
             |
             v
      Teachers and Devices
             |
             v
           Students
```

### Potential sustainability models

1.  Government or school-level licensing.
2.  CSR-funded deployment.
3.  NGO and education-foundation partnerships.
4.  Institutional implementation and maintenance contracts.
5.  Open-source core with paid institutional support.

These are models to validate, not guaranteed revenue streams.

### Product principles

-   No aggressive sales to parents.
-   No expensive mandatory student subscriptions.
-   No advertisements targeting children.
-   Transparent educational outcome reporting.
-   Financial sustainability without compromising access.

------------------------------------------------------------------------

## 15. Revised Feature Priorities

  Feature                         Priority          Complexity
  ------------------------------- ----------------- ---------------
  Lightweight student profiles    Essential         Low
  Offline lesson downloads        Essential         Medium
  Diagnostic assessment           Highest           Medium
  Concept mastery tracking        Highest           Medium
  Adaptive question difficulty    Highest           Medium
  Concept dependency graph        Highest           Medium
  Local-language lessons          Essential         Medium
  Teacher dashboard               Essential         Medium
  Cloud synchronization           Important         Medium
  Shared-device profiles          Essential         Medium
  Learning outcome tracking       Highest           Medium
  AI chatbot                      Future/optional   High
  Voice-based learning            Future            Medium
  Advanced ML knowledge tracing   Future            High
  Gamification                    Minimal           Low to medium

------------------------------------------------------------------------

## 16. Hackathon MVP Roadmap

A suggested 48-hour plan:

  -----------------------------------------------------------------------
  Time                                Work
  ----------------------------------- -----------------------------------
  0--6 hours                          Select one grade and subject; map
                                      concepts and prepare reviewed
                                      questions

  6--16 hours                         Build student profiles, lessons,
                                      quizzes and local persistence

  16--26 hours                        Implement prerequisite graph,
                                      mastery calculation and
                                      recommendations

  26--36 hours                        Build teacher dashboard and basic
                                      synchronization

  36--48 hours                        Test offline behavior, multiple
                                      profiles, recommendations and
                                      prepare demo
  -----------------------------------------------------------------------

Prioritize one complete workflow over many unfinished features.

### Recommended MVP

A Grade 6 mathematics application with three connected concepts:

1.  Multiplication.
2.  Division.
3.  Fractions.

Create two simulated student profiles:

-   Student A understands multiplication but struggles with division.
-   Student B understands all three concepts.

Demonstrate how Student A receives remedial division practice before
progressing to fractions, while Student B receives more advanced
practice.

Then disconnect the internet and demonstrate that both students can
continue learning with progress retained locally.

------------------------------------------------------------------------

## 17. Testing and Success Metrics

Two separate claims must be tested:

1.  The app works offline.
2.  The app provides meaningful learning adaptation.

### 17.1 Technical tests

-   Complete lessons in airplane mode.
-   Restart without losing progress.
-   Switch between student profiles.
-   Synchronize after reconnecting.
-   Measure content package size.
-   Test on lower-end Android devices.
-   Verify that recommendations work locally.
-   Test interrupted and repeated synchronization.

### 17.2 Educational tests

  Metric                      What it measures
  --------------------------- --------------------------
  Pre-test versus post-test   Learning improvement
  Concept mastery change      Skill progression
  Error patterns              Diagnostic quality
  Lesson completion           Engagement
  Time per concept            Learning efficiency
  Recommendation relevance    Usefulness of adaptation
  Teacher feedback            Classroom usefulness

Use informed consent, school approval and appropriate child-safeguarding
procedures.

A hackathon prototype can demonstrate functionality, but it cannot
establish causal educational impact from a short demo.

### 17.3 Primary KPI

The proposed primary KPI should be:

> Percentage of students demonstrating improvement in independently
> assessed foundational competencies.

Do not use daily active users, screen time, number of videos watched or
downloads as the primary measure of educational success.

------------------------------------------------------------------------

## 18. Risk Register and Pre-Mortem

  -----------------------------------------------------------------------
  Risk                    Severity                Prevention
  ----------------------- ----------------------- -----------------------
  Poor educational        Critical                Teacher-reviewed
  content                                         curriculum

  Incorrect mastery       High                    Transparent rules and
  predictions                                     validation

  Large offline downloads Medium                  Compression and
                                                  selective downloads

  Device incompatibility  High                    Test inexpensive
                                                  Android devices

  Low student interest    High                    Short activities and
                                                  meaningful feedback

  Teacher non-adoption    Critical                Involve teachers from
                                                  the beginning

  Shared profiles mix     High                    Individual local
  data                                            profiles

  Internet unavailable    Medium                  Queue locally and retry
  for sync                                        

  Existing platforms      High                    Differentiate through
  cover basic features                            adaptive functionality
  -----------------------------------------------------------------------

### Three critical assumptions to test

**Assumption 1: Students have enough device access.**

Test through teacher interviews and a small device-access survey.

**Assumption 2: Content can be converted into meaningful learning
paths.**

Create one concept graph and have subject teachers validate
prerequisites.

**Assumption 3: Adaptive recommendations improve learning compared with
fixed lessons.**

Test with a controlled pilot. App engagement alone is not evidence of
learning improvement.

------------------------------------------------------------------------

## 19. Hackathon Judging Strategy

### 19.1 Suggested pitch

Imagine a Grade 6 student attending a government school.

According to school records, the student is in Grade 6. But when asked
to solve a basic division problem, the student struggles.

The classroom continues with the Grade 6 syllabus, while the student's
foundational learning gaps remain unresolved.

Now imagine giving that student a learning companion that understands
their actual learning level.

Our solution is an offline-first adaptive learning application designed
for government-school students.

It works without continuous internet access, provides curriculum-aligned
lessons in regional languages, and adapts the learning experience based
on each student's performance.

If a student struggles with fractions, the application identifies
missing prerequisite concepts and recommends appropriate remedial
lessons instead of simply giving more difficult questions.

Every assessment and learning activity is stored locally and
synchronized when connectivity becomes available.

Teachers also receive insights into individual learning gaps and
classroom progress.

Our objective is simple: education should adapt to the student, rather
than expecting every student to learn at the same speed.

We are building a system where personalized learning does not depend on
expensive infrastructure or continuous internet connectivity.

### 19.2 Likely judge questions

  -----------------------------------------------------------------------
  Question                            Suggested answer
  ----------------------------------- -----------------------------------
  How is this different from DIKSHA?  We focus on an offline adaptive
                                      learning and concept-mastery layer
                                      rather than only providing content
                                      access.

  Why is AI necessary?                AI is optional. The initial engine
                                      uses explainable rules and
                                      curriculum prerequisites.

  How does it work without internet?  Content, assessment, mastery
                                      calculation and recommendations
                                      operate locally.

  How do you know the student is      Pre/post assessments, concept
  improving?                          mastery and repeated evaluation.

  What if a student shares a phone?   Separate student profiles and local
                                      progress records.

  How do you get content?             Curriculum-aligned content with
                                      licensing checks and teacher
                                      validation.

  Can it scale nationally?            The architecture can support more
                                      boards, grades and languages, but
                                      content validation and
                                      institutional deployment require
                                      separate work.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

## 20. Final Recommendation

### Recommended direction

**Offline-first, competency-based adaptive learning for
government-school students.**

The strongest differentiating capabilities are:

1.  Personalized learning based on concept mastery.
2.  Prerequisite-aware remedial learning.
3.  Fully offline assessment and recommendation engine.
4.  Regional-language educational content.
5.  Teacher-level learning analytics.
6.  Shared-device student profiles.
7.  Continuous optimization based on learning outcomes.

### Preliminary subjective scores

  Factor                                Score / 10
  ----------------------------------- ------------
  Social impact                                  9
  Technical feasibility                          9
  Hackathon demonstration potential              9
  Innovation potential                           7
  Scalability potential                          8
  Execution difficulty                           7

These are subjective preliminary hackathon assessments, not externally
measured scores.

### Go/no-go decision

**GO for a scoped MVP.**

The project is technically feasible as a focused prototype. Its
real-world educational impact, teacher adoption, device accessibility
and long-term deployment model remain to be validated.

### Single most important next action

Build and test one real adaptive learning path for a single grade and
subject. Validate the content and prerequisite graph with a teacher
before expanding the application.

------------------------------------------------------------------------

## 21. Research Source Register

The following sources were identified during the research process.
Verify publication dates, exact study details, current access and
licensing before using them in a formal submission.

### Government and education infrastructure

1.  DIKSHA --- https://diksha.gov.in/
2.  DIKSHA mobile app help ---
    https://diksha.gov.in/help/getting-started/diksha-mobile-app/index.html
3.  PM e-VIDYA --- https://pmevidya.education.gov.in/
4.  NIPUN Bharat --- https://nipunbharat.education.gov.in/
5.  National Education Policy ---
    https://www.education.gov.in/nep/about-nep
6.  NDEAR --- https://www.ndear.gov.in/
7.  Samagra Shiksha --- https://samagra.education.gov.in/
8.  NCERT textbooks --- https://ncert.nic.in/textbook.php
9.  ePathshala --- https://epathshala.nic.in/
10. ASER Centre --- https://asercentre.org/
11. MeitY Data Protection Framework ---
    https://www.meity.gov.in/data-protection-framework

### Research and evaluation

12. J-PAL, Scaling Personalized Adaptive Learning for Math and Language
    in India ---
    https://www.povertyactionlab.org/evaluation/scaling-personalized-adaptive-learning-pal-math-and-language-india
13. NBER research --- https://www.nber.org/papers/w34205
14. Pelánek (2017), Bayesian knowledge tracing and learner modeling ---
    https://doi.org/10.1007/s11257-017-9193-2
15. Pratham --- https://www.pratham.org/

### Existing products

16. Mindspark --- https://www.mindspark.in/
17. Khan Academy --- https://www.khanacademy.org/

### Research evidence requiring further bibliographic verification

-   Exact publication and study details for the individualization
    evaluation involving 1,528 students.
-   Exact NBER record and title for the 2026 Freadom personalization
    working paper.
-   Current BYJU'S financial and governance reporting from primary
    filings and reputable reporting.
-   Current UDISE+ 2024--25 tables and methodology.
-   ASER 2024 state-level and national tables relevant to the selected
    pilot geography.

------------------------------------------------------------------------

## 22. Open Questions for the Team

Before implementation, resolve these questions:

1.  Which state and school board will the first pilot target?
2.  Which grade and subject should be selected?
3.  Which curriculum and textbook version will be used?
4.  Are devices individually assigned or shared?
5.  How many days might a school operate without internet?
6.  Which regional languages are required?
7.  Who will validate lessons and concept prerequisites?
8.  What student information is actually necessary?
9.  Who will own content updates and maintenance?
10. How will educational outcomes be independently evaluated?

------------------------------------------------------------------------

## 23. Core Product Principle

> Build something that a school can keep using after the hackathon is
> over, when the internet is down and nobody is paying to advertise it.

The application should not become another content library. It should
become a reliable learning system that identifies what a student does
not understand, helps them learn it, checks whether understanding
improved and uses that evidence to decide what comes next.

**Education should adapt to the student, not the other way around.**
