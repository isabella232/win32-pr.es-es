---
title: Trasladar llamadas de plano de estarcido
description: En OpenGL, se asignan los planos de estarcido solicitando el formato de píxel adecuado con OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Migración de la contabilidad de IRIS, planos de estarcido
- portabilidad de IRIS GL, planos de estarcido
- trasladar a OpenGL desde IRIS GL, planos de estarcido
- Exportación de OpenGL desde IRIS GL, planos de estarcido
- planos de estarcido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 829ea033a75cb1153a475496c3f33398640dbc76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357353"
---
# <a name="porting-stencil-plane-calls"></a>Trasladar llamadas de plano de estarcido

En OpenGL, se asignan los planos de estarcido solicitando el formato de píxel adecuado con OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat). dia. En la tabla siguiente se enumeran las funciones de la contabilidad de IRIS que afectan a los planos de estarcido y sus funciones de OpenGL equivalentes.



| Función de GL de IRIS             | Función OpenGL                                         | Significado                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **Galería de símbolos**( **true**,...) | [**glEnable**](glenable.md) (GL \_ stencil \_ Test)      | Habilita las pruebas de estarcido.                                 |
| **estarcido**                  | [**glStencilOp**](glstencilop.md)                      | Establece las acciones de prueba de estarcido.                             |
| **Galería de símbolos**(... FUNC,...)  | [**glStencilFunc**](glstencilfunc.md)                  | Establece la función y el valor de referencia para las pruebas de estarcido. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Especifica los bits de estarcido que se pueden escribir.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Especifica el valor sin cifrar para el búfer de estarcido.      |
| **sclear**                   | [**glClear**](glclear.md) (bit de búfer de estarcido de GL \_ \_ \_ ) |                                                        |



 

Las funciones de comparación de estarcido y las operaciones de conmutación por error y de estarcido son casi equivalentes en OpenGL y IRIS GL. Las marcas de función de la galería de símbolos GL de IRIS están precedidas por SF; marcas OpenGL con GL. Las marcas de la operación Pass/Fail de IRIS se anteponen a ST; marcas OpenGL con GL.

 

 




