---
description: Método para eliminar este trabajo y los procesos subyacentes, y para quitar las asociaciones pendientes. Este método está en desuso; Use RequestChangeState en su lugar.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Método KillJob de la clase CIM_Job
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
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001776"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Método KillJob de la \_ clase de trabajo CIM

Un método para eliminar este trabajo y los procesos subyacentes, y para quitar cualquier asociación "pendiente". Este método está en desuso; Use **RequestChangeState** en su lugar. **KillJob** está en desuso porque no se realiza ninguna distinción entre un cierre ordenado y una eliminación inmediata. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() proporciona las opciones ' Terminate ' y ' Kill ' para permitir esta distinción.

## <a name="syntax"></a>Sintaxis


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DeleteOnKill* \[ de\]
</dt> <dd>

Indica si el trabajo debe eliminarse automáticamente tras la terminación. Este parámetro tiene prioridad sobre la propiedad **DeleteOnCompletion** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Desconocido** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Error** (4)
</dt> <dt>

**Acceso denegado** (6)
</dt> <dt>

**No encontrado** (7)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Trabajo de CIM \_**](cim-job.md)
</dt> </dl>

 

 




