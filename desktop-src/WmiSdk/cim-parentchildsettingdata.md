---
description: Asociación entre una instancia de CIM VirtualSystemSettingData y la instancia \_ de CIM VirtualSystemSettingData que representa la instantánea más reciente en la que se basa \_ este objeto.
ms.assetid: f6e93c22-077b-4604-8d0d-9584b1f4dce1
ms.tgt_platform: multiple
title: CIM_ParentChildSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParentChildSettingData
- Root\CIMV2.CIM_ParentChildSettingData.Antecedent
- Root\CIMV2.CIM_ParentChildSettingData.Dependent
- Root\CIMV2.CIM_ParentChildSettingData.Parent
- Root\CIMV2.CIM_ParentChildSettingData.Child
api_type:
- Schema
api_location:
- Root\CIMV2
ms.openlocfilehash: 2b6fa9dc11f7d5e17fbc74e24a079a56647bee37b7c0251a281b767797ab801c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244665"
---
# <a name="cim_parentchildsettingdata-class"></a>\_Cim ParentChildSettingData (clase)

Asociación entre una instancia de [**CIM \_ VirtualSystemSettingData**](/previous-versions/windows/desktop/clushyperv/cim-virtualsystemsettingdata) y la instancia **de CIM \_ VirtualSystemSettingData** que representa la instantánea más reciente en la que se basa este objeto.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
class CIM_ParentChildSettingData : CIM_Dependency
{
  CIM_ManagedSystemElement     REF Antecedent;
  CIM_ManagedSystemElement     REF Dependent;
  CIM_VirtualSystemSettingData REF Parent;
  CIM_VirtualSystemSettingData REF Child;
};
```

## <a name="members"></a>Miembros

La **clase \_ ParentChildSettingData** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ParentChildSettingData** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al objeto independiente de esta asociación.

Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Elemento secundario**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los datos de configuración del sistema virtual que representa el elemento secundario del elemento primario.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia al objeto que depende de la **propiedad Antecedente.**

Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Parent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los datos de configuración de instantánea en los que se basan los datos de la configuración secundaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------|------------------------|
| Espacio de nombres<br/> | \\CIMV2 raíz<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

