---
description: La clase CBaseFilter es una clase abstracta para implementar filtros.
ms.assetid: 4610c8d6-9d7d-47ca-b1d5-0a867153a5f6
title: CBaseFilter (clase, Amfilter.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361391"
---
# <a name="cbasefilter-class"></a>CBaseFilter (clase)

![Jerarquía de clases cbasefilter](images/filter01.png)

La `CBaseFilter` clase es una clase abstracta para implementar filtros. Para implementar un filtro mediante esta clase, debe realizar al menos los pasos siguientes:

-   Derive una nueva clase de `CBaseFilter` .
-   Incluya variables miembro que definan los pines en el filtro. Los pines deben heredar de la [**clase CBasePin.**](cbasepin.md)
-   Invalide el método virtual [**puro CBaseFilter::GetPin**](cbasefilter-getpin.md), que recupera los pines del filtro.
-   Invalide el método virtual [**puro CBaseFilter::GetPinCount**](cbasefilter-getpincount.md), que recupera el número de pines.
-   Proporcione métodos para generar, procesar o representar ejemplos multimedia.

Varias clases base derivan de `CBaseFilter` , [**incluidos CSource**](csource.md), [**CBaseRenderer**](cbaserenderer.md)y [**CTransformFilter.**](ctransformfilter.md) Normalmente es más fácil implementar un filtro con una de estas clases especializadas, en lugar de usar `CBaseFilter` directamente.



| Variables de miembro protegido                                     | Descripción                                                                                        |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [**m \_ State**](cbasefilter-m-state.md)                        | Estado actual del filtro.                                                                       |
| [**m \_ pClock**](cbasefilter-m-pclock.md)                      | Puntero al reloj de referencia del filtro.                                                           |
| [**m \_ tStart**](cbasefilter-m-tstart.md)                      | Tiempo de referencia que corresponde al tiempo de secuencia 0.                                                  |
| [**m \_ clsid**](cbasefilter-m-clsid.md)                        | Identificador de clase (CLSID) del filtro.                                                            |
| [**m \_ pLock**](cbasefilter-m-plock.md)                        | Puntero a una sección crítica que se usa para serializar los cambios de estado.                             |
| [**m \_ pName**](cbasefilter-m-pname.md)                        | Nombre del filtro.                                                                                       |
| [**m \_ pGraph**](cbasefilter-m-pgraph.md)                      | Puntero al administrador de gráficos de filtros.                                                               |
| [**m \_ pSink**](cbasefilter-m-psink.md)                        | Puntero a la [**interfaz IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) en el administrador de gráficos de filtros.   |
| [**m \_ PinVersion**](cbasefilter-m-pinversion.md)              | Versión actual del conjunto de pines de este filtro.                                                 |
| Métodos públicos                                                 | Descripción                                                                                        |
| [**CBaseFilter**](cbasefilter-cbasefilter.md)                 | Método constructor.                                                                                |
| [**~ CBaseFilter**](cbasefilter--cbasefilter.md)              | Método destructor.                                                                                 |
| [**StreamTime**](cbasefilter-streamtime.md)                   | Recupera el tiempo de secuencia actual. Virtual.                                                        |
| [**IsActive**](cbasefilter-isactive.md)                       | Determina si el filtro está activo actualmente (en ejecución o en pausa).                             |
| [**IsStopped**](cbasefilter-isstopped.md)                     | Determina si el filtro está detenido actualmente.                                                |
| [**NotifyEvent**](cbasefilter-notifyevent.md)                 | Envía una notificación de eventos al administrador de gráficos de filtros.                                           |
| [**GetFilterGraph**](cbasefilter-getfiltergraph.md)           | Recupera un puntero al administrador de gráficos de filtros.                                                   |
| [**ReconnectPin**](cbasefilter-reconnectpin.md)               | Interrumpe una conexión de pin existente y la vuelve a conectar al mismo pin, utilizando un tipo de medio especificado. |
| [**GetPinVersion**](cbasefilter-getpinversion.md)             | Recupera un número de versión para el conjunto de pines de este filtro. Virtual.                            |
| [**IncrementPinVersion**](cbasefilter-incrementpinversion.md) | Incrementa el número de versión en el conjunto de pines.                                                  |
| [**GetSetupData**](cbasefilter-getsetupdata.md)               | Recupera los datos de registro del filtro. Virtual.                                           |
| Métodos virtuales puros                                           | Descripción                                                                                        |
| [**GetPinCount**](cbasefilter-getpincount.md)                 | Recupera el número de pines.                                                                      |
| [**GetPin**](cbasefilter-getpin.md)                           | Recupera un pin.                                                                                   |
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
| [**EnumPins**](cbasefilter-enumpins.md)                       | Enumera los pines de este filtro.                                                                |
| [**FindPin**](cbasefilter-findpin.md)                         | Recupera el pin con el identificador especificado.                                                   |
| [**QueryFilterInfo**](cbasefilter-queryfilterinfo.md)         | Recupera información sobre el filtro.                                                            |
| [**JoinFilterGraph**](cbasefilter-joinfiltergraph.md)         | Notifica al filtro que se ha unido o ha dejado un gráfico de filtro.                                     |
| [**QueryVendorInfo**](cbasefilter-queryvendorinfo.md)         | Recupera una cadena que contiene información del proveedor.                                                  |
| Métodos de IAMovieSetup                                           | Descripción                                                                                        |
| [**Registro**](cbasefilter-register.md)                       | Agrega el filtro al Registro.                                                                   |
| [**Unregister**](cbasefilter-unregister.md)                   | Quita el filtro del Registro.                                                              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




