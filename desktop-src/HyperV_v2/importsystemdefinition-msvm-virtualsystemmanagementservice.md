---
description: Crea un nuevo sistema informático planeado basado en la definición de máquina virtual especificada.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Método ImportSystemDefinition de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ImportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ee8dd5bb7d17684216b747717c0adf32011dafa543f05c91a0c1264da89caf2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118149743"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ImportSystemDefinition de la clase \_ Msvm VirtualSystemManagementService

Crea un nuevo sistema informático planeado basado en la definición de máquina virtual especificada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ImportSystemDefinition(
  [in]  string                         SystemDefinitionFile,
  [in]  string                         SnapshotFolder,
  [in]  boolean                        GenerateNewSystemIdentifier,
  [out] Msvm_PlannedComputerSystem REF ImportedSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SystemDefinitionFile* \[ En\]
</dt> <dd>

Ruta de acceso completa al archivo de definición del sistema (.xml o .exp) que representa la máquina virtual que se va a importar. El archivo de definición no debe estar ya en uso por el sistema host o la plataforma de virtualización.

</dd> <dt>

*SnapshotFolder* \[ En\]
</dt> <dd>

Ruta de acceso completa a la carpeta donde se pueden encontrar las configuraciones de instantáneas para esta máquina virtual. Se buscará en esta carpeta para buscar las instantáneas a las que hace referencia la definición de máquina virtual. Las instantáneas a las que no se hace referencia en esta ubicación deben eliminarse mediante el método [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importarse mediante el [**método ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) antes de realizar el sistema informático planeado.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ En\]
</dt> <dd>

Indica si se debe volver a usar el identificador único para la máquina virtual. Si este parámetro es **True**, se genera un nuevo identificador del sistema. Si este parámetro es **False**, se usa el identificador del sistema existente.

</dd> <dt>

*ImportedSystem* \[ out\]
</dt> <dd>

Si la operación se completa sincrónicamente, una referencia a un objeto [**\_ Msvm PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa la máquina virtual importada.

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
| Cliente mínimo compatible<br/> | Windows 8 \[ solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

