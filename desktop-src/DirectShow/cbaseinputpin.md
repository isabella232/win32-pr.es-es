---
description: La clase CBaseInputPin es una clase base abstracta para implementar pasadores de entrada. Esta clase agrega compatibilidad con la interfaz IMemInputPin, además de la compatibilidad con la interfaz IPin proporcionada por CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: CBaseInputPin (clase, Amfilter.h)
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
ms.openlocfilehash: ab98a2dcb1503e7593912df0e5dff51539855611311d4704e4045816fd6380e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117823894"
---
# <a name="cbaseinputpin-class"></a>CBaseInputPin (clase)

![Jerarquía de clases cbaseinputpin](images/filter07.png)

La `CBaseInputPin` clase es una clase base abstracta para implementar los pines de entrada. Esta clase agrega compatibilidad con la [**interfaz IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) además de la compatibilidad con la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) proporcionada por [**CBasePin**](cbasepin.md).

Para usar esta clase, derive una nueva clase e invalide al menos los métodos siguientes:

-   [**CBaseInputPin::BeginFlush**](cbaseinputpin-beginflush.md)
-   [**CBaseInputPin::EndFlush**](cbaseinputpin-endflush.md)
-   [**CBaseInputPin::Receive**](cbaseinputpin-receive.md)
-   [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md)
-   [**CBasePin::GetMediaType**](cbasepin-getmediatype.md)

Dependiendo de la función del pin, es posible que tenga que invalidar métodos adicionales en `CBaseInputPin` o **CBasePin**.



| Variables de miembro protegido                                                 | Descripción                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseinputpin-m-pallocator.md)                        | Puntero al asignador de memoria.                                                                            |
| [**m \_ bReadOnly**](cbaseinputpin-m-breadonly.md)                          | Marca que indica si el asignador genera ejemplos multimedia de solo lectura.                                 |
| [**m \_ bFlushing**](cbaseinputpin-m-bflushing.md)                          | Marca que indica si el pin se está vacíando actualmente.                                                  |
| [**m \_ SampleProps**](cbaseinputpin-m-sampleprops.md)                      | Propiedades del ejemplo más reciente.                                                                       |
| Métodos públicos                                                             | Descripción                                                                                                 |
| [**CBaseInputPin**](cbaseinputpin-cbaseinputpin.md)                       | Método constructor.                                                                                         |
| [**~CBaseInputPin**](cbaseinputpin--cbaseinputpin.md)                     | Método destructor.                                                                                          |
| [**BreakConnect**](cbaseinputpin-breakconnect.md)                         | Libera el pin de una conexión.                                                                         |
| [**IsReadOnly**](cbaseinputpin-isreadonly.md)                             | Consulta si el asignador usa ejemplos multimedia de solo lectura.                                                 |
| [**IsFlushing**](cbaseinputpin-isflushing.md)                             | Consulta si el filtro se va a vaciar actualmente.                                                           |
| [**CheckStreaming**](cbaseinputpin-checkstreaming.md)                     | Determina si el pin puede aceptar muestras. Virtual.                                                     |
| [**PassNotify**](cbaseinputpin-passnotify.md)                             | Pasa un mensaje de control de calidad al objeto adecuado.                                                 |
| [**Inactivo**](cbaseinputpin-inactive.md)                                 | Notifica al pin que el filtro ya no está activo. Virtual.                                              |
| [**SampleProps**](cbaseinputpin-sampleprops.md)                           | Recupera las propiedades del ejemplo más reciente.                                                         |
| Métodos de IPin                                                               | Descripción                                                                                                 |
| [**BeginFlush**](cbaseinputpin-beginflush.md)                             | Comienza una operación de vaciado.                                                                                   |
| [**EndFlush**](cbaseinputpin-endflush.md)                                 | Finaliza una operación de vaciado.                                                                                     |
| Métodos IMemInputPin                                                       | Descripción                                                                                                 |
| [**GetAllocator**](cbaseinputpin-getallocator.md)                         | Recupera el asignador de memoria propuesto por este pin.                                                        |
| [**NotifyAllocator**](cbaseinputpin-notifyallocator.md)                   | Especifica un asignador para la conexión.                                                                  |
| [**GetAllocatorRequirements**](cbaseinputpin-getallocatorrequirements.md) | Recupera las propiedades del asignador solicitadas por el pin de entrada.                                              |
| [**Recibir**](cbaseinputpin-receive.md)                                   | Recibe el siguiente ejemplo multimedia de la secuencia.                                                               |
| [**ReceiveMultiple**](cbaseinputpin-receivemultiple.md)                   | Recibe varios ejemplos en la secuencia.                                                                    |
| [**ReceiveCanBlock**](cbaseinputpin-receivecanblock.md)                   | Determina si las llamadas al método [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) pueden bloquearse. |
| Métodos IQualityControl                                                    | Descripción                                                                                                 |
| [**Notificar**](cbaseinputpin-notify.md)                                     | Recibe un mensaje de control de calidad.                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




