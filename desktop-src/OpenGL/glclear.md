---
title: función glClear (GL. h)
description: La función glClear borra los búferes de los valores preestablecidos.
ms.assetid: 9818f969-3145-45ea-aa9c-2abed953a8e0
keywords:
- glClear (función) OpenGL
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
ms.openlocfilehash: 0db935e46c65c42976024a8afbb98028294710c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676785"
---
# <a name="glclear-function"></a>glClear función)

La función **glClear** borra los búferes de los valores preestablecidos.

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

Operadores OR bit a bit de las máscaras que indican los búferes que se van a borrar. Las cuatro máscaras son las siguientes.



| Value                                                                                                                                                                                   | Significado                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="GL_COLOR_BUFFER_BIT"></span><span id="gl_color_buffer_bit"></span><dl> <dt>**\_bit de \_ búfer de color de contabilidad \_**</dt> </dl>       | Búferes habilitados actualmente para la escritura de color.<br/> |
| <span id="GL_DEPTH_BUFFER_BIT"></span><span id="gl_depth_buffer_bit"></span><dl> <dt>**\_bit de \_ búfer de profundidad de contabilidad \_**</dt> </dl>       | Búfer de profundidad.<br/>                                |
| <span id="GL_ACCUM_BUFFER_BIT"></span><span id="gl_accum_buffer_bit"></span><dl> <dt>**\_bit de \_ búfer de acumulación de GL \_**</dt> </dl>       | Búfer de acumulación.<br/>                         |
| <span id="GL_STENCIL_BUFFER_BIT"></span><span id="gl_stencil_buffer_bit"></span><dl> <dt>**\_bit de \_ búfer de estarcido GL \_**</dt> </dl> | Búfer de estarcido.<br/>                              |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_valor no válido de GL \_**</dt> </dl>     | Cualquier otro bit que no sea los cuatro bits definidos se estableció en *Mask*.<br/>                                                                |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glClear** establece el área Bitplane de la ventana en valores previamente seleccionados por [**glClearColor**](glclearcolor.md), [**glClearIndex**](glclearindex.md), [**glClearDepth**](glcleardepth.md), [**glClearStencil**](glclearstencil.md)y [**glClearAccum**](glclearaccum.md). Puede borrar varios búferes de color simultáneamente seleccionando más de un búfer a la vez mediante [**glDrawBuffer**](gldrawbuffer.md).

La prueba de propiedad de píxeles, la prueba de tijera, la interpolación y el writemasks de búfer afectan al funcionamiento de **glClear**. El cuadro de tijera delimita la región borrada. La función **glClear** omite la función alfa, la función Blend, la operación lógica, el estarcido, la asignación de textura y el almacenamiento en búfer *z*.

La función **glClear** toma un solo argumento (*Mask*) que es la operación OR bit a bit de varios valores que indican qué búfer se va a borrar.

El valor en el que se borra cada búfer depende de la configuración del valor sin cifrar para ese búfer.

Si no hay ningún búfer, una llamada a **glClear** dirigida a ese búfer no tiene ningún efecto.

Las siguientes funciones recuperan información relacionada con **glClear**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ valor Clear acumulado de GL \_

**glGet** con valor de profundidad de GL de argumento \_ \_ \_

**glGet** con el argumento \_ \_ valor sin formato de índice de contabilidad \_

**glGet** con el argumento \_ GL \_ color \_ valor sin formato

**glGet** con el argumento \_ GL \_ \_ valor sin formato de estarcido

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

 

 





