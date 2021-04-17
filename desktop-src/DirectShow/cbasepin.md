---
description: La clase CBasePin es una clase abstracta que implementa un PIN genérico.
ms.assetid: 23b9a0e2-24fe-4ff9-b2bb-97630c237de9
title: Clase CBasePin (Amfilter. h)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670844"
---
# <a name="cbasepin-class"></a>Clase CBasePin

![jerarquía de clases cbasepin](images/filter02.png)

La `CBasePin` clase es una clase abstracta que implementa un PIN genérico.

En los temas siguientes se describe cómo utilizar esta clase:

-   [Proceso de conexión de CBasePin](cbasepin-connection-process.md)
-   [Notificar los cambios de estado de filtro de CBasePin](notifying-cbasepin-of-filter-state-changes.md)
-   [Derivación de CBasePin](deriving-from-cbasepin.md)



| Variables de miembro protegidas                                               | Descripción                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**m \_ pName**](cbasepin-m-pname.md)                                     | Nombre del PIN.                                                                                                  |
| [**m \_ conectadas**](cbasepin-m-connected.md)                             | Puntero al pin que está conectado a este pin.                                                          |
| [**\_dir m**](cbasepin-m-dir.md)                                         | Dirección del PIN.                                                                                      |
| [**m \_ Plock**](cbasepin-m-plock.md)                                     | Puntero a un objeto de sección crítica.                                                                      |
| [**m \_ bRunTimeError**](cbasepin-m-bruntimeerror.md)                     | Marca que indica si se ha producido un error en tiempo de ejecución.                                                 |
| [**m \_ bCanReconnectWhenActive**](cbasepin-m-bcanreconnectwhenactive.md) | Marca que indica si el PIN admite la reconexión dinámica.                                         |
| [**m \_ bTryMyTypesFirst**](cbasepin-m-btrymytypesfirst.md)               | Marca que indica si el PIN intenta sus propios tipos de medios preferidos antes de los del PIN receptor. |
| [**m \_ pFilter**](cbasepin-m-pfilter.md)                                 | Puntero al filtro que creó el código PIN.                                                                |
| [**m \_ pQSink**](cbasepin-m-pqsink.md)                                   | Puntero al objeto que controla los mensajes de calidad.                                                       |
| [**m \_ TypeVersion**](cbasepin-m-typeversion.md)                         | Versión actual del conjunto de tipos de medios preferidos.                                                       |
| [**m \_ MT**](cbasepin-m-mt.md)                                           | Tipo de medio para la conexión del PIN actual.                                                                 |
| [**m \_ tStart**](cbasepin-m-tstart.md)                                   | Hora de inicio del segmento.                                                                                        |
| [**m \_ tStop**](cbasepin-m-tstop.md)                                     | Hora de detención del segmento.                                                                                         |
| [**m \_ dRate**](cbasepin-m-drate.md)                                     | Velocidad de segmento.                                                                                              |
| Métodos protegidos                                                        | Descripción                                                                                                |
| [**DisplayPinInfo**](cbasepin-displaypininfo.md)                        | Realiza un seguimiento de una conexión de PIN durante la depuración.                                                                  |
| [**DisplayTypeInfo**](cbasepin-displaytypeinfo.md)                      | Muestra información de tipo de medio durante la depuración.                                                          |
| [**AttemptConnection**](cbasepin-attemptconnection.md)                  | Se conecta a otro pin con un tipo de medio especificado.                                                      |
| [**TryMediaTypes**](cbasepin-trymediatypes.md)                          | Dada una lista de tipos de medios, intenta completar una conexión con uno de esos tipos.                      |
| [**AgreeMediaType**](cbasepin-agreemediatype.md)                        | Busca un tipo de medio para establecer una conexión de PIN.                                                        |
| [**DisconnectInternal**](cbasepin-disconnectinternal.md)                | Interrumpe la conexión del PIN actual.                                                                         |
| Métodos públicos                                                           | Descripción                                                                                                |
| [**CBasePin**](cbasepin-cbasepin.md)                                    | Método de constructor.                                                                                        |
| [**~ CBasePin**](cbasepin--cbasepin.md)                                 | Método de destructor. Virtualiza.                                                                                |
| [**IsConnected**](cbasepin-isconnected.md)                              | Determina si el PIN está conectado a otro PIN.                                                    |
| [**GetConnected**](cbasepin-getconnected.md)                            | Recupera el PIN que está conectado a este pin.                                                           |
| [**IsStopped**](cbasepin-isstopped.md)                                  | Determina si el filtro que contiene este pin está detenido.                                              |
| [**GetMediaTypeVersion**](cbasepin-getmediatypeversion.md)              | Recupera un número de versión para el conjunto de tipos de medios preferidos. Virtualiza.                                  |
| [**IncrementTypeVersion**](cbasepin-incrementtypeversion.md)            | Incrementa el número de versión en el conjunto de tipos de medios preferidos.                                         |
| [**Active**](cbasepin-active.md)                                        | Notifica al pin que el filtro está activo ahora. Virtualiza.                                                   |
| [**Inactivo**](cbasepin-inactive.md)                                    | Notifica al pin que el filtro ya no está activo. Virtualiza.                                             |
| [**Ejecutar**](cbasepin-run.md)                                              | Notifica al pin que el filtro se está ejecutando ahora. Virtualiza.                                                  |
| [**SetMediaType**](cbasepin-setmediatype.md)                            | Establece el tipo de medio para la conexión. Virtualiza.                                                           |
| [**CheckConnect**](cbasepin-checkconnect.md)                            | Determina si una conexión de PIN es adecuada. Virtualiza.                                                  |
| [**BreakConnect**](cbasepin-breakconnect.md)                            | Libera el PIN de una conexión. Virtualiza.                                                               |
| [**CompleteConnect**](cbasepin-completeconnect.md)                      | Completa una conexión a otro PIN. Virtualiza.                                                            |
| [**GetMediaType**](cbasepin-getmediatype.md)                            | Recupera un tipo de medio preferido, por valor de índice. Virtualiza.                                                 |
| [**CurrentStopTime**](cbasepin-currentstoptime.md)                      | Recupera la hora de detención del segmento.                                                                           |
| [**CurrentStartTime**](cbasepin-currentstarttime.md)                    | Recupera la hora de inicio del segmento.                                                                          |
| [**InterésActual**](cbasepin-currentrate.md)                              | Recupera la velocidad del segmento.                                                                                |
| [**Name**](cbasepin-name.md)                                            | Recupera el identificador del PIN.                                                                              |
| [**SetReconnectWhenActive**](cbasepin-setreconnectwhenactive.md)        | Especifica si el PIN admite reconexiones dinámicas.                                                  |
| [**CanReconnectWhenActive**](cbasepin-canreconnectwhenactive.md)        | Consulta si el PIN admite reconexiones dinámicas.                                                    |
| Métodos virtuales puros                                                     | Descripción                                                                                                |
| [**CheckMediaType**](cbasepin-checkmediatype.md)                        | Determina si el PIN acepta un tipo de medio específico.                                                       |
| Métodos IPin                                                             | Descripción                                                                                                |
| [**Conectar**](cbasepin-connect.md)                                      | Conecta el PIN a otro PIN.                                                                           |
| [**ReceiveConnection**](cbasepin-receiveconnection.md)                  | Acepta una conexión desde otro PIN.                                                                     |
| [**Desconectar**](cbasepin-disconnect.md)                                | Interrumpe la conexión del PIN actual.                                                                         |
| [**Conectado a**](cbasepin-connectedto.md)                              | Recupera el PIN conectado a este pin.                                                                   |
| [**ConnectionMediaType**](cbasepin-connectionmediatype.md)              | Recupera el tipo de medio para la conexión del PIN actual, si existe.                                           |
| [**QueryPinInfo**](cbasepin-querypininfo.md)                            | Recupera información sobre el código PIN.                                                                       |
| [**QueryDirection**](cbasepin-querydirection.md)                        | Recupera la dirección del PIN (entrada o salida).                                                      |
| [**QueryId**](cbasepin-queryid.md)                                      | Recupera el identificador del PIN.                                                                              |
| [**QueryAccept**](cbasepin-queryaccept.md)                              | Determina si el PIN acepta un tipo de medio especificado.                                                 |
| [**EnumMediaTypes**](cbasepin-enummediatypes.md)                        | Enumera los tipos de medios preferidos del PIN.                                                                |
| [**QueryInternalConnections**](cbasepin-queryinternalconnections.md)    | Recupera los PIN que están conectados internamente a este pin (dentro del filtro).                          |
| [**EndOfStream**](cbasepin-endofstream.md)                              | Notifica al pin que no se espera ningún dato adicional.                                                      |
| [**NewSegment**](cbasepin-newsegment.md)                                | Notifica al pin que los ejemplos de multimedia recibieron después de que esta llamada se agrupe como un segmento.                     |
| Métodos IQualityControl                                                  | Descripción                                                                                                |
| [**Notificar**](cbasepin-notify.md)                                        | Notifica al pin que se ha solicitado un cambio de calidad.                                                       |
| [**SetSink**](cbasepin-setsink.md)                                      | Establece un administrador de calidad externo.                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




