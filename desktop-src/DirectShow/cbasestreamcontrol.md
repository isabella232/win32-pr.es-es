---
description: Esta clase implementa la interfaz IAMStreamControl para los pines de entrada y salida.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: CBaseStreamControl (clase, Strmctl.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb1d8d747d88a416792d59af79af41c047cb51aa61688aef9d6b105790bbae8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157212"
---
# <a name="cbasestreamcontrol-class"></a>CBaseStreamControl (clase)

![Jerarquía de clases cbasestreamcontrol](images/strmctl1.png)

Esta clase implementa la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para los pines de entrada y salida. Proporciona control sobre el inicio y la detención de un pin individual en el filtro. Un pin que admita **IAMStreamControl** debe heredar de esta clase base. A continuación se muestra una declaración típica para un pin de entrada:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Asegúrese de invalidar **NonDelegatingQueryInteface para** exponer **IAMStreamControl**. Para obtener más información, [vea How to Implement IUnknown](how-to-implement-iunknown.md).



| Métodos públicos                                                        | Descripción                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Método constructor.                                                                                  |
| [**~CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Método destructor.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Determina si se debe entregar o descartar un ejemplo multimedia.                                  |
| [**Lavado**](cbasestreamcontrol-flushing.md)                       | Notifica a la clase base que el pin se ha iniciado o detenido el vaciado.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifica al pin cuando cambia el estado del filtro.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Especifica el receptor de eventos para los eventos de control de flujo.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Notifica a la clase base el reloj de referencia actual.                                              |
| Métodos IAMStreamControl                                              | Descripción                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y de detenerse. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Informa al pin de cuándo empezar a entregar datos.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informa al pin de cuándo dejar de entregar datos.                                                        |



 

## <a name="remarks"></a>Comentarios

Esta clase requiere que el pin y el filtro propietario notifiquen a la clase cuando se producen varios eventos, como el filtro que une el gráfico o recibe un nuevo reloj de referencia. Debe llamar a los métodos de clase siguientes:

-   En el método [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro, llame al método [**CBaseStreamControl::SetSyncSource.**](cbasestreamcontrol-setsyncsource.md) Este método notifica a la clase el reloj de referencia actual.
-   En el método [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro, llame al método [**CBaseStreamControl::SetFilterGraph.**](cbasestreamcontrol-setfiltergraph.md) Este método proporciona a la clase un puntero a Filter Graph Manager, para que la clase pueda enviar los eventos de control de flujo correctos.
-   Cada vez que el filtro cambia de estado (a en ejecución, en pausa o detenido), llame al [**método CBaseStreamControl::NotifyFilterState.**](cbasestreamcontrol-notifyfilterstate.md)
-   En los métodos [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del pin, llame al método [**CBaseStreamControl::Flushing.**](cbasestreamcontrol-flushing.md)

La clase usa el reloj de referencia del gráfico de filtros para determinar qué muestras debe entregar el filtro `CBaseStreamControl` y cuáles debe descartar. En el método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del pin, llame al método [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntero al ejemplo multimedia entrante. Si el método devuelve el valor STREAM \_ FLOWING, entregue el ejemplo de nivel inferior. De lo contrario, descálala.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




