---
description: Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada.
ms.assetid: bddbdc35-4603-45c3-96b4-04f445dbb3a6
title: Método RealizePlannedSystem de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RealizePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fc69cbc9be9fc72bc7c1184ec30d9e2b58ba2b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278618"
---
# <a name="realizeplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RealizePlannedSystem de la \_ clase VirtualSystemManagementService de MSVM

Valida la configuración de una máquina virtual planeada y la convierte en una máquina virtual realizada. Los archivos de estado en tiempo de ejecución o guardados asociados a la máquina virtual se copiarán del directorio de importación a la raíz de datos de la máquina virtual, si procede.

## <a name="syntax"></a>Sintaxis


```mof
uint32 RealizePlannedSystem(
  [in]  Msvm_PlannedComputerSystem REF PlannedSystem,
  [out] CIM_ComputerSystem         REF ResultingSystem,
  [out] CIM_ConcreteJob            REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PlannedSystem* \[ de\]
</dt> <dd>

Referencia a la instancia de [**MSVM \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que se va a convertir en una máquina virtual realizada.

</dd> <dt>

*ResultingSystem* \[ enuncia\]
</dt> <dd>

Si la operación se completa de forma sincrónica, se trata de una referencia a un objeto [**\_ ComputerSystem de CIM**](msvm-computersystem.md) que representa la máquina virtual resultante.

DataType actualizado de [**MSVM \_ ComputerSystem**](msvm-computersystem.md) en Windows 10, versión 1703.

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

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se usa el método **RealizePlannedSystem** para obtener una máquina virtual planeada. Este código se toma del [ejemplo de máquinas virtuales planeadas de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm). Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and realizes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be realized.</param>
/// <returns>The Realized Virtual Machine.</returns>
internal static ManagementObject
RealizePvm(
    string pvmName
    )
{
    ManagementObject vm = null;
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("RealizePlannedSystem"))
    {
        inParams["PlannedSystem"] = pvm.Path;

        Console.WriteLine("Realizing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("RealizePlannedSystem", inParams, null))
        {
            if (WmiUtilities.ValidateOutput(outParams, scope, true, true))
            {
                using (ManagementObject job =
                    new ManagementObject((string)outParams["Job"]))
                using (ManagementObjectCollection pvmCollection =
                    job.GetRelated("Msvm_ComputerSystem",
                        "Msvm_AffectedJobElement", null, null, null, null, false, null))
                {
                    vm = WmiUtilities.GetFirstObjectFromCollection(pvmCollection);
                }
            }
        }
    }

    return vm;
}
```



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

 

