---
title: Función glIndexMask (Gl.h)
description: La función glIndexMask controla la escritura de bits individuales en los búferes de índice de color.
ms.assetid: f4b5df36-390f-4254-95fb-98589750a11b
keywords:
- Función glIndexMask OpenGL
topic_type:
- apiref
api_name:
- glIndexMask
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e022bb3cbb5be5ac15049b5e8bc128d2ac7e100d5bcec6a87988dd2d14c5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012203"
---
# <a name="glindexmask-function"></a>Función glIndexMask

La **función glIndexMask** controla la escritura de bits individuales en los búferes de índice de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glIndexMask(
   GLuint mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Máscara de bits para habilitar y deshabilitar la escritura de bits individuales en los búferes de índice de color. Inicialmente, la máscara es la única.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glIndexMask** controla la escritura de bits individuales en los búferes de índice de color. Los n *bits de* máscara menos significativos, donde *1* es el número de bits de un búfer de índice de color, especifique una máscara.  Siempre que aparezca uno en la máscara, el bit correspondiente en el búfer de índice de color (o búferes) se puede escribir. Cuando aparece un cero, el bit está protegido por escritura.

Esta máscara solo se usa en modo de índice de color y solo afecta a los búferes seleccionados actualmente para escribir (vea [**glDrawBuffer**](gldrawbuffer.md)). Inicialmente, todos los bits están habilitados para escritura.

La función siguiente recupera información relacionada con **glIndexMask**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ INDEX \_ WRITEMASK

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

[**glDepthMask**](gldepthmask.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glStencilMask**](glstencilmask.md)
</dt> </dl>

 

 





