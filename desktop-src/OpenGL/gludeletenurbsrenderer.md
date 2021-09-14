---
title: Función gluDeleteNurbsRenderer (Glu.h)
description: La función gluDeleteNurbsRenderer destruye un objeto B-Spline racionalizado no uniforme (RGBBS).
ms.assetid: 77063dcb-90b8-47e4-8b00-e1c46cf4f712
keywords:
- Función GluDeleteNurbsRenderer OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071490"
---
# <a name="gludeletenurbsrenderer-function"></a>Función gluDeleteNurbsRenderer

La **función gluDeleteNurbsRenderer** destruye un objeto B-Spline racionalizado no uniforme [(RGBBS).](using-nurbs-curves-and-surfaces.md)

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

Objeto RGBBS que se va a destruir (creado **con gluNewNurbsRenderer).**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluDeleteNurbsRenderer** destruye el objeto RGBBS y libera la memoria que usó. Después de llamar a **gluDeleteNurbsRenderer,** no puede volver a *usar nobj.*

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

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





