---
description: Esta clase implementa la interfaz IAMStreamControl para los terminales de entrada y salida.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Clase CBaseStreamControl (Strmctl. h)
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
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660432"
---
# <a name="cbasestreamcontrol-class"></a>Clase CBaseStreamControl

![jerarquía de clases cbasestreamcontrol](images/strmctl1.png)

Esta clase implementa la interfaz [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para los terminales de entrada y salida. Proporciona control sobre el inicio y la detención de un PIN individual en el filtro. Un PIN que admita **IAMStreamControl** debe heredar de esta clase base. A continuación se proporciona una declaración típica para un PIN de entrada:

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

Asegúrese de invalidar **NonDelegatingQueryInteface** para exponer **IAMStreamControl**. Para obtener más información, vea [How to implement IUnknown](how-to-implement-iunknown.md).



| Métodos públicos                                                        | Descripción                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [**CBaseStreamControl**](cbasestreamcontrol-cbasestreamcontrol.md)   | Método de constructor.                                                                                  |
| [**~ CBaseStreamControl**](cbasestreamcontrol--cbasestreamcontrol.md) | Método de destructor.                                                                                   |
| [**CheckStreamState**](cbasestreamcontrol-checkstreamstate.md)       | Determina si un ejemplo multimedia se debe entregar o descartar.                                  |
| [**Vaciar**](cbasestreamcontrol-flushing.md)                       | Notifica a la clase base que el PIN se ha iniciado o detenido.                                |
| [**NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md)     | Notifica al pin cuando cambia el estado del filtro.                                                    |
| [**SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md)           | Especifica el receptor de eventos para los eventos de control de flujo.                                                  |
| [**SetSyncSource**](cbasestreamcontrol-setsyncsource.md)             | Notifica a la clase base del reloj de referencia actual.                                              |
| Métodos IAMStreamControl                                              | Descripción                                                                                          |
| [**GetInfo**](cbasestreamcontrol-getinfo.md)                         | Recupera información sobre la configuración actual del control de flujo, incluidas las horas de inicio y detención. |
| [**StartAt**](cbasestreamcontrol-startat.md)                         | Informa al pin Cuándo debe comenzar a entregar los datos.                                                       |
| [**StopAt**](cbasestreamcontrol-stopat.md)                           | Informa al pin Cuándo detener la entrega de datos.                                                        |



 

## <a name="remarks"></a>Observaciones

Esta clase requiere que el PIN y el filtro propietario notifiquen a la clase cuando se producen varios eventos, como el filtro que une el gráfico o la recepción de un nuevo reloj de referencia. Debe llamar a los siguientes métodos de clase:

-   En el método [**IMediaFilter:: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) del filtro, llame al método [**CBaseStreamControl:: SetSyncSource**](cbasestreamcontrol-setsyncsource.md) . Este método notifica a la clase del reloj de referencia actual.
-   En el método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) del filtro, llame al método [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) . Este método proporciona a la clase un puntero al administrador de gráficos de filtro, de modo que la clase pueda enviar los eventos de control de flujo correctos.
-   Siempre que el filtro cambie de estado (a en ejecución, en pausa o detenido), llame al método [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .
-   En los métodos IPin:: [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) y [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) del PIN, llame al método [**CBaseStreamControl:: Flushing**](cbasestreamcontrol-flushing.md) .

La `CBaseStreamControl` clase usa el reloj de referencia del gráfico de filtro para determinar qué muestras debe enviar el filtro y cuáles deben descartarse. En el método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) del PIN, llame al método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) con un puntero al ejemplo de multimedia entrante. Si el método devuelve el flujo de valor que \_ fluye, entregue el ejemplo de nivel inferior. De lo contrario, descartarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Strmctl. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




