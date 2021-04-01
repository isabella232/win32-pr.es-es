---
title: MSAD_ReplNeighbor (clase)
description: Representa la \_ estructura de vecinos de REPL de DS \_ , que contiene la información de estado de la replicación de entrada para un par de contexto de nomenclatura (NC) y de servidor de origen determinados.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor clase Active Directory
- Active Directory de MSAD_ReplNeighbor de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor
- MSAD_ReplNeighbor.NamingContextDN
- MSAD_ReplNeighbor.SourceDsaObjGuid
- MSAD_ReplNeighbor.NamingContextObjGuid
- MSAD_ReplNeighbor.SourceDsaDN
- MSAD_ReplNeighbor.SourceDsaAddress
- MSAD_ReplNeighbor.SourceDsaInvocationID
- MSAD_ReplNeighbor.AsyncIntersiteTransportDN
- MSAD_ReplNeighbor.AsyncIntersiteTransportObjGuid
- MSAD_ReplNeighbor.USNLastObjChangeSynced
- MSAD_ReplNeighbor.USNAttributeFilter
- MSAD_ReplNeighbor.TimeOfLastSyncSuccess
- MSAD_ReplNeighbor.TimeOfLastSyncAttempt
- MSAD_ReplNeighbor.LastSyncResult
- MSAD_ReplNeighbor.NumConsecutiveSyncFailures
- MSAD_ReplNeighbor.ReplicaFlags
- MSAD_ReplNeighbor.Writeable
- MSAD_ReplNeighbor.SyncOnStartup
- MSAD_ReplNeighbor.DoScheduledSyncs
- MSAD_ReplNeighbor.UseAsyncIntersiteTransport
- MSAD_ReplNeighbor.TwoWaySync
- MSAD_ReplNeighbor.FullSyncInProgress
- MSAD_ReplNeighbor.FullSyncNextPacket
- MSAD_ReplNeighbor.NeverSynced
- MSAD_ReplNeighbor.IgnoreChangeNotifications
- MSAD_ReplNeighbor.DisableScheduledSync
- MSAD_ReplNeighbor.CompressChanges
- MSAD_ReplNeighbor.NoChangeNotifications
- MSAD_ReplNeighbor.SourceDsaSite
- MSAD_ReplNeighbor.SourceDsaCN
- MSAD_ReplNeighbor.Domain
- MSAD_ReplNeighbor.IsDeletedSourceDsa
- MSAD_ReplNeighbor.ModifiedNumConsecutiveSyncFailures
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9554c73c7fb84aad10ae6dda51480a7644d8434a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996436"
---
# <a name="msad_replneighbor-class"></a>MSAD \_ ReplNeighbor (clase)

Representa la estructura de [**\_ \_ vecinos de REPL de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) , que contiene la información de estado de la replicación de entrada para un determinado contexto de nomenclatura (NC) y de servidor de origen, tal y como lo devuelve la función [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplNeighbor
{
  String   NamingContextDN;
  String   SourceDsaObjGuid;
  String   NamingContextObjGuid;
  String   SourceDsaDN;
  String   SourceDsaAddress;
  String   SourceDsaInvocationID;
  String   AsyncIntersiteTransportDN;
  String   AsyncIntersiteTransportObjGuid;
  uint64   USNLastObjChangeSynced;
  uint64   USNAttributeFilter;
  datetime TimeOfLastSyncSuccess;
  datetime TimeOfLastSyncAttempt;
  uint32   LastSyncResult;
  uint32   NumConsecutiveSyncFailures;
  uint32   ReplicaFlags;
  boolean  Writeable = FALSE;
  boolean  SyncOnStartup = FALSE;
  boolean  DoScheduledSyncs = FALSE;
  boolean  UseAsyncIntersiteTransport = FALSE;
  boolean  TwoWaySync = FALSE;
  boolean  FullSyncInProgress = FALSE;
  boolean  FullSyncNextPacket = FALSE;
  boolean  NeverSynced = FALSE;
  boolean  IgnoreChangeNotifications = FALSE;
  boolean  DisableScheduledSync = FALSE;
  boolean  CompressChanges = FALSE;
  boolean  NoChangeNotifications = FALSE;
  String   SourceDsaSite;
  String   SourceDsaCN;
  String   Domain;
  boolean  IsDeletedSourceDsa = FALSE;
  uint32   ModifiedNumConsecutiveSyncFailures;
};
```

## <a name="members"></a>Miembros

La clase **MSAD \_ ReplNeighbor** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSAD \_ ReplNeighbor** tiene estos métodos.



| Método                                                           | Descripción                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MSAD \_ ReplNeighbor** tiene estas propiedades.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X. 500 del objeto [**interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) que corresponde al transporte en el que se realiza la replicación. Establezca en **null** para la replicación de RPC/IP.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID del objeto de transporte entre sitios que corresponde a la propiedad **AsyncIntersiteTransportDN** .

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS para \_ \_ \_ comprimir \_ cambios** en la propiedad **ReplicaFlags** .

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la propiedad NBR de la **replicación de DS \_ \_ \_ \_ \_** .

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre canónico del dominio del NC replicado.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de **\_ \_ \_ \_ \_ sincronización programada de NBR de replicación de DS** en la propiedad **ReplicaFlags** .

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ \_ \_ \_ de NBR de sincronización completa \_ en \_ curso en** la propiedad **ReplicaFlags** .

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la marca de **\_ \_ \_ \_ \_ \_ paquete de sincronización completa de NBR de replicación de DS** .

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** el marcador **\_ REPL de \_ NBR \_ omitir \_ \_ notificaciones de cambios** .

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si esta conexión representa un controlador de dominio de origen que se ha eliminado. **True** si esta conexión representa un controlador de dominio de origen que se ha eliminado; en caso contrario, **false**. Por diseño, el DS seguirá replicando estas conexiones durante algún tiempo durante algún tiempo después de que se elimine el controlador de dominio de origen.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el código de error **HRESULT** para el último intento de replicación.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número de intentos de replicación erróneos consecutivos, sin incluir las conexiones que se espera que generen un error. Por ejemplo, si la propiedad **IsDeletedSourceDsa** está establecida en **true**, se espera que se produzca un error.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X. 500 para el NC que replica esta conexión.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID para el NC replicado.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS no \_ \_ \_ \_ sincronizado nunca** en la propiedad **ReplicaFlags** .

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de **NBR de replicación de DS \_ \_ \_ no hay \_ \_ notificaciones de cambios** en la propiedad **ReplicaFlags** .

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número de intentos de replicación erróneos consecutivos.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el conjunto de marcadores que especifican los atributos y las opciones para los datos de replicación. Esta propiedad puede ser cero o una combinación de uno o varios de los siguientes marcadores.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ NBR \_ grabable** (16 (0x10))


</dt> <dd>

La copia local del contexto de nomenclatura es de escritura.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL \_ NBR \_ Sync \_ ON \_ Startup** (32 (0x20))


</dt> <dd>

La replicación de este contexto de nomenclatura desde este origen se intenta cuando se arranca el servidor de destino. Esta marca normalmente solo se aplica a vecinos dentro del sitio.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ NBR de REPL \_ \_ realiza \_ \_ sincronizaciones programadas** (64 (0x40))


</dt> <dd>

La replicación se realiza según una programación. Normalmente, esta marca se establece a menos que la programación para este contexto de nomenclatura o origen sea "Never", es decir, la programación vacía.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ usar \_ el \_ \_ transporte asincrónico entre sitios** (128 (0x80))


</dt> <dd>

La replicación se realiza indirectamente a través del servicio de mensajería entre sitios. Este marcador sólo se establece en la replicación a través de SMTP. Esta marca no se establece en la réplica a través de RPC/IP entre sitios.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ \_ \_ \_ \_ Sincronización de NBR bidireccional de REPL** (512 (0x200))


</dt> <dd>

Si se establece, indica que cuando se completa la replicación de entrada, el servidor de destino debe indicar al servidor de origen que se sincronice en la dirección inversa. Esta característica se utiliza en escenarios de acceso telefónico en los que sólo uno de los dos servidores puede iniciar una conexión de acceso telefónico. Por ejemplo, esta opción se puede usar en una oficina central y en una sucursal, donde la sucursal se conecta a la oficina central corporativa a través de Internet por medio de una conexión de ISP de acceso telefónico.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ devuelven \_ objetos \_ primarios** (2048 (0x800))


</dt> <dd>

Este vecino está devolviendo los objetos primarios antes que los objetos secundarios. Ha entrado en este estado después de recibir un objeto secundario antes que el elemento primario correspondiente.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ \_ \_ Sincronización completa de REPL NBR \_ \_ en \_ curso** (65536 (0x10000))


</dt> <dd>

El servidor de destino está realizando una sincronización completa desde el servidor de origen. Las sincronizaciones completas no usan vectores que crean actualizaciones (por ejemplo [**, \_ \_ cursores de replicación de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)) para filtrar las actualizaciones. Las sincronizaciones completas no se usan como parte del Protocolo de replicación predeterminado.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ \_ \_ \_ \_ Siguiente \_ paquete de sincronización completa de REPL NBR** (131072 (0x20000))


</dt> <dd>

El último paquete del origen indicó una modificación de un objeto que el servidor de destino aún no ha creado. El siguiente paquete que se va a solicitar indica al servidor de origen que ponga todos los atributos del objeto modificado en el paquete.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ nunca se \_ sincronizó** (2097152 (0x200000))


</dt> <dd>

Nunca se ha realizado una sincronización correcta desde este origen.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ adelantado** (16777216 (0x1000000))


</dt> <dd>

El motor de replicación ha detenido temporalmente el procesamiento de este vecino para poder atender a otro vecino de prioridad más alta, ya sea para esta partición o para otra partición. El motor de replicación reanudará el procesamiento de este vecino cuando finalice el trabajo de prioridad más alta.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ omitir \_ \_ notificaciones de cambios** (67108864 (0x4000000))


</dt> <dd>

Este vecino está configurado para deshabilitar las sincronizaciones basadas en notificaciones. Dentro de un sitio, los controladores de dominio se sincronizan entre sí basándose en las notificaciones de cambios. Esta configuración impide que este vecino realice sincronizaciones que se desencadenan mediante notificaciones. El vecino seguirá realizando sincronizaciones en función de su programación o en respuesta a las sincronizaciones solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ deshabilitar la \_ \_ sincronización programada** (134217728 (0x8000000))


</dt> <dd>

Este vecino está configurado para no realizar sincronizaciones en función de su programación. La única manera en que este vecino realiza sincronizaciones es responder a las notificaciones de cambio o a las sincronizaciones solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ NBR de REPL- \_ \_ comprimir \_ cambios** (268435456 (0x10000000))


</dt> <dd>

Los cambios recibidos de este origen se comprimirán. Normalmente, la compresión solo se produce si el servidor de origen está en un sitio diferente.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ no \_ \_ notificaciones de cambios** (536870912 (0x20000000))


</dt> <dd>

No deberían recibirse notificaciones de cambios desde este origen. Normalmente solo se establece si el servidor de origen está en un sitio diferente.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ \_Conjunto de \_ \_ atributos parciales \_ de REPL NBR** (1073741824 (0x40000000))


</dt> <dd>

Este vecino está recompilando el contenido de esta réplica debido a un cambio en el conjunto de atributos parciales.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la dirección DNS del controlador de dominio de origen.

> [!Note]  
> Esta cadena contiene un GUID modificado, no el nombre DNS canónico que se usa habitualmente.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el componente de ruta de acceso del objeto DSA que representa el controlador de dominio de origen. Esta cadena suele ser similar al nombre del equipo, pero no siempre es idéntica.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X. 500 del DSA que representa el controlador de dominio de origen.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el identificador de invocación utilizado por el servidor de origen a partir de la última replicación.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el GUID para el agente de servicios de directorio (DSA) que representa el controlador de dominio de origen (DC).

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el sitio que contiene el controlador de dominio de origen.

</dd> <dt>

**SyncOnStartup**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** la propiedad **\_ \_ NBR \_ de REPL de la sincronización en el indicador \_ de \_ Inicio** .

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo del último intento de replicación.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo del último intento de replicación correcto.

</dd> <dt>

**TwoWaySync**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de **\_ sincronización DS REPL \_ NBR \_ \_ Biway \_** en la propiedad **ReplicaFlags** .

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido en la propiedad **ReplicaFlags** el marcador REPL de NBR de uso de la marca de **\_ \_ \_ \_ \_ \_ transporte entre sitios asincrónica** .

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor de la propiedad **USNLastObjChangeSynced** al final del último ciclo de replicación completado correctamente. Cero si no se ha completado correctamente ningún ciclo de replicación.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor de atributo [**sin modificar**](/windows/desktop/ADSchema/a-usnchanged) de la última actualización de objeto que se recibió.

</dd> <dt>

**Writeable (Grabable)**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca de escritura de NBR de replicación de DS en la propiedad **ReplicaFlags** . **\_ \_ \_**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

