---
title: Función gluSphere (Glu.h)
description: La función gluSphere dibuja una esfera.
ms.assetid: 0f1919c6-0551-4d50-b782-767dacc088cb
keywords:
- Función gluSphere OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476698"
---
# <a name="glusphere-function"></a>función gluSphere

La **función gluSphere** dibuja una esfera.

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

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Radio* 
</dt> <dd>

Radio de la esfera.

</dd> <dt>

*Rebanadas* 
</dt> <dd>

Número de subdivisiones alrededor del eje Z (similar a las líneas de longitud).

</dd> <dt>

*Pilas* 
</dt> <dd>

Número de subdivisiones a lo largo del eje Z (similar a las líneas de latitud).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluSphere** dibuja una esfera del radio dado centrada alrededor del origen. La esfera se subdivide alrededor del eje z en segmentos y a lo largo del eje Z en pilas (similares a las líneas de longitud y latitud).

Si la orientación se establece en GLU \_ OUTSIDE (con **gluQuadricOrientation),** cualquier punto de normal generado lejos del centro de la esfera. De lo contrario, apuntan hacia el centro de la esfera.

Si texturing está activado (con **gluQuadricTexture):** las coordenadas de textura se generan para que *t* oscila entre 0,0 en *z* =*-* radius a 1,0 en el radio *z*(t aumenta linealmente a lo largo de las líneas de línea); y s oscila entre 0,0 en el eje  =   Y positivo, a 0,25 en el eje X positivo, a 0,5 en el eje Y negativo, a 0,75 en el eje X negativo y a 1,0 en el eje Y positivo. 

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

 

 





