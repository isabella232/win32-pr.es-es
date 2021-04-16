---
description: Registra un servicio que proporciona objetos relacionados con recursos específicos de la máquina virtual.
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540275"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>MSVM \_ VirtualSystemResourceRegistration (clase)

Registra un servicio que proporciona objetos relacionados con recursos específicos de la máquina virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualSystemResourceRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualSystemResourceRegistration** tiene estas propiedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que describe el objeto COM que implementa esta clase.

</dd> <dt>

**IsRootDevice**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

**True** si este registro indica si el tipo de recurso especificado es el dispositivo raíz (o el primario menos) para este servicio; en caso contrario, **false**. Solo puede existir un registro cuando **IsRootDevice** está establecido en **true**. De lo contrario, este registro representa una asignación a un subdispositivo. Esta propiedad siempre se establece en **false**.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que describe un tipo de recurso admitido por el servicio. Esta propiedad se hereda de [**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ VirtualSystemResourceRegistration** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Fin de compatibilidad de cliente<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ VirtualizationComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**MSVM \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

