---
description: Se usa para asociar una instancia de CIM RegisteredProfile a una instancia de CIM RegisteredProfile de otro perfil que hace referencia al perfil \_ dependiente como un perfil \_ relacionado.
ms.assetid: 631003de-477b-4447-9633-1601a7f8eadb
ms.tgt_platform: multiple
title: CIM_ReferencedProfile clase
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
ms.openlocfilehash: 39cfa6dac2fd827b2ce690afa5cdd7126322c2f81182db674517c75911791a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556829"
---
# <a name="cim_referencedprofile-class"></a>Cim \_ ReferencedProfile (clase)

Se usa para asociar una instancia [**de CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)) a una instancia de **CIM \_ RegisteredProfile** de otro perfil que hace referencia al perfil dependiente como un perfil relacionado.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

La **clase CIM \_ ReferencedProfile** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ ReferencedProfile** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica la instancia [**\_ registeredProfile**](/previous-versions//ee309375(v=vs.85)) de CIM a la que hace referencia el **perfil** dependiente.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica una instancia [**\_ registeredProfile de CIM**](/previous-versions//ee309375(v=vs.85)) que hace referencia a otros perfiles.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El uso de las propiedades **Dependent** y **Antecedent** en la asociación **CIM \_ ReferencedProfile** se define de forma que el perfil al que se hace referencia sea el antecedente y el perfil que realiza la referencia sea el dependiente.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | Interoperabilidad \\ raíz<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Interop.mof</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

