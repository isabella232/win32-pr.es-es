---
title: Función glStencilOp (Gl.h)
description: La función glStencilOp establece las acciones de prueba de la galería de símbolos.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- Función glStencilOp OpenGL
topic_type:
- apiref
api_name:
- glStencilOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b23162f8606ed68dc90a0cb6debdcc903e0ccd0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260095"
---
# <a name="glstencilop-function"></a>Función glStencilOp

La **función glStencilOp** establece las acciones de prueba de la galería de símbolos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glStencilOp(
   GLenum fail,
   GLenum zfail,
   GLenum zpass
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Fallar* 
</dt> <dd>

Acción que se debe realizar cuando se produce un error en la prueba de galería de símbolos. Se aceptan las seis constantes simbólicas siguientes.



| Value                                                                                                                                                | Significado                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**GL \_ KEEP**</dt> </dl>          | Mantiene el valor actual.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ ZERO**</dt> </dl>          | Establece el valor del búfer de galería de símbolos en cero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**GL \_ REPLACE**</dt> </dl> | Establece el valor del búfer de la galería de símbolos *en ref*, tal y como especifica **glStencilFunc.**<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**GL \_ INCR**</dt> </dl>          | Incrementa el valor del búfer de galería de símbolos actual. Fija al valor máximo que se puede representar sin signo.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ DECR**</dt> </dl>          | Disminuye el valor del búfer de galería de símbolos actual. Fija a cero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>    | Invierte bit a bit el valor del búfer de galería de símbolos actual.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Acción de galería de símbolos cuando se supera la prueba de galería de símbolos, pero se produce un error en la prueba de profundidad. Acepta las mismas constantes simbólicas que *error.*

</dd> <dt>

*Zpass* 
</dt> <dd>

Acción de galería de símbolos cuando se supera la prueba de galería de símbolos y la prueba de profundidad, o cuando se supera la prueba de galería de símbolos y no hay ningún búfer de profundidad o no está habilitada la prueba de profundidad. Acepta las mismas constantes simbólicas que el *error*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *fail*, *zfail* o *zpass* era cualquier valor distinto de los seis valores constantes definidos.<br/>                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La galería de símbolos, como *z*-buffering, habilita y deshabilita el dibujo por píxel. Dibuje en los planos de galería de símbolos mediante primitivas de dibujo openGL y, a continuación, represente la geometría y las imágenes, mediante los planos de galería de símbolos para enmascarar partes de la pantalla. La galería de símbolos se usa normalmente en algoritmos de representación multipass para lograr efectos especiales, como las decales, la delineación y la representación de geometría sólida recímétrica.

La prueba de galería de símbolos elimina condicionalmente un píxel en función del resultado de una comparación entre el valor del búfer de la galería de símbolos y un valor de referencia. La prueba se habilita con [**llamadas glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ STENCIL TEST y se controla con \_ [**glStencilFunc.**](glstencilfunc.md)

La **función glStencilOp** toma tres argumentos que indican lo que sucede con el valor de galería de símbolos almacenado mientras está habilitada la galería de símbolos. Si se produce un error en la prueba de galería de símbolos,  no se realiza ningún cambio en los búferes de color o profundidad del píxel, y fail especifica lo que ocurre con el contenido del búfer de galería de símbolos.

Los valores de búfer de galería de símbolos se tratan como enteros sin signo. Cuando se incrementan y disminuyen, los valores se fijan en 0 y 2 *n* 1, donde *n* es el valor devuelto consultando GL \_ STENCIL \_ BITS.

Los otros dos argumentos para **glStencilOp** especifican acciones de búfer de galería de símbolos si las pruebas de búfer de profundidad posteriores se realizan correctamente *(zpass*) o no (*zfail*). (Vea [**glDepthFunc).**](gldepthfunc.md) Se especifican mediante las mismas seis constantes simbólicas que no *se pueden usar.* Tenga en *cuenta que zfail* se omite cuando no hay ningún búfer de profundidad o cuando el búfer de profundidad no está habilitado. En estos casos, *fail y* *zpass* especifican la acción de galería de símbolos cuando se produce un error en la prueba de galería de símbolos y se supera, respectivamente.

Inicialmente, la prueba de galería de símbolos está deshabilitada. Si no hay ningún búfer de galería de símbolos, no se puede producir ninguna modificación de la galería de símbolos y es como si las pruebas de galería de símbolos siempre pasara, independientemente de cualquier llamada a **glStencilOp**.

Las siguientes funciones recuperan información relacionada **con glStencilOp**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ STENCIL \_ FAIL

**glGet con** el argumento GL \_ STENCIL \_ PASS DEPTH \_ \_ PASS

**glGet con** el argumento GL \_ STENCIL \_ PASS DEPTH \_ \_ FAIL

**glGet** con el argumento GL \_ STENCIL \_ BITS

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ STENCIL \_ TEST

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Biblioteca<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**glAlphaFunc**](glalphafunc.md)
</dt> <dt>

[**glBegin**](glbegin.md)
</dt> <dt>

[**glBlendFunc**](glblendfunc.md)
</dt> <dt>

[**glDepthFunc**](gldepthfunc.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glLogicOp**](gllogicop.md)
</dt> <dt>

[**glStencilFunc**](glstencilfunc.md)
</dt> </dl>

 

 





