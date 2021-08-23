---
description: Representa una asociación entre un trabajo y el elemento administrado que puede verse afectado por su ejecución.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f39d800516f96cf602257abc3bd8ed9ed5a8d5561f4b4a5e60f5eb140fc1c308
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693545"
---
# <a name="msvm_affectedjobelement-class"></a>Clase Msvm \_ AffectedJobElement

Representa una asociación entre un trabajo y el elemento administrado que puede verse afectado por su ejecución.

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ AffectedJobElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ AffectedJobElement** tiene estas propiedades.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Elemento administrado afectado por la ejecución del trabajo. Esta propiedad se hereda de [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Trabajo que afecta al elemento administrado. Esta propiedad se hereda de [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Enumeración que describe el efecto en el elemento administrado. Esta propiedad se hereda de [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona detalles sobre el efecto en la posición de la matriz correspondiente en **ElementEffects**. Esta propiedad se hereda de [**CIM \_ AffectedJobElement.**](/previous-versions//cc150663(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ Msvm AffectedJobElement** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ AffectedJobElement**](cim-affectedjobelement.md)
</dt> <dt>

[**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85))
</dt> <dt>

[Clases de administración de sistemas virtuales](virtual-system-management-classes.md)
</dt> </dl>

 

