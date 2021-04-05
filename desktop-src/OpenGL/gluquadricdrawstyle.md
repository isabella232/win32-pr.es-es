---
title: función gluQuadricDrawStyle (GLU. h)
description: La función gluQuadricDrawStyle especifica el estilo de dibujo deseado para Quadrics.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- gluQuadricDrawStyle (función) OpenGL
topic_type:
- apiref
api_name:
- gluQuadricDrawStyle
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8a1b44b7894ea9762b450c5a5d6c2b022c5e02f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996773"
---
# <a name="gluquadricdrawstyle-function"></a>gluQuadricDrawStyle función)

La función **gluQuadricDrawStyle** especifica el estilo de dibujo deseado para Quadrics.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluQuadricDrawStyle(
   GLUquadric *quadObject,
   GLenum     drawStyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*quadObject* 
</dt> <dd>

El objeto quadric (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> <dt>

*drawStyle* 
</dt> <dd>

Estilo de dibujo deseado. Los valores siguientes son válidos.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**relleno de GLU \_**</dt> </dl>                   | Quadrics se representan con primitivas de polígonos. Los polígonos se dibujan en sentido contrario a las agujas del reloj con respecto a sus normales (como se define con [**gluQuadricOrientation**](gluquadricorientation.md)).<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**\_línea Glu**</dt> </dl>                   | Quadrics se representan como un conjunto de líneas.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**\_silueta Glu**</dt> </dl> | Quadrics se representan como un conjunto de líneas, con la excepción de que los bordes que separan las caras coplanaras no se dibujarán.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**\_punto Glu**</dt> </dl>                | Quadrics se representan como un conjunto de puntos.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluQuadricDrawStyle** especifica el estilo de dibujo de Quadrics representado con **quadObject**.

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

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





