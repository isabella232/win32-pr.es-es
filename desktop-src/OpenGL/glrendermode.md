---
title: Función glRenderMode (Gl.h)
description: La función glRenderMode establece el modo de rasterización.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- Función glRenderMode OpenGL
topic_type:
- apiref
api_name:
- glRenderMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93eb3c7e2d7f4a6d261632e0f010cf0e1c7a2410a5a8364a6cf1fd65f36ada99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777935"
---
# <a name="glrendermode-function"></a>Función glRenderMode

La **función glRenderMode** establece el modo de rasterización.

## <a name="syntax"></a>Sintaxis


```C++
GLint WINAPI glRenderMode(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Modo de rasterización. Se aceptan los tres valores siguientes. El valor predeterminado es GL \_ RENDER.



| Value                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**GL \_ RENDER**</dt> </dl>       | Modo de representación. Las primitivas se rasterizan y producen fragmentos de píxeles, que se escriben en el búfer de fotogramas. Este es el modo normal y también el modo predeterminado.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**GL \_ SELECT**</dt> </dl>       | Modo de selección. No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido del búfer de fotogramas. En su lugar, se devuelve un registro de los nombres de primitivos que se hubieran dibujado si el modo de representación fuera GL RENDER en un búfer de selección, que se debe crear \_ (vea [**glSelectBuffer)**](glselectbuffer.md)antes de que se entre en modo de selección.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**COMENTARIOS \_ DE GL**</dt> </dl> | Modo de comentarios. No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido del búfer de fotogramas. En su lugar, las coordenadas y los atributos de los vértices que se hubieran dibujado si el modo de representación fuera GL RENDER se devuelven en un búfer de comentarios, que se debe crear \_ (consulte [**glFeedbackBuffer)**](glfeedbackbuffer.md)antes de que se entre en modo de comentarios.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *el modo* no era uno de los tres valores aceptados.<br/>                                                                                     |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función con el argumento GL SELECT antes de llamar a \_ [**glSelectBuffer**](glselectbuffer.md) al menos una vez.<br/>       |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función con el argumento GL \_ FEEDBACK antes de llamar a [**glBeedbackBuffer**](glfeedbackbuffer.md) al menos una vez.<br/> |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Comentarios

La **función glRenderMode** toma un argumento, *mode*, que puede suponer uno de los tres valores predefinidos anteriores.

El valor devuelto de la **función glRenderMode** viene determinado por el modo de representación en el momento en que se llama **a glRenderMode,** en lugar del *modo*. Los valores devueltos para los tres modos de representación son los siguientes.



| Value        | Significado                                                                 |
|--------------|-------------------------------------------------------------------------|
| GL \_ RENDER   | Cero.                                                                   |
| GL \_ SELECT   | Número de registros de llamadas transferidos al búfer seleccionado.             |
| COMENTARIOS \_ DE GL | Número de valores (no vértices) transferidos al búfer de comentarios. |



 

Consulte [**glSelectBuffer**](glselectbuffer.md) y [**glFeedbackBuffer**](glfeedbackbuffer.md) para obtener más detalles sobre la selección y la operación de comentarios.

Si se genera un error, **glRenderMode** devuelve cero independientemente del modo de representación actual.

La función siguiente recupera información relacionada con **glRenderMode**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ RENDER \_ MODE

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**glInitNames**](glinitnames.md)
</dt> <dt>

[**glLoadName**](glloadname.md)
</dt> <dt>

[**glPassThrough**](glpassthrough.md)
</dt> <dt>

[**glPushName**](glpushname.md)
</dt> <dt>

[**glSelectBuffer**](glselectbuffer.md)
</dt> </dl>

 

 





