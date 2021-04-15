---
title: función glStencilFunc (GL. h)
description: La función glStencilFunc establece la función y el valor de referencia para las pruebas de estarcido.
ms.assetid: 6c84415b-4d22-494b-90f2-6243d1406725
keywords:
- glStencilFunc (función) OpenGL
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
ms.openlocfilehash: cd4f9c0a5ec905ecb061ddb54984bf35ff8edc3d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677005"
---
# <a name="glstencilfunc-function"></a>glStencilFunc función)

La función **glStencilFunc** establece la función y el valor de referencia para las pruebas de estarcido.

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

La función de prueba. Los ocho tokens siguientes son válidos.



| Value                                                                                                                                                   | Significado                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="GL_NEVER"></span><span id="gl_never"></span><dl> <dt>**GL \_ nunca**</dt> </dl>          | Siempre produce un error.<br/>                                         |
| <span id="GL_LESS"></span><span id="gl_less"></span><dl> <dt>**CONTABILIDAD \_ inferior**</dt> </dl>             | Pasa si (  &  *máscara* de referencia) < (máscara de *estarcido*  &  ).<br/> |
| <span id="GL_LEQUAL"></span><span id="gl_lequal"></span><dl> <dt>**GL \_ LEQUAL**</dt> </dl>       | Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).<br/>    |
| <span id="GL_GREATER"></span><span id="gl_greater"></span><dl> <dt>**LIBRO \_ superior**</dt> </dl>    | Pasa si (  &  *máscara* de referencia) > (máscara de *estarcido*  &  ).<br/> |
| <span id="GL_GEQUAL"></span><span id="gl_gequal"></span><dl> <dt>**GL \_ GEQUAL**</dt> </dl>       | Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).<br/>    |
| <span id="GL_EQUAL"></span><span id="gl_equal"></span><dl> <dt>**igual a GL \_**</dt> </dl>          | Pasa si (  &  *máscara* de referencia) = (máscara de *estarcido*  &  ).<br/>    |
| <span id="GL_NOTEQUAL"></span><span id="gl_notequal"></span><dl> <dt>**NOTEQUAL en GL \_**</dt> </dl> | ¿Pasa si (máscara de *referencia*  &  )? (*Galería de símbolos*  &  *máscara*).<br/>    |
| <span id="GL_ALWAYS"></span><span id="gl_always"></span><dl> <dt>**GL \_ siempre**</dt> </dl>       | Siempre pasa.<br/>                                        |



 

</dd> <dt>

*ref* 
</dt> <dd>

El valor de referencia para la prueba de estarcido. El parámetro *ref* está fijado al intervalo \[ 0, 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido.

</dd> <dt>

*mask* 
</dt> <dd>

Máscara que es **y** Ed con el valor de referencia y el valor de estarcido almacenado cuando se realiza la prueba.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *FUNC* no era uno de los ocho valores aceptados.<br/>                                                                           |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La galería de símbolos, como el almacenamiento en búfer de *z*, habilita y deshabilita el dibujo en cada píxel. Dibuja en los planos de la galería de símbolos mediante primitivos de dibujo de OpenGL y, a continuación, representa geometría e imágenes mediante los planos de la galería de símbolos para enmascarar partes de la pantalla. La galería de símbolos se usa normalmente en algoritmos de representación de Multipass para lograr efectos especiales, como marcas, esquematización y representación de geometría sólida constructiva.

La prueba de estarcido elimina condicionalmente un píxel según el resultado de una comparación entre el valor de referencia y el valor en el búfer de estarcido. La prueba está habilitada por [**glEnable**](glenable.md) y [**glDisable**](gldisable.md) con el argumento GL de \_ estarcido \_ Test. Las acciones realizadas en función del resultado de la prueba de estarcido se especifican con [**glStencilOp**](glstencilop.md).

El parámetro *FUNC* es una constante simbólica que determina la función de comparación de estarcido. Acepta uno de los ocho valores mostrados anteriormente. El parámetro *ref* es un valor de referencia entero que se utiliza en la comparación de la galería de símbolos. Se fija en el intervalo comprendido entre \[ 0 y 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido. El parámetro *Mask* es bit **a bit y** Ed con el valor de referencia y el valor de estarcido almacenado, con los valores **y** Ed que participan en la comparación.

Si *cliché* representa el valor almacenado en la ubicación del búfer de estarcido correspondiente, la lista anterior muestra el efecto de cada función de comparación que se puede especificar mediante *FUNC*. Solo si la comparación se realiza correctamente, el píxel pasa a la siguiente fase del proceso de rasterización (vea [**glStencilOp**](glstencilop.md)). Todas las pruebas tratan los valores de la *Galería de símbolos* como enteros sin signo en el intervalo de \[ 0, 2 *n* 1 \] , donde *n* es el número de bitplanes en el búfer de estarcido.

Inicialmente, la prueba de galería de símbolos está deshabilitada. Si no hay ningún búfer de estarcido, no se puede modificar la galería de símbolos y es como si la prueba de estarcido siempre se supera.

Las siguientes funciones recuperan información relacionada con **glStencilFunc**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento de \_ estarcido GL \_ FUNC

**glGet** con el argumento \_ \_ máscara de valor \_ de la galería de símbolos GL

**glGet** con el argumento \_ referencia de la galería de símbolos GL \_

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

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





