---
title: Función gluCylinder (Glu.h)
description: La función gluCylinder dibuja un cilindro.
ms.assetid: 43329d2f-50bb-46ea-85cb-22956d0df375
keywords:
- Función gluCylinder OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071493"
---
# <a name="glucylinder-function"></a>función gluCylinder

La **función gluCylinder** dibuja un cilindro.

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

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*baseRadius* 
</dt> <dd>

Radio del cilindro en *z* = 0.

</dd> <dt>

*topRadius* 
</dt> <dd>

Radio del cilindro a la *altura z.*  =  

</dd> <dt>

*height* 
</dt> <dd>

Alto del cilindro.

</dd> <dt>

*Rebanadas* 
</dt> <dd>

Número de subdivisiones alrededor del eje Z.

</dd> <dt>

*Pilas* 
</dt> <dd>

Número de subdivisiones a lo largo del eje Z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluCylinder** dibuja un cilindro orientado a lo largo del eje Z. La base del cilindro se coloca en *z* = 0 y la parte superior a *la altura*  =  *z*. Al igual que una esfera, un cilindro se subdivide alrededor del eje Z en segmentos y a lo largo del eje Z en pilas.

Tenga en cuenta *que si topRadius* está establecido en cero, esta rutina generará un cono.

Si la orientación se establece en GLU \_ OUTSIDE (con [**gluQuadricOrientation),**](gluquadricorientation.md)las normales generadas apuntan fuera del eje Z. De lo contrario, apuntan hacia el eje Z.

Si texturing está activado (con [**gluQuadricTexture):**](gluquadrictexture.md)las coordenadas de textura se generan para que *t* oscila linealmente entre 0,0 y *z* = 0 a 1,0 a la altura *z;* y s oscila entre 0,0 en el eje  =  Y positivo, a 0,25 en el eje X positivo, a 0,5 en el eje Y negativo, a 0,75 en el eje X negativo y a 1,0 en el eje Y positivo. 

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

 

 





