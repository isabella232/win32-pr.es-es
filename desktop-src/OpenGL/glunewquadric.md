---
title: Función gluNewQuadric (Glu.h)
description: La función gluNewQuadric crea un objeto cuádigo.
ms.assetid: 5a4289bf-b57a-4c74-b0e3-b7536671e4df
keywords:
- función gluNewQuadric OpenGL
topic_type:
- apiref
api_name:
- gluNewQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: affedc7dcebd2b7925449e22cc1b902e88d936f5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161074"
---
# <a name="glunewquadric-function"></a>función gluNewQuadric

La **función gluNewQuadric** crea un objeto cuádigo.

## <a name="syntax"></a>Sintaxis


```C++
GLUquadric* WINAPI gluNewQuadric(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="remarks"></a>Observaciones

La **función gluNewQuadric** crea y devuelve un puntero a un nuevo objeto cuádigo. Haga referencia a este objeto al llamar a funciones de representación y control cuádricas. Un valor devuelto de cero significa que no hay suficiente memoria para asignar al objeto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**gluCylinder**](glucylinder.md)
</dt> <dt>

[**gluDeleteQuadric**](gludeletequadric.md)
</dt> <dt>

[**gluDisk**](gludisk.md)
</dt> <dt>

[**gluPartialDisk**](glupartialdisk.md)
</dt> <dt>

[*gluQuadricCallback*](gluquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> <dt>

[**gluSphere**](glusphere.md)
</dt> </dl>

 

 





