---
description: Asocia un dispositivo lógico al sistema primario.
ms.assetid: 2BEAAEC8-F8F2-4CC7-A209-EE3EE3C6FA90
title: Msvm_SystemDevice (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemDevice
- Msvm_SystemDevice.GroupComponent
- Msvm_SystemDevice.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: be31a51ad4e24bd31785e64400bf5b266624d8d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652373"
---
# <a name="msvm_systemdevice-class"></a>MSVM \_ SystemDevice (clase)

Un sistema puede agregar dispositivos lógicos. Esta relación se hace explícita mediante la Asociación de dispositivos del sistema.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemDevice : CIM_SystemDevice
{
  CIM_System        REF GroupComponent;
  CIM_LogicalDevice REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SystemDevice** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SystemDevice** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Sistema primario de la asociación. Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Dispositivo lógico que es un elemento de un sistema. Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ SystemDevice** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dt>

[**\_SYSTEMDEVICE CIM**](/windows/desktop/CIMWin32Prov/cim-systemdevice)
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

