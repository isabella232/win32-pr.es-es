---
title: función glRenderMode (GL. h)
description: La función glRenderMode establece el modo de rasterización.
ms.assetid: bcbc3bba-c552-425b-8284-6cadff0c9f56
keywords:
- glRenderMode (función) OpenGL
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
ms.openlocfilehash: af07d2492d70f9c0a3a764d767b52b2f71204939
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151125"
---
# <a name="glrendermode-function"></a>glRenderMode función)

La función **glRenderMode** establece el modo de rasterización.

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

Modo de rasterización. Se aceptan los siguientes tres valores. El valor predeterminado es GL \_ Render.



| Value                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_RENDER"></span><span id="gl_render"></span><dl> <dt>**representación en GL \_**</dt> </dl>       | Modo de representación. Las primitivas se rasterizan, lo que produce fragmentos de píxeles, que se escriben en el fotogramas. Este es el modo normal y también el modo predeterminado.<br/>                                                                                                                                                                                                      |
| <span id="GL_SELECT"></span><span id="gl_select"></span><dl> <dt>**selección de contabilidad \_**</dt> </dl>       | Modo de selección. No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido de fotogramas. En su lugar, se devuelve un registro de los nombres de primitivas que se habrían dibujado si el modo de representación se \_ representase en GL en un búfer de selección, que se debe crear (vea [**glSelectBuffer**](glselectbuffer.md)) antes de que se escriba el modo de selección.<br/>               |
| <span id="GL_FEEDBACK"></span><span id="gl_feedback"></span><dl> <dt>**Comentarios de contabilidad \_**</dt> </dl> | Modo de comentarios. No se generan fragmentos de píxeles y no se realiza ningún cambio en el contenido de fotogramas. En su lugar, las coordenadas y los atributos de los vértices que se habrían dibujado tenían el modo de representación \_ en GL se devuelve en un búfer de comentarios, que se debe crear (vea [**glFeedbackBuffer**](glfeedbackbuffer.md)) antes de que se escriba el modo de comentarios.<br/> |



 

</dd> </dl>

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* no era uno de los tres valores aceptados.<br/>                                                                                     |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función con el argumento GL \_ Select antes de que se llamara a [**glSelectBuffer**](glselectbuffer.md) al menos una vez.<br/>       |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función con los comentarios de GL del argumento \_ antes de que se llamara a [**glBeedbackBuffer**](glfeedbackbuffer.md) al menos una vez.<br/> |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/>       |



## <a name="remarks"></a>Observaciones

La función **glRenderMode** toma un argumento, *mode*, que puede suponer uno de los tres valores predefinidos anteriores.

El valor devuelto de la función **glRenderMode** viene determinado por el modo de representación en el momento en que se llama a **glRenderMode** , en lugar de por el *modo*. Los valores devueltos para los tres modos de representación son los siguientes.



| Value        | Significado                                                                 |
|--------------|-------------------------------------------------------------------------|
| representación en GL \_   | Cero.                                                                   |
| selección de contabilidad \_   | El número de registros de aciertos transferidos al búfer seleccionado.             |
| Comentarios de contabilidad \_ | El número de valores (no los vértices) transferidos al búfer de comentarios. |



 

Consulte [**glSelectBuffer**](glselectbuffer.md) y [**glFeedbackBuffer**](glfeedbackbuffer.md) para obtener más detalles sobre la operación de selección y comentarios.

Si se genera un error, **glRenderMode** devuelve cero independientemente del modo de presentación actual.

La siguiente función recupera información relacionada con **glRenderMode**:

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

 

 





