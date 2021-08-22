---
description: Asociación genérica que se usa para establecer parte de las relaciones entre los elementos administrados.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24b813e7b8460f3de24207ed91b2e113f0d6b9633e17263806ef8447c166bdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531755"
---
# <a name="msvm_concretecomponent-class"></a>Clase ConcreteComponent de Msvm \_

Asociación genérica que se usa para establecer relaciones "parte de" entre elementos administrados. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) se define como una subclase concreta de la clase [**abstracta CIM \_ Component,**](/windows/desktop/CIMWin32Prov/cim-component) que se usará en lugar de muchas subclases específicas de componente que no agregan semántica (es decir, subclases que no aclaran el tipo de composición, actualizan las cardinalidades o agregan o quitan calificadores).

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ ConcreteComponent de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ConcreteComponent de Msvm** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento primario de la asociación. Esta propiedad se hereda de [**CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento secundario de la asociación. Esta propiedad se hereda de [**CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ConcreteComponent de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ConcreteComponent**](cim-concretecomponent.md)
</dt> <dt>

[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Clases de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

