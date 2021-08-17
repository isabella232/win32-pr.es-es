---
description: Especifica el formato de salida de un dispositivo.
ms.assetid: 33a1b546-ece2-44ef-a1c0-5579c32be0bc
title: MF_DEVSOURCE_ATTRIBUTE_MEDIA_TYPE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb4685f419658ecf77782a4cef770fd205119bb6cfd95523edb7fbbe001fd700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105041"
---
# <a name="mf_devsource_attribute_media_type-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE \_ MEDIA \_ TYPE

Especifica el formato de salida de un dispositivo.

## <a name="data-type"></a>Tipo de datos

**[**MFT \_ REGISTER \_ TYPE \_ INFO almacenado**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info)** como **BYTE \[ \]**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

Para establecer este atributo, llame [**a IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).

## <a name="remarks"></a>Comentarios

Este atributo contiene un par de GUID: un tipo principal y un subtipo. Estos GUID describen el formato de salida predeterminado del dispositivo. El dispositivo puede admitir formatos de salida adicionales.

Por ejemplo, si un dispositivo de captura de vídeo genera vídeo RGB-32, el valor de este atributo es `{ MFMediaType_Video, MFVideoFormat_RGB32 }` .

Este atributo es una sugerencia para la aplicación. Para obtener el formato de salida exacto, cree el origen multimedia del dispositivo y obtenga el descriptor de presentación del origen multimedia.

Este atributo se establece en los objetos de activación devueltos por las siguientes funciones:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




