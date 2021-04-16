---
title: función gluNurbsCallback (GLU. h)
description: La función gluNurbsCallback define una devolución de llamada para un objeto no uniforme B-spline racional (NURBS).
ms.assetid: 1e9afc00-57c6-459e-a9fc-463f45df2084
keywords:
- gluNurbsCallback (función) OpenGL
topic_type:
- apiref
api_name:
- gluNurbsCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a716724546ef0df4300bedb9aba44f7a23f530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676655"
---
# <a name="glunurbscallback-function"></a>gluNurbsCallback función)

La función **gluNurbsCallback** define una devolución de llamada para un objeto no uniforme B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)).

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNurbsCallback(
   GLUnurbs *nobj,
   GLenum   which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*nobj* 
</dt> <dd>

El objeto NURBS (creado con [**gluNewNurbsRenderer**](glunewnurbsrenderer.md)).

</dd> <dt>

*cuales* 
</dt> <dd>

Devolución de llamada que se está definiendo. El único valor válido es GLU \_ error. El significado del \_ error Glu significa que se llama a la función de error cuando se produce un error. Su único argumento es de tipo **GLenum** y indica el error específico que se ha producido. Hay 37 errores exclusivos de NURBS, denominados GLU \_ NURBS \_ ERROR1 a Glu \_ NURBS \_ ERROR37. Las cadenas de caracteres que describen estos errores pueden recuperarse con [**gluErrorString**](gluerrorstring.md).

</dd> <dt>

*fn* 
</dt> <dd>

Puntero a la función de devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluNurbsCallback** para definir una devolución de llamada que se va a usar en un objeto NURBS. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *FN* es **null**, se borrarán todas las devoluciones de llamada existentes.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewNurbsRenderer**](glunewnurbsrenderer.md)
</dt> </dl>

 

 





