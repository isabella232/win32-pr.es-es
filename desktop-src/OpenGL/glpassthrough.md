---
title: función glPassThrough (GL. h)
description: La función glPassThrough coloca un marcador en el búfer de comentarios.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- glPassThrough (función) OpenGL
topic_type:
- apiref
api_name:
- glPassThrough
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1174dd933d46813a89c35b781d0408c3ac5476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802000"
---
# <a name="glpassthrough-function"></a>glPassThrough función)

La función **glPassThrough** coloca un marcador en el búfer de comentarios.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPassThrough(
   GLfloat token
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*token* 
</dt> <dd>

Un valor de marcador que se va a colocar en el búfer de comentarios. Se indica con el siguiente valor de identificación único.



| Value                                                                                                                                                                                   | Significado                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**\_token de paso \_ a través de GL \_**</dt> </dl> | Se mantiene el orden de los comandos **glPassThrough** con respecto a la especificación de primitivas de gráficos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el siguiente código de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Feedback es un modo de representación de OpenGL seleccionado llamando a [**glRenderMode**](glrendermode.md) con comentarios de contabilidad \_ . Cuando OpenGL está en modo de comentarios, no se genera ningún píxel mediante la rasterización. En su lugar, la información acerca de los primitivos que se habrían rasterizado se devolverá a la aplicación mediante OpenGL. Vea [**glFeedbackBuffer**](glfeedbackbuffer.md) para obtener una descripción del búfer de comentarios y los valores que hay en él.

La función **glPassThrough** inserta un marcador definido por el usuario en el búfer de comentarios cuando se ejecuta en modo de comentarios. El parámetro *token* se devuelve como si fuera un primitivo.

La función **glPassThrough** se omite si OpenGL no está en modo de comentarios.

La siguiente función recupera información relacionada con **glPassThrough**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de representación de contabilidad de argumentos \_

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

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





