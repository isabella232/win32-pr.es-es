---
title: función gluDeleteNurbsRenderer (GLU. h)
description: La función gluDeleteNurbsRenderer destruye un objeto de curva B-spline racional (NURBS) no uniforme.
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- gluDeleteNurbsRenderer (función) OpenGL
topic_type:
- apiref
api_name:
- gluDeleteNurbsRenderer
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fb6ecf0bbb7076d4d6292676d3d358586d0986c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802215"
---
# <a name="gludeletenurbsrenderer-function"></a>gluDeleteNurbsRenderer función)

La función **gluDeleteNurbsRenderer** destruye un objeto de curva B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluDeleteNurbsRenderer(
   GLUnurbs *nobj
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

Objeto NURBS que se va a destruir (creado con **gluNewNurbsRenderer**).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluDeleteNurbsRenderer** destruye el objeto NURBS y libera cualquier memoria que haya usado. Después de llamar a **gluDeleteNurbsRenderer**, no puede volver a usar *nobj* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





