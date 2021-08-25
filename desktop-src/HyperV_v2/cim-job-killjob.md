---
description: Método para eliminar este trabajo y los procesos subyacentes, y para quitar las asociaciones de dominio. Este método está en desuso; use RequestChangeState en su lugar.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Método KillJob de la CIM_Job clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 681d6a878f90f29708812fce2c39f27024ed588deb5f3b8066cc4833487fd91f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900335"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Método KillJob de la clase \_ Job de CIM

Método para eliminar este trabajo y los procesos subyacentes, y para quitar las asociaciones de "dominio". Este método está en desuso; use **RequestChangeState en** su lugar. **KillJob** está en desuso porque no hay ninguna distinción entre un apagado orden y una eliminación inmediata. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() proporciona las opciones "Terminate" y "Kill" para permitir esta distinción.

## <a name="syntax"></a>Sintaxis


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DeleteOnKill* \[ En\]
</dt> <dd>

Indica si el trabajo se debe eliminar automáticamente al finalizar. Este parámetro tiene prioridad sobre la **propiedad DeleteOnCompletion.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Desconocido** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Acceso denegado** (6)
</dt> <dt>

**No encontrado** (7)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Trabajo \_ cim**](cim-job.md)
</dt> </dl>

 

 




