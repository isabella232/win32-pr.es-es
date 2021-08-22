---
title: Función glStencilFunc (Gl.h)
description: La función glStencilFunc establece la función y el valor de referencia para las pruebas de galería de símbolos.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- Función glStencilFunc OpenGL
topic_type:
- apiref
api_name:
- glStencilFunc
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e529bd83cff8ffb25c8853b7d896926e63982370387f7e2fb5d2ca30a394c1cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491515"
---
# <a name="glstencilfunc-function"></a>Función glStencilFunc

La **función glStencilFunc** establece la función y el valor de referencia para las pruebas de galería de símbolos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glStencilFunc(
   GLenum func,
   GLint  ref,
   GLuint mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*func* 
</dt> <dd>

Función de prueba. Los ocho tokens siguientes son válidos.



| Valor                                                                                                                                                   | Significado                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ NEVER**</dt> </dl>          | Siempre se produce un error.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**GL \_ LESS**</dt> </dl>             | Pasa si (*ref*  &  *mask*) < (*máscara de galería de*  &  *símbolos*).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si (*ref*  &  *mask*) = (*máscara de galería de*  &  *símbolos*).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**GL \_ GREATER**</dt> </dl>    | Pasa si (*ref*  &  *mask*) > (*máscara de galería de*  &  *símbolos*).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Pasa si (*ref*  &  *mask*) = (*máscara de galería de*  &  *símbolos*).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**GL \_ EQUAL**</dt> </dl>          | Pasa si (*ref*  &  *mask*) = (*máscara de galería de*  &  *símbolos*).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**GL \_ NOTEQUAL**</dt> </dl> | Pasa si (*ref*  &  *mask*) ? (*galería de símbolos*  &  *mask*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ ALWAYS**</dt> </dl>       | Siempre pasa.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

Valor de referencia de la prueba de galería de símbolos. El *parámetro ref* se fija en el intervalo \[ 0, 2 *n* 1 , donde n es el número de planos de bits en el \] búfer de la galería de símbolos. 

</dd> <dt>

*mask* 
</dt> <dd>

Máscara que es **AND** ed con el valor de referencia y el valor de galería de símbolos almacenado cuando se realiza la prueba.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *func* no era uno de los ocho valores aceptados.<br/>                                                                           |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La galería de símbolos, como *z*-buffering, habilita y deshabilita el dibujo por píxel. Dibuje en los planos de galería de símbolos mediante primitivas de dibujo openGL y, a continuación, represente la geometría y las imágenes, mediante los planos de galería de símbolos para enmascarar partes de la pantalla. La galería de símbolos se usa normalmente en algoritmos de representación multipass para lograr efectos especiales, como las decales, la delineación y la representación de geometría sólida y recímétrica.

La prueba de galería de símbolos elimina condicionalmente un píxel en función del resultado de una comparación entre el valor de referencia y el valor del búfer de la galería de símbolos. La prueba se habilita mediante [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL \_ STENCIL \_ TEST. Las acciones realizadas en función del resultado de la prueba de galería de símbolos se especifican [**con glStencilOp**](glstencilop.md).

El *parámetro func* es una constante simbólica que determina la función de comparación de galería de símbolos. Acepta uno de los ocho valores mostrados anteriormente. El *parámetro ref* es un valor de referencia entero que se usa en la comparación de galería de símbolos. Se fija en el intervalo \[ 0, 2 *n* 1 , donde n es el número de planos de bits en el \] búfer de la galería de símbolos.  El *parámetro mask* es **and** bit a bit con el valor de referencia y el valor de galería de símbolos almacenado, con los valores de **and** participando en la comparación.

Si *la galería de* símbolos representa el valor almacenado en la ubicación de búfer de la galería de símbolos correspondiente, la lista anterior muestra el efecto de cada función de comparación que se puede especificar mediante *func*. Solo si la comparación se realiza correctamente es el píxel pasado a la siguiente fase del proceso de rasterización [**(vea glStencilOp**](glstencilop.md)). Todas las  pruebas tratan los valores de galería de símbolos como enteros sin signo en el intervalo \[ 0, 2 *n* 1 , donde n es el número de planos de bits en el búfer de la \] galería de símbolos. 

Inicialmente, la prueba de galería de símbolos está deshabilitada. Si no hay ningún búfer de galería de símbolos, no se puede producir ninguna modificación de la galería de símbolos y es como si siempre se supera la prueba de galería de símbolos.

Las siguientes funciones recuperan información relacionada **con glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento GL \_ STENCIL \_ FUNC

**glGet** con el argumento GL \_ STENCIL \_ VALUE \_ MASK

**glGet** con el argumento GL \_ STENCIL \_ REF

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





