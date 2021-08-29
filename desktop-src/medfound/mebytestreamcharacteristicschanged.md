---
description: Enviado por una secuencia de bytes cuando las características de la secuencia de bytes han cambiado.
ms.assetid: EC34A7A3-BF01-4F9E-BA79-131B76D4C58F
title: Evento MEByteStreamCharacteristicsChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1401f420bf1c40a5449a91e2af9a6e1c328ea6591ee3b8eeacedd34213eab4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941765"
---
# <a name="mebytestreamcharacteristicschanged-event"></a>Evento MEByteStreamCharacteristicsChanged

Enviado por una secuencia de bytes cuando las características de la secuencia de bytes han cambiado.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE               | Descripción                           |
|-----------------------|---------------------------------------|
| VT \_ EMPTY <br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Este evento indica que una o varias de las características siguientes han cambiado:

-   Marcas de funcionalidad ([**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities))
-   Marca de fin de flujo ([**IMFByteStream::IsEndOfStream**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-isendofstream))
-   Length ([**IMFByteStream::GetLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getlength))

No todas las [**implementaciones de IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) admiten este evento. Para recibir el evento, consulte el objeto byte-stream para la [**interfaz BYTEMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                               |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




