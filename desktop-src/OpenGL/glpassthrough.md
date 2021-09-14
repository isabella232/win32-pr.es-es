---
title: Función glPassThrough (Gl.h)
description: La función glPassThrough coloca un marcador en el búfer de comentarios.
ms.assetid: 14664ac6-eb25-46ae-86d8-7ece31df103f
keywords:
- Función glPassThrough OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375106"
---
# <a name="glpassthrough-function"></a>Función glPassThrough

La **función glPassThrough** coloca un marcador en el búfer de comentarios.

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

Valor de marcador que se va a colocar en el búfer de comentarios. Se indica con el siguiente valor de identificación único.



| Value                                                                                                                                                                                   | Significado                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_PASS_THROUGH_TOKEN"></span><span id="gl_pass_through_token"></span><dl> <dt>**TOKEN \_ DE PASO A TRAVÉS DE \_ \_ GL**</dt> </dl> | Se mantiene el **orden de los comandos glPassThrough** con respecto a la especificación de primitivas gráficas.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar el código de error siguiente.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Feedback es un modo de representación OpenGL seleccionado mediante una [**llamada a glRenderMode**](glrendermode.md) con GL \_ FEEDBACK. Cuando OpenGL está en modo de comentarios, la rasterización no genera píxeles. En su lugar, OpenGL vuelve a proporcionar información sobre las primitivas que se hubieran rasterizado a la aplicación. Consulte [**glFeedbackBuffer para**](glfeedbackbuffer.md) obtener una descripción del búfer de comentarios y los valores que incluye.

La **función glPassThrough** inserta un marcador definido por el usuario en el búfer de comentarios cuando se ejecuta en modo de comentarios. El *parámetro* de token se devuelve como si fuera una primitiva.

La **función glPassThrough** se omite si OpenGL no está en modo de comentarios.

La función siguiente recupera información relacionada con **glPassThrough**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ RENDER \_ MODE

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

[**glEnd**](glend.md)
</dt> <dt>

[**glFeedbackBuffer**](glfeedbackbuffer.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> </dl>

 

 





