---
title: Función gluQuadricTexture (Glu.h)
description: La función gluQuadricTexture especifica si se van a texturar los cuádigos.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- Función GluQuadricTexture OpenGL
topic_type:
- apiref
api_name:
- gluQuadricTexture
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbde88e0a878fd59e01ad0a450cf4cbe9831c4ad867c8029373586a8efe830eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937486"
---
# <a name="gluquadrictexture-function"></a>Función gluQuadricTexture

La **función gluQuadricTexture** especifica si se van a texturar los cuádigos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluQuadricTexture(
   GLUquadric *quadObject,
   GLboolean  textureCoords
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*quadObject* 
</dt> <dd>

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*textureCoords* 
</dt> <dd>

Marca que indica si se van a generar coordenadas de textura. Los valores siguientes son válidos.



| Value                                                                                                                                          | Significado                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ TRUE**</dt> </dl>    | Generar coordenadas de textura.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**GL \_ FALSE**</dt> </dl> | No genere coordenadas de textura. Este es el valor predeterminado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluQuadricTexture** especifica si se van a generar coordenadas de textura para los cuádigos representados con **quadObject**.

La manera en que se generan las coordenadas de textura depende del cuádigo específico representado.

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

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> </dl>

 

 





