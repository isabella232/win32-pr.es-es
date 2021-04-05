---
description: Generado por un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida. Este evento solo se aplica al contenido protegido.
ms.assetid: 0a13fc08-2bbe-46d8-a076-6165cca6ea36
title: Evento MEContentProtectionMessage (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4f96ac75711559881232ced4cec6bfca2bc030c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811036"
---
# <a name="mecontentprotectionmessage-event"></a>Evento MEContentProtectionMessage

Generado por un componente de canalización cuando cambia la configuración de uno de los esquemas de protección de salida. Este evento solo se aplica al contenido protegido.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE              | Descripción                           |
|----------------------|---------------------------------------|
| VT \_ vacío<br/> | Sin datos del evento.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Todas las salidas de confianza deben controlar este evento. Media Foundation transformaciones (MFTs) reciben este evento a través del método [**IMFTransform::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent) . Los receptores de medios reciben este evento a través del método [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) .

La salida de confianza debe aplicar los cambios de la Directiva o devolver el código de error MF \_ E \_ directiva \_ no compatible.

Los datos y atributos del evento dependen del sistema de protección de contenido en uso.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Vista \|\]<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 \|\]<br/>                                              |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




