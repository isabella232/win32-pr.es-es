---
description: La clase CBaseInputPin es una clase base abstracta para implementar clavijas de entrada. Esta clase agrega compatibilidad para la interfaz IMemInputPin, además de la compatibilidad con la interfaz IPin proporcionada por CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Clase CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670953"
---
# <a name="cbaseinputpin-class"></a>Clase CBaseInputPin

![jerarquía de clases cbaseinputpin](images/filter07.png)

La `CBaseInputPin` clase es una clase base abstracta para implementar clavijas de entrada. Esta clase agrega compatibilidad para la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , además de la compatibilidad con la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) proporcionada por [**CBasePin**](cbasepin.md).

Para usar esta clase, derive una nueva clase e invalide al menos los siguientes métodos:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Dependiendo de la función del PIN, es posible que deba invalidar métodos adicionales en `CBaseInputPin` o **CBasePin**.



| Variables de miembro protegidas                                                 | Descripción                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Puntero al asignador de memoria.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Marca que indica si el asignador genera ejemplos de medios de solo lectura.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Marca que indica si el PIN se está vaciando actualmente.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Propiedades de la muestra más reciente.                                                                       |
| Métodos públicos                                                             | Descripción                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Método de constructor.                                                                                         |
| [**~ CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Método de destructor.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Libera el PIN de una conexión.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Consulta si el asignador usa ejemplos de medios de solo lectura.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Consulta si el filtro se está vaciando actualmente.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina si el pin puede aceptar ejemplos. Virtualiza.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Pasa un mensaje de control de calidad al objeto adecuado.                                                 |
| [**Inactivo**](cbaseinputpin-inactive.md)                                 | Notifica al pin que el filtro ya no está activo. Virtualiza.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera las propiedades del ejemplo más reciente.                                                         |
| Métodos IPin                                                               | Descripción                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Comienza una operación de vaciado.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Finaliza una operación de vaciado.                                                                                     |
| Métodos IMemInputPin                                                       | Descripción                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | Recupera el asignador de memoria propuesto por este pin.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Especifica un asignador para la conexión.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera las propiedades de asignador solicitadas por el PIN de entrada.                                              |
| [**Aparecen**](cbaseinputpin-receive.md)                                   | Recibe el siguiente ejemplo multimedia en la secuencia.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Recibe varios ejemplos en la secuencia.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Determina si las llamadas al método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) podrían bloquearse. |
| Métodos IQualityControl                                                    | Descripción                                                                                                 |
| [**Notificar**](cbaseinputpin-notify.md)                                     | Recibe un mensaje de control de calidad.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




