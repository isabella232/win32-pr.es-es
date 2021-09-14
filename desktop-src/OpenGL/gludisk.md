---
title: Función gluDisk (Glu.h)
description: La función gluDisk dibuja un disco.
ms.assetid: c9260621-930d-47dd-a046-30895779473b
keywords:
- Función gluDisk OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071486"
---
# <a name="gludisk-function"></a>función gluDisk

La **función gluDisk** dibuja un disco.

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

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*innerRadius* 
</dt> <dd>

Radio interno del disco (puede ser cero).

</dd> <dt>

*outerRadius* 
</dt> <dd>

Radio exterior del disco.

</dd> <dt>

*Rebanadas* 
</dt> <dd>

Número de subdivisiones alrededor del eje Z.

</dd> <dt>

*Bucles* 
</dt> <dd>

Número de anillos concéntricas sobre el origen en el que se subdivide el disco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluDisk** representa un disco en el *plano z* = 0. El disco tiene un radio de *rado* externo y contiene un hueco circular concéntrica con un radio *de innerRadius*. Si *innerRadius* es 0, no se genera ningún hueco. El disco se subdivide alrededor del eje Z en segmentos (como los segmentos de pizza) y también sobre el eje z en anillos (como se especifica en *segmentos* y *bucles*, respectivamente).

Con respecto a la orientación, se considera que el lado *positivo z* del disco está fuera *(vea* [**gluQuadricOrientation).**](gluquadricorientation.md) Esto significa que si la orientación se establece en GLU OUTSIDE, cualquier punto normal generado a lo \_ largo del eje Z positivo.

Si texturing está activado (con [**gluQuadricTexture),**](gluquadrictexture.md)las coordenadas de textura se generan linealmente de forma que donde *r* outerRadius , el valor  =  en (*r*, 0, 0) es (1, 0,5); en (0, *r*, 0) es (0,5, 1); en (-*r*, 0, 0) es (0, 0,5); y en (0, -*r*, 0) es (0,5, 0).

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

 

 





