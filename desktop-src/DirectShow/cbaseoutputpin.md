---
description: La clase CBaseOutputPin es una clase base abstracta que implementa un PIN de salida.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Clase CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660982"
---
# <a name="cbaseoutputpin-class"></a>Clase CBaseOutputPin

![jerarquía de clases cbaseoutputpin](images/filter06.png)

La `CBaseOutputPin` clase es una clase base abstracta que implementa un PIN de salida.

Esta clase se deriva de [**CBasePin**](cbasepin.md). Difiere de **CBasePin** en los siguientes aspectos:

-   Solo se conecta a los pin de entrada que admiten la interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .
-   Admite el transporte de memoria local a través de la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .
-   Rechaza las notificaciones de final de secuencia, vaciado y segmento nuevo. (Estos no se deben enviar a un PIN de salida).
-   Proporciona métodos para entregar ejemplos de bajada.

Cuando el PIN se conecta, solicita un asignador de memoria del PIN de entrada. Si no es así, se crea un nuevo objeto de asignador. El PIN de salida es responsable de establecer las propiedades de asignador. Para ello, se realiza el método virtual puro [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md). Invalide este método en la clase derivada. Si el PIN de entrada tiene algún requisito de búfer, se pasan al método **DecideBufferSize** .

Llame al método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un ejemplo de medio vacío. Llame al método [**CBaseOutputPin::D Eliver**](cbaseoutputpin-deliver.md) para proporcionar ejemplos de bajada.

La clase derivada debe reemplazar el método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) virtual puro para validar el tipo de medio durante las conexiones del PIN.



| Variables de miembro protegidas                                      | Descripción                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | Puntero al asignador de memoria.                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | Puntero al pin de entrada conectado a este pin.                            |
| Métodos públicos                                                  | Descripción                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Método de constructor.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Completa una conexión a un PIN de entrada. Virtualiza.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Selecciona un asignador de memoria. Virtualiza.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Recupera un ejemplo multimedia que contiene un búfer vacío. Virtualiza.           |
| [**Entrega**](cbaseoutputpin-deliver.md)                       | Entrega un ejemplo multimedia a la clavija de entrada conectada. Virtualiza.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Crea un asignador de memoria. Virtualiza.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Determina si una conexión de PIN es adecuada.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Libera el PIN de una conexión.                                        |
| [**Active**](cbaseoutputpin-active.md)                         | Notifica al pin que el filtro está activo ahora.                            |
| [**Inactivo**](cbaseoutputpin-inactive.md)                     | Notifica al pin que el filtro ya no está activo.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Entrega una notificación de final de secuencia a la clavija de entrada conectada. Virtualiza. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Solicita la clavija de entrada conectada para iniciar una operación de vaciado. Virtualiza.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Solicita la clavija de entrada conectada para finalizar una operación de vaciado. Virtualiza.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Entrega una notificación de nuevo segmento al pin de entrada conectado. Virtualiza.   |
| Métodos virtuales puros                                            | Descripción                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Establece los requisitos de búfer.                                              |
| Métodos IPin                                                    | Descripción                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Comienza una operación de vaciado.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Finaliza una operación de vaciado.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifica al pin que no se espera ningún dato adicional.                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




