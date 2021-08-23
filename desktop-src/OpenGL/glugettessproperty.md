---
title: Función gluGetTessProperty (Glu.h)
description: La función gluGetTessProperty obtiene una propiedad de objeto de teselación.
ms.assetid: 6aa565d8-2257-4259-a959-b7d806a7ed96
keywords:
- Función GluGetTessProperty OpenGL
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
ms.openlocfilehash: d12e7ca8099197b663893b1edcf04dd8fa98348fe4f6d3d324b54f33904e026a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554245"
---
# <a name="glugettessproperty-function"></a>Función gluGetTessProperty

La **función gluGetTessProperty** obtiene una propiedad de objeto de teselación.

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

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess**](glunewtess.md)).

</dd> <dt>

*Que* 
</dt> <dd>

Propiedad cuyo valor se va a recuperar. Los valores siguientes son válidos: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY y GLU \_ \_ TESS \_ TOLERANCE.

</dd> <dt>

*value* 
</dt> <dd>

Puntero a la ubicación donde se escribe el valor de la propiedad con nombre.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use **gluGetTessProperty para** recuperar las propiedades almacenadas en un objeto de teselación. Estas propiedades afectan a la forma en que se interpretan y representan los objetos de teselación. Para obtener información sobre qué son las propiedades y qué hacen, [**vea gluTessProperty**](glutessproperty.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessProperty**](glutessproperty.md)
</dt> </dl>

 

 





