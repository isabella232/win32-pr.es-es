---
title: función gluQuadricTexture (GLU. h)
description: La función gluQuadricTexture especifica si se va a aplicar textura a Quadrics.
ms.assetid: 11681497-f099-4856-a0ac-6a44abd3e1a1
keywords:
- gluQuadricTexture (función) OpenGL
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
ms.openlocfilehash: 0cc395564b6c6f30f38a8c5129c489d0bfca6b80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150702"
---
# <a name="gluquadrictexture-function"></a>gluQuadricTexture función)

La función **gluQuadricTexture** especifica si se va a aplicar textura a Quadrics.

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

El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*textureCoords* 
</dt> <dd>

Marca que indica si se van a generar coordenadas de textura. Los valores siguientes son válidos.



| Value                                                                                                                                          | Significado                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="GL_TRUE"></span><span id="gl_true"></span><dl> <dt>**GL \_ true**</dt> </dl>    | Generar coordenadas de textura.<br/>                                   |
| <span id="GL_FALSE"></span><span id="gl_false"></span><dl> <dt>**CONTABILIDAD \_ falsa**</dt> </dl> | No genere coordenadas de textura. Este es el valor predeterminado.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluQuadricTexture** especifica si las coordenadas de textura se generarán para Quadrics representadas con **quadObject**.

La forma en que se generan las coordenadas de textura depende de la quadric específica que se representa.

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

[**gluNewQuadric**](glunewquadric.md)
</dt> <dt>

[**gluQuadricDrawStyle**](gluquadricdrawstyle.md)
</dt> <dt>

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> </dl>

 

 





