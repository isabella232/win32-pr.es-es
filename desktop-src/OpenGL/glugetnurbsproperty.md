---
title: función gluGetNurbsProperty (GLU. h)
description: La función gluGetNurbsProperty obtiene una propiedad no uniforme B-spline racional (NURBS).
ms.assetid: 7dbc75a0-d04e-4794-b3dd-a602addf9dfa
keywords:
- gluGetNurbsProperty (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150166"
---
# <a name="glugetnurbsproperty-function"></a>gluGetNurbsProperty función)

La función **gluGetNurbsProperty** obtiene una propiedad no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).

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

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*property* 
</dt> <dd>

Propiedad cuyo valor se va a recuperar. Los valores siguientes son válidos: GLU, la tolerancia de muestreo, el \_ modo de presentación de Glu, la selección de Glu, la \_ matriz de \_ \_ \_ \_ \_ carga automática de Glu, la \_ \_ tolerancia paramétrica de Glu, el \_ \_ \_ método de muestreo Glu, el paso de Glu \_ U \_ y Glu \_ V \_ .

</dd> <dt>

*value* 
</dt> <dd>

Puntero a la ubicación en la que se escribe el valor de la propiedad con nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluGetNurbsProperty** para recuperar las propiedades almacenadas en un objeto NURBS. Estas propiedades afectan a la manera en que se representan las curvas y curvas de NURBS. Para obtener información acerca de las propiedades de NURBS, vea [**gluNurbsProperty**](glunurbsproperty.md).

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
</dt> <dt>

[**gluNurbsProperty**](glunurbsproperty.md)
</dt> </dl>

 

 





