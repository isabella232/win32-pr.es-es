---
description: Quita las subredes de la red de migración del servicio de migración del sistema virtual.
ms.assetid: 6ae8de07-552b-4525-8806-bfb9da73bd42
title: Método RemoveNetworkSettings de la clase Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.RemoveNetworkSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66b7a9fd1ce29d9dd645242ec7cda346f79a6f0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686928"
---
# <a name="removenetworksettings-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método RemoveNetworkSettings de la \_ clase VirtualSystemMigrationService de MSVM

Quita las subredes de la red de migración del servicio de migración del sistema virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RemoveNetworkSettings(
  [in]  Msvm_VirtualSystemMigrationNetworkSettingData REF NetworkSettings[],
  [out] CIM_ConcreteJob                               REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NetworkSettings* \[ de\]
</dt> <dd>

Una matriz de instancias incrustadas de la clase [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que representan las subredes de red que se van a quitar.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AddNetworkSettings**](addnetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**ModifyNetworkSettings**](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> <dt>

[**MSVM \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

