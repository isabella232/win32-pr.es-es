---
title: Función glLogicOp (Gl.h)
description: La función glLogicOp especifica una operación de píxel lógico para la representación del índice de color.
ms.assetid: 29edf9bd-f3b8-4de7-9afb-07714f4efd92
keywords:
- Función glLogicOp OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272103"
---
# <a name="gllogicop-function"></a>Función glLogicOp

La **función glLogicOp** especifica una operación de píxel lógico para la representación del índice de color.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glLogicOp(
   GLenum opcode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*opcode* 
</dt> <dd>

Constante simbólica que selecciona una operación lógica. Se aceptan los símbolos siguientes donde s es igual al valor del bit de origen y d es el valor del bit de destino.



| Value                                                                                                                                                                   | Significado              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| <span id="GL_CLEAR"></span><span id="gl_clear"></span><dl> <dt>**GL \_ CLEAR**</dt> </dl>                          | 0<br/>         |
| <span id="GL_SET"></span><span id="gl_set"></span><dl> <dt>**GL \_ SET**</dt> </dl>                                | 1<br/>         |
| <span id="GL_COPY"></span><span id="gl_copy"></span><dl> <dt>**GL \_ COPY**</dt> </dl>                             | s<br/>         |
| <span id="GL_COPY_INVERTED"></span><span id="gl_copy_inverted"></span><dl> <dt>**GL \_ COPY \_ INVERTED**</dt> </dl> | !s<br/>        |
| <span id="GL_NOOP"></span><span id="gl_noop"></span><dl> <dt>**GL \_ NOOP**</dt> </dl>                             | d<br/>         |
| <span id="GL_INVERT"></span><span id="gl_invert"></span><dl> <dt>**GL \_ INVERT**</dt> </dl>                       | !d<br/>        |
| <span id="GL_AND"></span><span id="gl_and"></span><dl> <dt>**GL \_ AND**</dt> </dl>                                | s & d<br/>     |
| <span id="GL_NAND"></span><span id="gl_nand"></span><dl> <dt>**GL \_ NAND**</dt> </dl>                             | ! (s & d)<br/>  |
| <span id="GL_OR"></span><span id="gl_or"></span><dl> <dt>**GL \_ OR**</dt> </dl>                                   | s \| d<br/>    |
| <span id="GL_NOR"></span><span id="gl_nor"></span><dl> <dt>**GL \_ NI**</dt> </dl>                                | ! (s \| d)<br/> |
| <span id="GL_XOR"></span><span id="gl_xor"></span><dl> <dt>**GL \_ XOR**</dt> </dl>                                | s ^ d<br/>     |
| <span id="GL_EQUIV"></span><span id="gl_equiv"></span><dl> <dt>**GL \_ EQUIV**</dt> </dl>                          | ! (s ^ d)<br/>  |
| <span id="GL_AND_REVERSE"></span><span id="gl_and_reverse"></span><dl> <dt>**GL \_ Y \_ REVERSE**</dt> </dl>       | s & !d<br/>    |
| <span id="GL_AND_INVERTED"></span><span id="gl_and_inverted"></span><dl> <dt>**GL \_ E \_ INVERTIDO**</dt> </dl>    | !s & d<br/>    |
| <span id="GL_OR_REVERSE"></span><span id="gl_or_reverse"></span><dl> <dt>**GL \_ O \_ REVERSE**</dt> </dl>          | s \| !d<br/>   |
| <span id="GL_OR_INVERTED"></span><span id="gl_or_inverted"></span><dl> <dt>**GL \_ O \_ INVERTIDO**</dt> </dl>       | !s \| d<br/>   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | *opcode* no era un valor aceptado.<br/>                                                                                        |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glLogicOp** especifica una operación lógica que, cuando está habilitada, se aplica entre el índice de color entrante y el índice de color en la ubicación correspondiente del búfer de fotogramas. La operación lógica está habilitada o deshabilitada con [**glEnable**](glenable.md) y **glDisable** mediante la constante simbólica GL \_ LOGIC \_ OP.

El *parámetro opcode* es una constante simbólica elegida en la lista siguiente. En la explicación de las operaciones lógicas, *s* representa el índice de color entrante y *d* representa el índice en el búfer de fotogramas. Se usan operadores estándar del lenguaje C. Como sugieren estos operadores bit a bit, la operación lógica se aplica de forma independiente a cada par de bits de los índices de origen y destino.

Las operaciones de píxel lógico no se aplican a los búferes de color RGBA.

Cuando se habilita más de un búfer de índice de color para dibujar, las operaciones lógicas se realizan por separado para cada búfer habilitado, usando el contenido de ese búfer para el índice de destino (vea [**glDrawBuffer**](gldrawbuffer.md)).

El *parámetro opcode* debe ser uno de los 16 valores aceptados. Otros valores producirán un error.

Las funciones siguientes recuperan información relacionada **con glLogicOp**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ LOGIC OP \_ \_ MODE

[**glIsEnabled con**](glisenabled.md) el argumento GL \_ LOGIC \_ OP

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

 

 





