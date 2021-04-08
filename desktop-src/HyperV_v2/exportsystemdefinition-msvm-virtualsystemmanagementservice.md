---
description: Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808378"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ExportSystemDefinition de la \_ clase VirtualSystemManagementService de MSVM

Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo. La máquina virtual debe estar en el estado "apagado" o "guardado" que se va a exportar. La máquina virtual, sus valores de configuración asociados y su configuración de recursos asociada se conservarán en el archivo resultante.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ComputerSystem* \[ de\]
</dt> <dd>

Referencia a un [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ de\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la máquina virtual. Si la propiedad **CreateVmExportSubdirectory** de la [**clase \_ VirtualSystemExportSettingData de MSVM**](msvm-virtualsystemexportsettingdata.md) en el parámetro *ExportSettingData* está establecida en **true**, este directorio se puede reutilizar para exportar varias máquinas virtuales y este método coloca cada definición de máquina virtual en un subdirectorio independiente en esta ruta de acceso.

</dd> <dt>

*ExportSettingData* \[ de\]
</dt> <dd>

Instancia insertada de la clase [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa la configuración de la operación de exportación.

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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

