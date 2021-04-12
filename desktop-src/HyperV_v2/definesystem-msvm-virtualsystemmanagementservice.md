---
description: Crea una nueva instancia de máquina virtual.
ms.assetid: 15BC967D-F392-45A6-ACF6-5C2F2334AAE6
title: Método DefineSystem de la clase Msvm_VirtualSystemManagementService
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
ms.openlocfilehash: 965d24313607a767d546503d005a6493234b2f53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277993"
---
# <a name="definesystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método DefineSystem de la \_ clase VirtualSystemManagementService de MSVM

Crea una nueva instancia de máquina virtual. Las propiedades que no se especifican se rellenarán con los valores predeterminados.

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

*Configuración* \[ de\]
</dt> <dd>

Tipo: **String**

Instancia insertada de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que se usa para definir los atributos de la máquina virtual que se va a crear. Este parámetro es necesario.

</dd> <dt>

*ResourceSettings* \[ de\]
</dt> <dd>

Tipo: **String \[ \]**

Varias instancias incrustadas de la clase [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) (o clases derivadas de ella). Juntas, estas instancias describen los recursos virtuales de la máquina virtual. Se creará un conjunto de dispositivos predeterminado para la máquina virtual, independientemente de si este parámetro está establecido. Por ejemplo, el procesador y la memoria se crean y configuran automáticamente con los valores predeterminados.

</dd> <dt>

*ReferenceConfiguration* \[ de\]
</dt> <dd>

Tipo: **CIM \_ VirtualSystemSettingData**

Una referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que es el objeto de nivel superior de una configuración de máquina virtual de referencia. La configuración de referencia se utiliza para complementar la configuración de la nueva máquina virtual si los parámetros *configuración* y *ResourceSettings* no proporcionaron la información correspondiente.

</dd> <dt>

*ResultingSystem* \[ enuncia\]
</dt> <dd>

Tipo: **CIM \_ ComputerSystem**

Una referencia a una instancia de la clase de [**\_ ComputerSystem de CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representa la máquina virtual recién creada.

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

 

