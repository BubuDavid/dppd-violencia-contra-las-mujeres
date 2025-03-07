<p align="center">
<img src="http://codeandomexico.org/resources/img/codeandomexico.png" width="500" alt="Codeando México"><br>
<a href="http://www.codeandomexico.org/" target="_blank"><img src="https://img.shields.io/badge/website-CodeandoMexico-00D88E.svg"></a>
<a href="http://slack.codeandomexico.org/" target="_blank"><img src="https://img.shields.io/badge/slack-CodeandoMexico-EC0E4F.svg"></a>
</p>
<!-- __ -->

# Data Powered Positive Deviance

Aplicamos la metodología de Data Powered Positive Deviance, usando una variedad de datos y métodos estadísticos para identificar lugares en la CDMX donde las mujeres están más seguras o donde la violencia de género es menor que en otras áreas con atributos similares. 

### Herramientas de análisis
1. R para el análisis de datos
2. La paquetería sf (simple features) en R para trabajar con objetos espaciales
3. Kepler para realizar mapas de calor 

### Conjuntos de datos utilizados
[Aquí](https://drive.google.com/drive/folders/1PtFnnuCuYEj69Za_8wBCEitDXOW6Y7CF) puedes encontrar las bases de datos para ejecutar los scripts

## Tabla de contenidos

- [Scripts](#scripts)
- [Mapas](#mapas)
- [Contribuir](#contribuir)
- [Atribuciones](#atribuciones)
- [Licencia](#licencia)

## Scripts
Los scripts están agrupados en cuatro carpetas (de acuerdo con las etapas de la metodología de Data Powered Positive Deviance):

1. Homogeneous groups: sirve para agrupar las AGEBS de la CDMX en grupos con características similares en cuanto a factores no controlables en el mediano y corto plazo.  Se hace un análisis de clusters utilizando K medias. 
2. Performance measure: sirve para construir las variables explicativas y de resultados que se usan para crear los modelos de regresión. 
3. PD identification: se ejecutan modelos de regresión para identificar los valores atípicos positivos en los residuos (desviaciones positivas). Se crearon tres tipos de modelos: regresiones binomiales negativas, regresiones lineales y regresiones LASSO. Para cada tipo de regresión se crearon modelos por variable de resultado y por grupo homogéneo.   
4. PD understanding: después de identificar las desviaciones positivas (PDs) se realiza una comparación de las variables modificables en el corto plazo y que pueden incidir en la seguridad de los espacios públicos entre el grupo de PDs y no PDs. 


### Requerimientos
Los scripts se crearon usando RStudio v3.6.2. 
Los scripts están numerados y deben ejecutarse siguiendo el orden de la numeración. 

### Instalación
Al principio de cada script se enlistan las librerías que deben instalarse e importarse para poder ejecutar los scripts. 

### Uso
Los scripts identifican las AGEBS en la CDMX que son desviaciones positivas. Solo ejecuta siguiendo los comentarios de los scripts.


## Outputs

**Mapas**:

- AGEBS urbanas de la CDMX (script 1.1)
- AGEBS por grupos homogéneos (script 1.1) 
- Número de víctimas mujeres en carpetas de investigación de los delitos de los tres niveles de severidad por AGEB (script 1.2)
- AGEBS que son desviaciones positivas (PDs) (script 3.4) 

**Datasets**:

- Variables para crear los grupos homogéneos (basecluster.csv) (script 1.1).
- Variables para ejecutar los modelos (baseageb.csv) (script 2.1). 
- PDs por tipo de regresión (pd_linearreg.csv; pd_lasso.csv; pd_nb.csv) (scripts 3.1.4, 3.2.4 y 3.3.4).
- Variables para hacer la comparación entre PDs y no PDs (base_pdunderstanding.csv) (script 4.1).

[Aquí](https://drive.google.com/drive/u/1/folders/1HgBpSf1u-Oo_6oaWaX5g3mN24ydkcxIs) encontrarás los datasets creados en los scprits 1.1, 2.1, 3.1.4, 3.2.4, 3.3.4 y 4.1 (outputs) 

## Contribuir
Las contribuciones son bienvenidas, puedes abrir un Issue, mandar un Pull Request o contacta a @ricardomiron. 

## Atribuciones

- Itzel Soto @itzsp 
- Alma Rangel @almarngl
- Ricardo Mirón @ricardomiron
- Nadia Neri 


## Licencia
Los contenidos y productos de este repositorio pertenecen a Codeando México, publicado bajo el licenciamiento MIT.
