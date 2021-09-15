---
description: Especifica el rol de dispositivo para un dispositivo de captura de audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474211"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>Atributo MF \_ DEVSOURCE \_ ATTRIBUTE SOURCE TYPE \_ \_ \_ AUDCAP \_ ROLE

Especifica el rol de dispositivo para un dispositivo de captura de audio.

## <a name="data-type"></a>Tipo de datos

**ERole** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame [**aATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

El **tipo de enumeración eRole** se documenta en la documentación de Core Audio API.

El valor del atributo especifica un rol de dispositivo. Este atributo se usa con las siguientes funciones.

Este atributo se puede usar como entrada para las funciones [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) y [**MFCreateDeviceSourceActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) Si se especifica el atributo , la función crea un origen multimedia que usa el dispositivo de captura de audio predeterminado para el rol de dispositivo especificado.

Este atributo también se puede usar como entrada para la [**función MFEnumDeviceSources.**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) Si se especifica el atributo , la enumeración está restringida al rol de dispositivo especificado. Además, cada objeto de activación devuelto por la **función MFEnumDeviceSources** contiene este atributo. A continuación, el objeto de activación usa internamente el atributo cuando crea el origen multimedia.

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

 

 




