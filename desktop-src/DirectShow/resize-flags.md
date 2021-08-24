---
description: Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.
ms.assetid: f740b732-ba05-4fda-aafb-ed04bc3efd33
title: Cambiar el tamaño de las marcas (Qedit.h)
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
ms.openlocfilehash: c38f4b1913eb7676832374e57e4d65e14dc87831c13f3cdb0de96edf9b83ebec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747115"
---
# <a name="resize-flags"></a>Cambiar el tamaño de las marcas

\[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

Estas marcas especifican cómo se representa un origen de vídeo si su tamaño no coincide con las dimensiones de salida.



| Constante o valor                                                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RESIZEF_STRETCH"></span><span id="resizef_stretch"></span><dl> <dt>**RESIZEF \_ STRETCH**</dt> <dt>0</dt> </dl>                                                                          | La imagen se ajusta para ajustarse al tamaño del marco de destino en ambas dimensiones, sin conservar la relación de aspecto.<br/>                                                                                                            |
| <span id="RESIZEF_CROP"></span><span id="resizef_crop"></span><dl> <dt>**RESIZEF \_ CROP**</dt> <dt>1</dt> </dl>                                                                                   | No se cambia el tamaño de la imagen. Si la imagen es menor que el marco de destino, el área circundante es negra. Si la imagen es mayor que el marco de destino, la imagen se recorta.<br/>                                             |
| <span id="RESIZEF_PRESERVEASPECTRATIO"></span><span id="resizef_preserveaspectratio"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO**</dt> <dt>2</dt> </dl>                                      | Se cambia el tamaño de la imagen para ajustarse al marco de destino a lo largo de una dimensión, a la vez que se conserva la relación de aspecto. Si la proporción de ancho a alto de la imagen no coincide con la relación del marco de destino, crea un cuadro de letras.<br/> |
| <span id="RESIZEF_PRESERVEASPECTRATIO_NOLETTERBOX"></span><span id="resizef_preserveaspectratio_noletterbox"></span><dl> <dt>**RESIZEF \_ PRESERVEASPECTRATIO \_ NOLETTERBOX**</dt> <dt>3</dt> </dl> | Se cambia el tamaño de la imagen para rellenar todo el marco de destino, a la vez que se conserva la relación de aspecto. En lugar de crear un cuadro de letras, este modo recorta la imagen, ya sea a lo largo de los lados o en la parte superior e inferior.<br/>                 |



## <a name="remarks"></a>Comentarios

Las imágenes siguientes muestran los efectos de estas marcas.

![marcas de cambio de tamaño](images/stretch14.png)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IAMTimelineSrc::GetStretchMode**](iamtimelinesrc-getstretchmode.md)
</dt> <dt>

[**IAMTimelineSrc::SetStretchMode**](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 




