---
description: Quita la máquina virtual definida previamente del ámbito de administración del sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Método DestroySystem de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DestroySystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c41b1f985b55d1f1756d49308ebda4db1beb92264945bd7418bdea4460e4e72b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119254155"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DestroySystem de la clase \_ Msvm VirtualSystemManagementService

Quita la máquina virtual definida previamente del ámbito de administración del sistema host. También se quitarán las definiciones de recursos asociadas. La máquina virtual debe estar apagada o guardada antes de llamar a este método.

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

Tipo: **CIM \_ ComputerSystem**

Referencia a una instancia de [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la instancia de máquina virtual que se va a destruir.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Si este método se ejecuta sincrónicamente, devuelve 0 si se ejecuta correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida *Job* se puede usar para realizar un seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

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

**Parámetros de método activados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la [**clase \_ VirtualSystemManagementService de Msvm**](msvm-virtualsystemmanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se usa **el método DestroySystem** para quitar una máquina virtual planeada. Este código se toma del ejemplo de máquinas virtuales planeadas [de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm). Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Para funcionar correctamente, el código siguiente debe ejecutarse en el servidor host de la máquina virtual y debe ejecutarse con privilegios de administrador.

 


```CSharp
/// <summary>
/// Finds the first Planned VM matching pvmName and removes it.
/// </summary>
/// <param name="pvmName">The name of the PVM to be removed.</param>
internal static void
RemovePvm(
    string pvmName
    )
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\v2");

    using (ManagementObject pvm = WmiUtilities.GetPlannedVirtualMachine(pvmName, scope))
    using (ManagementObject managementService = WmiUtilities.GetVirtualMachineManagementService(scope))
    using (ManagementBaseObject inParams =
        managementService.GetMethodParameters("DestroySystem"))
    {
        inParams["AffectedSystem"] = pvm.Path;

        Console.WriteLine("Removing Planned Virtual Machine \"{0}\" ({1})...",
                pvm["ElementName"], pvm["Name"]);

        using (ManagementBaseObject outParams =
            managementService.InvokeMethod("DestroySystem", inParams, null))
        {
            WmiUtilities.ValidateOutput(outParams, scope);
        }
    }
}
```



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

 

