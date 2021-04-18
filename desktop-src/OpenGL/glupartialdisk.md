---
title: función gluPartialDisk (GLU. h)
description: La función gluPartialDisk dibuja un arco de un disco.
ms.assetid: 46809c15-88c3-40fa-965a-7aeeedc1c598
keywords:
- gluPartialDisk (función) OpenGL
topic_type:
- apiref
api_name:
- gluPartialDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36e35a6ea905f20e1cb30eddc5b270786614403b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665915"
---
# <a name="glupartialdisk-function"></a>gluPartialDisk función)

La función **gluPartialDisk** dibuja un arco de un disco.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluPartialDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops,
   GLdouble   startAngle,
   GLdouble   sweepAngle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qobj* 
</dt> <dd>

Objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

Radio interior del disco parcial (puede ser cero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Radio exterior del disco parcial.

</dd> <dt>

*segmento* 
</dt> <dd>

Número de subdivisiones alrededor del eje z.

</dd> <dt>

*bucles* 
</dt> <dd>

El número de anillos concéntricos sobre el origen en el que se subdivide el disco parcial.

</dd> <dt>

*startAngle* 
</dt> <dd>

Ángulo inicial, en grados, de la parte del disco.

</dd> <dt>

*sweepAngle* 
</dt> <dd>

Ángulo de barrido, en grados, de la parte del disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluPartialDisk** representa un disco parcial en el plano *z* = 0. Un disco parcial es similar a un disco completo, excepto en que solo se incluye el subconjunto del *disco desde la* entrada de la misma a la   +  *sweepAngle* (donde 0 grados se encuentra a lo largo del eje y positivo, 90 grados está a lo largo del eje x positivo, 180 grados se encuentra a lo largo del 270 eje y de la x negativo).

El disco parcial tiene un radio de *outerRadius* y contiene un orificio circular concéntrico con un radio de *innerRadius*. Si *innerRadius* es cero, no se genera ningún hueco. El disco parcial se divide por el eje z en segmentos (por ejemplo, segmentos de pizza) y también sobre el eje z en anillos (como se especifica en *segmentos* y *bucles*, respectivamente).

Con respecto a la orientación, se considera que el lado z positivo del disco parcial está fuera (vea [**gluQuadricOrientation**](gluquadricorientation.md)). Esto significa que si la orientación se establece en GLU \_ fuera de, cualquier punto normal generado a lo largo del eje z positivo.

Si ha activado la texturización (con [**gluQuadricTexture**](gluquadrictexture.md)), **gluPartialDisk** genera coordenadas de textura de forma lineal, de modo que, donde *r*  =  *outerRadius*, el valor de (*r*, 0,0) es (1, 0,5); en (0, *r*, 0) es (0,5, 1); en (*r*, 0, 0) es (0, 0,5) y en (0, *r*, 0) es (0,5, 0).

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

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





