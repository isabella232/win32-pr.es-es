---
title: función gluLookAt (GLU. h)
description: La función gluLookAt define una transformación de visualización.
ms.assetid: 1fd87701-19c2-49b9-99ac-10e70aaedbfd
keywords:
- gluLookAt (función) OpenGL
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
ms.openlocfilehash: 5866f3c06ef6969c95eeef4b23fff7a4e7852eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905651"
---
# <a name="glulookat-function"></a>gluLookAt función)

La función **gluLookAt** define una transformación de visualización.

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

Posición del punto de ojo.

</dd> <dt>

*eyey* 
</dt> <dd>

Posición del punto de ojo.

</dd> <dt>

*eyez* 
</dt> <dd>

Posición del punto de ojo.

</dd> <dt>

*CenterX* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*CenterY* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*centerz* 
</dt> <dd>

Posición del punto de referencia.

</dd> <dt>

*UPX* 
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

## <a name="remarks"></a>Observaciones

La función **gluLookAt** crea una matriz de visualización derivada de un punto de vista, un punto de referencia que indica el centro de la escena y un vector hacia arriba. La matriz asigna el punto de referencia al eje z negativo y el punto de mira al origen, de modo que cuando se usa una matriz de proyección típica, el centro de la escena se asigna al centro de la ventanilla. Del mismo modo, la dirección que describe el vector hacia arriba proyectado en el plano de visualización se asigna al eje y positivo para que apunte hacia arriba en la ventanilla. El vector hacia arriba no debe ser paralelo a la línea de visión desde el ojo hasta el punto de referencia.

La matriz generada por **gluLookAt** postmultiplica la matriz actual.

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

[**glFrustum**](glfrustum.md)
</dt> <dt>

[**gluPerspective**](gluperspective.md)
</dt> </dl>

 

 





