A simple fortran program to set the input (case.ing file) of GIBBS2 code (https://aoterodelaroza.github.io/gibbs2/ )

to compile the program:
     :>     gfortran set_input_gibbs2.f90  -o  set_input_gibbs2
to execute:
      :>   ./set_input_gibbs2
 
Example: 
 =================================================================
          set  input data for Gibbs2                               
       https://aoterodelaroza.github.io/gibbs2/                    
   --------------------------------------------------------        
   Necessary  input paramaters obtained from your ab initio code 
           The bulmk modulus        : B    (GPa)                         
          The prussure derivative  : Bp                            
          The volume               : V0   ( a.u^3)                         
          The total energy at V0   : E0   (Ry  )                       
           MM, the molecularmass of the primitive cell (in a.m.u )      
          VFREE,the total number of atoms in the primitive cell.   
   ********************* 07/01/2024 pg@G.Benabdellah *****************
 
 ---> Enter the volume (in  a.u^3)  : V0=   200
 ---> Enter the bulmk modulus (in GPa ) : B=  120
 ---> Enter the prussure derivative of B: Bp= 4.5
 ---> Enter the equilibrium total energy at V0 ( in Ry) : E0= -3500.  
 
 for  Equation of state: Murnaghan       enter:  m  
 for  Equation of state: Birch-Murnaghan enter:  mb 
 
 ---> Enter your choose (  m | mb) :  m
 
  ---| Equilibrium volume V0 =    200.     
  ---> Eneter the Number of fitted points:(default n=100) : n = 100
 ---> Enter the total number of atoms in the primitive cell: VFREE = 4
 ---> Enter :The molecular Masse of the primitive cell in a.m.u: mm = 98.2
 ---> Enter the phase name (free format) : phase_name =  XXXX
           
 ---> Enter the pressure range: P_init; P_step ;P_final :
  --> pressure range: P_init = 0 
  --> pressure range: P_step = 1
  --> pressure range: P_final = 20
---> Enter the temperature range: T_init; T_step ; T_final :
  --> temperature range: T_init = 50
  --> temperature range: T_step = 50
  --> temperature range: T_final= 500
 
 The units of Gibbs2 : volumes (in bohr^3  ) and energies (in Hartree ).
 
      out data  in file:   case.ing  
 ===
mm   98.2000
vfree  4
pressure      0.00      1.00     20.00
temperature     50.00     50.00    500.00
phase XXXX          fit        murn 
   170.000004768372       -1749.98750289720     
   170.600004673004       -1749.98808042011     
   171.200004577637       -1749.98864033153     
   171.800004482269       -1749.98918296826     
   172.400004386902       -1749.98970865954     
   173.000004291534       -1749.99021772720     
   173.600004196167       -1749.99071048587     
   174.200004100800       -1749.99118724319     
   ...
   ....
  endphase
