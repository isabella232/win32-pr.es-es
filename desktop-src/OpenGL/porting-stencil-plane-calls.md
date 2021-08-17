---
title: Porte de llamadas de plano de galería de símbolos
description: En OpenGL, puede asignar planos de galería de símbolos solicitando el formato de píxel adecuado con los valores de OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: faea8a10-860a-4495-80fb-e83303e397df
keywords:
- Porte de IRIS GL, planos de galería de símbolos
- porting from IRIS GL,stencil planes
- porte a OpenGL desde IRIS GL, planos de galería de símbolos
- Porte de OpenGL desde IRIS GL, planos de galería de símbolos
- planos de galería de símbolos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d2c9ea8a9c025c06f179b51cab1301f8ff871740576a6c9e28cdfc1f15ad3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485395"
---
# <a name="porting-stencil-plane-calls"></a>Porte de llamadas de plano de galería de símbolos

En OpenGL, puede asignar planos de galería de símbolos solicitando el formato de píxel adecuado con los valores **de OpenGL auxInitDisplayMode** o [**ChoosePixelFormat.**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) Funciones. En la tabla siguiente se enumeran las funciones GL de IRIS que afectan a los planos de galería de símbolos y sus funciones OpenGL equivalentes.



| Función GL de IRIS             | Función OpenGL                                         | Significado                                                |
|------------------------------|---------------------------------------------------------|--------------------------------------------------------|
| **stensize**                 | **ChoosePixelFormat**                                   |                                                        |
| **galería de símbolos**( **TRUE**, ... ) | [**glEnable**](glenable.md) ( GL \_ STENCIL \_ TEST )      | Habilita las pruebas de galería de símbolos.                                 |
| **Plantilla**                  | [**glStencilOp**](glstencilop.md)                      | Establece acciones de prueba de galería de símbolos.                             |
| **galería de símbolos**(... func, ... )  | [**glStencilFunc**](glstencilfunc.md)                  | Establece la función y el valor de referencia para las pruebas de galería de símbolos. |
| **swritemask**               | [**glStencilMask**](glstencilmask.md)                  | Especifica qué bits de galería de símbolos se pueden escribir.           |
|                              | [**glClearStencil**](glclearstencil.md)                | Especifica el valor sin formato para el búfer de galería de símbolos.      |
| **sclear**                   | [**glClear**](glclear.md) ( GL \_ STENCIL \_ BUFFER BIT \_ ) |                                                        |



 

Las funciones de comparación de galerías de símbolos y las operaciones de paso/error de galería de símbolos son casi equivalentes en OpenGL e IRIS GL. Las marcas de función de galería de símbolos IRIS GL van precedida de SF; las marcas OpenGL con GL. Las marcas de operación de paso/error de IRIS GL van precedida de ST; las marcas OpenGL con GL.

 

 




