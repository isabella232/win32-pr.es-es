---
description: Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284a31a8d3fc661c15e7de991972455468efbd40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423800"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>\_ \_ Atributo Delta SESSIONCAPS de evento MF \_

Contiene marcas que indican qué capacidades han cambiado en la sesión multimedia, en función de la presentación actual.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo contiene una máscara de máscara que indica qué marcas de capacidades han cambiado. Para obtener una lista de posibles marcas, vea [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Los bits se establecen en 1 en la máscara de bits por cualquiera de los siguientes motivos:

-   El bit de funcionalidad correspondiente cambió de 0 a 1.
-   El bit de funcionalidad correspondiente cambió de 1 a 0.
-   El bit de funcionalidad correspondiente seguía siendo 1, pero los detalles de la funcionalidad cambiaron. Por ejemplo, la velocidad de reproducción máxima ha cambiado.

Este atributo se usa con el evento [MESessionCapabilitiesChanged](mesessioncapabilitieschanged.md) .

La constante GUID para este atributo se exporta desde mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                     |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




