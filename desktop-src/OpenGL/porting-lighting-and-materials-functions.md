---
title: Trasladar funciones de iluminación y de materiales
description: Las funciones OpenGL para iluminación y materiales difieren considerablemente de las funciones de contabilidad de IRIS. A diferencia de IRIS GL, OpenGL tiene funciones independientes para establecer luces, modelos claros y materiales.
ms.assetid: de57d041-1ea1-46d0-b584-009608625ea5
keywords:
- Migración de la contabilidad de IRIS, iluminación
- trasladar de IRIS GL, iluminación
- trasladar a OpenGL desde IRIS GL, iluminación
- Exportación de OpenGL desde IRIS GL, iluminación
- Migración de la contabilidad de IRIS, materiales
- portabilidad de IRIS GL, materiales
- portabilidad a OpenGL desde IRIS GL, materiales
- Exportación de OpenGL desde IRIS GL, materiales
- iluminación
- prima
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c775670b7ae49e41fed35c192385c72e72e880b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903670"
---
# <a name="porting-lighting-and-materials-functions"></a>Trasladar funciones de iluminación y de materiales

Las funciones OpenGL para iluminación y materiales difieren considerablemente de las funciones de contabilidad de IRIS. A diferencia de IRIS GL, OpenGL tiene funciones independientes para establecer luces, modelos claros y materiales.

Tenga en cuenta los siguientes puntos al trasladar las funciones de iluminación y materiales:

-   OpenGL no tiene ninguna tabla de definiciones almacenadas. Puede usar listas de visualización para imitar el mecanismo de definición/enlace de la contabilidad de IRIS. Para obtener más información acerca de las detenidas y los enlaces, consulte [Porting, BIND y sets](porting-defs--binds--and-sets.md).
-   Con OpenGL, la atenuación está asociada con cada fuente de luz, en lugar del modelo de iluminación global.
-   Los componentes difusos y especulares se separan en orígenes de OpenGL Light.
-   Los orígenes de OpenGL Light tienen un componente alfa. Al migrar el código de la contabilidad de IRIS, establezca este componente alfa en 1,0, que indica que el 100 por ciento es opaco. Los valores alfa solo se determinan mediante el componente alfa de los materiales, por lo que los objetos de la escena tendrán la misma apariencia que tenían en la contabilidad de IRIS.

En la tabla siguiente se enumeran las funciones de iluminación y materiales de IRIS GL y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS                 | Función OpenGL                               | Significado                                                       |
|----------------------------------|-----------------------------------------------|---------------------------------------------------------------|
| **Imdef (desvuelo**,... **)**    | [glLight](gllight-functions.md)              | Defina una fuente de luz.                                        |
| **Imdef (DEFLMODEL**,... **)**   | [glLightModel](gllightmodel-functions.md)    | Defina un modelo de iluminación.                                      |
| **Enlazar**                       | [**glEnable**](glenable.md) (GL \_ Light *i*) | Habilitar la luz *i*.                                             |
| **Enlazar**                       | **glEnable**(iluminación de contabilidad \_ )                  | Habilitar la iluminación.                                              |
| **Imdef (DEFMATERIAL**,... **)** | [**glMaterial**](glmaterial-functions.md)    | Defina un material.                                            |
| **Imcolor**                      | [**glColorMaterial**](glcolormaterial.md)    | Cambiar el efecto de los comandos de color mientras la iluminación está activa. |
|                                  | [**glGetMaterial**](glgetmaterial.md)        | Obtener parámetros de material.                                      |



 

En la tabla siguiente se enumeran varios parámetros de material de contabilidad de IRIS y sus parámetros de OpenGL equivalentes.



| Índice de Imdef  | parámetro glMaterial                              | Valor predeterminado              | Significado                                                                                       |
|--------------|---------------------------------------------------|----------------------|-----------------------------------------------------------------------------------------------|
| ALPHA        | difusión en contab. \_                                       |                      | El cuarto valor del \_ parámetro difuso de GL especifica el valor alfa.                      |
| AMBIENTES      | ambiente de contabilidad general \_                                       | (0,2, 0,2, 0,2, 1,0) | Color ambiente.                                                                                |
| DIFUSO      | difusión en contab. \_                                       | (0,8, 0,8, 0,8, 1,0) | Color difuso.                                                                                |
| ESPECULA     | \_especular GL                                      | (0,0, 0,0, 0,0, 1,0) | Color de emisor.                                                                               |
| BRILLO    | \_ \_ ambiente \_ y difusión SHININESSGL de \_ GL<br/> | 0,0                  | Exponente especular. Equivalente a llamar a **glMaterial** dos veces con los mismos valores.<br/> |
| COLORINDEXES | \_índices de color de GL \_                                |                      | Índices de color para la iluminación ambiente, difuso y especular.                                    |



 

Cuando el primer parámetro de **Imdef** es DEFMODEL, la traducción de OpenGL equivalente es la función [**glLightModel**](gllightmodel-functions.md). La excepción es cuando el parámetro siguiente a DEFMODEL es ATENUAción: la función de OpenGL equivalente es [**glLight**](gllight-functions.md).

En la tabla siguiente se enumeran los parámetros de modelo de iluminación equivalentes para IRIS GL y OpenGL.



| Índice de Imdef | parámetro glLightModel          | Valor predeterminado              | Significado                                          |
|-------------|---------------------------------|----------------------|--------------------------------------------------|
| AMBIENTES     | \_ambiente de \_ modelo de luz de contabilidad \_       | (0,2, 0,2, 0,2, 1,0) | Color ambiente de la escena.                          |
| ATENUACIÓN |                                 |                      | Vea [**glLight**](gllight-functions.md).        |
| LOCALVIEWER | \_ \_ \_ visor local del modelo \_ de contabilidad solar | CONTABILIDAD \_ falsa            | Visor local (**true**) o infinito (**false**). |
| TWOSIDE     | GL \_ LIGHTMODEL \_ dos \_ lados       | CONTABILIDAD \_ falsa            | Use la iluminación de dos caras cuando sea **true**.            |



 

Cuando el primer parámetro de **Imdef** es deflight, la traducción de OpenGL equivalente es la función [**glLight**](gllight-functions.md) .

En la tabla siguiente se enumeran los parámetros de iluminación equivalentes para IRIS GL y OpenGL.



| Índice de Imdef           | parámetro glLight                                                                                 | Valor predeterminado                                                                             | Significado                                                                        |
|-----------------------|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| AMBIENTES               | \_difusión AMBIENTGL de GL \_<br/> \_especular GL<br/>                                         | (0,0, 0,0, 0,0, 1,0) (1,0, 1,0, 1,0, 1,0)<br/> (1,0, 1,0, 1,0, 1,0)<br/> | Intensidad ambiente. Intensidad difusa.<br/> Intensidad especular.<br/> |
| LCOLOR                | No equivalente.                                                                                    |                                                                                     |                                                                                |
| POSITION              | posición de contabilidad \_                                                                                      | (0,0, 0,0, 1,0, 0,0)                                                                | Posición de la luz.                                                             |
| SPOTDIRECTION         | Dirección de la zona de contabilidad \_ \_                                                                               | (0, 0, 1)                                                                           | Dirección de Spotlight.                                                        |
| PRINCIPALES             | límite de la \_ \_ zona de EXPONENTGL \_ \_<br/>                                                     | 0180<br/>                                                                     | Distribución de intensidad. Ángulo de propagación máximo de la fuente de luz.<br/>        |
| DEFMODEL, ATENUACIÓN | \_ \_ atenuación lineal de ATTENUATIONGL de constantes \_ de contabilidad \_<br/> \_atenuación cuadrática de GL \_<br/> | (1, 0, 0)                                                                           | Factores de atenuación.                                                           |



 

 

 





