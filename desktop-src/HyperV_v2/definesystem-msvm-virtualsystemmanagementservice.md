---
description: Crea una nueva instancia de máquina virtual.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Método DefineSystem de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 47b01a2fb0935873b5a36d69376eb09bfe6d4555613c0eb8dc8907589d4f5f7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118645839"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DefineSystem de la clase Msvm \_ VirtualSystemManagementService

Crea una nueva instancia de máquina virtual. Las propiedades que no se especifican se rellenarán con valores predeterminados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SystemSettings* \[ En\]
</dt> <dd>

Tipo: **cadena**

Instancia incrustada de la [**clase Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que se usa para definir los atributos de la máquina virtual que se va a crear. Este parámetro es obligatorio.

</dd> <dt>

*ResourceSettings* \[ En\]
</dt> <dd>

Tipo: **\[ \] cadena**

Número de instancias insertadas de la clase [**\_ ResourceAllocationSettingData de Msvm**](msvm-resourceallocationsettingdata.md) (o clases derivadas de la misma). Juntas, estas instancias describen los recursos virtuales de la máquina virtual. Se creará un conjunto predeterminado de dispositivos para la máquina virtual, independientemente de si se establece este parámetro. Por ejemplo, el procesador y la memoria se crean y configuran automáticamente con valores predeterminados.

</dd> <dt>

*ReferenceConfiguration* \[ En\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Referencia a una instancia de la clase [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración de máquina virtual de referencia. La configuración de referencia se usa para complementar la configuración de la nueva máquina virtual si los parámetros *SystemSettings* y *ResourceSettings* no proporcionaron la información respectiva.

</dd> <dt>

*ResultingSystem* \[ out\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Referencia a una instancia de la clase [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual recién creada.

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

**DMTF reservado** (..)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Método reservado** (4097..32767)
</dt> <dt>

**Específico del** proveedor (32768..65535)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a [**la clase \_ VirtualSystemManagementService de Msvm**](msvm-virtualsystemmanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

 

