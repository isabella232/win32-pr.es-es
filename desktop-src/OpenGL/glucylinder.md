---
title: función gluCylinder (GLU. h)
description: La función gluCylinder dibuja un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- gluCylinder (función) OpenGL
topic_type:
- apiref
api_name:
- gluCylinder
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fd201d1ddd720501715d1ead08d94bab72f7b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666031"
---
# <a name="glucylinder-function"></a>gluCylinder función)

La función **gluCylinder** dibuja un cilindro.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluCylinder(
   GLUquadric *qobj,
   GLdouble   baseRadius,
   GLdouble   topRadius,
   GLdouble   height,
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

*baseRadius* 
</dt> <dd>

Radio del cilindro en *z* = 0.

</dd> <dt>

*Radio* 
</dt> <dd>

Radio del cilindro en el alto de *z*  =  .

</dd> <dt>

*height* 
</dt> <dd>

Alto del cilindro.

</dd> <dt>

*segmento* 
</dt> <dd>

Número de subdivisiones alrededor del eje z.

</dd> <dt>

*pilas* 
</dt> <dd>

Número de subdivisiones a lo largo del eje z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluCylinder** dibuja un cilindro orientado a lo largo del eje z. La base del cilindro se coloca en *z* = 0 y la parte superior en la   =  *altura* z. Al igual que una esfera, un cilindro se subdivide alrededor del eje z en segmentos y a lo largo del eje z en pilas.

Tenga en cuenta que si el valor de *RADIUS* es cero, esta rutina generará un cono.

Si la orientación se establece en GLU \_ fuera de (con [**gluQuadricOrientation**](gluquadricorientation.md)), cualquier normal generado apunta al eje z. De lo contrario, apuntan hacia el eje z.

Si la texturización está activada (con [**gluQuadricTexture**](gluquadrictexture.md)): se generan coordenadas de textura para que *t* se rango linealmente de 0,0 a *z* = 0 a 1,0 a  =  *altura* z; y *s* va de 0,0 en el eje y positivo, a 0,25 en el eje x positivo, a 0,5 en el eje y positivo, a 0,75 en el eje x negativo y de nuevo a 1,0 en el eje y positivo.

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

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





