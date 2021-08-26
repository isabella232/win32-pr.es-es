---
description: Destruye un sistema virtual.
ms.assetid: 8d2504dc-ce23-4257-9dfd-6a35dfd84b2d
title: Método DestroySystem de la CIM_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fa7bf479e1e861e8425376fa0ebb610cd0b728cc9f02ba80acc9c1faa284fc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980555"
---
# <a name="destroysystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método DestroySystem de la clase \_ CIM VirtualSystemManagementService

Destruye un sistema virtual.

El sistema virtual al que se hace referencia se destruye, incluidos los elementos que tiene como ámbito. Los recursos virtuales se devuelven a sus grupos de recursos, lo que puede implicar la destrucción de esos recursos (dependiente de la implementación). Si el sistema virtual está activo cuando se invoca la operación, primero se desactiva y, a continuación, se destruye. Si las instantáneas se crearon desde el sistema virtual, también se destruyen.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSystem* \[ En\]
</dt> <dd>

Referencia a una instancia de la clase [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema de equipo virtual que se va a destruir.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación es de larga duración, opcionalmente se puede devolver [**un \_ concretejob CIM**](cim-concretejob.md) que representa el trabajo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un 0 si se ejecuta correctamente; de lo contrario, devuelve un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de** espera (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




