---
description: La clase CBasePin es una clase abstracta que implementa un pin genérico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: CBasePin (clase, Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3ba7b3a85b512b2ad8d6e85aa38627a2abc68c21
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160199"
---
# <a name="cbasepin-class"></a>CBasePin (clase)

![Jerarquía de clases cbasepin](images/filter02.png)

La `CBasePin` clase es una clase abstracta que implementa un pin genérico.

En los temas siguientes se describe cómo usar esta clase:

-   [Proceso de conexión de CBasePin](cbasepin-connection-process.md)
-   [Notificación a CBasePin de cambios de estado de filtro](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivación de CBasePin](deriving-from-cbasepin.md)



| Variables miembro protegidas                                               | Descripción                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Nombre del pin.                                                                                                  |
| [**m \_ Conectado**](cbasepin-m-connected.md)                             | Puntero al pin que está conectado a este pin.                                                          |
| [**m \_ dir**](cbasepin-m-dir.md)                                         | Dirección del pin.                                                                                      |
| [**m \_ pLock**](cbasepin-m-plock.md)                                     | Puntero a un objeto de sección crítica.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Marca que indica si se ha producido un error en tiempo de ejecución.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Marca que indica si el pin admite la reconexión dinámica.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Marca que indica si el pin intenta sus propios tipos de medios preferidos antes que los del pin receptor. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Puntero al filtro que creó el pin.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Puntero al objeto que controla los mensajes de calidad.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Versión actual del conjunto de tipos de medios preferidos.                                                       |
| [**m \_ mt**](cbasepin-m-mt.md)                                           | Tipo de medio para la conexión de pin actual.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Hora de inicio del segmento.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Tiempo de detenerse del segmento.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Velocidad de segmento.                                                                                              |
| Métodos protegidos                                                        | Descripción                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Hace un seguimiento de una conexión de pin durante la depuración.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Muestra información de tipo de medio durante la depuración.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Se conecta a otro pin mediante un tipo de medio especificado.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Dada una lista de tipos de medios, intenta completar una conexión mediante uno de esos tipos.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Busca un tipo de medio para realizar una conexión de pin.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrumpe la conexión de pin actual.                                                                         |
| Métodos públicos                                                           | Descripción                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Método constructor.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Método destructor. Virtual.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Determina si el pin está conectado a otro pin.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera el pin que está conectado a este pin.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina si se detiene el filtro que contiene este pin.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera un número de versión para el conjunto de tipos de medios preferidos. Virtual.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa el número de versión en el conjunto de tipos de medios preferidos.                                         |
| [**Activo**](cbasepin-active.md)                                        | Notifica al pin que el filtro ahora está activo. Virtual.                                                   |
| [**Inactivo**](cbasepin-inactive.md)                                    | Notifica al pin que el filtro ya no está activo. Virtual.                                             |
| [**Ejecutar**](cbasepin-run.md)                                              | Notifica al pin que el filtro se está ejecutando. Virtual.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Establece el tipo de medio para la conexión. Virtual.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Determina si una conexión de pin es adecuada. Virtual.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Libera el pin de una conexión. Virtual.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Completa una conexión a otro pin. Virtual.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Recupera un tipo de medio preferido, por valor de índice. Virtual.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera el tiempo de detenerse del segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera la hora de inicio del segmento.                                                                          |
| [**CurrentRate**](cbasepin-currentrate.md)                              | Recupera la velocidad de segmento.                                                                                |
| [**Nombre**](cbasepin-name.md)                                            | Recupera el identificador de pin.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Especifica si el pin admite reconexiones dinámicas.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Consulta si el pin admite reconexiones dinámicas.                                                    |
| Métodos virtuales puros                                                     | Descripción                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina si el pin acepta un tipo de medio específico.                                                       |
| Métodos de IPin                                                             | Descripción                                                                                                |
| [**Conectar**](cbasepin-connect.md)                                      | Conecta el pin a otro pin.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Acepta una conexión desde otro pin.                                                                     |
| [**Desconectar**](cbasepin-disconnect.md)                                | Interrumpe la conexión de pin actual.                                                                         |
| [**ConnectedTo**](cbasepin-connectedto.md)                              | Recupera el pin conectado a este pin.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Recupera el tipo de medio para la conexión de pin actual, si la hay.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Recupera información sobre el pin.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Recupera la dirección del pin (entrada o salida).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Recupera el identificador de pin.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Determina si el pin acepta un tipo de medio especificado.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Enumera los tipos de medios preferidos del pin.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Recupera los pines que están conectados internamente a este pin (dentro del filtro).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifica al pin que no se espera ningún dato adicional.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Notifica al pin que los ejemplos de medios recibidos después de esta llamada se agrupan como un segmento.                     |
| Métodos IQualityControl                                                  | Descripción                                                                                                |
| [**Notificar**](cbasepin-notify.md)                                        | Notifica al pin que se solicita un cambio de calidad.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Establece un administrador de calidad externo.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




