---
title: Función glRasterPos2d (Gl.h)
description: Especifica la posición de trama para las operaciones de píxeles. | Función glRasterPos2d (Gl.h)
ms.assetid: 3aad4085-8957-433c-8822-765df6278af8
keywords:
- Función glRasterPos2d OpenGL
topic_type:
- apiref
api_name:
- glRasterPos2d
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0567843e157f869bc6caf5fa0932e238e54bcf61
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244995"
---
# <a name="glrasterpos2d-function"></a>Función glRasterPos2d

Especifica la posición de trama para las operaciones de píxeles.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glRasterPos2d(
   GLdouble x,
   GLdouble y
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Especifica la coordenada X para la posición de trama actual.

</dd> <dt>

*y* 
</dt> <dd>

Especifica la coordenada Y para la posición de trama actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

OpenGL mantiene una posición 3D en coordenadas de ventana. Esta posición, denominada posición de trama, se mantiene con precisión de subpíxel. Se usa para colocar las operaciones de escritura de píxeles y mapas de bits. Vea [**glBitmap,**](glbitmap.md) [**glDrawPixels**](gldrawpixels.md)y [**glCopyPixels.**](glcopypixels.md)

La posición de trama actual consta de tres coordenadas de ventana *(x, y, z),* un valor *w* de coordenada de recorte, una distancia de coordenada de ojo, un bit válido y las coordenadas de textura y datos de color asociados. La *coordenada w* es una coordenada de recorte, porque *w* no se proyecta en coordenadas de ventana. La [función glRasterPos4](glrasterpos-functions.md) especifica las coordenadas de objeto *x, y, z* y *w* explícitamente. La función glRasterPos3 especifica las coordenadas de objeto *x, y* y *z* explícitamente, mientras *que w* se establece implícitamente en una. La función glRasterPos2 usa los valores de argumento para *x* e *y* mientras se establece implícitamente *z* y *w* en cero y uno.

Las coordenadas de objeto presentadas [por glRasterPos](glrasterpos-functions.md) se tratan igual que las de un [comando glVertex.](glvertex-functions.md) Se transforman mediante las matrices de proyección y vista de modelo actuales y se pasan a la fase de recorte. Si el vértice no se ha seleccionado, se proyecta y escala a coordenadas de ventana, que se convierten en la nueva posición de trama actual, y se establece la marca GL \_ CURRENT \_ RASTER POSITION \_ \_ VALID. Si se hace la selección del vértice, se borra el bit válido y la posición del trama actual y las coordenadas de color y textura asociadas no están definidas.

La posición de trama actual también incluye algunos datos de color asociados y coordenadas de textura. Si la iluminación está habilitada, GL CURRENT RASTER COLOR, en modo RGBA o GL CURRENT RASTER INDEX, en modo de índice de color, se establece en el color generado por el cálculo de iluminación \_ \_ \_ \_ \_ \_ (vea [glLight](gllight-functions.md), [glLightModel](gllightmodel-functions.md)y [**glShadeModel).**](glshademodel.md) Si la iluminación está deshabilitada, se usa el color actual (en modo RGBA, la variable de estado GL CURRENT COLOR) o el índice de color (en modo de índice de color, variable de estado GL CURRENT INDEX) para actualizar el color de \_ \_ trama \_ \_ actual.

Del mismo modo, GL CURRENT RASTER TEXTURE COORDS se actualiza como una función de GL CURRENT TEXTURE COORDS, en función de la matriz de textura y las funciones de generación de textura \_ \_ \_ \_ \_ \_ \_ [(vea glTexGen).](gltexgen-functions.md) Por último, la distancia desde el origen del sistema de coordenadas de los ojos hasta el vértice, tal como se transforma solo mediante la matriz modelview, reemplaza a GL \_ CURRENT \_ RASTER \_ DISTANCE.

Inicialmente, la posición del trama actual es (0,0,0,1), la distancia de trama actual es 0, se establece el bit válido, el color RGBA asociado es (1,1,1,1), el índice de color asociado es 1 y las coordenadas de textura asociadas son (0, 0, 0, 1). En el modo RGBA, GL CURRENT RASTER INDEX siempre es 1; en el modo de índice de color, el color RGBA de trama actual siempre mantiene \_ \_ su valor \_ inicial.

> [!Note]  
> [GlRasterPos](glrasterpos-functions.md) y [**glBitmap**](glbitmap.md)modifican la posición del trama.

 

> [!Note]  
> Cuando las coordenadas de la posición del trama no son válidas, se omiten los comandos de dibujo basados en la posición del trama (es decir, no tienen como resultado cambios en el estado OpenGL).

 

Las funciones siguientes recuperan información relacionada [con glRasterPos](glrasterpos-functions.md):

<dl>

[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ POSITION  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER POSITION \_ \_ \_ VALID  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ DISTANCE  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ COLOR  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER \_ \_ INDEX  
[**glGet con**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) el argumento GL \_ CURRENT RASTER TEXTURE \_ \_ \_ COORDS  
</dl>

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

 

 





