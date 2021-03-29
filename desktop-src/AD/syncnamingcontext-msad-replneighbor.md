---
title: Método SyncNamingContext de la clase MSAD_ReplNeighbor
description: Llama a la función DsReplicaSync que sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Método SyncNamingContext Active Directory
- Método SyncNamingContext Active Directory, clase MSAD_ReplNeighbor
- MSAD_ReplNeighbor de clase Active Directory, método SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691bd3e943f491ba93d867097ac0167c97be6108
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492178"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Método SyncNamingContext de la \_ clase ReplNeighbor de MSAD

Llama a la función [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) que sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.

## <a name="syntax"></a>Sintaxis


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Datos adicionales que determinan cómo el método procesa la solicitud. Este parámetro puede ser una combinación de los valores siguientes.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**\_ \_ Agregar referencia de REPSYNC de DS \_**


</dt> <dd>

Hace que el agente de sistema de directorio de origen (DSA) Compruebe que el DSA local está presente en la lista replicaciones de origen a. Si el DSA local no está presente, se agrega. Esto garantiza que el origen envíe notificaciones de cambios.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**\_REPSYNC de \_ todos los \_ orígenes de DS**


</dt> <dd>

Este valor no se admite.

**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** Sincroniza desde todos los orígenes.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ operación asincrónica REPSYNC de \_ DS**


</dt> <dd>

Realiza esta operación de forma asincrónica.

**Windows server 2008 R2, Windows server 2008 y Windows server 2003:** Se requiere cuando se usa **DS \_ REPSYNC \_ todos los \_ orígenes**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_fuerza de REPSYNC de DS \_**


</dt> <dd>

Sincroniza aunque el vínculo esté deshabilitado actualmente.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**\_REPSYNC DS \_ completo**


</dt> <dd>

Sincroniza a partir del primer número de secuencia de actualización (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_ \_ mensajería entre sitios de DS REPSYNC \_**


</dt> <dd>

Sincroniza con ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**REPSYNC de DS \_ \_ no \_ descartar**


</dt> <dd>

No descarta esta solicitud de sincronización, aunque esté pendiente una sincronización similar.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**\_REPSYNC DS \_ periódico**


</dt> <dd>

Indica que esta operación es una solicitud de sincronización periódica programada por el administrador.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**REPSYNC de DS \_ \_ urgente**


</dt> <dd>

Indica que esta operación es una notificación de una actualización marcada como urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**\_REPSYNC DS \_ grabable**


</dt> <dd>

Indica que se puede escribir en esta réplica. Si no se establece esta marca, la réplica es de solo lectura.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





