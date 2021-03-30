---
title: función gluDisk (GLU. h)
description: La función gluDisk dibuja un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- gluDisk (función) OpenGL
topic_type:
- apiref
api_name:
- gluDisk
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9a9e8b547790049c93360f060e944aafcea4511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079340"
---
# <a name="gludisk-function"></a>gluDisk función)

La función **gluDisk** dibuja un disco.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluDisk(
   GLUquadric *qobj,
   GLdouble   innerRadius,
   GLdouble   outerRadius,
   GLint      slices,
   GLint      loops
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*qobj* 
</dt> <dd>

El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*innerRadius* 
</dt> <dd>

El radio interno del disco (puede ser cero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Radio exterior del disco.

</dd> <dt>

*segmento* 
</dt> <dd>

Número de subdivisiones alrededor del eje z.

</dd> <dt>

*bucles* 
</dt> <dd>

El número de anillos concéntricos sobre el origen en el que se subdivide el disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluDisk** representa un disco en el plano *z* = 0. El disco tiene un radio de *outerRadius* y contiene un orificio circular concéntrico con un radio de *innerRadius*. Si *innerRadius* es 0, no se genera ningún hueco. El disco se subdivide alrededor del eje z en segmentos (por ejemplo, segmentos de pizza) y también sobre el eje z en anillos (como se especifica en *segmentos* y *bucles*, respectivamente).

Con respecto a la orientación, se considera que el lado *z* positivo del disco está *fuera* de (vea [**gluQuadricOrientation**](gluquadricorientation.md)). Esto significa que si la orientación se establece en GLU \_ fuera de, cualquier punto normal generado a lo largo del eje z positivo.

Si la texturización está activada (con [**gluQuadricTexture**](gluquadrictexture.md)), las coordenadas de textura se generan de forma lineal , de modo que  =  *outerRadius* de r, el valor de (*r*, 0,0) es (1, 0,5); en (0, *r*, 0) es (0,5, 1); en (-*r*, 0,0) es (0, 0,5) y en (0,-*r*, 0) es (0,5, 0).

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

 

 





