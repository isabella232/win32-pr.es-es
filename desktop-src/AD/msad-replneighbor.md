---
title: MSAD_ReplNeighbor clase
description: Representa la estructura DS REPL NEIGHBOR, que contiene la información de estado de replicación de entrada para un contexto de nomenclatura (NC) determinado y un par de \_ \_ servidor de origen.
ms.assetid: fdd3934b-a3f6-49ad-827b-077bcd21cf23
ms.tgt_platform: multiple
keywords:
- MSAD_ReplNeighbor clase Active Directory
- MSAD_ReplNeighbor clase Active Directory , descrita
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
ms.openlocfilehash: 0598116413d34334e0610895a9c3b0629399fed8bb482e0d08cdae9cafb17fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025763"
---
# <a name="msad_replneighbor-class"></a>Clase \_ ReplNeighbor de MSAD

Representa la estructura [**\_ DS REPL \_ NEIGHBOR,**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw) que contiene la información de estado de replicación de entrada para un contexto de nomenclatura (NC) y un par de servidor de origen determinados, tal como lo devuelve la función [**DsReplicaGetInfo.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)

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

La **clase \_ ReplNeighbor de MSAD** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ ReplNeighbor de MSAD** tiene estos métodos.



| Método                                                           | Descripción                                                                   |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**SyncNamingContext**](syncnamingcontext-msad-replneighbor.md) | Sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ ReplNeighbor de MSAD** tiene estas propiedades.

<dl> <dt>

**AsyncIntersiteTransportDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X.500 del [**objeto interSiteTransport**](/windows/desktop/ADSchema/c-intersitetransport) que corresponde al transporte en el que se realiza la replicación. Se establece **en NULL para** la replicación RPC/IP.

</dd> <dt>

**AsyncIntersiteTransportObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID del objeto de transporte entre sitios que corresponde a la **propiedad AsyncIntersiteTransportDN.**

</dd> <dt>

**CompressChanges**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si la marca **\_ DS REPL \_ NBR \_ COMPRESS \_ CHANGES** se ha establecido en la **propiedad ReplicaFlags.**

</dd> <dt>

**DisableScheduledSync**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ DISABLE \_ SCHEDULED \_ SYNC** en la **propiedad ReplicaFlags.**

</dd> <dt>

**Dominio**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el nombre canónico del dominio del controlador de red replicado.

</dd> <dt>

**DoScheduledSyncs**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ DO \_ SCHEDULED \_ SYNCS** en la **propiedad ReplicaFlags.**

</dd> <dt>

**FullSyncInProgress**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ FULL SYNC IN \_ \_ \_ PROGRESS** en la **propiedad ReplicaFlags.**

</dd> <dt>

**FullSyncNextPacket**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ FULL SYNC NEXT \_ \_ \_ PACKET** en la **propiedad ReplicaFlags.**

</dd> <dt>

**IgnoreChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ REPL \_ NBR \_ IGNORE CHANGE \_ \_ NOTIFICATIONS** de DS en la propiedad **ReplicaFlags.**

</dd> <dt>

**IsDeletedSourceDsa**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si esta conexión representa un controlador de dominio de origen que se ha eliminado. **TRUE** si esta conexión representa un controlador de dominio de origen que se ha eliminado; de lo contrario, **FALSE**. Por diseño, el DS seguirá replicando estas conexiones durante algún tiempo después de eliminar el controlador de dominio de origen.

</dd> <dt>

**LastSyncResult**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el código de error **HRESULT** del último intento de replicación.

</dd> <dt>

**ModifiedNumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número de intentos consecutivos de replicación con errores, sin incluir las conexiones que se espera que no se puedan realizar correctamente. Por ejemplo, si la **propiedad IsDeletedSourceDsa** está establecida en **TRUE,** se espera que se producirá un error.

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene la ruta de acceso X.500 para el NC replicado por esta conexión.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el GUID del NC replicado.

</dd> <dt>

**NeverSynced**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ NEVER \_ SYNCED** en la **propiedad ReplicaFlags.**

</dd> <dt>

**NoChangeNotifications**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **DS \_ REPL \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS** en la **propiedad ReplicaFlags.**

</dd> <dt>

**NumConsecutiveSyncFailures**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el número de intentos consecutivos de replicación con errores.

</dd> <dt>

**ReplicaFlags**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el conjunto de marcas que especifican atributos y opciones para los datos de replicación. Esta propiedad puede ser cero o una combinación de una o varias de las marcas siguientes.

<dt>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>

<span id="DS_REPL_NBR_WRITEABLE"></span><span id="ds_repl_nbr_writeable"></span>**DS \_ REPL \_ NBR \_ WRITEABLE** (16 (0x10))


</dt> <dd>

La copia local del contexto de nomenclatura es de escritura.

</dd> <dt>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>

<span id="DS_REPL_NBR_SYNC_ON_STARTUP"></span><span id="ds_repl_nbr_sync_on_startup"></span>**DS \_ REPL \_ NBR \_ SYNC ON \_ \_ STARTUP** (32 (0x20))


</dt> <dd>

La replicación de este contexto de nomenclatura desde este origen se intenta cuando se arranca el servidor de destino. Normalmente, esta marca solo se aplica a los vecinos dentro del sitio.

</dd> <dt>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>

<span id="DS_REPL_NBR_DO_SCHEDULED_SYNCS"></span><span id="ds_repl_nbr_do_scheduled_syncs"></span>**DS \_ REPL \_ NBR \_ DO \_ SCHEDULED \_ SYNCS** (64 (0x40))


</dt> <dd>

La replicación se realiza según una programación. Normalmente, esta marca se establece a menos que la programación de este contexto de nomenclatura o origen sea "never", es decir, la programación vacía.

</dd> <dt>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>

<span id="DS_REPL_NBR_USE_ASYNC_INTERSITE_TRANSPORT"></span><span id="ds_repl_nbr_use_async_intersite_transport"></span>**DS \_ REPL \_ NBR \_ USE \_ ASYNC \_ INTERSITE \_ TRANSPORT** (128 (0x80))


</dt> <dd>

La replicación se realiza indirectamente a través del servicio de mensajería entre sitios. Este marcador sólo se establece en la replicación a través de SMTP. Esta marca no se establece en la réplica a través de RPC/IP entre sitios.

</dd> <dt>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>

<span id="DS_REPL_NBR_TWO_WAY_SYNC"></span><span id="ds_repl_nbr_two_way_sync"></span>**DS \_ REPL \_ NBR \_ TWO WAY \_ \_ SYNC** (512 (0x200))


</dt> <dd>

Si se establece, indica que cuando se completa la replicación entrante, el servidor de destino debe indicar al servidor de origen que se sincronice en la dirección inversa. Esta característica se utiliza en escenarios de acceso telefónico en los que sólo uno de los dos servidores puede iniciar una conexión de acceso telefónico. Por ejemplo, esta opción podría usarse en una oficina central corporativa y una sucursal, donde la sucursal se conecta a la oficina central corporativa a través de Internet mediante una conexión de ACCESO telefónico de ISP.

</dd> <dt>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>

<span id="DS_REPL_NBR_RETURN_OBJECT_PARENTS"></span><span id="ds_repl_nbr_return_object_parents"></span>**DS \_ REPL \_ NBR \_ RETURN OBJECT \_ \_ PARENTS** (2048 (0x800))


</dt> <dd>

Este vecino está devolviendo los objetos primarios antes que los objetos secundarios. Ha entrado en este estado después de recibir un objeto secundario antes que el elemento primario correspondiente.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>

<span id="DS_REPL_NBR_FULL_SYNC_IN_PROGRESS"></span><span id="ds_repl_nbr_full_sync_in_progress"></span>**DS \_ REPL \_ NBR \_ FULL SYNC \_ IN \_ \_ PROGRESS** (65536 (0x10000))


</dt> <dd>

El servidor de destino está realizando una sincronización completa desde el servidor de origen. Las sincronizaciones completa no usan vectores que crean actualizaciones (como [**CURSORES \_ DE REPL \_ de DS)**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)para filtrar las actualizaciones. Las sincronizaciones completa no se usan como parte del protocolo de replicación predeterminado.

</dd> <dt>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>

<span id="DS_REPL_NBR_FULL_SYNC_NEXT_PACKET"></span><span id="ds_repl_nbr_full_sync_next_packet"></span>**DS \_ PAQUETE \_ SIGUIENTE DE REPL NBR \_ \_ FULL SYNC \_ \_** (131072 (0x20000))


</dt> <dd>

El último paquete del origen indicaba una modificación de un objeto que el servidor de destino aún no ha creado. El siguiente paquete que se va a solicitar indica al servidor de origen que coloque todos los atributos del objeto modificado en el paquete.

</dd> <dt>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>

<span id="DS_REPL_NBR_NEVER_SYNCED"></span><span id="ds_repl_nbr_never_synced"></span>**DS \_ REPL \_ NBR \_ NEVER \_ SYNCED** (2097152 (0x200000))


</dt> <dd>

Nunca se ha realizado una sincronización correcta desde este origen.

</dd> <dt>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>

<span id="DS_REPL_NBR_PREEMPTED"></span><span id="ds_repl_nbr_preempted"></span>**DS \_ REPL \_ NBR \_ PREEMPTED** (16777216 (0x1000000))


</dt> <dd>

El motor de replicación ha dejado temporalmente de procesar este vecino para dar servicio a otro vecino de mayor prioridad, ya sea para esta partición o para otra partición. El motor de replicación reanudará el procesamiento de este vecino cuando finalice el trabajo de prioridad más alta.

</dd> <dt>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>

<span id="DS_REPL_NBR_IGNORE_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_ignore_change_notifications"></span>**DS \_ REPL \_ NBR \_ OMITIR NOTIFICACIONES \_ DE \_ CAMBIO** (67108864 (0x4000000))


</dt> <dd>

Este vecino está establecido para deshabilitar las sincronizaciones basadas en notificaciones. Dentro de un sitio, los controladores de dominio se sincronizan entre sí basándose en las notificaciones de cambios. Esta configuración impide que este vecino realice sincronizaciones desencadenadas por notificaciones. El vecino seguirá haciendo sincronizaciones según su programación o en respuesta a las sincronizaciones solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>

<span id="DS_REPL_NBR_DISABLE_SCHEDULED_SYNC"></span><span id="ds_repl_nbr_disable_scheduled_sync"></span>**DS \_ REPL \_ NBR \_ DISABLE \_ SCHEDULED \_ SYNC** (134217728 (0x8000000))


</dt> <dd>

Este vecino está establecido para no realizar sincronizaciones en función de su programación. La única manera en que este vecino realizará sincronizaciones es en respuesta a las notificaciones de cambio o a las sincronizaciones solicitadas manualmente.

</dd> <dt>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>

<span id="DS_REPL_NBR_COMPRESS_CHANGES"></span><span id="ds_repl_nbr_compress_changes"></span>**DS \_ CAMBIOS DE \_ COMPRESIÓN DE REPL NBR \_ \_** (268435456 (0x10000000))


</dt> <dd>

Los cambios recibidos de este origen se van a comprimir. Normalmente, la compresión solo se produce si el servidor de origen está en un sitio diferente.

</dd> <dt>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>

<span id="DS_REPL_NBR_NO_CHANGE_NOTIFICATIONS"></span><span id="ds_repl_nbr_no_change_notifications"></span>**DS \_ REPL \_ NBR \_ NO CHANGE \_ \_ NOTIFICATIONS** (536870912 (0x20000000))


</dt> <dd>

No deberían recibirse notificaciones de cambios desde este origen. Normalmente solo se establece si el servidor de origen está en un sitio diferente.

</dd> <dt>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>

<span id="DS_REPL_NBR_PARTIAL_ATTRIBUTE_SET"></span><span id="ds_repl_nbr_partial_attribute_set"></span>**DS \_ CONJUNTO DE ATRIBUTOS PARCIALES DE REPL \_ NBR \_ \_ \_** (1073741824 (0x40000000))


</dt> <dd>

Este vecino está recompilando el contenido de esta réplica debido a un cambio en el conjunto de atributos parciales.

</dd> </dl>

</dd> <dt>

**SourceDsaAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la dirección DNS del controlador de dominio de origen.

> [!Note]  
> Esta cadena contiene un GUID modificado, no el nombre DNS canónico que se usa habitualmente.

 

</dd> <dt>

**SourceDsaCN**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el componente de ruta de acceso del objeto para el DSA que representa el controlador de dominio de origen. Esta cadena suele ser similar al nombre del equipo, pero no siempre es idéntica.

</dd> <dt>

**SourceDsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X.500 para el DSA que representa el controlador de dominio de origen.

</dd> <dt>

**SourceDsaInvocationID**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el identificador de invocación que usó el servidor de origen en la última replicación.

</dd> <dt>

**SourceDsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el GUID del agente de servicio de directorio (DSA) que representa el controlador de dominio (DC) de origen.

</dd> <dt>

**SourceDsaSite**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
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

Obtiene el valor que indica si la marca **\_ DS REPL \_ NBR \_ SYNC ON \_ \_ STARTUP** se ha establecido en la **propiedad ReplicaFlags.**

</dd> <dt>

**TimeOfLastSyncAttempt**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la marca de tiempo del último intento de replicación.

</dd> <dt>

**TimeOfLastSyncSuccess**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
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

Obtiene el valor que indica si se ha establecido la marca **\_ DS REPL \_ NBR \_ TWO WAY \_ \_ SYNC** en la **propiedad ReplicaFlags.**

</dd> <dt>

**UseAsyncIntersiteTransport**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **DS \_ REPL \_ NBR \_ USE \_ ASYNC \_ INTERSITE \_ TRANSPORT** en la **propiedad ReplicaFlags.**

</dd> <dt>

**USNAttributeFilter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el **valor de la propiedad USNLastObjChangeSynced** al final del último ciclo de replicación completado correctamente. Cero si no se completaron correctamente los ciclos de replicación.

</dd> <dt>

**USNLastObjChangeSynced**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint64**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el [**valor de atributo sin**](/windows/desktop/ADSchema/a-usnchanged) cambios de la última actualización de objeto que se recibió.

</dd> <dt>

**Writeable (Grabable)**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor que indica si se ha establecido la marca **\_ \_ REPL NBR \_ WRITEABLE** de DS en la **propiedad ReplicaFlags.**

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

