---
title: Función gluPerspective (Glu.h)
description: La función gluPerspective configura una matriz de proyección de perspectiva.
ms.assetid: 125e2828-a2d7-4c6c-9370-eb21a581ced8
keywords:
- Función gluPerspective OpenGL
topic_type:
- apiref
api_name:
- gluPerspective
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf30fc7dc4c6ba5a56efd3def6a5a7178f81ed49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244934"
---
# <a name="gluperspective-function"></a>función gluPerspective

La **función gluPerspective** configura una matriz de proyección de perspectiva.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluPerspective(
   GLdouble fovy,
   GLdouble aspect,
   GLdouble zNear,
   GLdouble zFar
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*fovy* 
</dt> <dd>

Campo de ángulo de vista, en grados, en la dirección y.

</dd> <dt>

*aspect* 
</dt> <dd>

Relación de aspecto que determina el campo de vista en la dirección X. La relación de aspecto es la proporción de *x* (ancho) a *y* (alto).

</dd> <dt>

*zNear* 
</dt> <dd>

Distancia desde el visor hasta el plano de recorte cercano (siempre positivo).

</dd> <dt>

*zFar* 
</dt> <dd>

Distancia desde el visor hasta el plano de recorte lejano (siempre positivo).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluPerspective** especifica un frustum de visualización en el sistema de coordenadas mundial. En general, la relación de aspecto de **gluPerspective** debe coincidir con la relación de aspecto de la ventanilla asociada. Por ejemplo, *aspect* = 2.0 significa que el ángulo de vista del visor es el doble de ancho en *x* que en *y*. Si la ventanilla tiene el doble de ancho que la alta, muestra la imagen sin distorsión.

La matriz generada **por gluPerspective** se multiplica por la matriz actual, como si se llamara [**a glMultMatrix**](glmultmatrix.md) con la matriz generada. Para cargar la matriz de perspectiva en la pila de matriz actual en su lugar, anteponga la llamada a **gluPerspective** con una llamada a [**glLoadIdentity**](glloadidentity.md).

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**glLoadIdentity**](glloadidentity.md)
</dt> <dt>

[**glMultMatrix**](glmultmatrix.md)
</dt> <dt>

[**gluOrtho2D**](gluortho2d.md)
</dt> </dl>

 

 





