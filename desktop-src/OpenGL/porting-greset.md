---
title: Trasladar greset
description: OpenGL reemplaza la función de contabilidad de IRIS, greset, con las funciones, glPushAttrib y glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Puerto de GL de IRIS, variables de estado
- portabilidad de IRIS GL, variables de estado
- trasladar a OpenGL desde IRIS GL, variables de estado
- Exportación de OpenGL desde IRIS GL, variables de estado
- variables de estado
- Migración de la contabilidad de IRIS, función greset
- portabilidad de IRIS GL, función greset
- portabilidad a OpenGL desde IRIS GL, función greset
- Exportación de OpenGL desde IRIS GL, función greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418883"
---
# <a name="porting-greset"></a>Trasladar greset

OpenGL reemplaza la función de contabilidad de IRIS, **greset**, con las funciones, [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md). Use estas funciones para guardar y restaurar grupos de variables de estado. Por ejemplo,

``` syntax
void glPushAttrib( GLbitfield mask );
```

En este ejemplo se toma una operación OR bit a bit de constantes simbólicas, que indican qué grupos de variables de estado se van a enviar a una pila de atributos. Cada constante hace referencia a un grupo de variables de estado. En la tabla siguiente se muestran los grupos de atributos con sus nombres de constantes simbólicos equivalentes. Para obtener una lista completa de las variables de estado de OpenGL asociadas a cada constante, vea [**glPushAttrib**](glpushattrib.md).



| Atributo                       | Constante                  |
|---------------------------------|---------------------------|
| valor de eliminación de búfer de acumulación | \_bit de \_ búfer de acumulación de GL \_    |
| búfer de color                    | \_bit de \_ búfer de color de contabilidad \_    |
| actuales                         | \_bits actual de GL \_          |
| búfer de profundidad                    | \_bit de \_ búfer de profundidad de contabilidad \_    |
| enable                          | \_bit de habilitación de GL \_           |
| evaluadores                      | \_bit de Val de EGL \_             |
| luz                             | \_bit de niebla de contabilidad \_              |
| Configuración de base de \_ lista de contabilidad \_          | \_bit de lista de contab. \_             |
| variables de sugerencia                  | \_bit de sugerencia de GL \_             |
| variables de iluminación              | \_bit de iluminación de GL \_         |
| modo de dibujo de líneas               | \_bit de línea de contabilidad \_             |
| variables de modo de píxel            | \_bit de \_ modo de píxel de contabilidad \_      |
| variables de punto                 | \_bit de punta de contabilidad \_            |
| polygon                         | \_bit de polígono de GL \_          |
| punteado de polígono                 | \_bit de \_ punteado de los polígonos de contabilidad \_ |
| tijera                         | \_bit de tijera de GL \_          |
| búfer de estarcido                  | \_bit de \_ búfer de estarcido GL \_  |
| textura                         | \_bit de textura de GL \_          |
| transform                       | \_bit de transformación de contabilidad \_        |
| ventanilla                        | \_bit de ventanilla de GL \_         |
|                                 | núm. \_ todos los \_ \_ bits attrib     |



 

Para restaurar los valores de las variables de estado a los guardados con el último [**glPushAttrib**](glpushattrib.md), basta con llamar a [**glPopAttrib**](glpopattrib.md). Las variables que no guardó permanecerán sin cambios. La pila de atributo tiene una profundidad finita de al menos 16.

 

 




