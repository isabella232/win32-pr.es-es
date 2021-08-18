---
title: Greset de porte
description: OpenGL reemplaza la función GL de IRIS, greset, por las funciones glPushAttrib y glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Porte de IRIS GL, variables de estado
- porte desde IRIS GL, variables de estado
- porte a OpenGL desde IRIS GL, variables de estado
- Porte de OpenGL desde IRIS GL, variables de estado
- variables de estado
- Porte de IRIS GL, función greset
- porting from IRIS GL,greset function
- porte a OpenGL desde IRIS GL, función greset
- Porte de OpenGL desde IRIS GL, función greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf5a48c09e7078f3eccd316de9cb86872d61343aabfa0faf60fbe5af2bef218c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936153"
---
# <a name="porting-greset"></a>Greset de porte

OpenGL reemplaza la función GL de IRIS, **greset**, por las funciones [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md). Use estas funciones para guardar y restaurar grupos de variables de estado. Por ejemplo,

``` syntax
void glPushAttrib( GLbitfield mask );
```

En este ejemplo se toma un OR bit a bit de constantes simbólicas, lo que indica qué grupos de variables de estado se insertarán en una pila de atributos. Cada constante hace referencia a un grupo de variables de estado. En la tabla siguiente se muestran los grupos de atributos con sus nombres de constantes simbólicas equivalentes. Para obtener una lista completa de las variables de estado de OpenGL asociadas a cada [**constante, vea glPushAttrib**](glpushattrib.md).



| Atributo                       | Constante                  |
|---------------------------------|---------------------------|
| valor clear del búfer de acumulación | BIT \_ DE BÚFER DE GL ACCUM \_ \_    |
| búfer de color                    | BIT DE \_ BÚFER DE COLOR \_ \_ GL    |
| actuales                         | GL \_ CURRENT \_ BIT          |
| búfer de profundidad                    | BIT DE \_ BÚFER DE PROFUNDIDAD DE \_ \_ GL    |
| enable                          | GL \_ ENABLE \_ BIT           |
| Evaluadores                      | EGL \_ VAL \_ BIT             |
| luz                             | GL \_ FOG \_ BIT              |
| Configuración de GL \_ LIST \_ BASE          | GL \_ LIST \_ BIT             |
| variables de sugerencias                  | GL \_ HINT \_ BIT             |
| variables de iluminación              | GL \_ LIGHTING \_ BIT         |
| modo de dibujo de línea               | GL \_ LINE \_ BIT             |
| variables de modo de píxel            | BIT DE \_ MODO \_ DE PÍXEL \_ GL      |
| variables de punto                 | GL \_ POINT \_ BIT            |
| polygon                         | GL \_ POLYGON \_ BIT          |
| polygon stipple                 | GL \_ POLYGON \_ STIPPLE \_ BIT |
| Tijera                         | BIT \_ DE \_ TORDO DE GL          |
| búfer de galería de símbolos                  | BIT DE \_ BÚFER DE GALERÍA DE SÍMBOLOS DE \_ \_ GL  |
| textura                         | GL \_ TEXTURE \_ BIT          |
| transform                       | GL \_ TRANSFORM \_ BIT        |
| ventanilla                        | BIT DE \_ VENTANILLA \_ DE GL         |
|                                 | GL \_ ALL \_ ATTRIB \_ BITS     |



 

Para restaurar los valores de las variables de estado a los guardados con el último [**glPushAttrib**](glpushattrib.md), simplemente llame [**a glPopAttrib**](glpopattrib.md). Las variables que no ha guardado permanecerán sin cambios. La pila de atributos tiene una profundidad finita de al menos 16.

 

 




