---
title: Método SyncNamingContext de la MSAD_ReplNeighbor clase
description: Llama a la función DsReplicaSync que sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Método SyncNamingContext Active Directory
- Método SyncNamingContext Active Directory , MSAD_ReplNeighbor clase
- MSAD_ReplNeighbor clase Active Directory , método SyncNamingContext
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
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024673"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Método SyncNamingContext de la clase ReplNeighbor de MSAD \_

Llama a [**la función DsReplicaSync que**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) sincroniza un contexto de nomenclatura de destino con uno de sus orígenes.

## <a name="syntax"></a>Sintaxis


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Opciones* \[ En\]
</dt> <dd>

Datos adicionales que determinan cómo procesa el método la solicitud. Este parámetro puede ser una combinación de los valores siguientes.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**REFERENCIA DE ADICIÓN \_ DE REPSYNC \_ DE DS \_**


</dt> <dd>

Hace que el agente del sistema de directorios de origen (DSA) compruebe que el DSA local está presente en la lista de replicaciones a de origen. Si el DSA local no está presente, se agrega. Esto garantiza que el origen envía notificaciones de cambio.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**DS \_ REPSYNC \_ ALL \_ SOURCES**


</dt> <dd>

Este valor no se admite.

**Windows Server 2008 R2, Windows Server 2008 y Windows Server 2003:** Sincroniza desde todos los orígenes.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**OPERACIÓN ASINCRÓNICA \_ DE REPSYNC \_ DE DS \_**


</dt> <dd>

Realiza esta operación de forma asincrónica.

**Windows Server 2008 R2, Windows Server 2008 y Windows Server 2003:** Obligatorio cuando se **usa DS \_ REPSYNC \_ ALL \_ SOURCES**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**DS \_ REPSYNC \_ FORCE**


</dt> <dd>

Se sincroniza incluso si el vínculo está deshabilitado actualmente.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**DS \_ REPSYNC \_ FULL**


</dt> <dd>

Se sincroniza a partir del primer número de secuencia de actualización (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**MENSAJERÍA ENTRE SITIOS \_ DE REPSYNC \_ DE DS \_**


</dt> <dd>

Se sincroniza mediante un ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**DS \_ REPSYNC \_ NO \_ DISCARD**


</dt> <dd>

No descarta esta solicitud de sincronización, incluso si hay una sincronización similar pendiente.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**DS \_ REPSYNC \_ PERIODIC**


</dt> <dd>

Indica que esta operación es una solicitud de sincronización periódica programada por el administrador.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**DS \_ REPSYNC \_ URGENT**


</dt> <dd>

Indica que esta operación es una notificación de una actualización marcada como urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**DS \_ REPSYNC \_ WRITEABLE**


</dt> <dd>

Indica que esta réplica se puede escribir. Si no se establece esta marca, la réplica es de solo lectura.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





