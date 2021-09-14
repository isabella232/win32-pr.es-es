---
title: Porte de funciones de iluminación y materiales
description: Las funciones de OpenGL para iluminación y materiales difieren considerablemente de las funciones GL de IRIS. A diferencia de IRIS GL, OpenGL tiene funciones independientes para configurar luces, modelos claros y materiales.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Porte de IRIS GL, iluminación
- porte desde IRIS GL, iluminación
- porte a OpenGL desde IRIS GL, iluminación
- Porte de OpenGL desde IRIS GL, iluminación
- Porte de IRIS GL, materiales
- porting from IRIS GL,materials
- porte a OpenGL desde IRIS GL, materiales
- Porte de OpenGL desde IRIS GL, materiales
- iluminación
- Materiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074020"
---
# <a name="porting-lighting-and-materials-functions"></a>Porte de funciones de iluminación y materiales

Las funciones de OpenGL para iluminación y materiales difieren considerablemente de las funciones GL de IRIS. A diferencia de IRIS GL, OpenGL tiene funciones independientes para configurar luces, modelos claros y materiales.

Tenga en cuenta los siguientes puntos al portear funciones de iluminación y materiales:

-   OpenGL no tiene ninguna tabla de definiciones almacenadas. Puede usar listas de visualización para imitar el mecanismo de def/bind de IRIS GL. Para obtener más información sobre defs y binds, vea [Porting Defs, Binds, and Sets](porting-defs--binds--and-sets.md).
-   Con OpenGL, la atenuación está asociada a cada fuente de luz, en lugar del modelo de iluminación general.
-   Los componentes difusos y especulares se separan en orígenes de luz OpenGL.
-   Las fuentes de luz OpenGL tienen un componente alfa. Al porte el código GL de IRIS, establezca este componente alfa en 1.0, lo que indica un 100 % opaco. A continuación, los valores alfa solo los determina el componente alfa de los materiales, por lo que los objetos de la escena tendrán el mismo aspecto que en IRIS GL.

En la tabla siguiente se enumeran las funciones de iluminación y materiales de IRIS GL y sus funciones OpenGL equivalentes.



| Función GL de IRIS                 | Función OpenGL                               | Significado                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef(DEFLIGHT**, ... **)**    | [glLight](gllight-functions.md)              | Defina una fuente de luz.                                        |
| **Imdef(DEFLMODEL**, ... **)**   | [glLightModel](gllightmodel-functions.md)    | Defina un modelo de iluminación.                                      |
| **Imbind**                       | [**glEnable**](glenable.md) ( GL \_ LIGHT *i*) | Habilite light *i*.                                             |
| **Imbind**                       | **glEnable**( GL \_ LIGHTING )                  | Habilite la iluminación.                                              |
| **Imdef(DEFMATERIAL**, ... **)** | [**glMaterial**](glmaterial-functions.md)    | Defina un material.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Cambie el efecto de los comandos de color mientras la iluminación está activa. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Obtener parámetros de material.                                      |



 

En la tabla siguiente se enumeran varios parámetros de material IRIS GL y sus parámetros OpenGL equivalentes.



| Índice imdef  | parámetro glMaterial                              | Valor predeterminado              | Significado                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| ALPHA        | GL \_ DIFUSO                                       |                      | El cuarto valor del parámetro \_ GL DIFFUSE especifica el valor alfa.                      |
| AMBIENTE      | GL \_ AMBIENT                                       | (0.2, 0.2, 0.2, 1.0) | Color ambiente.                                                                                |
| DIFUSO      | GL \_ DIFUSO                                       | (0.8, 0.8, 0.8, 1.0) | Color difuso.                                                                                |
| ESPECULAR     | GL \_ SPECULAR                                      | (0.0, 0.0, 0.0, 1.0) | Color emisivo.                                                                               |
| BRILLO    | GL \_ GL GLINESSGL \_ AMBIENT AND \_ \_ DIFFUSE<br/> | 0,0                  | Exponente especular. Equivalente a llamar **a glMaterial dos** veces con los mismos valores.<br/> |
| COLORINDEXES | ÍNDICES \_ DE COLOR \_ GL                                |                      | Índices de color para la iluminación ambiental, difusa y especular.                                    |



 

Cuando el primer parámetro de **Imdef** es DEFMODEL, la traducción de OpenGL equivalente es la función [**glLightModel**](gllightmodel-functions.md). La excepción es cuando el parámetro que sigue a DEFMODEL es DEFMODEL: then the equivalent OpenGL function is [**glLight**](gllight-functions.md).

En la tabla siguiente se enumeran los parámetros de modelo de iluminación equivalentes para IRIS GL y OpenGL.



| Índice imdef | parámetro glLightModel          | Valor predeterminado              | Significado                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| AMBIENTE     | GL \_ LIGHT \_ MODEL \_ AMBIENT       | (0.2, 0.2, 0.2, 1.0) | Color ambiente de la escena.                          |
| ATENUACIÓN |                                 |                      | Vea [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | VISOR \_ LOCAL DE GL LIGHT \_ MODEL \_ \_ | GL \_ FALSE            | Visor local (**TRUE**) o infinito (**FALSE**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ TWO \_ SIDE       | GL \_ FALSE            | Use la iluminación de dos lados cuando **sea TRUE.**            |



 

Cuando el primer parámetro de **Imdef** es DEFLIGHT, la traducción de OpenGL equivalente es la [**función glLight.**](gllight-functions.md)

En la tabla siguiente se enumeran los parámetros de iluminación equivalentes para IRIS GL y OpenGL.



| Índice imdef           | parámetro glLight                                                                                 | Valor predeterminado                                                                             | Significado                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| AMBIENTE               | GL \_ AMBIENTGL \_ DIFUSO<br/> GL \_ SPECULAR<br/>                                         | (0.0, 0.0, 0.0, 1.0) (1.0, 1.0, 1.0, 1.0)<br/> (1.0, 1.0, 1.0, 1.0)<br/> | Intensidad ambiente. Intensidad difusa.<br/> Intensidad especular.<br/> |
| LCOLOR                | No equivalente.                                                                                    |                                                                                     |                                                                                |
| POSITION              | POSICIÓN \_ DE GL                                                                                      | (0.0, 0.0, 1.0, 0.0)                                                                | Posición de la luz.                                                             |
| SPOTDIRECTION         | DIRECCIÓN DE \_ SPOT \_ DE GL                                                                               | (0, 0, 1)                                                                           | Dirección de los focos destacados.                                                        |
| FOCO             | GL \_ SPOT \_ EXPONENTGL \_ SPOT \_ CUTOFF<br/>                                                     | 0180<br/>                                                                     | Distribución de intensidad. Ángulo de propagación máximo de la fuente de luz.<br/>        |
| DEFMODEL, ATENUACIÓN | ATENUACIÓN LINEAL DE GL \_ CONSTANT \_ \_ \_ ATTENUATIONGL<br/> ATENUACIÓN \_ CUADRÁTICA DE GL \_<br/> | (1, 0, 0)                                                                           | Factores de atenuación.                                                           |



 

 

 





