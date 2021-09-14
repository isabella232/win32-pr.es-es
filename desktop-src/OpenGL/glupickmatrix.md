---
title: Función gluPickMatrix (Glu.h)
description: La función gluPickMatrix define una región de selección.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- Función gluPickMatrix OpenGL
topic_type:
- apiref
api_name:
- gluPickMatrix
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c54e62f82f52fedc7de7c7c4af1cd3ed1ccdf149
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244928"
---
# <a name="glupickmatrix-function"></a>Función gluPickMatrix

La **función gluPickMatrix** define una región de selección.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluPickMatrix(
   GLdouble x,
   GLdouble y,
   GLdouble height,
   GLdouble width,
   GLint    viewport[4]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

Coordenada de ventana x de una región de selección.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada de la ventana Y de una región de selección.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la región de selección en coordenadas de ventana.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la región de selección en coordenadas de ventana.

</dd> <dt>

*Viewport* 
</dt> <dd>

La ventanilla actual (como desde una [**llamada a glGetIntegerv).**](glgetintegerv.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluPickMatrix** crea una matriz de proyección que puede usar para restringir el dibujo a una pequeña región de la ventanilla.

1.  Use **gluPickMatrix para** restringir el dibujo a una pequeña región alrededor del cursor.
2.  Escriba el modo de selección [**(con glRenderMode)**](glrendermode.md)y vuelva a mostrar la escena.

    Todas las primitivas que se hubieran dibujado cerca del cursor se identifican y almacenan en el búfer de selección.

La matriz creada por **gluPickMatrix** se multiplica por la matriz actual como si se llamara [**a glMultMatrix**](glmultmatrix.md) con la matriz generada.

1.  Llame [**a glLoadIdentity para**](glloadidentity.md) cargar una matriz de identidad en la pila de la matriz de perspectiva.
2.  Llame **a gluPickMatrix.**
3.  Llame a una función (como [**gluPerspective)**](gluperspective.md)para multiplicar la matriz de perspectiva por la matriz pick.

Al usar **gluPickMatrix para** seleccionar B-Spline no uniformes de tipo Rational [(SPLINEBS),](using-nurbs-curves-and-surfaces.md)tenga cuidado de desactivar la propiedad DE GLUBS, GLU \_ AUTO LOAD \_ \_ MATRIX. Si GLU AUTO LOAD MATRIX no está desactivado, cualquier superficie DE LA BASE de datos de carga automática que se represente se subdivide de forma diferente con la matriz de selección de la forma en que se subdividió sin la \_ \_ \_ matriz de selección.

## <a name="examples"></a>Ejemplos

Al representar una escena de la siguiente manera:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



el código siguiente selecciona una parte de la ventanilla:


```
glMatrixMode(GL_PROJECTION);  
glLoadIdentity( );  
gluPickMatrix(x, y, width, height, viewport);  
gluPerspective(. . .);  
glMatrixMode(GL_MODELVIEW);  
/* Draw the scene */
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGetIntegerv**](glgetintegerv.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**glRenderMode**](glrendermode.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





