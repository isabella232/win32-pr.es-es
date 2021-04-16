---
title: función glRasterPos3d (GL. h)
description: Especifica la posición de la trama para las operaciones de píxel. | función glRasterPos3d (GL. h)
ms.assetid: 82e526f2-7ccd-4d31-a281-7cd6d7a488c1
keywords:
- glRasterPos3d (función) OpenGL
topic_type:
- apiref
api_name:
- glRasterPos3d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f50429867471697afb4df9c9c99e4a61012737d5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105670203"
---
# <a name="glrasterpos3d-function"></a>glRasterPos3d función)

Especifica la posición de la trama para las operaciones de píxel.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRasterPos3d(
   GLdouble x,
   GLdouble y,
   GLdouble z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica la coordenada x de la posición de la trama actual.

</dd> <dt>

*y* 
</dt> <dd>

Especifica la coordenada y de la posición de la trama actual.

</dd> <dt>

*z* 
</dt> <dd>

Especifica la coordenada z de la posición de la trama actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

OpenGL mantiene una posición 3D en las coordenadas de la ventana. Esta posición, denominada posición de la trama, se mantiene con una precisión de subpíxeles. Se utiliza para colocar las operaciones de escritura de píxeles y de mapas de bits. Vea [**glBitmap**](glbitmap.md), [**glDrawPixels**](gldrawpixels.md)y [**glCopyPixels**](glcopypixels.md).

La posición de rasterización actual consta de tres coordenadas de ventana (*x, y, z*), un valor de coordenada de clip *w* , una distancia de coordenadas ocular, un bit válido y las coordenadas de textura y datos de color asociados. La coordenada *w* es una coordenada de clip, porque *w* no se proyecta en coordenadas de ventana. La función [glRasterPos4](glrasterpos-functions.md) especifica las coordenadas de objeto *x, y, z* y *w* explícitamente. La función glRasterPos3 especifica las coordenadas de objeto *x,* y y *z* explícitamente, mientras que *w* se establece implícitamente en una. La función glRasterPos2 usa los valores de argumento para *x* e *y mientras establece* implícitamente *z* y *w* en cero y en uno.

Las coordenadas de objeto presentadas por [glRasterPos](glrasterpos-functions.md) se tratan igual que las de un comando [glVertex](glvertex-functions.md) . Los transforman las matrices de proyección y MODELVIEW actuales y se pasan a la fase de recorte. Si no se selecciona el vértice, se proyecta y se escala a las coordenadas de la ventana, que se convierten en la nueva posición de la trama actual y \_ \_ \_ \_ se establece la marca válida de la posición de rasterización actual de GL. Si se selecciona el vértice, se borra el bit válido y la posición de la trama actual y las coordenadas de textura y color asociadas no están definidas.

La posición de la trama actual también incluye algunos datos de color y coordenadas de textura asociados. Si está habilitada la iluminación, \_ \_ el color de rasterizado actual \_ de GL, en el modo RGBA o el \_ Índice de \_ rasterización actual de GL \_ , en modo de índice de color, se establece en el color producido por el cálculo de iluminación (vea [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)y [**glShadeModel**](glshademodel.md)). Si la iluminación está deshabilitada, se usa el color actual (en modo RGBA, la variable de estado GL \_ Current \_ color) o el índice de color (en modo de índice de color, variable de estado, \_ índice actual de contabilidad \_ ) para actualizar el color de la trama actual.

Del mismo modo, las \_ \_ coordenadas de textura de rasterizado actual \_ de GL \_ se actualizan como una función de las \_ coordenadas de textura actual de GL \_ \_ , en función de la matriz de textura y las funciones de generación de textura (vea [glTexGen](gltexgen-functions.md)). Por último, la distancia desde el origen del sistema de coordenadas del ojo hasta el vértice, tal y como se transforma solo en la matriz MODELVIEW, reemplaza a la distancia de la \_ trama actual de contabilidad \_ \_ .

Inicialmente, la posición de la trama actual es (0, 0, 0, 1), la distancia de la trama actual es 0, se establece el bit válido, el color RGBA asociado es (1, 1, 1, 1), el índice de color asociado es 1 y las coordenadas de textura asociadas son (0, 0, 0, 1). En el modo RGBA, \_ el índice de rasterizado actual de GL siempre \_ \_ es 1; en el modo de índice de color, el color RGBA de trama actual siempre mantiene su valor inicial.

> [!Note]  
> [GlRasterPos](glrasterpos-functions.md) y [**glBitmap**](glbitmap.md)modifican la posición de la trama.

 

> [!Note]  
> Cuando las coordenadas de posición de trama no son válidas, los comandos de dibujo que se basan en la posición de la trama se omiten (es decir, no producen cambios en el estado de OpenGL).

 

Las siguientes funciones recuperan información relacionada con [glRasterPos](glrasterpos-functions.md):

<dl>

[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ posición de RASTERIZAción actual de GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ posición de rasterizado actual de GL \_ \_ \_ válido  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ distancia de trama actual de GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ color de RASTERIZAdo actual de GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con el argumento \_ \_ Índice de trama actual de GL \_  
[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) con argumento de \_ \_ textura de RASTERIZAdo actual \_ de GL \_  
</dl>

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glCopyPixels**](glcopypixels.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[glLight](gllight-functions.md)
</dt> <dt>

[glLightModel](gllightmodel-functions.md)
</dt> <dt>

[**glShadeModel**](glshademodel.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[glTexGen](gltexgen-functions.md)
</dt> <dt>

[glVertex](glvertex-functions.md)
</dt> </dl>

 

 





