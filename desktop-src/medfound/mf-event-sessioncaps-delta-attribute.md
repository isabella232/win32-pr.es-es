---
description: Contiene marcas que indican qué funcionalidades han cambiado en la sesión multimedia, en función de la presentación actual.
ms.assetid: aa01d17f-f2ac-4504-b278-3edd90ab8a23
title: MF_EVENT_SESSIONCAPS_DELTA atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a2e227e5608296a9b30fa2fc68f37215d687349516367d8689b20825e1ed4e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119714854"
---
# <a name="mf_event_sessioncaps_delta-attribute"></a>Atributo MF \_ EVENT \_ SESSIONCAPS \_ DELTA

Contiene marcas que indican qué funcionalidades han cambiado en la sesión multimedia, en función de la presentación actual.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

Este atributo contiene una máscara de bits que indica qué marcas de funcionalidad han cambiado. Para obtener una lista de las marcas posibles, vea [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities). Los bits se establecen en 1 en la máscara de bits por cualquiera de los siguientes motivos:

-   El bit de funcionalidades correspondiente cambió de 0 a 1.
-   El bit de funcionalidades correspondiente cambió de 1 a 0.
-   El bit de funcionalidades correspondiente sigue siendo 1, pero los detalles de la funcionalidad han cambiado. Por ejemplo, ha cambiado la velocidad de reproducción máxima.

Este atributo se usa con el [evento MESessionCapabilitiesChanged.](mesessioncapabilitieschanged.md)

La constante GUID para este atributo se exporta desde mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de eventos](event-attributes.md)
</dt> <dt>

[**ATTRIBUTEAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> </dl>

 

 




