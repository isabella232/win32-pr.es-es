---
description: Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6eecfefc8c542eeb3a06c509533060f8036d447e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156685"
---
# <a name="msvm_resourcepoolregistration-class"></a>MSVM \_ ResourcePoolRegistration (clase)

Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ResourcePoolRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ResourcePoolRegistration** tiene estas propiedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que describe el objeto COM que implementa esta clase.

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

El acceso a la clase **MSVM \_ ResourcePoolRegistration** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

 

