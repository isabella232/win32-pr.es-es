---
description: Quita la máquina virtual definida previamente del ámbito de administración del sistema host.
ms.assetid: 16E6EEB0-CB29-4FFC-AEFF-872E099337FA
title: Método DestroySystem de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: 1caf4e4a590bdbfe2f7543e23d5ca00018300fb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911693"
---
# <a name="destroysystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DestroySystem de la \_ clase VirtualSystemManagementService de MSVM

Quita la máquina virtual definida previamente del ámbito de administración del sistema host. También se quitarán las definiciones de recursos asociadas. La máquina virtual debe estar en estado apagado o guardado antes de llamar a este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DestroySystem(
  [in]  CIM_ComputerSystem REF AffectedSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AffectedSystem* \[ de\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Referencia a una instancia del ComputerSystem de [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la instancia de máquina virtual que se va a destruir.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Tipo: **CIM \_ ConcreteJob**

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Si este método se ejecuta sincrónicamente, devuelve 0 si se realiza correctamente. Si este método se ejecuta de forma asincrónica, devuelve 4096 y el parámetro de salida del *trabajo* se puede usar para realizar el seguimiento del progreso de la operación asincrónica. Cualquier otro valor devuelto indica un error.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**No compatible** (1)
</dt> <dt>

**Error** (2)
</dt> <dt>

**Tiempo de espera** (3)
</dt> <dt>

**Parámetro no válido** (4)
</dt> <dt>

**Estado no válido** (5)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (de no.. 32767)
</dt> <dt>

**Específico del proveedor** (32768... 65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase [**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se usa el método **DestroySystem** para quitar una máquina virtual planeada. Este código se toma del [ejemplo de máquinas virtuales planeadas de Hyper-V](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Hyper-V/Pvm). Las utilidades a las que se hace referencia se pueden encontrar en [utilidades comunes para los ejemplos de virtualización (V2)](common-utilities-for-the-virtualization-samples-v2.md).

> [!IMPORTANT]
> Para que funcione correctamente, se debe ejecutar el código siguiente en el servidor host de máquina virtual y se debe ejecutar con privilegios de administrador.

 


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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

