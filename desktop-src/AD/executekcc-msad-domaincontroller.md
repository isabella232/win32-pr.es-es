---
title: Método ExecuteKCC de la clase MSAD_DomainController
description: Llama a la función DsReplicaConsistencyCheck, que invoca el comprobador de coherencia de la información (KCC) para comprobar la topología de replicación.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Método ExecuteKCC Active Directory
- Método ExecuteKCC Active Directory, clase MSAD_DomainController
- MSAD_DomainController de clase Active Directory, método ExecuteKCC
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
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658241"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Método ExecuteKCC de la \_ clase MSAD DomainController

Llama a la función [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , que invoca el comprobador de coherencia de la información (KCC) para comprobar la topología de replicación.

## <a name="syntax"></a>Sintaxis


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TaskID* \[ de\]
</dt> <dd>

Tarea que el KCC debe ejecutar. **DS \_ La \_ \_ \_ topología de actualización de TASKID de KCC** es el único valor que se admite actualmente.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un conjunto de marcas que modifican el comportamiento del método **ExecuteKCC** . Este parámetro puede ser cero o una combinación de uno o varios de los valores siguientes.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**marca de KCC de DS \_ \_ \_ \_ OP asincrónica**


</dt> <dd>

La tarea se pone en cola y, a continuación, la función devuelve sin esperar a que se complete la tarea.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**marca de KCC de DS \_ \_ \_ atenuada**


</dt> <dd>

La tarea no se agregará a la cola si otra tarea en cola se ejecutará pronto.

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

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





