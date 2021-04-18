---
description: Representa el registro de un servicio en la plataforma de Microsoft Hyper-V.
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e9704dcade0474a10ca60383280941ec2e3591b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686599"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>MSVM \_ VirtualizationComponentRegistration (clase)

Representa el registro de un servicio en la plataforma de Microsoft Hyper-V.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF).

## <a name="syntax"></a>Sintaxis

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualizationComponentRegistration** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualizationComponentRegistration** tiene estas propiedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**
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

Referencia a una instancia de que describe un tipo de recurso admitido por el servicio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ VirtualizationComponentRegistration** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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



 

