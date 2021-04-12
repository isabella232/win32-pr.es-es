---
title: función gluQuadricCallback (GLU. h)
description: La función gluQuadricCallback define una devolución de llamada para un objeto quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- gluQuadricCallback (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534798"
---
# <a name="gluquadriccallback-function"></a>gluQuadricCallback función)

La función **gluQuadricCallback** define una devolución de llamada para un objeto quadric.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qobj* 
</dt> <dd>

El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*cuales* 
</dt> <dd>

Devolución de llamada que se está definiendo. El único valor válido es GLU \_ error.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**\_error Glu**</dt> </dl> | Se llama a la función **gluQuadricCallback** cuando se produce un error. Su único argumento es de tipo **GLenum** y indica el error específico que se ha producido. Las cadenas de caracteres que describen estos errores se pueden recuperar con la llamada a [**gluErrorString**](gluerrorstring.md) .<br/> |



 

</dd> <dt>

*fn* 
</dt> <dd>

Función a la que se va a llamar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluQuadricCallback** para definir una nueva devolución de llamada que se va a usar en un objeto quadric. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *FN* es **null**, se borra cualquier devolución de llamada existente.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





