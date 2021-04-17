---
description: La clase CBaseFilter es una clase abstracta para implementar filtros.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: Clase CBaseFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe032d0614b1067c9351b643d457a718b4917a8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660961"
---
# <a name="cbasefilter-class"></a>Clase CBaseFilter

![jerarquía de clases cbasefilter](images/filter01.png)

La `CBaseFilter` clase es una clase abstracta para implementar filtros. Para implementar un filtro mediante esta clase, debe realizar al menos los siguientes pasos:

-   Derive una nueva clase de `CBaseFilter` .
-   Incluya variables de miembro que definan los pin en el filtro. Los pin deben heredar de la clase [**CBasePin**](cbasepin.md) .
-   Invalide el método virtual puro [**CBaseFilter:: GetPin**](cbasefilter-getpin.md), que recupera los PIN del filtro.
-   Invalide el método virtual puro [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md), que recupera el número de clavijas.
-   Proporcionan métodos para generar, procesar o representar ejemplos de multimedia.

Varias clases base derivan de `CBaseFilter` , incluidas [**CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)y [**CTransformFilter**](ctransformfilter.md). Normalmente es más fácil implementar un filtro con una de estas clases especializadas, en lugar de usarse `CBaseFilter` directamente.



| Variables de miembro protegidas                                     | Descripción                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**\_Estado m**](cbasefilter-m-state.md)                        | Estado actual del filtro.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Puntero al reloj de referencia del filtro.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Tiempo de referencia que corresponde al tiempo de secuencia 0.                                                  |
| [**CLSID de m \_**](cbasefilter-m-clsid.md)                        | Identificador de clase (CLSID) del filtro.                                                            |
| [**m \_ Plock**](cbasefilter-m-plock.md)                        | Puntero a una sección crítica que se usa para serializar los cambios de estado.                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | Nombre del filtro.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Puntero al administrador de gráficos de filtro.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Puntero a la interfaz [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) en el administrador de gráficos de filtro.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Versión actual del conjunto de PIN de este filtro.                                                 |
| Métodos públicos                                                 | Descripción                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Método de constructor.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Método de destructor.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Recupera la hora de la secuencia actual. Virtualiza.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Determina si el filtro está activo actualmente (en ejecución o en pausa).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina si el filtro está detenido actualmente.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Envía una notificación de eventos al administrador de gráficos de filtro.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera un puntero al administrador de gráficos de filtro.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Interrumpe una conexión de PIN existente y lo vuelve a conectar al mismo pin, utilizando un tipo de medio especificado. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Recupera un número de versión para el conjunto de PIN de este filtro. Virtualiza.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa el número de versión en el conjunto de PIN.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Recupera los datos de registro para el filtro. Virtualiza.                                           |
| Métodos virtuales puros                                           | Descripción                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera el número de clavijas.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Recupera un código PIN.                                                                                   |
| Métodos IPersist                                               | Descripción                                                                                        |
| [**GetClassID**](cbasefilter-getclassid.md)                   | Recupera el identificador de clase.                                                                    |
| Métodos IMediaFilter                                           | Descripción                                                                                        |
| [**GetState**](cbasefilter-getstate.md)                       | Recupera el estado del filtro (en ejecución, detenido o en pausa).                                        |
| [**SetSyncSource**](cbasefilter-setsyncsource.md)             | Establece un reloj de referencia para el filtro.                                                             |
| [**GetSyncSource**](cbasefilter-getsyncsource.md)             | Recupera el reloj de referencia que usa el filtro.                                            |
| [**Stop**](cbasefilter-stop.md)                               | Detiene el filtro.                                                                                  |
| [**Pausar**](cbasefilter-pause.md)                             | Pausa el filtro.                                                                                 |
| [**Ejecutar**](cbasefilter-run.md)                                 | Ejecuta el filtro.                                                                                   |
| Métodos IBaseFilter                                            | Descripción                                                                                        |
| [**EnumPins**](cbasefilter-enumpins.md)                       | Enumera los pin de este filtro.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Recupera el pin con el identificador especificado.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera información sobre el filtro.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifica al filtro que se ha unido o ha dejado un gráfico de filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera una cadena que contiene información del proveedor.                                                  |
| Métodos IAMovieSetup                                           | Descripción                                                                                        |
| [**Registro**](cbasefilter-register.md)                       | Agrega el filtro al registro.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Quita el filtro del registro.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




