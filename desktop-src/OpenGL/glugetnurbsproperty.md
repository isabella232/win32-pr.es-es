---
title: Función gluGetNurbsProperty (Glu.h)
description: La función gluGetNurbsProperty obtiene una propiedad NON-Uniform Rational B-Spline (SPLINEBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- Función GluGetNurbsProperty OpenGL
topic_type:
- apiref
api_name:
- gluGetNurbsProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583da688e3495ebc2eb9d6f71972658c6426469c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071473"
---
# <a name="glugetnurbsproperty-function"></a>Función gluGetNurbsProperty

La **función gluGetNurbsProperty** obtiene una propiedad Non-Uniform Rational B-Spline [(SPLINEBS).](using-nurbs-curves-and-surfaces.md)

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluGetNurbsProperty(
   GLUnurbs *nobj,
   GLenum   property,
   GLfloat  *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto RGBBS (creado [**con gluNewNurbsRenderer).**](glunewnurbsrenderer.md)

</dd> <dt>

*property* 
</dt> <dd>

Propiedad cuyo valor se va a recuperar. Los valores siguientes son válidos: GLU \_ SAMPLING \_ TOLERANCE, GLU \_ DISPLAY \_ MODE, GLU \_ CULLING, GLU \_ AUTO LOAD \_ \_ MATRIX, GLU \_ PARAMETRIC \_ TOLERANCE, GLU SAMPLING METHOD, GLU U \_ STEP \_ \_ \_ \_ \_ y GLU V STEP.

</dd> <dt>

*value* 
</dt> <dd>

Puntero a la ubicación en la que se escribe el valor de la propiedad con nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluGetNurbsProperty para** recuperar las propiedades almacenadas en un objeto RECORDSETBS. Estas propiedades afectan a la forma en que se representan las curvas y superficies DE LABS. Para obtener información sobre las propiedades de LABS, [**vea gluNurbsProperty**](glunurbsproperty.md).

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
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





