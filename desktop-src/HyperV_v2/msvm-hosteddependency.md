---
description: Asocia una instancia de máquina virtual con el objeto de sistema de equipo que representa el sistema de hospedaje físico.
ms.assetid: 755624D7-04D0-47EA-8623-DEDE6B1D5CBC
title: Msvm_HostedDependency clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedDependency
- Msvm_HostedDependency.Antecedent
- Msvm_HostedDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0c67df565be0085d4579bf82b2a2d2e542f856e93321240821bc512be692c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014523"
---
# <a name="msvm_hosteddependency-class"></a>Clase \_ HostedDependency de Msvm

Asocia una instancia de máquina virtual con el objeto de sistema de equipo que representa el sistema de hospedaje físico.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedDependency : CIM_HostedDependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ HostedDependency de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ HostedDependency de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al sistema del equipo host. Esta propiedad se hereda de [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual. Esta propiedad se hereda de [**CIM \_ HostedDependency.**](/previous-versions//cc136861(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ HostedDependency de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ HostedDependency**](cim-hosteddependency.md)
</dt> <dt>

[**CIM \_ HostedDependency**](/previous-versions//cc136861(v=vs.85))
</dt> <dt>

[Clases de administración de sistemas virtuales](virtual-system-management-classes.md)
</dt> </dl>

 

