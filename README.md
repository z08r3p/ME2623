java c
Module Code: ME2623
Module Title: Engineering Mathematics and Programming
Assessment Title: Solving the 2D Wave   Equation Using the Finite Difference Method
Weighting: 40%
Main objectives of the assessment: 
To develop and document a MATLAB program that solves the 2D wave equation using the finite difference method, demonstrating an understanding of numerical methods, code implementation, and validation techniques.
Brief Description of the assessment: 
The student is required to develop a MATLAB program to solve the 2D wave equation using the finite difference method. Additionally, the student must provide a user guide explaining the functionality of the code, validate its results, and propose potential enhancements for future applications.
Learning outcomes for the assessment: 
1.          Understanding of analytical methods that are 
useful for Mechanical and Aerospace Engineering 
2.          Understanding how to employ programming to solve basic engineering computational problems. 
3.          Applying best-practice programming techniques to solve Mathematical models of Engineering 
problems. 
4.          Understanding the usefulness of programming techniques in the process of solving Engineering problems. 
5.          Presenting computational results in a clear and concise manner including validation and 
verification. 
Assessment and marking criteria 
This assignment will be assessed based on several criteria, each contributing to the final grade as 
indicated by the percentage in brackets: 
● Explaining the interface (20%) 
● Providing a quickstart example (20%) 
● Code annotation (20%) 
● Verification and validation (20%) 
● Suggesting future extensions (10%) 
● Including an appendix with the code (10%) 
Your submission will be assessed based on: 
•             Accuracy       and          stability  of the          numerical implementation. 
•             Clarity          and          comprehensiveness          of  your documentation. 
•             Creativity             and             feasibility             of             proposed extensions. 
Assessment method by which a student can demonstrate learning outcomes: 
Completion of the assignment defined above, which must be submitted via WISEflow for marking.
Format for the assessment/coursework (Guidelines on the expected format and length of submission): 
The university takes academic misconduct very seriously. Further information about this subject can be found here:
• Senate regulation 6: https://www.brunel.ac.uk/about/documents/pdf/Senate-Regulation-6-2020-07-01.pdf
• Library: https://www.brunel.ac.uk/life/library/SubjectSupport/Plagiarism
The university’s policy on using artificial intelligence in your studies can be found here:
https://students.brunel.ac.uk/study/using-artificial-intelligence-in-your-studies

Distribution date to students: 6th December 2024 
Submission Deadline: 6th January 2025 
Indicative Reading List: 
Further information: 
Assignments must be submitted to WISEflow in PDF format (unless stated otherwise), using Arial size 
11 font and limited to no more than three pages. Students are strongly advised to submit their   assignments well ahead of the deadline. 
Late submissions are subject to penalties. 
Assignment Brief 
Solve the following free-vibration 2D hyperbolic equation using the finite difference method: 


Initial condition: 


Boundary condition: 
u(0,y,   t)=u(1,y,   t)=u(x,0,   t)=u(x,1,   t)=0,            t>0
Stability condition: It is suggested that   Δx=ΔY.   Ensure your   numerical scheme satisfies   the   explicit   stability   condition:Note: the stability condition of the explicit time scheme of the 2D wave equation 
Using   afunction   with   the   following   interface,
function u = solve_wave_eq(uinitial,c, Lx, Ly, Mx, My,maxIter,showplot) 
Where: 
Inputs 
u_initial 
Initial displacement field (size MX XMY) representing u(x,y,0) . 
c 
Wave speed (c= 1.5). 
Lx,Ly 
Length of the domain in the x andy directions 
Mx,My 
Number of cells in the  andy directions (e.g., MX=20, MY=20). 
dt 
Time step size (must satisfy the stability condition) 
maxIter 
Maximum number of time steps to solve 
showplot 
Boolean flag to enable/disable plotting of the wave 
Output 
u 
Final displacement field after solving the 2D wave equation for maxIter steps 
Task 
1. Explain the Interface 
1.1    Describe   what   an   interface   is   in   computing   and   explain the   scope   of the   function   in terms   of   its   inputs   and outputs.
1.2    Detail the shapes of uinitial   and the   returned u.
2. Quickstart Example 2.1   Write   a   quickstart   guide   explaining   how   to   use   the   function.   Include   at   least   one   example   test   case
(e.g.,         u   initial=s   in(2mx).s   in(4my),             L   X=LY=1,          MX=MY= 代 写ME2623 Engineering Mathematics and ProgrammingR
代做程序编程语言20)
2.2    Include   plots showing the wave   propagation at various time steps, and   explain   the   physical   significance   of these   results.
2.3    If the code doesn’t work   as expected, explain what   behaviour   you   would   anticipate.
3. Code Annotation 
3.1 Choose two critical snippets of   code and   describe   how   they   work:
3.1.1 Calculating u   at the   next time step   using the finite   difference   method.   3.1.2   Implementing the   boundary conditions.
4. Verification and Validation 
4.1    Discuss   how you verified and validated the code.
Verification:   Ensuring the code   is solving the equations correctly   (e.g., stability   tests).
Validation:   Confirming   the   code   produces   realistic   and   accurate   results   (e.g.,   comparing   to   analytical   solutions or expected   behaviours).
4.2   Suggest      at      least      one      validation      case         (e.g.,   u(x,y,0)=s   in(2mx).s   in(4my)) and      comparing      with analytical   solutions   for   specific   times).
5. Future Extensions 
5.1   Suggest      possible    extensions    to      the      code       (e.g.,    adding      absorbing       boundary    conditions,       modelling   nonlinear waves, or   introducing energy   loss).   Briefly explain   how these could   be   implemented.
6. Appendix 
6.1    Include   the   full   MATLAB   code   as   an   appendix.   Ensure   the   code   is   thoroughly   commented   to   describe   each step.
Example Test Case: 
Run the following scenario to validate your code:
● u   initial(x,   y)=s   in(2nx).s   in(4ny)
● L   X=LY=1
● MX=MY=20
●          dt= 0.002   (ensuring   stability   condition   is   met)
● max   lter=   100Visualize the   results   in several time steps (e.g.,   t=0,0.02,0.04) and describe the   behaviour of the wave.
Code Requirements: 
i.                      Use the explicit finite difference   method to   solve the   wave   equation.
ii.                      Implement fixed   boundary conditions as   specified.
iii.                      Include   input validation to   check:
•               dt   satisfies the stability condition.
• u_initial matches the   size Mx × My   .
•             All   inputs   are   numeric   and   have   appropriate   dimensions.
Suggestions: 
i.                      Format your   submission to include the   required   sections:   Interface   explanation,   quickstart   example,   annotated   code, verification/validation, and future extensions.
ii.                      Use   plots and error analysis   from   the   code   to   support   your   explanations.
iii.                      Ensure the   MATLAB   code   is   included as an   appendix with   additional   comments   if   necessary.
Notes: 
i.                      Refer to   lecture slides, textbooks, or   MATLAB   documentation   if   needed.
ii.                      Unit tests are encouraged to   ensure correct   implementation.
MATLAB Code 
clc; clear all; close all; 
%2D WAVE EQUATION utt = c^2(uxx+uyy) 
%with initial condition    u(x,y,0) = sin(p*pi*x)*sin(q*pi*y), 0 0   % and boundary conditions u(0,y,t) = u(1,y,t)= u(x,0,t)= u(x,1,t) = 0 t>0 c = 1.5;  
dx = 0.01; dy = dx; 
sigma = 1/sqrt(2); gamma = 1/sqrt(2); %Courant-Friedrich Stability   Condition dt = sigma*(dx/c); 
t = 0:dt:1; x = 0:dx:1; y = 0:dy:1; 
u = zeros(length(x),length(y),length(t)); p = 2; q = 4; 
u(:,:,1) = transpose(sin(p.*pi.*x))*sin(q.*pi.*y); %u(x,y,0) = sin(p*pi*x)*sin(q*pi*y) %u(x,y,dt) 
for i=2:length(x)-1 
for j=2:length(y)-1 
u(i,j,2)= (sigma^2)*(u(i+1,j,1)-2*u(i,j,1)+u(i-1,j,1))... 
+(gamma^2)*(u(i,j+1,1)-2*u(i,j,1)+u(i,j-1,1))+2*u(i,j,1) - u(i,j,1); 
end end 
for n=2:length(t)-1 
for i=2:length(x)-1 
for j=2:length(y)-1 
u(i,j,n+1)= (sigma^2)*(u(i+1,j,n)-2*u(i,j,n)+u(i-1,j,n))... 
+(gamma^2)*(u(i,j+1,n)-2*u(i,j,n)+u(i,j-1,n)) + 2*u(i,j,n) - u(i,j,n-1); 
end end 
end 
%Analytic solution SOL = zeros(length(x),length(y),length(t));   S = transpose(sin(p.*pi.*x))*sin(q.*pi.*y); for i=1:length(t) 
SOL(:,:,i) = S*cos(c.*pi.*(sqrt(p^2+q^2).*t(i))); 
end 
%Absolute error E = abs(SOL-u); 
[X,Y] = meshgrid(x,y); 
max_e = max(max(max(E))); for j=1:length(t) 
subplot(2,1,1) colormap(cool); 
p1 = surf(X,Y,u(:,:,j)); 
title(sprintf('2D wave equation at t = %1.2f, con sigma = %1.2fy gamma = %1.2f',t(j),sigma, gamma),'Fontsize',11); xlabel('x','Fontsize',11); ylabel('y','Fontsize',11); 
zlabel(sprintf('u(x,y,t = %1.2f)',t(j)),'Fontsize',11); axis ([0 1 0 1 -1 1]); 
subplot(2,1,2) 
p2 = surf(X,Y,E(:,:,j)); 
title(sprintf('Absolute error at t = %1.2f',t(j)),'Fontsize',11);   xlabel('x','Fontsize',11); ylabel('y','Fontsize',11); 
zlabel(sprintf('E(x,y,t = %1.2f)',t(j)),'Fontsize',11); axis ([0 1 0 1 0 max_e]); 
pause(0.001); hold on; 
if(j~=length(t)) delete(p1); 
delete(p2); 
end end 



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
