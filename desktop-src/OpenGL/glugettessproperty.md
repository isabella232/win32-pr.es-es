---
title: función gluGetTessProperty (GLU. h)
description: La función gluGetTessProperty obtiene una propiedad de objeto de teselación.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- gluGetTessProperty (función) OpenGL
topic_type:
- apiref
api_name:
- gluGetTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 482f32b227dbcf0c2a62405e344aa719bb4b9e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422213"
---
# <a name="glugettessproperty-function"></a>gluGetTessProperty función)

La función **gluGetTessProperty** obtiene una propiedad de objeto de teselación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluGetTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      *value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*cuales* 
</dt> <dd>

Propiedad cuyo valor se va a recuperar. Los valores siguientes son válidos: \_ Glu \_ Tess \_ , Glu \_ Tess \_ BOUNDARY \_ y Glu \_ Tess \_ Tolerance.

</dd> <dt>

*value* 
</dt> <dd>

Puntero a la ubicación donde se escribe el valor de la propiedad con nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluGetTessProperty** para recuperar las propiedades almacenadas en un objeto de teselación. Estas propiedades afectan a la manera en que se interpretan y representan los objetos de teselación. Para obtener información sobre qué son las propiedades y qué hacen, vea [**gluTessProperty**](glutessproperty.md).

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





