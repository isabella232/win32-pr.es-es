---
description: Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration clase
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
ms.openlocfilehash: bbcb0f2e3d5b0dfad884572c90f889d28e47fcffaf328b39d78f02d4c2baa3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535484"
---
# <a name="msvm_resourcepoolregistration-class"></a>Clase \_ ResourcePoolRegistration de Msvm

Registra un servicio que proporciona objetos globales relacionados con el grupo de recursos.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>Miembros

La **clase \_ ResourcePoolRegistration de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ResourcePoolRegistration de Msvm** tiene estas propiedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que describe el objeto COM que implementa esta clase.

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de que describe un tipo de recurso admitido por el servicio. Esta propiedad se hereda de [**Msvm \_ VirtualizationComponentRegistration.**](msvm-virtualizationcomponentregistration.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ResourcePoolRegistration de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

[**Virtualización de \_ MsvmComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Virtualización de \_ MsvmComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

