Note de synthèse sur les Series Chronologiques
================
Hissein Tidei[^1]
2023-05-06

# Nature des series

## Concepts de Base

> **Qu’est ce qu’une série chronologique ou Time Series (TS)?**

C’est une suite finie des observations effectuer à un intervalle
régulier au cours du temps. Dite aussi série temporelles, elle se
matérialise économiquement par l’observation des grandeurs telles que:
IPC, PNB, PIB, etc.

> **La notion de processus stationnaire au sens large (SSL) d’une TS :**

Un processus est $X_t$ est SSL, au sens faible, ou dite de “second
ordre” si et seulement si:

1.  $\mathbb{E}(X_t)=\mu$: constant ou ne croit pas avec le temps ($t$):
    ;
2.  $\mathbb{E}(X^{2}_t)=Var(X_t)=\sigma^2 \neq \infty$: c’est dire et
    ne tend pas vers l’infinie au fil du temps ;
3.  $\gamma\left(k\right)$, sa fonction d’auto-covariance , est
    dépendante de $k$ et non de la position en $t$, celle-ci étant:
    - $\gamma \left( k \right) = Cov \left( X_t, X_{t+k}\right)=E\left\lbrace \left(X_t-\mathbb{E}\left(X_t\right)\right) \left(X_{t+k}-\mathbb{E}\left(X_{t+k}\right) \right)\right\rbrace$
      $\;\forall k \in \mathbb{Z}$
    - $\gamma\left(k=0\right)=\gamma\left(0\right)=\sigma^{2}_x=Var\left(X\right)$
      $=>$ confirme le respect de (2.).

> **La fonction d’auto-corrélation d’un processus $X_t$ SSL**

Confondue avec la covariance dans le cadre de la stationnarité des
séries chrono, elle écrit comme suit [^2]:

.

> **Bruit blanc (BB) ou White noise**

a- ***Simple BB***:

$X_t \rightsquigarrow BB\left(0,\sigma^2\right)$ si :

- $\mathbb{E}\left(X_t\right)=0$;
- $Var\left(X_t\right)= \sigma^2$;
- $\gamma \left( k \right) = Cov \left( X_t, X_{t+k}\right)=0 \quad \forall k \neq O$
  $\Longrightarrow$
  - $\gamma \left( k = o \right)=\sigma^2$
  - $\gamma \left( k \neq o \right) =0$

NB: .

b- ***BB Gaussien(BBG)***:

$X_t \rightsquigarrow BBG\left(0,\sigma^2\right)$ *ssi* :

- $X_t: i.i.d \rightsquigarrow N\left(0,\sigma^2\right)$

Attention : si $X_t\rightsquigarrow BB\left(0,\sigma^2\right)$
$\longrightarrow$
$\rho\left(k\right)= \frac{\gamma\left(k\right)}{ \gamma\left(0\right)}$

## Un processsus moyen Mobile d’ordre q: MA(q)

### Un MA(q=1):

$MA(1)$ est un processus tel $X_t$, tel que :

où:

avec comme:

[^1]: [Twitter](https://twitter.com/HisseinTidei)

[^2]: Cf au démonstration
