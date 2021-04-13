---
title: función glLogicOp (GL. h)
description: La función glLogicOp especifica una operación de píxeles lógicos para la representación del índice de color.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- glLogicOp (función) OpenGL
topic_type:
- apiref
api_name:
- glLogicOp
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb29e8f845e99f6d3c988dfd0c0201de129bee69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535512"
---
# <a name="gllogicop-function"></a>glLogicOp función)

La función **glLogicOp** especifica una operación de píxeles lógicos para la representación del índice de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Código* 
</dt> <dd>

Una constante simbólica que selecciona una operación lógica. Los siguientes símbolos se aceptan donde s es igual al valor del bit de origen y d es el valor del bit de destino.



| Value                                                                                                                                                                   | Significado              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**\_borrado de contabilidad**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**conjunto de contabilidad \_**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**copia en GL \_**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**copia en contab \_ \_ invertida**</dt> </dl> | ! s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**NOOP de GL \_**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**inversión en contab \_**</dt> </dl>                       | ! d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ y**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**CC \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ o**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ y**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**cont. de GL \_**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**EQUIV. cont. \_**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ e \_ inverso**</dt> </dl>       | s &! d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ y \_ invertido**</dt> </dl>    | ! s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ o \_ inverso**</dt> </dl>          | s \| ! d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ o \_ invertido**</dt> </dl>       | ! s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | *OpCode* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glLogicOp** especifica una operación lógica que, cuando se habilita, se aplica entre el índice de color entrante y el índice de color en la ubicación correspondiente en fotogramas. La operación lógica está habilitada o deshabilitada con [**glEnable**](glenable.md) y **glDisable** con la constante simbólica de la lógica de contabilidad \_ \_ .

El parámetro *OpCode* es una constante simbólica elegida en la lista siguiente. En la explicación de las operaciones lógicas, *s* representa el índice de color entrante y *d* representa el índice en fotogramas. Se usan los operadores estándar de lenguaje C. Como sugieren estos operadores bit a bit, la operación lógica se aplica independientemente a cada par de bits de los índices de origen y de destino.

Las operaciones de píxeles lógicos no se aplican a los búferes de color RGBA.

Cuando se habilita más de un búfer de índice de color para dibujar, las operaciones lógicas se realizan por separado para cada búfer habilitado, utilizando el contenido de ese búfer para el índice de destino (vea [**glDrawBuffer**](gldrawbuffer.md)).

El parámetro *OpCode* debe ser uno de los 16 valores aceptados. Otros valores producen un error.

Las siguientes funciones recuperan información relacionada con **glLogicOp**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de \_ OP \_ Logic de contabilidad de argumentos

[**glIsEnabled**](glisenabled.md) con el argumento \_ OP lógica de contabilidad \_

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

[**glDrawBuffer**](gldrawbuffer.md)
</dt> <dt>

[**glEnable**](glenable.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glIsEnabled**](glisenabled.md)
</dt> <dt>

[**glStencilOp**](glstencilop.md)
</dt> </dl>

 

 





