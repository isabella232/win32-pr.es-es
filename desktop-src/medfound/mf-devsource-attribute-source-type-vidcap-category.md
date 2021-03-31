---
description: Especifica la categoría de dispositivos para un dispositivo de captura de vídeo.
ms.assetid: 008ff9df-ebe0-4efd-a62c-24f4a4239ebd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_CATEGORY atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc65af267df38486f6ad7859d16aff4de5973a27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154632"
---
# <a name="mf_devsource_attribute_source_type_vidcap_category-attribute"></a>\_Tipo de origen de atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ categoría VIDCAP

Especifica la categoría de dispositivos para un dispositivo de captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**GUID**

Se define el siguiente valor.



| Value                                                                                                                                                                                                                                                             | Significado                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="CLSID_VideoInputDeviceCategory"></span><span id="clsid_videoinputdevicecategory"></span><span id="CLSID_VIDEOINPUTDEVICECATEGORY"></span><dl> <dt>**CLSID \_ VideoInputDeviceCategory**</dt> </dl> | Dispositivo de captura de vídeo.<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame a [**IMFAttributes:: SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Observaciones

Use este atributo como entrada de la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) al enumerar los dispositivos de captura de vídeo.

Además, este atributo se establece en los objetos de activación devueltos por las siguientes funciones:

-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

El atributo solo se aplica a los dispositivos de captura de vídeo.

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

 

 




