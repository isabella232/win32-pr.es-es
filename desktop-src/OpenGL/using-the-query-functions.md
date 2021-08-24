---
title: Uso de las funciones de consulta
description: Uso de las funciones de consulta
ms.assetid: 5f874a0e-77c0-4009-a18f-a852d7ffe891
keywords:
- OpenGL, funciones de consulta
- funciones de consulta OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e3e883bdf8730dac7b1a8e07448b771109bef0ac5ec2246411703e8f841a53
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776485"
---
# <a name="using-the-query-functions"></a>Uso de las funciones de consulta

Hay cuatro funciones de consulta para obtener variables de estado simples y una para determinar si un estado determinado está habilitado o deshabilitado:

-   [**glGetBooleanv**](glgetbooleanv.md)
-   [**glGetIntegerv**](glgetintegerv.md)
-   [**glGetFloatv**](glgetfloatv.md)
-   [**glGetDoublev**](glgetdoublev.md)
-   [**glIsEnabled**](glisenabled.md)

Los prototipos de las funciones de consulta son:

**void** **glGetBooleanv**(**GLenum** *pname* , **GLboolean \** _ _params* );

**void** **glGetIntegerv**(**GLenum** *pname* , **GLint \** _ _params* );

**void** **glGetFloatv**(**GLenum** *pname* , **GLfloat \** _ _params* );

**void** **glGetDoublev**(**GLenum** *pname* , **GLdouble \** _ _params* );

Respectivamente, las funciones de consulta obtienen variables de estado booleanos, enteros, de punto flotante o de precisión doble. El *parámetro pname* es una constante simbólica que indica la variable de estado que se va a devolver y *params* es un puntero a una matriz del tipo indicado en la que se colocarán los datos devueltos. Los valores posibles para *pname se* enumeran en [Variables de estado openGL](opengl-state-variables.md). Se realiza una conversión de tipos si es necesario para devolver la variable deseada como el tipo de datos solicitado.

El prototipo de [**glIsEnabled**](glisenabled.md) es:

**GLboolean** **glIsEnabled**(GLenum *cap* );

Si el modo especificado por *cap está* habilitado, **glIsEnabled** devuelve GL \_ TRUE. Si el modo especificado por *cap está* deshabilitado, **glIsEnabled** devuelve GL \_ FALSE. Los valores posibles para *cap* se enumeran en [Variables de estado OpenGL](opengl-state-variables.md).

Otras funciones especializadas devuelven variables de estado específicas. Para averiguar cuándo usar estas funciones, vea Variables de estado de OpenGL y el *Manual de referencia de OpenGL.* Para obtener más información sobre la instalación de control de errores de OpenGL y la función **glGetError,** vea [Control de errores.](error-handling.md)

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

 

 




