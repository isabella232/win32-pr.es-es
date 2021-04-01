---
title: función glStencilMask (GL. h)
description: La función glStencilMask controla la escritura de bits individuales en los planos de la galería de símbolos.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- glStencilMask (función) OpenGL
topic_type:
- apiref
api_name:
- glStencilMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63790fa30e88abbde6e1ba47e624c6caf2dcfc4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151192"
---
# <a name="glstencilmask-function"></a>glStencilMask función)

La función **glStencilMask** controla la escritura de bits individuales en los planos de la galería de símbolos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glStencilMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Máscara de bits para habilitar y deshabilitar la escritura de bits individuales en los planos de la galería de símbolos. Inicialmente, la máscara es todas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glStencilMask** controla la escritura de bits individuales en los planos de la galería de símbolos. Los *n* bits menos significativos de la *máscara*, donde *n* es el número de bits en el búfer de estarcido, especifique una máscara. Siempre que aparezca una en la máscara, el bit correspondiente en el búfer de estarcido se convierte en grabable. Cuando aparece un cero, el bit está protegido contra escritura. Inicialmente, todos los bits están habilitados para escritura.

Las siguientes funciones recuperan información relacionada con **glStencilMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ Galería de símbolos \_ WRITEMASK

glGet con el argumento \_ bits de estarcido GL \_

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glColorMask**](glcolormask.md)
</dt> <dt>

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndexMask**](glindexmask.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





