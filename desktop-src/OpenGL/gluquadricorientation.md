---
title: Función gluQuadricOrientation (Glu.h)
description: La función gluQuadricOrientation especifica la orientación interna o externa de los cuádigos.
ms.assetid: 4e3fc6d3-5a39-455b-bd24-8eb497333096
keywords:
- Función GluQuadricOrientation OpenGL
topic_type:
- apiref
api_name:
- gluQuadricOrientation
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baa02c3b6d207cbcc2bf487f51c0e96dc2f2dd98748edc81efb58ac957fac4ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937631"
---
# <a name="gluquadricorientation-function"></a>función gluQuadricOrientation

La **función gluQuadricOrientation** especifica la orientación interna o externa de los cuádigos.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluQuadricOrientation(
   GLUquadric *quadObject,
   GLenum     orientation
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*quadObject* 
</dt> <dd>

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*Orientación* 
</dt> <dd>

Orientación deseada. Los valores siguientes son válidos.



| Value                                                                                                                                                   | Significado                                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="GLU_OUTSIDE"></span><span id="glu_outside"></span><dl> <dt>**GLU \_ OUTSIDE**</dt> </dl> | Dibuje cuádigos con normales que apunten hacia fuera. Este es el valor predeterminado.<br/> |
| <span id="GLU_INSIDE"></span><span id="glu_inside"></span><dl> <dt>**GLU \_ INSIDE**</dt> </dl>    | Dibuje cuádigos con normales que apuntan hacia dentro.<br/>                             |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluQuadricOrientation** especifica qué tipo de orientación se desea para los cuádigos representados con **quadObject**. La interpretación de hacia fuera y hacia dentro depende del cuádigo que se dibuja.

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
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





