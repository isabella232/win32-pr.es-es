---
description: Generado por un origen multimedia cuando cambian las características de los orígenes.
ms.assetid: df7bb9a3-5949-4a4a-8835-c5b1d01b5cb3
title: Evento MESourceCharacteristicsChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 659e9eea0352d131aac4959b2952e8426ae408a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715659"
---
# <a name="mesourcecharacteristicschanged-event"></a>Evento MESourceCharacteristicsChanged

Generado por un origen multimedia cuando cambian las características del origen.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Para este evento, se definen los atributos siguientes.



| Atributo                                                                                                   | Descripción                                                          |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_características del \_ origen de eventos MF \_**](mf-event-source-characteristics-attribute.md)<br/>          | Nuevas características del origen multimedia.<br/> <br/>      |
| [**\_características de origen de eventos MF \_ \_ \_ anteriores**](mf-event-source-characteristics-old-attribute.md)<br/> | Características anteriores del origen multimedia.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




