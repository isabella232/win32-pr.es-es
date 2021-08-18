---
description: La clase CBaseOutputPin es una clase base abstracta que implementa un pin de salida.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: CBaseOutputPin (clase, Amfilter.h)
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
ms.openlocfilehash: 67a4051f904b27b75273d553e1d0604b068b3910fbfb322b5a2df716c996a1ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872595"
---
# <a name="cbaseoutputpin-class"></a>CBaseOutputPin (clase)

![cbaseoutputpin (jerarquía de clases)](images/filter06.png)

La `CBaseOutputPin` clase es una clase base abstracta que implementa un pin de salida.

Esta clase se deriva de [**CBasePin**](cbasepin.md). Difiere de **CBasePin** en los aspectos siguientes:

-   Solo se conecta a los pines de entrada que admiten la [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)
-   Admite el transporte de memoria local a través de [**la interfaz IMemAllocator.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)
-   Rechaza las notificaciones de fin de flujo, vaciado y nuevo segmento. (No se deben enviar a un pin de salida).
-   Proporciona métodos para entregar ejemplos de nivel inferior.

Cuando se conecta el pin, solicita un asignador de memoria del pin de entrada. Si no lo hace, crea un nuevo objeto de asignador. El pin de salida es responsable de establecer las propiedades del asignador. Esto se hace mediante el método virtual puro [**CBaseOutputPin::D ecideBufferSize**](cbaseoutputpin-decidebuffersize.md). Invalide este método en la clase derivada. Si el pin de entrada tiene algún requisito de búfer, se pasan al **método DecideBufferSize.**

Llame al [**método CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obtener un ejemplo multimedia vacío. Llame al [**método CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) para entregar ejemplos de nivel inferior.

La clase derivada debe invalidar el método [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) virtual puro para validar el tipo de medio durante las conexiones de pin.



| Variables de miembro protegido                                      | Descripción                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [**m \_ pAllocator**](cbaseoutputpin-m-pallocator.md)            | Puntero al asignador de memoria.                                           |
| [**m \_ pInputPin**](cbaseoutputpin-m-pinputpin.md)              | Puntero al pin de entrada conectado a este pin.                            |
| Métodos públicos                                                  | Descripción                                                                |
| [**CBaseOutputPin**](cbaseoutputpin-cbaseoutputpin.md)         | Método constructor.                                                        |
| [**CompleteConnect**](cbaseoutputpin-completeconnect.md)       | Completa una conexión a un pin de entrada. Virtual.                           |
| [**DecideAllocator**](cbaseoutputpin-decideallocator.md)       | Selecciona un asignador de memoria. Virtual.                                       |
| [**GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md)   | Recupera un ejemplo multimedia que contiene un búfer vacío. Virtual.           |
| [**Entrega**](cbaseoutputpin-deliver.md)                       | Entrega un ejemplo multimedia al pin de entrada conectado. Virtual.               |
| [**InitAllocator**](cbaseoutputpin-initallocator.md)           | Crea un asignador de memoria. Virtual.                                       |
| [**CheckConnect**](cbaseoutputpin-checkconnect.md)             | Determina si una conexión de pin es adecuada.                           |
| [**BreakConnect**](cbaseoutputpin-breakconnect.md)             | Libera el pin de una conexión.                                        |
| [**Activo**](cbaseoutputpin-active.md)                         | Notifica al pin que el filtro ahora está activo.                            |
| [**Inactivo**](cbaseoutputpin-inactive.md)                     | Notifica al pin que el filtro ya no está activo.                      |
| [**DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) | Entrega una notificación de fin de flujo al pin de entrada conectado. Virtual. |
| [**DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md)   | Solicita el pin de entrada conectado para iniciar una operación de vaciado. Virtual.      |
| [**DeliverEndFlush**](cbaseoutputpin-deliverendflush.md)       | Solicita el pin de entrada conectado para finalizar una operación de vaciado. Virtual.        |
| [**DeliverNewSegment**](cbaseoutputpin-delivernewsegment.md)   | Entrega una notificación de nuevo segmento al pin de entrada conectado. Virtual.   |
| Métodos virtuales puros                                            | Descripción                                                                |
| [**DecideBufferSize**](cbaseoutputpin-decidebuffersize.md)     | Establece los requisitos del búfer.                                              |
| Métodos de IPin                                                    | Descripción                                                                |
| [**BeginFlush**](cbaseoutputpin-beginflush.md)                 | Comienza una operación de vaciado.                                                  |
| [**EndFlush**](cbaseoutputpin-endflush.md)                     | Finaliza una operación de vaciado.                                                    |
| [**EndOfStream**](cbaseoutputpin-endofstream.md)               | Notifica al pin que no se espera ningún dato adicional.                      |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




