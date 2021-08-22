---
title: Función gluNewNurbsRenderer (Glu.h)
description: La función gluNewNurbsRenderer crea un objeto B-Spline racionalizado no uniforme (RGBBS).
ms.assetid: f47badb0-6b75-4bfd-9771-516668d9e255
keywords:
- función GluNewNurbsRenderer OpenGL
topic_type:
- apiref
api_name:
- gluNewNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 089c1a88ac0fe9ac246efd435ae941ba5e66e2412595e4f5f96dc73e85e90478
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937800"
---
# <a name="glunewnurbsrenderer-function"></a>Función gluNewNurbsRenderer

La **función gluNewNurbsRenderer** crea un objeto B-Spline racionalizado no uniforme [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
GLUnurbs* WINAPI gluNewNurbsRenderer(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="remarks"></a>Comentarios

La **función gluNewNurbsRenderer** crea y devuelve un puntero a un nuevo objeto RGBBS. Haga referencia a este objeto al llamar a las funciones de representación y control DEBS. Un valor devuelto de cero significa que no hay suficiente memoria para asignar al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluBeginCurve**](glubegincurve.md)
</dt> <dt>

[**gluBeginSurface**](glubeginsurface.md)
</dt> <dt>

[**gluBeginTrim**](glubegintrim.md)
</dt> <dt>

[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md)
</dt> <dt>

[*gluNurbsCallback*](glunurbs.md)
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





