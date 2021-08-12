---
title: Función glPolygonMode (Gl.h)
description: La función glPolygonMode selecciona un modo de rasterización de polígono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- Función glPolygonMode OpenGL
topic_type:
- apiref
api_name:
- glPolygonMode
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f040b3e44ee34d819752bae5deffbf1a02f0d38ab1249f2e32de67c262bd5f2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118615211"
---
# <a name="glpolygonmode-function"></a>Función glPolygonMode

La **función glPolygonMode** selecciona un modo de rasterización de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Cara* 
</dt> <dd>

Polígonos a los *que se* aplica el modo. Debe ser GL FRONT para polígonos orientados al frente, GL BACK para polígonos orientados hacia atrás o GL FRONT AND BACK para \_ \_ \_ \_ polígonos orientados hacia delante \_ y hacia atrás.

</dd> <dt>

*mode* 
</dt> <dd>

La forma en que se rasterizarán los polígonos. Se definen los modos siguientes y se pueden especificar en *el modo*. El valor predeterminado es GL FILL para los polígonos orientados hacia delante \_ y hacia atrás.



| Value                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**GL \_ POINT**</dt> </dl> | Los vértices de polígono que están marcados como el inicio de un borde de límite se dibujan como puntos. Los atributos de punto como GL \_ POINT SIZE y GL POINT SMOOTH controlan la \_ \_ \_ rasterización de los puntos. Los atributos de rasterización de polígono que no son GL \_ POLYGON MODE no tienen ningún \_ efecto.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**GL \_ LINE**</dt> </dl>    | Los bordes de límite del polígono se dibujan como segmentos de línea. Se tratan como segmentos de línea conectados para el contrabando de líneas; El contador y el patrón de stipple de línea no se restablecen entre segmentos (vea [**glLineStipple).**](gllinestipple.md) Los atributos de línea como GL \_ LINE WIDTH y GL LINE SMOOTH controlan la \_ \_ \_ rasterización de las líneas. Los atributos de rasterización de polígono que no son GL \_ POLYGON MODE no tienen ningún \_ efecto.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**GL \_ FILL**</dt> </dl>    | El interior del polígono se rellena. Los atributos de polígono como GL \_ POLYGON \_ STIPPLE y GL \_ POLYGON SMOOTH controlan la \_ rasterización del polígono.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ \_ NO VÁLIDA DE GL**</dt> </dl>      | La *cara* o *el modo* no era un valor aceptado.<br/>                                                                         |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La **función glPolygonMode** controla la interpretación de polígonos para la rasterización. El *parámetro face* describe a qué modo de polígonos se aplica: polígonos orientados al frente (GL FRONT), polígonos orientados hacia atrás (GL BACK) o ambos  \_ \_ (GL FRONT Y \_ \_ \_ BACK). El modo de polígono solo afecta a la rasterización final de los polígonos. En concreto, los vértices de un polígono están encendidos y el polígono se recorta y posiblemente se recorta antes de aplicar estos modos.

Para dibujar una superficie con polígonos orientados hacia atrás rellenos y polígonos frontales descritos, llame a

**glPolygonMode**(GL \_ FRONT, GL \_ LINE);

Los vértices se marcan como límite o no delimitadores con una marca perimetral. OpenGL genera internamente marcas perimetrales cuando descompone polígonos y se pueden establecer explícitamente mediante [**glEdgeFlag**](gledgeflag-functions.md).

La función siguiente recupera información relacionada con **glPolygonMode**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ POLYGON \_ MODE

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLineStipple**](gllinestipple.md)
</dt> <dt>

[**glLineWidth**](gllinewidth.md)
</dt> <dt>

[**glPointSize**](glpointsize.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> </dl>

 

 





