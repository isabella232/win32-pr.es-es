---
description: Especifica el rol de dispositivo para un dispositivo de captura de audio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148ae6697151698eef58d3c0148de3ed81822a05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082350"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>Tipo de origen de atributo MF DEVSOURCE atributo de \_ \_ \_ \_ \_ \_ rol AUDCAP

Especifica el rol de dispositivo para un dispositivo de captura de audio.

## <a name="data-type"></a>Tipo de datos

**ERole** almacenado como **UINT32**

## <a name="getset"></a>Obtener o establecer

Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Observaciones

El tipo de enumeración **eRole** se documenta en la documentación básica de la API de audio.

El valor del atributo especifica un rol de dispositivo. Este atributo se utiliza con las siguientes funciones.

Este atributo se puede usar como entrada para las funciones [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) y [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Si se especifica el atributo, la función crea un origen de medios que usa el dispositivo de captura de audio predeterminado para el rol de dispositivo especificado.

Este atributo también se puede usar como entrada para la función [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Si se especifica el atributo, la enumeración se restringe al rol de dispositivo especificado. Además, cada objeto de activación devuelto por la función **MFEnumDeviceSources** contiene este atributo. El objeto de activación usa el atributo internamente al crear el origen de medios.

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

 

 




