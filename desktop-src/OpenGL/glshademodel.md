---
title: Función glShadeModel (Gl.h)
description: La función glShadeModel selecciona sombreado plano o suave.
ms.assetid: 52985ad7-1d6c-48fc-8f1e-4eb2c0324c8e
keywords:
- Función glShadeModel OpenGL
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
ms.openlocfilehash: 505ff0e2d74f9eb4f252e4e663ceec00fd86469b3d69374623b2763915a08b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491615"
---
# <a name="glshademodel-function"></a>Función glShadeModel

La **función glShadeModel** selecciona sombreado plano o suave.

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

Valor simbólico que representa una técnica de sombreado. Los valores aceptados son GL \_ FLAT y GL \_ SMOOTH. El valor predeterminado es GL \_ SMOOTH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="error-codes"></a>Códigos de error

La función [**glGetError**](glgeterror.md) puede recuperar los siguientes códigos de error.



| Nombre                                                                                                  | Significado                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**ENUMERACIÓN \_ NO \_ VÁLIDA DE GL**</dt> </dl>      | *el* modo era un valor distinto de \_ GL GL O GL \_ SMOOTH.<br/>                                                                      |
| <dl> <dt>**OPERACIÓN \_ NO VÁLIDA DE \_ GL**</dt> </dl> | Se llamó a la función entre una llamada a [**glBegin**](glbegin.md) y la llamada correspondiente [**a glEnd**](glend.md).<br/> |



## <a name="remarks"></a>Comentarios

Las primitivas openGL pueden tener sombreado plano o suave. El sombreado suave, el valor predeterminado, hace que los colores calculados de los vértices se interpolan a medida que se rasteriza la primitiva, normalmente asignando colores diferentes a cada fragmento de píxel resultante. El sombreado plano selecciona el color calculado de un solo vértice y lo asigna a todos los fragmentos de píxeles generados mediante la rasterización de una sola primitiva. En cualquier caso, el color calculado de un vértice es el resultado de la iluminación, si la iluminación está habilitada, o es el color actual en el momento en que se especificó el vértice, si la iluminación está deshabilitada.

El sombreado plano y suave no se puededistinguir para los puntos. Contar vértices y primitivos a partir de uno, a partir de la emisión de [**glBegin,**](glbegin.md) cada segmento de línea sombreada *plana i* tiene el color calculado del vértice *i* + 1, su segundo vértice. Contando de forma similar a partir de uno, a cada polígono sombreado plano se le da el color calculado del vértice que se muestra en la tabla siguiente. Este es el último vértice que especifica el polígono en todos los casos excepto en los polígonos individuales, donde el primer vértice especifica el color sombreado plano.



| Tipo primitivo de polygon i | Vértice   |
|-----------------------------|----------|
| Polígono único (*I*=1)      | 1        |
| Franja de triángulo              | *i* + 2  |
| Ventilador de triángulo                | *i* + 2  |
| Triángulo independiente        | 3 *I*     |
| Banda cuád cuatro                  | 2 *i* + 2 |
| Quad independiente            | 4 *I*     |



 

**GlShadeModel** especifica el sombreado plano y  suave con el modo establecido en GL FLAT y \_ GL \_ SMOOTH, respectivamente.

La función siguiente recupera información relacionada con **glShadeModel**:

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ SHADE \_ MODEL

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

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





