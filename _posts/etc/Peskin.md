# Introduction to Quantum Field Theory-Peskin

# 2. The Klein-Gordon Field

## 2.1 The Necessity of the Field Viewpoint

*QM*의 기초적인 과정이 입자의 *dynamical system*의 양자화와 관련이 있다는 것과 같은 흐름으로, *QFT*는 *field*의 *dynamical system*에 대한 *QM*의 응용이다. *QFT*는 *QM*의 현황을 파악하는데 반드시 필요하다. 
우리가 매우 작은 *scale(QM)*과 매우 큰 에너지*(relativistic)*에서 발생하는 과정을 이해하기를 원한다는 것을 고려하였을 때, 왜 *field quantization*을 공부해야 하는지 물을 수 있다. 왜 우리는 *nonrelativistic particle*을 양자화하는 방법으로 *relativistic particle*을 양자화할 수 없는 것일까?
이 질문은 높은 수준에서 대답할 수 있다. 아마 가장 좋은 접근 방법은 *single-particle relativistic wave equation*이 *negative-energy state*와 다른 모순적인 상황이 도출되는 것을 보는 것이다. 이는 *graduate-level QM*의 끝에서 다루지만 왜 이런 방법이 작동하지 않는지 이해하기 쉽다. 우리는 $E=mc^2$가 *particle-antiparticle* 쌍을 생성할 수 있도록 하기 때문에 임의의 상대론적 과정이 *single particle*로 설명할 수 있다고 가정할 수 없다. *pair-creation*에 충분한 에너지가 없다고 하더라도 *second-order perturbation theory*의 중간 과정처럼 *multiparticle state*가 나타날 수 있다. 우리는 이런 *state*가 *uncertainty principle*에 의해 아주 짧은 시간에만 존재한다고 생각할 수 있다. *Perturbation theory*의 *order*를 더 높여가며 접근할 수록 임의의 많은 *‘virtual particle’*이 생성될 수 있다.
*Multiparticle theory*의 필요성은 인과성의 고려로부터 그리 명백하지 않은 방법으로 야기된다. $\mathbf x_0$에서 $\mathbf x$로 *propagate*하는 입자의 *amplitude*는

$
U(t) = \left<\mathbf x
\left|e^{-iHt}\right|\mathbf x_0\right>
$

이다. *Nonrelativistic QM*에서 우리는 $H=\bm p^2/2m$으로 정의하였으므로

$$
\begin{align*}  U(t) &= \left<\mathbf{x}\left|e^{-i(\mathbf{p}^2/2m)t}  \right| \mathbf{x_0}\right> \\  &=\int \frac{d^3p}{(2\pi)^3}\left<\mathbf{x}\left|e^{-i(\mathbf{p}^2/2m)t}  \right| \mathbf{p}\right>\left<\mathbf{p}|\mathbf{x_0}\right> \\  &=\frac{1}{(2\pi)^3}\int d^3p e^{-i(\mathbf{p}^2/2m)t}\cdot  e^{i\mathbf{p}\cdot(\mathbf{x}-\mathbf{x_0})} \\  &=\left(\frac{m}{2\pi it}\right)^{\frac{3}{2}}  e^{im(\mathbf{x}-\mathbf{x_0}^2)/2t}\end{align*}
$$

와 같이 *amplitude* $U(t)$를 계산할 수 있다. *Relativistic QM*에서 우리는 *causality*가 위반되는 결론을 얻을 수 있다. 여기서는 $E=\sqrt{p^2+m^2}$이므로

$$
\begin{align*}  U(t) &= \left<\mathbf{x}\left|e^{-it\sqrt{\mathbf{p}^2+m^2}}  \right| \mathbf{x_0}\right> \\  &=\frac{1}{(2\pi)^3}\int d^3p e^{-it\sqrt{\mathbf{p}^2+m^2}}\cdot  e^{i\mathbf{p}\cdot(\mathbf{x}-\mathbf{x_0})} \\  &=\frac{1}{2\pi^2|\mathbf{x}-\mathbf{x_0}|}  \int^\infty_0dp\,p\,\sin(p|\mathbf{x}-\mathbf{x_0}|)e^{-it\sqrt{p^2+m^2}}\end{align*}
$$

인데 이 적분은 *Bessel function*으로 표현할 수 있다. 우리는 $x^2\gg t^2$, *light cone*의 확실한 바깥 영역에서 점근적인 양상을 볼 것이다. *Phase function* $px-t\sqrt{p^2+m^2}$는 $p=imx/\sqrt{x^2-t^2}$에서 *stationary point*를 가지고 *contour*를 위로 올려 이 점을 지나게 할 수 있다. 따라서 우리는 다음을 발견할 수 있다.

$$
U(t) = e^{-m\sqrt{x^2-t^2}}
$$

이 *propagation amplitude*는 매우 작지만 *spacelike*인 영역에서 $0$이 아니므로 *causality*를 위반한다.

*QFT*는 2.4에서 보게될 흥미로운 방법으로 이 문제를 해결한다. 간단하게 말하자면 *multiparticle field theory*에서  *spacelike interval*을 지나는 *particle propagation*이 반대로 향하는 *antiparticle propagation*과 구별할 수 없다.  $\mathbf x_0$에서의 관측이 $\mathbf x$에서의 관측에 영향을 주는지 물을 수도 있지만 *particle propagation*과 *antiparticle propagation*이 서로 *cancel*되어 *causality*가 보존된다.

또한 *QFT*는 *multiparticle states*와 다른 갯수의 *particle state* 사이의 *transition*을 조정하는 자연스러운 길을 제공한다. 이는 *antiparticle*을 도입하여 *causality problem*을 해결하고 *spin*과 *statistics* 사이의 관계를 설명한다. 하지만 가장 중요한 것은, 수많은 *scattering cross section, lifetime*과 같은 물리량들을 계산하는데 필요한 도구를 제공한다는 점이다.

## 2.2 Elements of Classical Field Theory

### Lagrangian Field Theory

### Hamiltonian Field Theory

### Noether’s Theorem

*Field* $\phi$의 *continuous infinitesimal transformation*을 고려해보자.

$$
\phi(x)\longrightarrow \phi'(x)
= \phi(x)+\alpha\Delta\phi(x)
$$

만약 이 *transformation*이 *equation of motion*에 적용되더라도 *equation*을 변화시키지 않는다면(*invariant*), 이 *transformation*을 ***symmetry***라고 부를 것이다. 이는 *action*이 위의 *transformation*에 불변일 때 특히나 보장된다. 더 일반적으로, 우리는 *action*이 *surface term*에 의해 변하도록 허용할 수 있는데 *surface term*은 *Euler-Lagrange equation*에 영향을 주지 않기 때문이다. 따라서 Lagrangian은 위의 transformation에 의해 다음과 같이 써질 수 있다.

$$
\mathcal{L}(x)\longrightarrow \mathcal{L}'(x)
= \mathcal{L}(x)+\alpha\partial_\mu\mathcal{J}^\mu(x)
$$

이제 Lagrangian의 변화 $\Delta\mathcal{L}$는 

$$
\begin{align*}  \alpha\Delta\mathcal{L}& = \frac{\partial \mathcal{L}}{\partial \phi}  (\alpha\Delta\phi)+\left(\frac{\partial\mathcal{L}}  {\partial(\partial_\mu\phi)}\right)\partial_\mu(\alpha\Delta\phi) \\  &=\alpha\partial_\mu\left(\frac{\partial\mathcal{L}}  {\partial(\partial_\mu\phi)}\Delta\phi\right)+\alpha\left[    \frac{\partial\mathcal{L}}{\partial\phi}-\partial_\mu\left(      \frac{\partial\mathcal{L}}{\partial(\partial_\mu\phi)}    \right)  \right]\Delta\phi\end{align*}
$$

두번째 항은 *Euler-Lagrange equation*에 의해 사라지고 남은 부분 Lagrangian의 변화와 같으므로 다음과 같이 정리할 수 있다.

$$
\begin{align*}  \alpha\partial_\mu\mathcal{J}^\mu(x)=\alpha\partial_\mu  \left(\frac{\partial\mathcal{L}}  {\partial(\partial_\mu\phi)}\Delta\phi\right)\end{align*}
$$

따라서 우리는 다음을 알 수 있다.

$$
\partial_\mu  \left(\frac{\partial\mathcal{L}}  {\partial(\partial_\mu\phi)}\Delta\phi  -\mathcal{J}^\mu(x)\right)  =0
$$

Current $j^\mu(x)$는 다음과 같이 정의할 수 있다.

$$
  j^\mu(x) = \frac{\partial\mathcal{L}}  {\partial(\partial_\mu\phi)}\Delta\phi  -\mathcal{J}^\mu(x)
$$

## 2.3 The Klein-Gordon Field as Harmonic Oscillators

이제 가장 일반적이고 간단한 타입인 *real Klein-Gordon field*의 *quantum field thoery*를 다뤄보자. 이 발상은 *classical field thoery*와 이를 *quantize*하여 *dynamical variable*을 *canonical commutation relation*에 있는 연산자로 재해석하면서 시작한다. 그리고 우리는 *harmonic oscillator*를 이용해 *Hamiltonian*의 *eigenvalue*와 *eigenstate*를 찾아 이론을 풀어갈 것이다.

이를 *quantize*하기 위해 위에서 한 과정을 따라 $\phi,\,\pi$와 적합한 *commutation relation*을 도입한다. *Discrete system*에 대한 *commutation relation*은 다음과 같았다.

$$
[q_i,p_j]=i\delta_{ij};\newline
[q_i,q_j]=[p_i,p_j]=0.
$$

*Continuous system*에서는$\phi,\,\pi$에 대한 *generalization*이 자연스럽다. $\pi(\mathbf{x})$가 *momentum density*이므로 우리는 *Kronecker delta* 대신에 *Dirac delta function*을 이용한다.

$$
[\phi(\mathbf{x}),\pi(\mathbf{y})]=i\delta^{(3)}(\mathbf{x}-\mathbf{y});\newline
[\phi(\mathbf{x}),\phi(\mathbf{y})]=[\pi(\mathbf{x}),\pi(\mathbf{y})]=0.
$$

$\phi,\,\pi$의 함수로 표현되는 *Hamiltonian* 또한 연산자로 해석할 수 있으므로 *spectrum*을 찾을 수 있다. 다만 이를 할 수 있는 명백한 방법이 없기 때문에 우선 *Klein-Gordon equation*을 *Fourier space*에서 다루어 보자. *Klein-Gordon field*를 *expansion*한다면

$$
\phi(\mathbf{x},t) = \int \frac{d^3p}{(2\pi)^3}e^{i\mathbf{p}\cdot\mathbf{x}}\phi(\mathbf{p},t)
$$

이고 *Klein-Gordon equation*은 다음과 같다.

$$
\left[\frac{\partial^2}{\partial t^2}+(|\mathbf{p}|^2+m^2)\right]=\phi(\mathbf{p},t)=0
$$

이 방정식은 다음의 *frequency*를 가진 *SHO*의 *equation of motion*과 같다.

$$
\omega_{\mathbf{p}}=\sqrt{|\mathbf{p}|^2+m^2}.
$$

*SHO*는 우리가 이미 *spectrum*을 어떻게 찾는지 알고 있는 *system*이다. *SHO*의 *Hamiltonian*은

$$
H_\mathrm{SHO}=\frac12 p^2+\frac12\omega^2\phi^2
$$

이고 *Hamiltonian*의 *eigenvalue*를 찾기 위해 $\phi$와 $p$를 *ladder operator*로 표현할 것이다.

$$
\phi = \frac{1}{\sqrt{2\omega}}(a+a^\dagger);\,\,\,\,\,
p=-i\sqrt{\frac{\omega}{2}}(a-a^\dagger).
$$

*Canonical commutation relation* $[\phi,p]=i$는 다음과 동치임을 확인할 수 있다.

$$
[a,a^\dagger]=1.
$$

따라서  Hamiltonian은

$$
H_{\mathrm{SHO}}= \omega\left(a^{\dagger}a+\frac{1}{2}\right)
$$

로 쓸 수 있다.

## 2.4 The Klein-Gordon Field in Space-Time

### Causality

### The Klein-Gordon Propagator

### Particle Creation by a Classical Source

# 3. The Dirac Field

## 3.1 Lorentz invariance in Wave Equations

임의의 *transformation*에 대해 *equation*이 *invariant*하다는 것은 그 *equation*에 *transformation*을 가하더라도 **형태가 일정하게 유지됨을 의미한다**.  예를 들어, $F=ma$는 *position transition* $x\longrightarrow x+a$에 대해 *invariant*하다. *Special relativity*에서 우리는 서로 다른 운동상태에 있는 좌표계 사이의 *transformation*인 *Lorentz transformation*에 대해 배웠고 이에 대해 *invariant*한 대표적인 *quantity*로 *interval*에 대해 알아보았다.

$$
(ds')^2=dx'_\mu dx'^\mu
=a^\alpha_\mu dx_\alpha
a^\mu_\beta dx^\beta
=a^\alpha_\mu a^\mu_\beta dx_\alpha dx^\beta=dx_\alpha dx^\alpha=ds^2
$$

우리의 목표는 이를 *field theory*에 접목시키는 것이다. 그리고 다음과 같은 자연스러운 질문이 떠오른다: ***Lorentz transformation에 대해 invariant한 equation이 존재하는가?*** 그런 *equation*이 존재한다면, 이는 *special relativity*에서 다루는 모든 좌표계에서 만족하는 equation이 존재한다는 것이다. 마치 ******$F=ma$가 외력이 없는 *3-dimensional Euclidean space*에서 성립하는 것처럼. ******이 방정식을 찾기 위해 *active Lorentz transformation*에서 다양한 *quantity*들이 어떻게 영향을 받는지 알아볼 것이다. 

<aside>
💡 **Active transformation**
*Active transformation*은 대상에 작용하고 *passive transformation*은 좌표계에 작용한다. 다음과 같은 *transformation*을 다룬다고 하자.

$$
x'=\Lambda x
$$

*Active transformation*은 *field* $\phi(x)$를 변화시키고 좌표는 그대로 유지하므로 *transform*한 *field*를 $\phi'(x)$라고 쓸 수 있다. *Rotation*을 예시로 생각했을 때, $\phi(x_0)$는 *rotation*의 영향을 받아 $\phi'(x_0')$과 같아진다. 즉,

$$
\phi(x_0) = \phi'(x'_0)
$$

이다. *Rotation*을 예시로 한 이유는 앞으로 다룰 *Lorentz transformation*이 4-*dimensional Minkovski space*에서의 *rotation*으로 볼 수 있기 때문이다. 따라서 *active*한 관점으로 바라본 *field transformation*은 다음과 같이 쓸 수 있다.

$$
\phi(x)\longrightarrow \phi'(x)=\phi(\Lambda^{-1} x).
$$

$\Lambda^{-1}$이 *argument*에 가해진 이유는 *transformation* 이후 $x$에서의 *field*가 *transformation*하기 전($\Lambda$를 가하기 전)의 *field*와 같기 때문이다. *Passive transformation*은 반대로 생각하면 된다.

</aside>

*Least action principle*에서 시작해보자. 이 원리가 항상 유효하려면 *Lorentz transformation*에 대해 *invariant*하여 모든 좌표계에서 성립해야 한다. 이는 *Lagrangian*이 *invariant*하다는 사실을 알려준다. *Lagrangian*이 *transformation*에 대해 *invariant*하다면 *Lagrangian*의 *argument*인 *field*가 극한인 위치가 *transform*되어도 *field*는 그대로 극한을 유지할 것이다. 예를 들어, *field* $\phi(x)$가 $x_0$에서 극한이라면 *Lorentz transformation*을 가한 $x'_0 = \Lambda x_0$에서도 $\phi(x)$는 극한이다.

*Klein-Gordon theory*를 살펴보자. *Lorentz transformation*은 다음과 같이 쓰여진다.

$$
x^\mu\longrightarrow x'^\mu=\Lambda^\mu_\nu x^\nu
$$

이에 관련된 *field transformation*은

$$
\phi(x)\longrightarrow \phi'(x)=\phi(\Lambda^{-1}x)

$$

로 쓸 수 있다. 

## 3.2 The Dirac Equation

## 3.3 Free-Particle Solutions of the Dirac Equation

## 3.4 Dirac Matrices and Dirac Field Bilinears

## 3.5 Quantization of the Dirac Field

## 3.6 Discrete Symmetries of the Dirac Theory

# 4. Interacting Field and Feynman Diagrams

## 4.1 Perturbation Theory

우리는 두가지 실제로 찾을 수 있는 많은 입자들에 대한 *approximate description*을 주는 *field theory*의 *quantization*을 자세하게 다루어 왔다. 여기서 *free particle state*는 *Hamiltonian*의 *eigenstate*를 가질 수 있지만 *interaction*이나 *scattering*을 본 적이 없다. 실제에 더 가까운 *description*을 얻기 위해 우리는 *Hamiltonian*에 새로운 *nonlinear term*을 추가해야 한다. 이 *term*은 서로 다른 *Fourier mode*가 다른 하나에 결합된 형태일 것이다. *Causality*를 보존하기 위해, 우리는 같은 *spacetime poin*t에 있는 *field*의 *product*만을 수반하는 새로운 *term*을 주장한다. 따라서 *interaction*을 서술하는 이 *term*은 아마 다음과 같은 형태일 것이다. 

$$
H_{int} = \int d^3x\,\mathcal{H}_{\mathrm{int}}[\phi(x)]
=-\int d^3x\, \mathcal{L}_{\mathrm{int}}[\phi(x)]
$$

이제 우리는 $\mathcal{H}_{\mathrm{int}}$가 오직 *field*에 대한 *function*이도록 *theory*를 제한할 것이다.

이 chapter에서 우리는 세 가지 중요한 interacting field theory의 예시를 다루게 된다. 첫 번째는 ‘phi-forth” theory로

$$
\mathcal{L}= \frac{1}{2}(\partial_\mu \phi)^2-\frac12 m^2\phi^2-\frac{\lambda}{4!}\phi^4
$$

의 형태를 다룬다. $\lambda$는 coupling constant라 부른다. 이 이론을 순수하게 pedagogical reason으로 설명할지라도, 실제 세상의 model은 $\phi^4$ interaction을 포함한다. 가장 중요한 예시는 electroweak theory의 Higgs field self-interaction이다. $\phi^4$ theory의 equation of motion은 다음과 같이 주어진다.

$$
(\partial^2+m^2)\phi=-\frac{\lambda}{3!}\phi^3.
$$

이는 Klein-Gordon equation에서 가능했던 Fourier analysis로는 풀 수 없다. Quantum theory에서 우리는 equal-time commutation relation $[\phi(\textbf{x}),\pi(\textbf{y})]
=i\delta^{(3)}(\textbf{x}-\textbf{y})$를 도입하였다. 이 theory의 Hamilitonian을 구하는 것과 Heisenberg equation of motion을 구하는 것은 쉬운 연습문제이고 그 결과는 free theory에서 처럼 위 equation of motion과 같다.

두  번째 예시는 QED이다: 

$$
\mathcal{L}_{\rm QED}=
\mathcal{L}_{\rm Dirac}+
\mathcal{L}_{\rm Maxwell}+
\mathcal{L}_{\rm int}
=\bar{\psi}(i\gamma^\mu\partial_\mu-m)\psi
-\frac14(F_{\mu\nu})^2-e\bar{\psi}\gamma^\mu\psi A_\mu.
$$

Gauge covariant derivative $D_\mu=\partial_\mu-ieA_\mu(x)$를 쓰면

$$
\mathcal{L}_{\rm QED}=
\bar{\psi}(i\gamma^\mu D_\mu-m)\psi
-\frac14(F_{\mu\nu})^2
$$

으로 더 쉽게 적을 수 있다. QED Lagrangian의 중요한 성질은 gauge transformation$\psi(x)\longrightarrow e^{i\alpha(x)}\psi(x),\,A_\mu
\longrightarrow A_\mu-\frac1e\partial_\mu\alpha(x)$에 invariant하다는 것이다. 이 transformation은 Dirac field의 local phase rotation이다. 이 invariance는 covariant derivative term을 부여하는 fundamental geomatrical한 중요성을 가진다. 현재 우리의 목적에서 이 transformation은 theory의 symmetry로 인지해도 충분하다.

QED Lagrangian의 equation of motion은 canonical procedure를 따른다. $\psi$에 대한 Euler-Lagrange equation은

$$
(i\gamma^\mu D_\mu-m)\psi(x)=0
$$

이며 이는 minimal coupling prescription $\partial\longrightarrow D$에 의해 eletromagnetic field와 결합된 Dirac equation이다. $A_\nu$에 대한 Euler-Lagrange equation은

$$
\partial_\mu F^{\mu\nu}=e\bar{\psi}\gamma^\nu\psi=ej^\nu
$$

으로 쓰여진다. 이는 inhomogeneous Maxwell equation으로 conserved Dirac current에서 주어진 current density $j^\nu=\bar{\psi}\gamma^\nu\psi$가 포함되어 있다. $\phi^4$ theory와 같이 equation of motion은  $\psi(x)$와  $A_\mu(x)$의 Heisenberg equation of motion으로 얻을 수 있다.

Scattering amplitude를 계산하기 위한 Feynman rule은 functional integral formulation으로 더 쉽게 유도된다. 이 방법은 non-Abelian gauge field의 경우를 일반화한다는 장점이 있다.  현재 chapter에서 우리는photon에 대한 Feynman rule을 간단하게 추측한다. 이는 Yukawa theory의 Feynman rule을 유도한 후에는 더 쉬워질 것이다:  

$$
\mathcal{L}_{\rm Yukawa}=
\mathcal{L}_{\rm Dirac}+
\mathcal{L}_{\rm Klein-Gordon}-
g\bar{\psi}\psi\phi.
$$

이것이 세 번째 예시이다. QED와 유사하지만 photon이 scalar particle $\phi$에 의해 대체되었음을 볼 수 있따. Interaction term은 coupling constant $g$를 포함하고 QED의 $e$에 대응된다. Yukawa는 nucleon $\psi$와 pion $\phi$를 서술하기 위해 이 thoery를 개발했다. Modern particle theory에서 standard model은 scalar Higgs field를 quark과 lepton에 결합하는 Yukawa interaction term을 포함한다. Standard model에서 free parameter의 대부분은 Yukawa coupling constant이다.

## 4.2 Perturbation Expansion of Correlation Functions

## 4.3 Wick’s Theorem

## 4.4 Feynman Diagrams