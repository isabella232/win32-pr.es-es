---
title: Usar las funciones de consulta
description: Usar las funciones de consulta
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funciones de consulta
- funciones de consulta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14804b260451d4b51b0146b1cb2f796ba6b6778e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665666"
---
# <a name="using-the-query-functions"></a>Usar las funciones de consulta

Hay cuatro funciones de consulta para obtener variables de estado simples y otra para determinar si un estado determinado está habilitado o deshabilitado:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

Los prototipos de las funciones de consulta son:

**void** **glGetBooleanv**(**GLenum** *PName* , **GLboolean \*** *params* );

**void** **glGetIntegerv**(**GLenum** *PName* , **GLint \*** *params* );

**void** **glGetFloatv**(**GLenum** *PName* , **GLfloat \*** *params* );

**void** **glGetDoublev**(**GLenum** *PName* , **GLdouble \*** *params* );

Respectivamente, las funciones de consulta obtienen variables de estado Boolean, integer, de punto flotante o de doble precisión. El parámetro *PName* es una constante simbólica que indica la variable de estado que se va a devolver y *params* es un puntero a una matriz del tipo indicado en el que se colocan los datos devueltos. Los valores posibles de *PName* se enumeran en [variables de estado de OpenGL](opengl-state-variables.md). Si es necesario, se realiza una conversión de tipos para devolver la variable deseada como el tipo de datos solicitado.

El prototipo para [**glIsEnabled**](glisenabled.md) es:

**GLboolean** **glIsEnabled**(GLenum *Cap* );

Si el modo especificado por *Cap* está habilitado, **glIsEnabled** devuelve GL \_ true. Si el modo especificado por *Cap* está deshabilitado, **glIsEnabled** devuelve GL \_ false. Los valores posibles para *Cap* se enumeran en [variables de estado de OpenGL](opengl-state-variables.md).

Otras funciones especializadas devuelven variables de estado específicas. Para averiguar cuándo usar estas funciones, consulte las variables de estado de OpenGL y el *manual de referencia de OpenGL*. Para obtener más información sobre la funcionalidad de control de errores de OpenGL y la función **glGetError** , vea [control de errores](error-handling.md).

Las funciones que devuelven variables de estado específicas son:

-   [**glGetClipPlane**](glgetclipplane.md)
-   [**glGetError**](glgeterror.md)
-   [**glGetLight**](glgetlight.md)
-   [**glGetMap**](glgetmap.md)
-   [**glGetMaterial**](glgetmaterial.md)
-   [**glGetPixelMap**](glgetpixelmap.md)
-   [**glGetPolygonStipple**](glgetpolygonstipple.md)
-   [**glGetString**](glgetstring.md)
-   [**glGetTexEnv**](glgettexenv.md)
-   [**glGetTexGen**](glgettexgen.md)
-   [**glGetTexImage**](glgetteximage.md)
-   [**glGetTexLevelParameter**](glgettexlevelparameter.md)
-   [**glGetTexParameter**](glgettexparameter.md)

 

 




