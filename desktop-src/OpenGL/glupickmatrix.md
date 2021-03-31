---
title: función gluPickMatrix (GLU. h)
description: La función gluPickMatrix define una región de picking.
ms.assetid: 2f57345c-17a0-4716-8ab8-170aaed2b4f9
keywords:
- gluPickMatrix (función) OpenGL
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995905"
---
# <a name="glupickmatrix-function"></a>gluPickMatrix función)

La función **gluPickMatrix** define una región de picking.

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

La coordenada x de la ventana de una región de picking.

</dd> <dt>

*y* 
</dt> <dd>

La coordenada de la ventana y de una región de picking.

</dd> <dt>

*height* 
</dt> <dd>

Alto de la región de selección en coordenadas de la ventana.

</dd> <dt>

*width* 
</dt> <dd>

Ancho de la región de selección en coordenadas de la ventana.

</dd> <dt>

*encuadre* 
</dt> <dd>

La ventanilla actual (a partir de una llamada a [**glGetIntegerv**](glgetintegerv.md) ).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluPickMatrix** crea una matriz de proyección que puede usar para restringir el dibujo a una región pequeña de la ventanilla.

1.  Use **gluPickMatrix** para restringir el dibujo a una región pequeña alrededor del cursor.
2.  Escriba el modo de selección (con [**glRenderMode**](glrendermode.md)) y, a continuación, represente la escena.

    Todos los primitivos que se habrían dibujado cerca del cursor se identifican y almacenan en el búfer de selección.

La matriz creada por **gluPickMatrix** se multiplica por la matriz actual como si se llamara a [**glMultMatrix**](glmultmatrix.md) con la matriz generada.

1.  Llame a [**glLoadIdentity**](glloadidentity.md) para cargar una matriz de identidad en la pila de la matriz de perspectiva.
2.  Llame a **gluPickMatrix**.
3.  Llame a una función (como [**gluPerspective**](gluperspective.md)) para multiplicar la matriz de perspectiva por la matriz de picking.

Al usar **gluPickMatrix** para elegir la spline B-spline racional ([NURBS](using-nurbs-curves-and-surfaces.md)) no uniforme, tenga cuidado de desactivar la propiedad NURBS, Glu \_ \_ autoload \_ Matrix. Si \_ \_ \_ la matriz de carga automática de Glu no está desactivada, cualquier superficie de NURBS presentada se subdivide de manera diferente con la matriz de picking de cómo se subdividió sin la matriz de picking.

## <a name="examples"></a>Ejemplos

Al representar una escena de la manera siguiente:


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
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
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

 

 





