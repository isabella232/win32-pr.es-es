---
title: Función gluQuadricDrawStyle (Glu.h)
description: La función gluQuadricDrawStyle especifica el estilo de dibujo deseado para los cuádigos.
ms.assetid: 30f6da40-9306-46bb-a815-f51722e57e18
keywords:
- Función GluQuadricDrawStyle OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244899"
---
# <a name="gluquadricdrawstyle-function"></a>Función gluQuadricDrawStyle

La **función gluQuadricDrawStyle** especifica el estilo de dibujo deseado para los cuádigos.

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

Objeto cuádigo (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> <dt>

*drawStyle* 
</dt> <dd>

Estilo de dibujo deseado. Los valores siguientes son válidos.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_FILL"></span><span id="glu_fill"></span><dl> <dt>**GLU \_ FILL**</dt> </dl>                   | Los cuádigos se representan con primitivas de polígono. Los polígonos se dibujan en sentido contrario a las agujas del reloj con respecto a sus normales (como se define con [**gluQuadricOrientation).**](gluquadricorientation.md)<br/> |
| <span id="GLU_LINE"></span><span id="glu_line"></span><dl> <dt>**LÍNEA \_ DE GLU**</dt> </dl>                   | Los cuádigos se representan como un conjunto de líneas.<br/>                                                                                                                                                                    |
| <span id="GLU_SILHOUETTE"></span><span id="glu_silhouette"></span><dl> <dt>**GLU \_ LO QUE SE VA A HACER**</dt> </dl> | Los cuádigos se representan como un conjunto de líneas, salvo que no se dibujarán los bordes que separan las caras coplanares.<br/>                                                                                                     |
| <span id="GLU_POINT"></span><span id="glu_point"></span><dl> <dt>**GLU \_ POINT**</dt> </dl>                | Los cuádigos se representan como un conjunto de puntos.<br/>                                                                                                                                                                   |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluQuadricDrawStyle** especifica el estilo de dibujo para los cuádigos representados con **quadObject**.

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

[**gluQuadricNormals**](gluquadricnormals.md)
</dt> <dt>

[**gluQuadricOrientation**](gluquadricorientation.md)
</dt> <dt>

[**gluQuadricTexture**](gluquadrictexture.md)
</dt> </dl>

 

 





