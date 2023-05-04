# SPRI-based_Qunatitative_Reseptor_Density_Model
Here would like to introduce a numerical approach, building on our previous work \cite{weerakkody_optical_2020, weerakkody_surface_2020}, with the aim to approximately evaluate immobilized peptide densities based on the change in reflectivity observed on the SPRI sensor chip during gas phase analysis.

Based on the definition of the refractive index sensitivity $\partial R/\partial n$, an observed reflectivity shift $\Delta R$ may be accounted for with a change in refractive index along the $z-$direction $\Delta n (z)$:

\begin{equation}
\label{eq:DeltaRd}
    \Delta R = \int_0^{\infty} \frac{\partial R}{\partial n} \Delta n (z) \exp \left(-\frac{z}{L_z} \right) \frac{dz}{L_z}.
\end{equation}

\noindent where the penetration depth $L_z$ a simple exponential decay of the plasmonic wave at proximity of the \ce{Au}-air interface is defined as:

\begin{equation}
\label{eq:Lz}
L_{z} = \frac{\lambda_{w}}{4\pi Im[\frac{\epsilon_{air}}{\sqrt{\epsilon_{air}+\epsilon_{Au}}}]}, 
\end{equation}

In this work $L_{z}\simeq165\,nm$, which was evaluated by setting $\lambda_{w}=632.8\,nm$, while $\epsilon_{Au}$ and $\epsilon_{air}$ were evaluated from the permittivity model \cite{chen_dielectric_2014, weerakkody_optical_2020} and refractive index model \cite{ciddor_refractive_1996}, respectively, at $T = 25^{\circ}C$. 

For the purpose of estimating its grafting densities, this equation was solved to give:

\begin{equation}
\label{eq:deltaRpep}
    \Delta R  = \frac{\partial R}{\partial n} \frac{d_{peptide}}{L_{z}} \Delta n_{peptide} (c)
\end{equation}

\noindent $d_{peptide}$ is the layer thickness of the SAM and $\Delta n_{peptide}(c)$ is the concentration dependent refractive index change caused by the SAM. In fact, $\Delta n_{peptide}$ may also be consider as calculating the refractivity of a single peptide assuming pure additivity with no cooperative effects. Since low concentration SAM formation has also been demonstrated in gas phase \cite{poirier_self-assembly_1996, berger_surface_1997}, we can assume that the shift in refractive index for an added gas of molar mass $M$ in $g.mol^{-1}$ and partial pressure $P$ is $\Delta n_{peptide} \simeq A M P/P_0$ with $P_0 = 1.0135\,bar = 1.0135\times10^5\,Pa$ and $A$ is a molar uniquely a peptide SAM dependant constant $10^6 (n-1)/M$ in $mol.g^{-1}$.  Assuming the ideal gas law, $P V = n R T$ with $R = 8.314\,J\cdot K^{-1}\cdot mol^{-1}$, $P$ the pressure in $Pa = J/m^3$ ($10^5\,Pa = 1\,bar$), $V$ the volume in $m^3$, $n$ the amount of molecules in $mol$ and $T$ the temperature in Kelvin. The concentration of the gas molecules ($c$ in $M = mol.L^{-1}$) is given by $c = P/RT$ from which we deduce:

\begin{equation}
    \Delta n_{peptide} = A M R T c/P_0.
\end{equation}

Now, this can be substituted into equation \ref{eq:deltaRpep}. However, since we are dealing with a monolayer, instead of $d_{peptide}$ we consider a more representative $\sigma_{peptide}=d_{peptide} c/N_A$ referring to the receptor density per unit surface. Knowing that  $V_0 = RT/P_{0}$ and using the Avogadro's number $N_A = 6.022\times 10^{23}$, we can achieve the final form of the equation:

\begin{equation}
   \sigma_{peptide} = \frac{\Delta R N_{A} L_{z}}{\frac{\partial R}{\partial n} A M V_{0}}
\end{equation}

Here, we can see that $A$ is a concentration independent form of $\Delta n_{peptide}/M$. Even though this value is unique for different compounds, generally, similar compounds have shown to have near equivalent values. Therefore, $A$ was assumed to be $20\,mol.g^{-1}$ for all peptide SAMs similar to other equivalent weighted hydrocarbons \cite{w_c_kaye_tables_2019}. It is important to point out that this value provides the largest discrepancy in this approach. Based on recent peptide-related refractive index studies \cite{santi_real-time_2013, de_la_torre_refractive_2021}, we believe that the nature of the receptor and its conformation in the SAM could potentially cause variations in this value. On that account, we caution the use of this value with larger proteins and complex supramolecular assemblies. 
