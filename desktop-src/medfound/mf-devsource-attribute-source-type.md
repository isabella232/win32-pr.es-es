---
description: Especifica un tipo de dispositivo, como la captura de audio o la captura de vídeo.
ms.assetid: c6c05267-1c93-48e2-b463-b5a1514f1b7b
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3445c74b1a77472bad564f6988f9ae2f4696fef7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474199"
---
# <a name="mf_devsource_attribute_source_type-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE

Especifica el tipo de dispositivo, como la captura de audio o la captura de vídeo.

## <a name="data-type"></a>Tipo de datos

**GUID**

Para este atributo se definen los valores siguientes:



| Value                                                                                                                                                                                                                                                                 | Significado                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------|
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_audcap_guid"></span><dl> <dt>**MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE \_ AUDCAP \_ GUID**</dt> </dl> | Dispositivo de captura de audio.<br/> |
| <span id="MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_GUID"></span><span id="mf_devsource_attribute_source_type_vidcap_guid"></span><dl> <dt>**MF \_ DEVSOURCE \_ ATTRIBUTE \_ SOURCE \_ TYPE \_ VIDCAP \_ GUID**</dt> </dl> | Dispositivo de captura de vídeo.<br/> |



 

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid).

Para establecer este atributo, llame [**a IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).

## <a name="remarks"></a>Observaciones

Use este atributo como entrada para las siguientes funciones:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

Además, este atributo se establece en los objetos de activación devueltos por la [**función MFEnumDeviceSources.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                         |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




