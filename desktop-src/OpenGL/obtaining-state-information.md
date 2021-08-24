---
title: Obtener información de estado
description: Obtener información de estado
ms.assetid: 86fc8503-92b9-4b5b-8a28-4c9783983ac6
keywords:
- OpenGL, información de estado
- OpenGL, variables de estado
- información de estado OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d13719964412bf8b74b9d2f4ef58d5a153a56fc2f8d15a3d8788cef94762637
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144168"
---
# <a name="obtaining-state-information"></a>Obtener información de estado

OpenGL mantiene muchas variables de estado que afectan al comportamiento de muchas funciones. Algunas de estas variables tienen funciones de consulta especializadas.

:::row:::
    :::column:::
        [**glGetClipPlane**](glgetclipplane.md)
    :::column-end:::
    :::column:::
        [**glGetPixelMap**](glgetpixelmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexImage**](glgetteximage.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetLight**](glgetlight.md)
    :::column-end:::
    :::column:::
        [**glGetPolygonStipple**](glgetpolygonstipple.md)
    :::column-end:::
    :::column:::
        [**glGetTexLevelParameter**](glgettexlevelparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMap**](glgetmap.md)
    :::column-end:::
    :::column:::
        [**glGetTexEnv**](glgettexenv.md)
    :::column-end:::
    :::column:::
        [**glGetTexParameter**](glgettexparameter.md)
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        [**glGetMaterial**](glgetmaterial.md)
    :::column-end:::
    :::column:::
        [**glGetTexGen**](glgettexgen.md)
    :::column-end:::
    :::column:::

    :::column-end:::
:::row-end:::

Para obtener el valor de otras variables de estado, use [**glGetBooleanv**](glgetbooleanv.md), [**glGetDoublev**](glgetdoublev.md), [**glGetFloatv**](glgetfloatv.md)o [**glGetIntegerv**](glgetintegerv.md), según corresponda. Consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) para obtener información sobre cómo usar estas funciones. Otras funciones de consulta que puede usar son [**glGetError,**](glgeterror.md) [**glGetString**](glgetstring.md)y [**glIsEnabled.**](glisenabled.md) (Consulte [Control de errores](handling-errors.md) para obtener más información sobre las funciones relacionadas con el control de errores). Para guardar y restaurar conjuntos de variables de estado, use [**glPushAttrib**](glpushattrib.md) y [**glPopAttrib**](glpopattrib.md).

-   [Uso de las funciones de consulta](using-the-query-functions.md)
-   [Tratamiento de errores](error-handling.md)
-   [Códigos de error de OpenGL](opengl-error-codes.md)
-   [Guardar y restaurar conjuntos de variables de estado](saving-and-restoring-sets-of-state-variables.md)
-   [Variables de estado OpenGL](opengl-state-variables.md)
-   [Referencia de información de estado](state-information-reference.md)

 

 




