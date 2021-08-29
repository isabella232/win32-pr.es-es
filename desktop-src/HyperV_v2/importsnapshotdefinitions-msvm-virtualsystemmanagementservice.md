---
description: Busca en la carpeta especificada los archivos de definición de instantánea asociados al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.
ms.assetid: d240c24b-f788-4ea9-b3bd-af1f75f4f460
title: Método ImportSnapshotDefinitions de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSnapshotDefinitions
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9cfa20eb845546f58201bdc167cfbe38bd4a3bd0ad327a04e009db4504ce0966
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694595"
---
# <a name="importsnapshotdefinitions-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ImportSnapshotDefinitions de la clase \_ Msvm VirtualSystemManagementService

Busca en la carpeta especificada los archivos de definición de instantánea asociados al sistema de equipo planeado especificado y crea una nueva instantánea en el sistema del equipo planeado para cada archivo de definición asociado en esta ubicación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportSnapshotDefinitions(
  [in]  Msvm_PlannedComputerSystem    REF PlannedSystem,
  [in]  string                            SnapshotFolder,
  [out] Msvm_VirtualSystemSettingData REF ImportedSnapshots[],
  [out] CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PlannedSystem* \[ En\]
</dt> <dd>

Referencia a un objeto [**\_ Msvm PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa la máquina virtual planeada que hace referencia a las instantáneas que se importarán.

</dd> <dt>

*SnapshotFolder* \[ En\]
</dt> <dd>

Ruta de acceso completa a la carpeta donde se pueden encontrar las configuraciones de instantáneas para esta máquina virtual.

</dd> <dt>

*ImportedSnapshots* \[ out\]
</dt> <dd>

Si la operación se completa sincrónicamente, una matriz de referencias a las instancias de [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representan las instantáneas que se importaron correctamente.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo en uso** (32779)
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

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

