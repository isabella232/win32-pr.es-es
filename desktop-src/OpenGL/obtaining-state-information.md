---
title: Obtención de información de estado
description: Obtención de información de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, información de estado
- OpenGL, variables de estado
- información de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfac92233e971104fd4d343970a9ecc79496ed54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775253"
---
# <a name="obtaining-state-information"></a>Obtención de información de estado

OpenGL mantiene muchas variables de estado que afectan al comportamiento de muchas funciones. Algunas de estas variables tienen funciones de consulta especializadas.



|                                          |                                                    |                                                          |
|------------------------------------------|----------------------------------------------------|----------------------------------------------------------|
| [**glGetClipPlane**](glgetclipplane.md) | [**glGetPixelMap**](glgetpixelmap.md)             | [**glGetTexImage**](glgetteximage.md)                   |
| [**glGetLight**](glgetlight.md)         | [**glGetPolygonStipple**](glgetpolygonstipple.md) | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |
| [**glGetMap**](glgetmap.md)             | [**glGetTexEnv**](glgettexenv.md)                 | [**glGetTexParameter**](glgettexparameter.md)           |
| [**glGetMaterial**](glgetmaterial.md)   | [**glGetTexGen**](glgettexgen.md)                 |                                                          |



 

Para obtener el valor de otras variables de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), según corresponda. Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obtener información sobre cómo usar estas funciones. Otras funciones de consulta que podría querer usar son [**glGetError**](glgeterror.md), [**glGetString**](glgetstring.md)y [**glIsEnabled**](glisenabled.md). (Consulte [control de errores](handling-errors.md) para obtener más información acerca de las funciones relacionadas con el control de errores). Para guardar y restaurar conjuntos de variables de estado, use [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).

-   [Usar las funciones de consulta](using-the-query-functions.md)
-   [Tratamiento de errores](error-handling.md)
-   [Códigos de error de OpenGL](opengl-error-codes.md)
-   [Guardar y restaurar conjuntos de variables de estado](saving-and-restoring-sets-of-state-variables.md)
-   [Variables de estado de OpenGL](opengl-state-variables.md)
-   [Referencia de información de estado](state-information-reference.md)

 

 




