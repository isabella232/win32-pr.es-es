---
description: Especifica el formato de salida de un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a05283f33fa3b3bf4b9e339b830c2ae6a948ea82
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105697953"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>Atributo \_ de \_ \_ tipo de medio de atributo MF DEVSOURCE \_

Especifica el formato de salida de un dispositivo.

## <a name="data-type"></a>Tipo de datos

**[**MFT \_ REGISTRAR \_ \_ información de tipo**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** almacenada como **byte \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame a [**IMFAttributes:: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Observaciones

Este atributo contiene un par de GUID: un tipo principal y un subtipo. Estos GUID describen el formato de salida predeterminado del dispositivo. Es posible que el dispositivo admita formatos de salida adicionales.

Por ejemplo, si un dispositivo de captura de vídeo genera vídeo RGB-32, el valor de este atributo es `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Este atributo es una sugerencia para la aplicación. Para obtener el formato de salida exacto, cree el origen de medios para el dispositivo y obtenga el descriptor de presentación del origen del medio.

Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                         |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




