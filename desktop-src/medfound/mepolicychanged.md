---
description: Lo genera un componente de canalización cuando cambia la directiva de salida de la secuencia. Este evento solo se aplica al contenido protegido.
ms.assetid: 9dc78dc6-3fc2-4a81-ad41-45ff3fdbdade
title: Evento MEPolicyChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac87d3dae63b20d19c91f0fdef5471060753152901d9096b1be315cd76e9974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957415"
---
# <a name="mepolicychanged-event"></a>Evento MEPolicyChanged

Lo genera un componente de canalización cuando cambia la directiva de salida de la secuencia. Este evento solo se aplica al contenido protegido.

## <a name="event-values"></a>Valores de evento

Entre los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) se incluyen los siguientes.



| VARTYPE                | Descripción                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Puntero a la [**interfaz IMFOutputPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputpolicy) de la nueva directiva para la secuencia.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Todas las salidas de confianza deben controlar este evento. Media Foundation transformaciones (MFT) reciben este evento a través del método [**MFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Los receptores multimedia reciben este evento a través del [**método IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

La salida de confianza debe aplicar la nueva directiva o devolver el código de error MF \_ E \_ POLICY \_ UNSUPPORTED.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                                              |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




