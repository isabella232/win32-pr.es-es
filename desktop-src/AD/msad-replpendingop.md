---
title: MSAD_ReplPendingOp (clase)
description: Representa la estructura de operaciones de REPL de DS \_ \_ , que describe una tarea de replicación que se está ejecutando actualmente o está pendiente de ejecución.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp clase Active Directory
- Active Directory de MSAD_ReplPendingOp de clase, se describe
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422324"
---
# <a name="msad_replpendingop-class"></a>MSAD \_ ReplPendingOp (clase)

Representa la estructura de [**\_ \_ operaciones de REPL de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , que describe una tarea de replicación que se está ejecutando actualmente o está pendiente de ejecución. La función [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) devuelve esta estructura.

## <a name="syntax"></a>Sintaxis

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a>Miembros

La clase **MSAD \_ ReplPendingOp** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSAD \_ ReplPendingOp** tiene estas propiedades.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la dirección de red específica del transporte del servidor remoto que está asociado a esta operación. Es **null** si no hay ningún servidor remoto asociado a esta operación.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X. 500 del DSA asociado al servidor remoto que corresponde a esta operación. **Es null** si no hay ningún servidor remoto que se corresponda con esta operación.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor del atributo [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) del DSA identificado por la propiedad **DsaDN** .

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X. 500 del contexto de nomenclatura (NC) que está asociado a esta operación.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el atributo [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) del NC identificado por la propiedad **NamingContextDN** .

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la hora a la que se inició la operación. Es **null** si esta operación todavía está en la cola.

</dd> <dt>

**Opciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el conjunto de marcadores que proporciona datos adicionales sobre la operación. El contenido de este miembro viene determinado por el valor de la propiedad **OpType** .

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_sincronización de \_ tipo de operación de REPL de DS \_ \_**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores ** \_ DS \_ \* REPSYNC* _ definidos para el parámetro _Options * en [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**\_ \_ Agregar tipo de operación de replicación de \_ DS \_**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores ** \_ DS \_ \* REPADD* _ definidos para el parámetro _Options * en [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**tipo de operación de REPL de DS \_ \_ \_ \_ Delete**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores ** \_ DS \_ \* REPDEL* _ definidos para el parámetro _Options * en [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**tipo de operación de REPL de DS \_ \_ \_ \_ modificar**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores ** \_ DS \_ \* REPMOD* _ definidos para el parámetro _Options * en [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_referencias de \_ actualización del tipo de operación de replicación de \_ \_ DS \_**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores ** \_ DS \_ \* REPSUPD* _ definidos para el parámetro _Options * en [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor de [**\_ \_ \_ tipo**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) de operación de replicación de DS que indica el tipo de operación que esta clase representa.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la posición de esta operación en la cola.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la prioridad de esta operación. Las tareas de prioridad más alta se ejecutan en primer lugar. El servidor calcula la prioridad basándose en el tipo de operación que esta clase representa y en los parámetros de la operación.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el identificador de la operación, que es único por equipo y por arranque.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la hora a la que se agregó esta operación a la cola.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\MicrosoftActiveDirectory raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

