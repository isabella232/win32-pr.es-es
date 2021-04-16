---
description: Asocia un servicio a su sistema de hospedaje.
ms.assetid: 888ABA71-6D67-4933-89E6-40F731AA7153
title: Msvm_HostedService (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedService
- Msvm_HostedService.Antecedent
- Msvm_HostedService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 284254d32e788e374d56b3822f5c00868552e1f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686946"
---
# <a name="msvm_hostedservice-class"></a>MSVM \_ HostedService (clase)

Asocia un servicio a su sistema de hospedaje. Las instancias de [**MSVM \_ VirtualizationManagementService**](msvm-virtualsystemmanagementservice.md) se pueden detectar a través de su asociación con un host.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedService : CIM_HostedService
{
  CIM_ManagedElement REF Antecedent;
  CIM_Service        REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ HostedService** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ HostedService** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al sistema del equipo host. Esta propiedad se hereda de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al servicio que se hospeda. Esta propiedad se hereda de [**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ HostedService** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Ejemplos

Consulte [consultar objetos de red](querying-networking-objects.md).

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

[**HostedService de CIM \_**](cim-hostedservice.md)
</dt> <dt>

[**HostedService de CIM \_**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> <dt>

[Clases de administración de sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

