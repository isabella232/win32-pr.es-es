---
description: Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Marcas de redimensionamiento (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RESIZEF_STRETCH
- RESIZEF_CROP
- RESIZEF_PRESERVEASPECTRATIO
- RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 9e2ef2766f7f54fea4fad16fc26242a8c2ee08db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690711"
---
# <a name="resize-flags"></a>Cambiar el tamaño de las marcas

\[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | La imagen se ajusta para ajustarse al tamaño del marco de destino en ambas dimensiones, sin conservar la relación de aspecto.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ Recortar**</dt> <dt>1</dt> </dl>                                                                                   | No se cambia el tamaño de la imagen. Si la imagen es más pequeña que el marco de destino, el área circundante es negro. Si la imagen es mayor que el marco de destino, se recorta la imagen.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | Se cambia el tamaño de la imagen para ajustarse al marco de destino a lo largo de una dimensión, a la vez que se conserva la relación de aspecto. Si la relación entre el ancho y el alto de la imagen no coincide con la relación en el marco de destino, se crea una pantalla panorámica.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ noancha**</dt> <dt>3</dt> </dl> | Se cambia el tamaño de la imagen para rellenar todo el marco de destino al tiempo que se conserva la relación de aspecto. En lugar de crear una panorámica, este modo recorta la imagen, ya sea a lo largo de los lados o en la parte superior e inferior.<br/>                 |



## <a name="remarks"></a>Observaciones

En las siguientes imágenes se muestran los efectos de estas marcas.

![cambiar el tamaño de las marcas](images/stretch14.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




