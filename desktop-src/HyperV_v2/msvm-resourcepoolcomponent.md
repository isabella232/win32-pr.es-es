---
description: Representa un elemento del grupo de recursos de la plataforma Windows Hyper-V de Microsoft.
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 470317d3afd961ad74eb788ebdb70e67617749446fa4a432f40f00f43214cd92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535615"
---
# <a name="msvm_resourcepoolcomponent-class"></a>Clase ResourcePoolComponent de Msvm \_

Representa un elemento del grupo de recursos de la plataforma Windows Hyper-V de Microsoft.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>Miembros

La **clase \_ ResourcePoolComponent de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ResourcePoolComponent de Msvm** tiene estas propiedades.

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase derivada de [**\_ AllocationCapabilities de CIM**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) que describe las funcionalidades de asignación de este grupo de recursos.

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID **que** representa el identificador de clase del objeto COM del servicio. Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Contexto**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contexto en el que se ejecutará el objeto recién creado. Este valor se pasa en el *parámetro dwClsContext* a **CoCreateInstance.** Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en 1.

</dd> <dt>

**Habilitado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; de lo contrario, **False**. Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en **True.**

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Número máximo de grupos de recursos primarios que admite un grupo secundario.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Cadena neutra del idioma que identifica de forma única el elemento. Se sugiere el formato siguiente para evitar conflictos de nomenclatura: "versión del \| componente \| de proveedor". Por ejemplo, este nombre representa la versión 1.0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Esta propiedad se hereda de [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase derivada de [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que implementa el dispositivo físico desde el que este grupo asigna recursos. Esta propiedad puede ser **Null si** la clase de dispositivo virtual asignada desde este grupo es la misma que la clase de dispositivo físico.

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase derivada de [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) que implementa el grupo de recursos.

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase derivada de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) que describe la configuración no relacionada con la asignación del grupo de recursos.

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

GUID **que** representa el identificador de clase del generador de objetos WMI del componente.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ResourcePoolComponent de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Virtualización de \_ MsvmComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Virtualización de \_ MsvmComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

