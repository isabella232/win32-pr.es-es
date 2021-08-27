---
title: Función glStencilMask (Gl.h)
description: La función glStencilMask controla la escritura de bits individuales en los planos de galería de símbolos.
ms.assetid: c586f9db-bad5-4f06-a194-a8d979842d0c
keywords:
- Función glStencilMask OpenGL
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
ms.openlocfilehash: 9eb2e0af89bf2c66e7fa73cf6e4ace8bc8272e8ea581e17bab17754164d3f068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036525"
---
# <a name="glstencilmask-function"></a>Función glStencilMask

La **función glStencilMask** controla la escritura de bits individuales en los planos de galería de símbolos.

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

Máscara de bits para habilitar y deshabilitar la escritura de bits individuales en los planos de galería de símbolos. Inicialmente, la máscara es todas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glStencilMask** controla la escritura de bits individuales en los planos de galería de símbolos. Los n *bits de máscara* menos significativos, donde *n* es el número de bits del búfer de galería de símbolos, especifique una máscara.  Siempre que aparezca uno en la máscara, se puede escribir el bit correspondiente en el búfer de la galería de símbolos. Cuando aparece un cero, el bit está protegido por escritura. Inicialmente, todos los bits están habilitados para la escritura.

Las funciones siguientes recuperan información relacionada con **glStencilMask**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ STENCIL \_ WRITEMASK

glGet con el argumento GL \_ STENCIL \_ BITS

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
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

 

 





