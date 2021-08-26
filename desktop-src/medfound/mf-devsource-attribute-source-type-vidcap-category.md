---
description: Especifica la categoría de dispositivo para un dispositivo de captura de vídeo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140a9055bdc8081d5cdea1931b199dcd00f537e73051f30790f036be4af57fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060795"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>Atributo MF \_ DEVSOURCE \_ SOURCE \_ TYPE \_ \_ VIDCAP \_ CATEGORY

Especifica la categoría de dispositivo para un dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**GUID**

Se define el siguiente valor.



| Value                                                                                                                                                                                                                                                             | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**CLSID \_ VideoInputDeviceCategory**</dt> </dl> | Dispositivo de captura de vídeo.<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Comentarios

Use este atributo como entrada para la [**función MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) al enumerar los dispositivos de captura de vídeo.

Además, este atributo se establece en los objetos de activación devueltos por las siguientes funciones:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

El atributo solo se aplica a los dispositivos de captura de vídeo.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




