---
title: Función glClear (Gl.h)
description: La función glClear borra los búferes en valores preestablecidos.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- Función glClear OpenGL
topic_type:
- apiref
api_name:
- glClear
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb48a1b2832a5f9c046bb450b7cfba9ec4f83a759b093df91f3ec2064f23a3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082105"
---
# <a name="glclear-function"></a>función glClear

La **función glClear** borra los búferes en valores preestablecidos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glClear(
   GLbitfield mask
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mask* 
</dt> <dd>

Operadores OR bit a bit de máscaras que indican los búferes que se deben borrar. Las cuatro máscaras son las siguientes.



| Value                                                                                                                                                                                   | Significado                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**BIT DE \_ BÚFER DE COLOR \_ \_ GL**</dt> </dl>       | Búferes habilitados actualmente para la escritura de colores.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**BIT DE \_ BÚFER DE PROFUNDIDAD DE \_ \_ GL**</dt> </dl>       | Búfer de profundidad.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**BIT \_ DE BÚFER DE GL ACCUM \_ \_**</dt> </dl>       | Búfer de acumulación.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**BIT DE \_ BÚFER DE GALERÍA DE SÍMBOLOS DE \_ \_ GL**</dt> </dl> | Búfer de galería de símbolos.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**VALOR \_ NO VÁLIDO DE \_ GL**</dt> </dl>     | Cualquier bit distinto de los cuatro bits definidos se estableció en *mask*.<br/>                                                                |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

La **función glClear** establece el área de plano de bits de la ventana en valores previamente seleccionados por [**glClearColor**](glclearcolor.md), [**glClearIndex,**](glclearindex.md) [**glClearDepth,**](glcleardepth.md) [**glClearStencil**](glclearstencil.md)y [**glClearAccum**](glclearaccum.md). Puede borrar varios búferes de color simultáneamente seleccionando más de un búfer a la vez mediante [**glDrawBuffer.**](gldrawbuffer.md)

La prueba de propiedad de píxeles, la prueba de desenlazamiento, la dithering y las máscaras de escritura del búfer afectan al funcionamiento de **glClear**. El cuadro de verificación delimita la región borrada. La **función glClear** omite la función alfa, la función blend, la operación lógica, la galería de símbolos, la asignación de texturas *y z*-buffering.

La **función glClear** toma un único argumento (*mask*) que es el OR bit a bit de varios valores que indican qué búfer se va a borrar.

El valor para el que se borra cada búfer depende de la configuración del valor sin borrar para ese búfer.

Si un búfer no está presente, una **llamada glClear** dirigida a ese búfer no tiene ningún efecto.

Las siguientes funciones recuperan información relacionada con **glClear**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento \_ GL ACCUM CLEAR \_ \_ VALUE

**glGet con** el argumento GL \_ DEPTH CLEAR \_ \_ VALUE

**glGet con** el argumento GL \_ INDEX CLEAR \_ \_ VALUE

**glGet con** el argumento GL \_ COLOR CLEAR \_ \_ VALUE

**glGet con** el argumento GL \_ STENCIL \_ CLEAR \_ VALUE

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

[**glClearAccum**](glclearaccum.md)
</dt> <dt>

[**glClearColor**](glclearcolor.md)
</dt> <dt>

[**glClearDepth**](glcleardepth.md)
</dt> <dt>

[**glClearIndex**](glclearindex.md)
</dt> <dt>

[**glClearStencil**](glclearstencil.md)
</dt> <dt>

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glScissor**](glscissor.md)
</dt> </dl>

 

 





