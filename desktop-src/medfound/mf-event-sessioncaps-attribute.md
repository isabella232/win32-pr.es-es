---
description: Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.
ms.assetid: a78a3f3f-4ba1-41f3-b808-43f1e4975bb9
title: MF_EVENT_SESSIONCAPS atributo (mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af38d61f07bf038d1906d6f11e46fea63e800efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659855"
---
# <a name="mf_event_sessioncaps-attribute"></a>\_Atributo SESSIONCAPS de evento MF \_

Contiene marcas que definen las funciones de la sesión multimedia, basándose en la presentación actual.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

Este atributo contiene un or **bit a** bit de cero o más marcadores. Para obtener una lista de posibles marcas, vea [**IMFMediaSession:: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities).

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

 

 




