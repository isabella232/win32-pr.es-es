---
title: función gluSphere (GLU. h)
description: La función gluSphere dibuja una esfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- gluSphere (función) OpenGL
topic_type:
- apiref
api_name:
- gluSphere
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899ff4833c705aae34fdb7830c264fee91414116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491908"
---
# <a name="glusphere-function"></a>gluSphere función)

La función **gluSphere** dibuja una esfera.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluSphere(
   GLUquadric *qobj,
   GLdouble   radius,
   GLint      slices,
   GLint      stacks
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qobj* 
</dt> <dd>

El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*tórica* 
</dt> <dd>

Radio de la esfera.

</dd> <dt>

*segmento* 
</dt> <dd>

Número de subdivisiones alrededor del eje z (similar a las líneas de longitud).

</dd> <dt>

*pilas* 
</dt> <dd>

El número de subdivisiones a lo largo del eje z (similar a las líneas de la latitud).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluSphere** dibuja una esfera del radio determinado centrado alrededor del origen. La esfera se subdivide alrededor del eje z en segmentos y a lo largo del eje z en pilas (similar a las líneas de longitud y latitud).

Si la orientación se establece en GLU \_ fuera de (con **gluQuadricOrientation**), cualquier normal generado apunta fuera del centro de la esfera. De lo contrario, apuntan hacia el centro de la esfera.

Si la texturización está activada (con **gluQuadricTexture**): se generan coordenadas de textura para que *t* vaya de 0,0 a *z* =*-RADIUS* a 1,0 en radio *z*  =   (*t* aumenta linealmente a lo largo de las líneas longitudinales); y *s* van desde 0,0 en el eje y positivo hasta 0,25 en el eje x positivo, a 0,5 en el eje y negativo, a 0,75 en el eje x negativo y de nuevo a 1,0 en el eje y positivo.

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

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





