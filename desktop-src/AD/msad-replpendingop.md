---
title: MSAD_ReplPendingOp clase
description: Representa la estructura DS REPL OP, que describe una tarea de replicación que se está \_ ejecutando actualmente o pendiente de \_ ejecución.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp clase Active Directory
- MSAD_ReplPendingOp clase Active Directory , descrita
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
ms.openlocfilehash: 164c5ebe672a52bb399727940e5e51b98904f7db322cc362425dabda25f547a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186080"
---
# <a name="msad_replpendingop-class"></a>Clase \_ ReplPendingOp de MSAD

Representa la [**estructura DS \_ REPL \_ OP,**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) que describe una tarea de replicación que se está ejecutando actualmente o pendiente de ejecución. La función [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) devuelve esta estructura.

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

La **clase \_ ReplPendingOp de MSAD** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ReplPendingOp de MSAD** tiene estas propiedades.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la dirección de red específica del transporte del servidor remoto asociado a esta operación. **NULL** si no hay ningún servidor remoto asociado a esta operación.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X.500 del DSA que está asociada al servidor remoto que corresponde a esta operación. **NULL** si ningún servidor remoto corresponde a esta operación.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el valor del [**atributo objectGuid**](/windows/desktop/ADSchema/a-objectguid) del DSA identificado por la **propiedad DsaDN.**

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la ruta de acceso X.500 del contexto de nomenclatura (NC) asociado a esta operación.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el [**atributo objectGuid**](/windows/desktop/ADSchema/a-objectguid) del NC identificado por la **propiedad NamingContextDN.**

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la hora a la que se inició la operación. **NULL** si esta operación sigue en la cola.

</dd> <dt>

**Opciones**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el conjunto de marcas que proporciona datos adicionales sobre la operación. El contenido de este miembro viene determinado por el valor de la **propiedad OpType.**

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS \_ REPL \_ OP \_ TYPE \_ SYNC**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores **DS \_ \_ \* REPSYNC* _ definidos para el parámetro _Options* en [**DsReplicaSync.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS \_ REPL \_ OP \_ TYPE \_ ADD**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores **DS \_ REPADD \_ \** _ definidos para el parámetro _Options* en [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS \_ REPL \_ OP \_ TYPE \_ DELETE**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores **DS \_ REPDEL \_ \** _ definidos para el parámetro _Options* en [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**MODIFICACIÓN DEL \_ TIPO DE OPERACIÓN DE REPL \_ \_ de \_ DS**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores **DS \_ \_ \* REPMOD* _ definidos para el parámetro _Options* en [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**REFERENCIA DE ACTUALIZACIÓN \_ DEL TIPO DE OPERACIÓN DE REPL de \_ \_ \_ \_ DS**


</dt> <dd>

Contiene cero o una combinación de uno o varios de los valores **DS \_ \_ \* REPSUPD* _ definidos para el parámetro _Options* en [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene el [**valor DS \_ REPL \_ OP \_ TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) que indica el tipo de operación que representa esta clase.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la posición de esta operación en la cola.

</dd> <dt>

**Prioridad**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la prioridad de esta operación. Las tareas de prioridad más alta se ejecutan primero. El servidor calcula la prioridad en función del tipo de operación que representa esta clase y de los parámetros de la operación.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtiene el identificador de la operación, que es único por equipo y por arranque.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Obtiene la hora a la que se agregó esta operación a la cola.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

