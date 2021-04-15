---
title: función glShadeModel (GL. h)
description: La función glShadeModel selecciona el sombreado plano o suave.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- glShadeModel (función) OpenGL
topic_type:
- apiref
api_name:
- glShadeModel
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 142ac518c91c6378f1606235e25502be8c06dd6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676715"
---
# <a name="glshademodel-function"></a>glShadeModel función)

La función **glShadeModel** selecciona el sombreado plano o suave.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glShadeModel(
   GLenum mode
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*mode* 
</dt> <dd>

Un valor simbólico que representa una técnica de sombreado. Los valores aceptados son contabilidad \_ plana y contabilidad \_ suave. El valor predeterminado es GL \_ Smooth.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_enumeración GL no válida \_**</dt> </dl>      | el *modo* era un valor distinto de GL \_ Glat o GL \_ Smooth.<br/>                                                                      |
| <dl> <dt>**\_operación no válida GL \_**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente a [**glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Observaciones

Los primitivos de OpenGL pueden tener un sombreado plano o suave. El sombreado suave, el valor predeterminado, hace que los colores calculados de los vértices se interpolen a medida que se rasteriza la primitiva, normalmente asignando distintos colores a cada fragmento de píxel resultante. El sombreado plano selecciona el color calculado de un solo vértice y lo asigna a todos los fragmentos de píxeles generados mediante la rasterización de un solo primitivo. En cualquier caso, el color calculado de un vértice es el resultado de la iluminación, si está habilitada la iluminación o es el color actual en el momento en que se especificó el vértice, si la iluminación está deshabilitada.

No se distinguen los sombreados planos y suaves en los puntos. Contando los vértices y los primitivos de uno, a partir del momento en que se emite [**glBegin**](glbegin.md) , cada segmento de línea con sombra plana *i* recibe el color calculado del vértice *i* + 1, su segundo vértice. Contando de forma similar a una, cada polígono con sombra plana recibe el color calculado del vértice mostrado en la tabla siguiente. Este es el último vértice para especificar el polígono en todos los casos excepto en polígonos únicos, donde el primer vértice especifica el color de sombra plana.



| Tipo primitivo de Polygon i | Vértice   |
|-----------------------------|----------|
| Un solo Polígono (*I*= 1)      | 1        |
| Franja de triángulo              | *i* + 2  |
| Ventilador de triángulo                | *i* + 2  |
| Triángulo independiente        | 3 *I*     |
| Banda cuádruple                  | 2 *i* + 2 |
| Cuádruple independiente            | 4 *I*     |



 

Los sombreados planos y suaves se especifican mediante **glShadeModel** con el *modo* establecido en GL \_ plano y GL \_ Smooth, respectivamente.

La siguiente función recupera información relacionada con **glShadeModel**:

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ modelo de SOMBREAdo de contabilidad \_

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





