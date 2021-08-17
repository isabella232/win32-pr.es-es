---
description: Proporciona comentarios al administrador de calidad sobre la calidad de reproducción.
ms.assetid: 1b4b6a2d-411e-42d1-a44b-bb1928e1c063
title: Evento MEQualityNotify (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dd019db55a0791ec5464cf67c7ee4d3e4a86f918efc2b4e87f4ddde2f3574ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061880"
---
# <a name="mequalitynotify-event"></a>Evento MEQualityNotify

Proporciona comentarios al administrador de calidad sobre la calidad de reproducción.

## <a name="event-values"></a>Valores de evento

Los valores posibles recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluyen lo siguiente.



| VARTYPE           | Descripción                         |
|-------------------|-------------------------------------|
| VT \_ I8<br/> | Vea la sección Comentarios.<br/> <br/> |



## <a name="remarks"></a>Comentarios

Algunos componentes de canalización genera este evento. La sesión multimedia reenvía el evento al administrador de calidad llamando al método [**IMFQualityManager::NotifyQualityEvent.**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyqualityevent)

El tipo extendido del evento indica el significado de los datos del evento.



| Tipo extendido                            | Datos de evento                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LATENCIA DE \_ PROCESAMIENTO DE NOTIFICACIONES \_ DE CALIDAD \_ \_ DE MF | Latencia de procesamiento aproximada introducida por el componente, en unidades de 100 nanosegundos.<br/> La latencia de procesamiento es la cantidad de latencia que un componente introduce en la canalización mediante el procesamiento de una muestra. En algunos casos, la latencia no se puede derivar simplemente si se consultan las llamadas a [**IMFQualityManager::NotifyProcessInput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessinput) y [**IMFQualityManager::NotifyProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput). Por ejemplo, puede que no haya una correspondencia uno a uno entre los ejemplos de entrada y los ejemplos de salida. En este caso, el componente podría enviar un evento MEQualityNotify con la latencia de procesamiento. Si cambia la latencia de procesamiento, el componente puede enviar un nuevo evento en cualquier momento durante el streaming.<br/> |
| MF \_ QUALITY \_ NOTIFY \_ SAMPLE \_ LAG         | Tiempo de retraso para el ejemplo, en unidades de 100 nanosegundos. Si el valor es positivo, el ejemplo se ha retrasado. Si el valor es negativo, la muestra era temprana.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Para obtener el tipo extendido, llame [**a IMFMediaEvent::GetExtendedType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype).

Los componentes de canalización no son necesarios para enviar este evento.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Mfobjects.h (incluir Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




