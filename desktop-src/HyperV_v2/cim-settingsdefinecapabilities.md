---
description: Representa una asociación entre las propiedades de una instancia \_ de Cim SettingData y una instancia de \_ Capacidades de CIM.
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: CIM_SettingsDefineCapabilities clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SettingsDefineCapabilities
- CIM_SettingsDefineCapabilities.GroupComponent
- CIM_SettingsDefineCapabilities.PartComponent
- CIM_SettingsDefineCapabilities.PropertyPolicy
- CIM_SettingsDefineCapabilities.ValueRole
- CIM_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b53f0e72e21b73932c144602308ee599c523ea755b45dae12774109f6a9e010f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899665"
---
# <a name="cim_settingsdefinecapabilities-class"></a>Cim \_ SettingsDefineCapabilities (clase)

Representa una asociación entre las propiedades de una instancia [**\_ de Cim SettingData**](cim-settingdata.md) y una [**instancia de \_ Capacidades de CIM.**](cim-capabilities.md)

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Abstract, Version("2.22.1"), UMLPackagePath("CIM::Core::Settings"), AMENDMENT]
class CIM_SettingsDefineCapabilities : CIM_Component
{
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ SettingsDefineCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ SettingsDefineCapabilities** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Funcionalidades cim \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a la instancia [**de \_ capacidades de CIM.**](cim-capabilities.md)

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a la instancia [**de Cim \_ SettingData**](cim-settingdata.md) que se usa para definir la [**instancia de \_ capacidades de CIM.**](cim-capabilities.md)

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**", "**Configuración \_ de CIMDefineCapabilities**.**ValueRange**")
</dt> </dl>

Indica si las propiedades no null y no clave de la instancia [**de CIM \_ SettingData**](cim-settingdata.md) asociada se tratan de forma independiente o como un conjunto correlacionado. Por ejemplo, se podría definir un conjunto independiente de propiedades máximas cuando no hay ninguna relación entre cada propiedad. Por el contrario, es posible que sea necesario definir varios conjuntos correlacionados de propiedades máximas cuando los valores máximos de cada uno de ellos dependen de algunos de los demás.

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

**Independiente** (0)


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

**Correlacionado** (1)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Configuración de \_ CIMDefineCapabilities**.**PropertyPolicy**", "**Configuración \_ de CIMDefineCapabilities**.**ValueRole**")
</dt> </dl>

Indica el tipo de intervalo de valores utilizado por las propiedades de las propiedades que no son null y que no son clave de la [**instancia \_ settingData de CIM.**](cim-settingdata.md)

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punto** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Mínimos** (1)


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

**Máximos** (2)


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

**Incrementos** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Configuración de \_ CIMDefineCapabilities**.**PropertyPolicy**", "**Configuración \_ de CIMDefineCapabilities**.**ValueRange**")
</dt> </dl>

Semántica adicional para la interpretación de las propiedades no null y no clave de la [**instancia \_ settingData de CIM.**](cim-settingdata.md)

"Default" indica que los valores de propiedad de la instancia settingData del componente se usarán como valores predeterminados cuando se cree una nueva instancia settingData para los elementos cuyas funcionalidades se definen mediante la instancia capabilities asociada.

En todas las instancias de settingdata, para determinadas propiedades que tienen el mismo propósito semántico, como máximo una de estas instancias settingdata se debe especificar como valor predeterminado.

"Optimal" indica que la instancia SettingData representa los valores de configuración óptimos para los elementos asociados a la instancia de funcionalidades asociada. Las instancias settingData de varios componentes se pueden declarar como óptimas". Mean" indica que las propiedades numéricas no null, no clave, no enumeradas, no booleanas de la instancia settingData asociada representan un punto medio a lo largo de alguna dimensión. Para diferentes combinaciones de propiedades SettingData, las instancias settingData de varios componentes se pueden declarar como "Mean". "Supported" indica que las propiedades que no son null y que no son de clave de la instancia de Component SettingData representan un conjunto de valores de propiedad admitidos que no se califican de otro modo.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valor** predeterminado (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Óptimo** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Media** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Compatible** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

