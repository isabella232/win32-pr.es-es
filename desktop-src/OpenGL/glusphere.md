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
ms.openlocfilehash: 590c4b7335fe0596c5b5b0f3dc709998fafc21f7be78f493a05f6520ed9fd368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488735"
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

## <a name="remarks"></a>Comentarios

La **función gluSphere** dibuja una esfera del radio dado centrada alrededor del origen. La esfera se subdivide alrededor del eje Z en segmentos y a lo largo del eje Z en pilas (similares a las líneas de longitud y latitud).

Si la orientación se establece en GLU \_ OUTSIDE (con **gluQuadricOrientation),** cualquier punto de normal generado lejos del centro de la esfera. De lo contrario, apuntan hacia el centro de la esfera.

Si texturing está activado (con **gluQuadricTexture):** las coordenadas de textura se generan para que *t* oscila entre 0,0 a *z* = -*radius* a 1,0 en el radio *z*(t aumenta linealmente a lo largo de las líneas de línea); y s oscila entre 0,0 en el eje  =   Y positivo, a 0,25 en el eje X positivo, a 0,5 en el eje Y negativo, a 0,75 en el eje X negativo y a 1,0 en el eje Y positivo. 

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

 

 





