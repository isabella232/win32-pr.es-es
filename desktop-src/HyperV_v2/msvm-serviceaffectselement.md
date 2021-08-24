---
description: Asocia una instancia de máquina virtual al servicio de administración que controla su estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db9ab0ff0aa3eab6f0268f7e85cb5f4efd0e7d2624c7e97a95abb3dd3b414ab2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582285"
---
# <a name="msvm_serviceaffectselement-class"></a>Clase \_ ServiceAffectsElement de Msvm

Asocia una instancia de máquina virtual al servicio de administración que controla su estado.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Miembros

La **clase \_ ServiceAffectsElement de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ServiceAffectsElement de Msvm** tiene estas propiedades.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual. Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Servicio CIM \_**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al servicio que controla la máquina virtual. Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de control que representa la asociación. Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre se establece en el siguiente valor.



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Administra<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Detalles del tipo de asociación en la posición de la matriz correspondiente en la matriz de propiedades **ElementAffects.** Esta información es necesaria si **ElementAffects** está establecido en 1 (Otros). Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre se establece en **Null.**

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ServiceAffectsElement de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**CIM \_ ServiceAffectsElement**](cim-serviceaffectselement.md)
</dt> <dt>

[**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

