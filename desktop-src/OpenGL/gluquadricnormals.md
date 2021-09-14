---
title: Función gluQuadricNormals (Glu.h)
description: La función gluQuadricNormals especifica qué tipo de normales se van a usar para los cuádigos.
ms.assetid: 945759ec-ed4a-480f-8243-49fc785867c1
keywords:
- Función gluQuadricNormals OpenGL
topic_type:
- apiref
api_name:
- gluQuadricNormals
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11f9d8cd1884d7a5d1bc4cd03797517ba484126
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244904"
---
# <a name="gluquadricnormals-function"></a>función gluQuadricNormals

La **función gluQuadricNormals** especifica qué tipo de normales se van a usar para los cuádigos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluQuadricNormals(
   GLUquadric *quadObject,
   GLenum     normals
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*quadObject* 
</dt> <dd>

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Normales* 
</dt> <dd>

Tipo deseado de normales. Los valores siguientes son válidos.



| Value                                                                                                                                                | Significado                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="GLU_NONE"></span><span id="glu_none"></span><dl> <dt>**GLU \_ NONE**</dt> </dl>       | No se generan normales.<br/>                                                         |
| <span id="GLU_FLAT"></span><span id="glu_flat"></span><dl> <dt>**GLU \_ FLAT**</dt> </dl>       | Se genera una normal para cada faceta de un cuádigo.<br/>                             |
| <span id="GLU_SMOOTH"></span><span id="glu_smooth"></span><dl> <dt>**GLU \_ SMOOTH**</dt> </dl> | Se genera una normal para cada vértice de un cuádigo. Este es el valor predeterminado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluQuadricNormals** especifica qué tipo de normales se van a usar para los cuádigos representados **con quadObject**.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





