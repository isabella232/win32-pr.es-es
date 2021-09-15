---
description: Lo genera un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida. Este evento solo se aplica al contenido protegido.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579949"
---
# <a name="mecontentprotectionmessage-event"></a>Evento MEContentProtectionMessage

Lo genera un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida. Este evento solo se aplica al contenido protegido.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ EMPTY<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Todas las salidas de confianza deben controlar este evento. Media Foundation transformaciones (MFT) reciben este evento a través del método [**MFTransform::P rocessEvent.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) Los receptores multimedia reciben este evento a través del [**método IMFStreamSink::P laceMarker.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)

La salida de confianza debe aplicar los cambios de directiva o devolver el código de error MF \_ E \_ POLICY \_ UNSUPPORTED.

Los datos y atributos del evento dependen del sistema de protección de contenido en uso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Aplicaciones de escritorio de Vista \[ \| para aplicaciones para UWP\]<br/>                                                    |
| Servidor mínimo compatible<br/> | Windows Aplicaciones de escritorio de Server 2008 \[ \| para aplicaciones para UWP\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




