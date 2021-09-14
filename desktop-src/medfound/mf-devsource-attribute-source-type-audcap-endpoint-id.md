---
description: Especifica el identificador de punto de conexión para un dispositivo de captura de audio.
ms.assetid: a0d8b54b-7a05-4307-a756-a34bb22f1afd
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ENDPOINT_ID atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1448dc753a8e3b8221fa040309d3f5b60c4879
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127364090"
---
# <a name="mf_devsource_attribute_source_type_audcap_endpoint_id-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ AUDCAP \_ ENDPOINT \_ ID

Especifica el identificador de punto de conexión para un dispositivo de captura de audio.

## <a name="data-type"></a>Tipo de datos

**WCHAR\***

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**a IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para establecer este atributo, llame [**a IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="remarks"></a>Observaciones

El valor del atributo es un identificador de punto de conexión. Este atributo se usa con las siguientes funciones:

-   Se puede usar como entrada para las funciones [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) y [**MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) En este contexto, el atributo especifica el dispositivo de captura de audio para la función. Puede obtener el identificador de punto de conexión de un dispositivo determinado llamando al [**método IMMDevice::GetId.**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) Consulte la documentación de Core Audio API para obtener más información.
-   Cuando la [**función MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) enumera los dispositivos de audio, los objetos de activación devueltos contienen este atributo. El objeto de activación utiliza internamente el atributo cuando crea el origen multimedia.

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de audio y vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 
