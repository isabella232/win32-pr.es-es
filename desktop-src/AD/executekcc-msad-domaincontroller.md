---
title: Método ExecuteKCC de la MSAD_DomainController clase
description: Llama a la función DsReplicaConsistencyCheck, que invoca el Corrector de coherencia de conocimiento (KCC) para comprobar la topología de replicación.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Método ExecuteKCC Active Directory
- Método ExecuteKCC Active Directory , MSAD_DomainController clase
- MSAD_DomainController clase Active Directory , método ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48295638f105b79ea24a55965ca3ec75ee0ad6b9982c74664f8bfecdd0681cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189627"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Método ExecuteKCC de la clase \_ DomainController de MSAD

Llama a [**la función DsReplicaConsistencyCheck,**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) que invoca el Corrector de coherencia de conocimiento (KCC) para comprobar la topología de replicación.

## <a name="syntax"></a>Sintaxis


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TaskID* \[ En\]
</dt> <dd>

Tarea que KCC debe ejecutar. **DS \_ KCC \_ TASKID \_ UPDATE \_ TOPOLOGY** es el único valor que se admite actualmente.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Conjunto de marcas que modifican el comportamiento del **método ExecuteKCC.** Este parámetro puede ser cero o una combinación de uno o varios de los valores siguientes.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**DS \_ KCC \_ FLAG \_ ASYNC \_ OP**


</dt> <dd>

La tarea se pone en cola y, a continuación, la función vuelve sin esperar a que se complete la tarea.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**MARCA \_ KCC DS \_ \_ DESERIDA**


</dt> <dd>

La tarea no se agregará a la cola si pronto se ejecutará otra tarea en cola.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz \\ MicrosoftActiveDirectory<br/>                                               |
| MOF<br/>                      | <dl> <dt>Replprov.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DomainController de MSAD \_**](msad-domaincontroller.md)
</dt> </dl>

 

 





