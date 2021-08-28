---
description: Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.
ms.assetid: 45f1ec8f-aa96-4060-8f8c-0471d0ad4a21
title: Método ApplySnapshot de la clase Msvm_VirtualSystemSnapshotService aplicación
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6a03a76bb874ac63c8684841f3a13e413a193db8b17d85a6cad4dd62e361bc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765605"
---
# <a name="applysnapshot-method-of-the-msvm_virtualsystemsnapshotservice-class"></a>Método ApplySnapshot de la clase Msvm \_ VirtualSystemSnapshotService

Aplica una instantánea de máquina virtual a la máquina virtual desde la que se creó.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ApplySnapshot(
  [in]  CIM_VirtualSystemSettingData REF Snapshot,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Instantánea* \[ En\]
</dt> <dd>

Referencia a una clase derivada de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa la instantánea de máquina virtual que se va a aplicar.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Esta operación siempre se realiza de forma asincrónica. Este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

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

**Tipo no válido** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**Estado no** válido (32775)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemSnapshotService**](msvm-virtualsystemsnapshotservice.md)
</dt> <dt>

[**ApplyVirtualSystemSnapshot (V1)**](/previous-versions/windows/desktop/virtual/applyvirtualsystemsnapshot-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**ApplyVirtualSystemSnapshotEx (V1)**](/previous-versions/windows/desktop/virtual/msvm-virtualsystemmanagementservice-applyvirtualsystemsnapshotex)
</dt> </dl>

 

