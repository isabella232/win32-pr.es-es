---
title: función glStencilOp (GL. h)
description: La función glStencilOp establece las acciones de prueba de la galería de símbolos.
ms.assetid: 16809735-5624-49cf-bfa5-9908d008b234
keywords:
- glStencilOp (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676873"
---
# <a name="glstencilop-function"></a>glStencilOp función)

La función **glStencilOp** establece las acciones de prueba de la galería de símbolos.

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

*puedan* 
</dt> <dd>

Acción que se realizará cuando se produzca un error en la prueba de estarcido. Se aceptan las seis constantes simbólicas siguientes.



| Value                                                                                                                                                | Significado                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="GL_KEEP"></span><span id="gl_keep"></span><dl> <dt>**mantenimiento de contabilidad \_**</dt> </dl>          | Mantiene el valor actual.<br/>                                                                         |
| <span id="GL_ZERO"></span><span id="gl_zero"></span><dl> <dt>**GL \_ cero**</dt> </dl>          | Establece el valor del búfer de la galería de símbolos en cero.<br/>                                                           |
| <span id="GL_REPLACE"></span><span id="gl_replace"></span><dl> <dt>**reemplazo de contabilidad \_**</dt> </dl> | Establece el valor del búfer de estarcido en *ref*, tal y como se especifica en **glStencilFunc**.<br/>                       |
| <span id="GL_INCR"></span><span id="gl_incr"></span><dl> <dt>**INCR del libro de contabilidad \_**</dt> </dl>          | Incrementa el valor del búfer de estarcido actual. Se fija en el valor sin signo máximo que se puede representar.<br/> |
| <span id="GL_DECR"></span><span id="gl_decr"></span><dl> <dt>**GL \_ decr (**</dt> </dl>          | Disminuye el valor del búfer de estarcido actual. Se fija en cero.<br/>                                     |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**inversión en contab \_**</dt> </dl>    | Bit a bit invierte el valor del búfer de estarcido actual.<br/>                                                |



 

</dd> <dt>

*zfail* 
</dt> <dd>

Acción de estarcido cuando se supera la prueba de estarcido, pero se produce un error en la prueba de profundidad. Acepta las mismas constantes simbólicas que *Fail.*

</dd> <dt>

*zpass* 
</dt> <dd>

Acción de estarcido cuando la prueba de estarcido y la prueba de profundidad superan o cuando se supera la prueba de estarcido y no hay ningún búfer de profundidad o la prueba de profundidad no está habilitada. Acepta las mismas constantes simbólicas que *FAIL*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *FAIL*, *zfail* o *ZPass* era cualquier valor distinto de los seis valores constantes definidos.<br/>                                      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La galería de símbolos, como el almacenamiento en búfer de *z*, habilita y deshabilita el dibujo en cada píxel. Dibuja en los planos de la galería de símbolos mediante primitivos de dibujo de OpenGL y, a continuación, representa geometría e imágenes mediante los planos de la galería de símbolos para enmascarar partes de la pantalla. La galería de símbolos se usa normalmente en algoritmos de representación de Multipass para lograr efectos especiales, como marcas, esquematización y representación de geometría sólida constructiva.

La prueba de estarcido elimina condicionalmente un píxel según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia. La prueba se habilita con llamadas a [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL de \_ estarcido \_ Test y se controla con [**glStencilFunc**](glstencilfunc.md).

La función **glStencilOp** toma tres argumentos que indican lo que sucede con el valor de estarcido almacenado mientras está habilitado el estarcido. Si se produce un error en la prueba de estarcido, no se realiza ningún cambio en los búferes de color o de profundidad del píxel y se *produce un error* y se especifica lo que sucede con el contenido del búfer de estarcido.

Los valores de búfer de estarcido se tratan como enteros sin signo. Cuando se incrementa y disminuye, los valores se fijan a 0 y 2 *n* 1, donde *n* es el valor devuelto por la consulta de los bits de la \_ Galería de símbolos GL \_ .

Los otros dos argumentos de **glStencilOp** especifican las acciones de búfer de estarcido deben realizarse correctamente las pruebas de búfer de profundidad (*ZPass*) o Fail (*zfail*). (Consulte [**glDepthFunc**](gldepthfunc.md)). Se especifican con las mismas seis constantes simbólicas que *producen un error*. Tenga en cuenta que *zfail* se omite cuando no hay ningún búfer de profundidad o cuando el búfer de profundidad no está habilitado. En estos casos, *FAIL* y *ZPass* especifican la acción de estarcido cuando se produce un error en la prueba de estarcido y se pasan, respectivamente.

Inicialmente, la prueba de galería de símbolos está deshabilitada. Si no hay ningún búfer de estarcido, no se puede realizar ninguna modificación en la galería de símbolos y es como si el estarcido probara siempre, independientemente de cualquier llamada a **glStencilOp**.

Las siguientes funciones recuperan información relacionada con **glStencilOp**:

error de [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL de la \_ Galería de símbolos \_

**glGet** con el argumento de la profundidad de la fase de estarcido de GL \_ \_ \_ \_

 error de profundidad de \_ paso de estarcido de glGet con el argumento \_ \_ \_

**glGet** con el argumento \_ bits de estarcido GL \_

[**glIsEnabled**](glisenabled.md) con el argumento, \_ prueba de estarcido GL \_

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

 

 





