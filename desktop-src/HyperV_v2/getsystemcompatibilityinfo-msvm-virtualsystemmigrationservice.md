---
description: Genera un blob opaco de datos que contiene información de compatibilidad para el sistema especificado.
ms.assetid: 5cfb50c4-d695-4867-ac6a-234ce5120a6d
title: Método GetSystemCompatibilityInfo de la Msvm_VirtualSystemMigrationService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.GetSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4866b54bb6f5d5b90d4221b81e8a847e910e4486edc55eb4f932684397072504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118392819"
---
# <a name="getsystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método GetSystemCompatibilityInfo de la clase \_ Msvm VirtualSystemMigrationService

Genera un blob opaco de datos que contiene información de compatibilidad para el sistema especificado. Este método se usa junto con el método [**CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) para determinar si una migración rápida o en vivo de una máquina virtual a otro sistema de equipo host es posible sin intentar realmente la migración.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSystemCompatibilityInfo(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] uint8                  CompatibilityInfo[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a una clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual para la que se recuperará la información de compatibilidad. Si este parámetro hace referencia al sistema del equipo host, los datos devueltos en el parámetro *CompatibilityInfo* se pueden usar para determinar si alguna de las máquinas virtuales del sistema del equipo host se puede migrar rápidamente a otro sistema de equipo host.

</dd> <dt>

*CompatibilityInfo* \[ out\]
</dt> <dd>

Blob opaco de datos que se puede pasar al [**método CheckSystemCompatibilityInfo**](checksystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) en otro sistema de equipo host para confirmar la compatibilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




