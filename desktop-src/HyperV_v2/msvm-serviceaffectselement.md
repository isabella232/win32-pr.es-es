---
description: Asocia una instancia de máquina virtual con el servicio de administración que controla su estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement (clase)
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
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154845"
---
# <a name="msvm_serviceaffectselement-class"></a>MSVM \_ ServiceAffectsElement (clase)

Asocia una instancia de máquina virtual con el servicio de administración que controla su estado.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La clase **MSVM \_ ServiceAffectsElement** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ServiceAffectsElement** tiene estas propiedades.

<dl> <dt>

**AffectedElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a la máquina virtual. Esta propiedad se hereda de [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al servicio que controla la máquina virtual. Esta propiedad se hereda de [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el tipo de control que representa la asociación. Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre se establece en el valor siguiente.



| Value                                                                        | Significado            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Administra<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los detalles del tipo de asociación en la posición de la matriz correspondiente en la matriz de propiedades **ElementAffects** . Esta información es necesaria si **ElementAffects** está establecido en 1 (otro). Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre está establecida en **null**.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ServiceAffectsElement** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SERVICEAFFECTSELEMENT CIM**](cim-serviceaffectselement.md)
</dt> <dt>

[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

