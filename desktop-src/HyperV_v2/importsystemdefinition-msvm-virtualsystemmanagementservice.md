---
description: Crea un nuevo sistema de equipo planeado basado en la definición de máquina virtual especificada.
ms.assetid: 885d399f-5bcf-4f34-b2f1-582cbfcd7c10
title: Método ImportSystemDefinition de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: bb38ab343a3d92fabd1dc44ed100d2d2f7f7bf01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687199"
---
# <a name="importsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ImportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM

Crea un nuevo sistema de equipo planeado basado en la definición de máquina virtual especificada.

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

*SystemDefinitionFile* \[ de\]
</dt> <dd>

Ruta de acceso completa al archivo de definición del sistema (. XML o. exp) que representa la máquina virtual que se va a importar. El sistema host o la plataforma de virtualización no deben usar el archivo de definición.

</dd> <dt>

*SnapshotFolder* \[ de\]
</dt> <dd>

Ruta de acceso completa a la carpeta donde se pueden encontrar las configuraciones de instantáneas para esta máquina virtual. Se buscará en esta carpeta para buscar las instantáneas a las que hace referencia la definición de la máquina virtual. Todas las instantáneas a las que se hace referencia que no se encuentren en esta ubicación se deben eliminar con el método [**DestroySnapshot**](destroysnapshot-msvm-virtualsystemsnapshotservice.md) o importarse mediante el método [**ImportSnapshotDefinitions**](importsnapshotdefinitions-msvm-virtualsystemmanagementservice.md) antes de realizar el sistema planeado del equipo.

</dd> <dt>

*GenerateNewSystemIdentifier* \[ de\]
</dt> <dd>

Indica si se debe reutilizar el identificador único de la máquina virtual. Si este parámetro es **true**, se genera un nuevo identificador de sistema. Si este parámetro es **false**, se usa el identificador del sistema existente.

</dd> <dt>

*ImportedSystem* \[ enuncia\]
</dt> <dd>

Si la operación se completa de forma sincrónica, se trata de una referencia a un objeto [**\_ PlannedComputerSystem de MSVM**](msvm-plannedcomputersystem.md) que representa la máquina virtual importada.

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
</dt> <dt>

**Archivo en uso** (32779)
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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

