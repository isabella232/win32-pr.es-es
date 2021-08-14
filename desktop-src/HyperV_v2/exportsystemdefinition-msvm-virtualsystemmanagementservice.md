---
description: Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo.
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Método ExportSystemDefinition de la Msvm_VirtualSystemManagementService clase
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
ms.openlocfilehash: 72198055a81ce13a6b38859ed5ba6370faf7de046bc9f2cc3a158548c2679685
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254045"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método ExportSystemDefinition de la clase Msvm \_ VirtualSystemManagementService

Exporta una máquina virtual, o una instantánea de una máquina virtual, a un archivo. La máquina virtual debe estar en el estado "apagado" o "guardado" para exportarse. La máquina virtual, sus opciones de configuración asociadas y sus valores de recursos asociados se conservarán en el archivo resultante.

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

*ComputerSystem* \[ En\]
</dt> <dd>

Referencia a un sistema [**\_ de equipos CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual que se va a exportar.

</dd> <dt>

*ExportDirectory* \[ En\]
</dt> <dd>

Ruta de acceso completa del directorio al que se va a exportar la máquina virtual. Si la propiedad **CreateVmExportSubdirectory** de la clase [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) del *parámetro ExportSettingData* está establecida en **True,** este directorio se puede reutilizar para exportar varias máquinas virtuales y este método coloca cada definición de máquina virtual en un subdirectorio independiente bajo esta ruta de acceso.

</dd> <dt>

*ExportSettingData* \[ En\]
</dt> <dd>

Instancia incrustada de la [**clase Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) que representa la configuración de la operación de exportación.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ CIM ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

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

 

