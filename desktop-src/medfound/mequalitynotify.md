---
description: Proporciona comentarios al administrador de calidad sobre la calidad de la reproducción.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d8f486bfebfd137ba341176af0fdad257776df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544387"
---
# <a name="mequalitynotify-event"></a>Evento MEQualityNotify

Proporciona comentarios al administrador de calidad sobre la calidad de la reproducción.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) son los siguientes.



| VARTYPE           | Descripción                         |
|-------------------|-------------------------------------|
| VT \_ i8<br/> | Vea la sección Comentarios.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Este evento es desencadenado por algunos componentes de canalización. La sesión multimedia reenvía el evento al administrador de calidad mediante una llamada al método [**IMFQualityManager:: NotifyQualityEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent) .

El tipo extendido del evento indica el significado de los datos del evento.



| Tipo extendido                            | Datos de evento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_latencia de \_ procesamiento de notificaciones de calidad MF \_ \_ | Latencia de procesamiento aproximada introducida por el componente, en unidades de 100-nanosegundos.<br/> La latencia de procesamiento es la cantidad de latencia que un componente introduce en la canalización mediante el procesamiento de un ejemplo. En algunos casos, la latencia no se puede derivar simplemente examinando las llamadas a [**IMFQualityManager:: NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) y [**IMFQualityManager:: NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Por ejemplo, puede que no haya una correspondencia uno a uno entre los ejemplos de entrada y los ejemplos de salida. En este caso, el componente podría enviar un evento MEQualityNotify con la latencia de procesamiento. Si la latencia de procesamiento cambia, el componente puede enviar un nuevo evento en cualquier momento durante el streaming.<br/> |
| retardo de muestra de notificación de \_ calidad MF \_ \_ \_         | Tiempo de retardo para el ejemplo, en unidades de 100-nanosegundos. Si el valor es positivo, el ejemplo estaba atrasado. Si el valor es negativo, el ejemplo era temprano.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Para obtener el tipo extendido, llame a [**IMFMediaEvent:: GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

No es necesario que los componentes de canalización envíen este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Mfobjects. h (incluye Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




