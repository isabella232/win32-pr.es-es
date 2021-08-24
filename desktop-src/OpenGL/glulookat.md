---
title: Función gluLookAt (Glu.h)
description: La función gluLookAt define una transformación de visualización.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- Función gluLookAt OpenGL
topic_type:
- apiref
api_name:
- gluLookAt
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b21d0cb2fac6573ab2999eb96b2af8b1ecb670f4e51d1ffd2ad91ba001c9ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675305"
---
# <a name="glulookat-function"></a>función gluLookAt

La **función gluLookAt** define una transformación de visualización.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluLookAt(
   GLdouble eyex,
   GLdouble eyey,
   GLdouble eyez,
   GLdouble centerx,
   GLdouble centery,
   GLdouble centerz,
   GLdouble upx,
   GLdouble upy,
   GLdouble upz
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*eyex* 
</dt> <dd>

Posición del punto del ojo.

</dd> <dt>

*eyey* 
</dt> <dd>

Posición del punto del ojo.

</dd> <dt>

*Eyez* 
</dt> <dd>

Posición del punto del ojo.

</dd> <dt>

*centerx* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*central* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*centerz* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*Upx* 
</dt> <dd>

Dirección del vector hacia arriba.

</dd> <dt>

*upy* 
</dt> <dd>

Dirección del vector hacia arriba.

</dd> <dt>

*upz* 
</dt> <dd>

Dirección del vector hacia arriba.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluLookAt** crea una matriz de visualización derivada de un punto de vista, un punto de referencia que indica el centro de la escena y un vector hacia arriba. La matriz asigna el punto de referencia al eje Z negativo y el punto de los ojos al origen, de modo que cuando se usa una matriz de proyección típica, el centro de la escena se asigna al centro de la ventanilla. De forma similar, la dirección descrita por el vector hacia arriba proyectado en el plano de visualización se asigna al eje Y positivo para que apunta hacia arriba en la ventanilla. El vector hacia arriba no debe ser paralelo a la línea de visión desde el ojo hasta el punto de referencia.

La matriz generada **por gluLookAt** posmultiplica la matriz actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





