---
title: Función gluQuadricCallback (Glu.h)
description: La función gluQuadricCallback define una devolución de llamada para un objeto cuádigo.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- Función GluQuadricCallback OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244910"
---
# <a name="gluquadriccallback-function"></a>función gluQuadricCallback

La **función gluQuadricCallback** define una devolución de llamada para un objeto cuádigo.

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

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Que* 
</dt> <dd>

Devolución de llamada que se está definindo. El único valor válido es GLU \_ ERROR.



| Value                                                                                                                                             | Significado                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <dt>**ERROR DE GLU \_**</dt> </dl> | Se llama a la función **gluQuadricCallback** cuando se encuentra un error. Su único argumento es de tipo **GLenum** e indica el error específico que se produjo. Las cadenas de caracteres que describen estos errores se pueden recuperar con la [**llamada a gluErrorString.**](gluerrorstring.md)<br/> |



 

</dd> <dt>

*fn* 
</dt> <dd>

Función a la que se va a llamar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use **gluQuadricCallback para** definir una nueva devolución de llamada que usará un objeto cuádigo. Si la devolución de llamada especificada ya está definida, se reemplaza. Si *fn* es **NULL,** se borra cualquier devolución de llamada existente.

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

[**gluErrorString**](gluerrorstring.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





