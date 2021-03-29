---
title: función glPolygonMode (GL. h)
description: La función glPolygonMode selecciona un modo de rasterización de polígono.
ms.assetid: d8781bae-e78c-40fb-9f33-c742c70ebda1
keywords:
- glPolygonMode (función) OpenGL
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
ms.openlocfilehash: 23d133243c1655432842a939b8da0f3a981fdffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666081"
---
# <a name="glpolygonmode-function"></a>glPolygonMode función)

La función **glPolygonMode** selecciona un modo de rasterización de polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glPolygonMode(
   GLenum face,
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Portada* 
</dt> <dd>

Polígonos a los que se aplica el *modo* . Debe estar \_ en la parte frontal de los polígonos frontales, en el libro \_ de reserva para los polígonos de respaldo, o en la \_ parte frontal \_ y \_ posterior para los polígonos frontal y trasero.

</dd> <dt>

*mode* 
</dt> <dd>

La forma en que se rasterizarán los polígonos. Se definen los siguientes modos y se pueden especificar en el *modo*. El valor predeterminado es el \_ relleno de contabilidad para los polígonos delante y detrás.



| Value                                                                                                                                          | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINT"></span><span id="gl_point"></span><dl> <dt>**punto de contabilidad \_**</dt> </dl> | Los vértices de polígono que se marcan como el inicio de un borde del límite se dibujan como puntos. Los atributos de punto, como el \_ \_ tamaño de los puntos de la contabilidad y \_ \_ el punto de contabilidad suavizado controlan la rasterización de los puntos. Los atributos de rasterización de polígono distintos del modo de polígono de contabilidad \_ \_ no tienen ningún efecto.<br/>                                                                                                                                                    |
| <span id="GL_LINE"></span><span id="gl_line"></span><dl> <dt>**línea de contabilidad \_**</dt> </dl>    | Los bordes de los límites del polígono se dibujan como segmentos de línea. Se tratan como segmentos de línea conectados para el punteado de línea; el contador y el patrón punteado de línea no se restablecen entre segmentos (vea [**glLineStipple**](gllinestipple.md)). Los atributos de línea como \_ \_ el ancho de línea de libro de contabilidad y \_ \_ el control suavizado de línea de contabilidad controlan la rasterización de las líneas. Los atributos de rasterización de polígono distintos del modo de polígono de contabilidad \_ \_ no tienen ningún efecto.<br/> |
| <span id="GL_FILL"></span><span id="gl_fill"></span><dl> <dt>**relleno de contabilidad \_**</dt> </dl>    | El interior del polígono se rellena. Los atributos Polygon, como GL \_ Polygon \_ punteate y GL \_ poligonal \_ controlan la rasterización del polígono.<br/>                                                                                                                                                                                                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | Cualquier *esfera* o *modo* no era un valor aceptado.<br/>                                                                         |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

La función **glPolygonMode** controla la interpretación de polígonos para la rasterización. El parámetro *facial* describe el *modo* de polígonos que se aplica a: polígonos frontales ( \_ front-end), polígonos de orientación hacia atrás ( \_ retroceder) o ambos (de la \_ parte frontal \_ y \_ posterior). El modo de polígono afecta solo a la rasterización final de los polígonos. En concreto, los vértices de un polígono están iluminados y el polígono se recorta y, posiblemente, se selecciona antes de que se apliquen estos modos.

Para dibujar una superficie con polígonos de orientación hacia atrás rellenados y polígonos de cara frontal detallados, llame a

**glPolygonMode**(libro \_ frontal, línea de contabilidad \_ );

Los vértices se marcan como límite o no límite con una marca de borde. OpenGL genera internamente marcas de borde cuando descompone polígonos y se pueden establecer explícitamente mediante [**glEdgeFlag**](gledgeflag-functions.md).

La siguiente función recupera información relacionada con **glPolygonMode**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el \_ modo de polígono de contabilidad de argumentos \_

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

 

 





