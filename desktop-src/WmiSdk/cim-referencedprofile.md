---
description: Se usa para asociar una instancia \_ de CIM RegisteredProfile con una instancia de \_ REGISTEREDPROFILE de CIM de otro perfil que hace referencia al perfil dependiente como perfil relacionado.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ReferencedProfile
- CIM_ReferencedProfile.Antecedent
- CIM_ReferencedProfile.Dependent
api_type:
- Schema
api_location:
- Root\interop
ms.openlocfilehash: 8fdc0d8dccd325ae7e13de971e09cce6faf93455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648595"
---
# <a name="cim_referencedprofile-class"></a>\_Clase ReferencedProfile de CIM

Se usa para asociar una instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) con una instancia de **\_ RegisteredProfile de CIM** de otro perfil que hace referencia al perfil dependiente como perfil relacionado.

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Version("2.8.0"), UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_ReferencedProfile : CIM_Dependency
{
  CIM_RegisteredProfile REF Antecedent;
  CIM_RegisteredProfile REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ReferencedProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ReferencedProfile** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a la que hace referencia el perfil **dependiente** .

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica una instancia de [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) que hace referencia a otros perfiles.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El uso de las propiedades **dependent** y **Antecedent** de la **Asociación \_ ReferencedProfile de CIM** se define de tal forma que el perfil al que se hace referencia es el antecedente y el perfil que hace referencia es el dependiente.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\Interoperabilidad raíz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop. mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

