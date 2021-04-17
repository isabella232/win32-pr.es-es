---
description: Representa una asociación entre las propiedades de una \_ instancia de SettingData de CIM y una instancia de funciones de CIM \_ .
ms.assetid: f3364779-baeb-4b84-a0e6-b2a60d1661bd
title: CIM_SettingsDefineCapabilities (clase)
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
ms.openlocfilehash: d3c36e7c24702578704e849820abf2b1769c91c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667951"
---
# <a name="cim_settingsdefinecapabilities-class"></a>\_Clase SettingsDefineCapabilities de CIM

Representa una asociación entre las propiedades de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) y una instancia de [**\_ funciones de CIM**](cim-capabilities.md) .

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

La clase **CIM \_ SettingsDefineCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ SettingsDefineCapabilities** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ capacidades de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a la instancia [**de \_ funcionalidades de CIM**](cim-capabilities.md) .

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ SettingData de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a la instancia [**de \_ SettingData de CIM**](cim-settingdata.md) utilizada para definir la instancia de [**\_ capacidades de CIM**](cim-capabilities.md) .

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**\_ SettingsDefineCapabilities CIM**.**ValueRange**")
</dt> </dl>

Indica si las propiedades que no son NULL y que no son de clave de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) asociada se tratan de forma independiente o como un conjunto correlacionado. Por ejemplo, se puede definir un conjunto independiente de propiedades máximas cuando no hay ninguna relación entre cada propiedad. En cambio, es posible que sea necesario definir varios conjuntos correlacionados de propiedades máximas si los valores máximos de cada uno de ellos dependen de algunos de los demás.

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

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**\_ SettingsDefineCapabilities CIM**.**ValueRole**")
</dt> </dl>

Indica el tipo de intervalo de valores utilizado por las propiedades de las propiedades no NULL y no clave de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) .

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

**Punto** (0)


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

**Mínimo** (1)


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

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**\_ SettingsDefineCapabilities CIM**.**ValueRange**")
</dt> </dl>

La semántica adicional para la interpretación de las propiedades no clave no nulas de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) .

"Default" indica que los valores de propiedad de la instancia de SettingData del componente se utilizarán como valores predeterminados, cuando se crea una nueva instancia de SettingData para los elementos cuyas funciones están definidas por la instancia de funcionalidades asociada.

En las instancias de settingdata, para propiedades particulares que tienen el mismo propósito semántico, como máximo, se especificará como valor predeterminado una instancia de settingdata como predeterminada.

"Optimal" indica que la instancia de SettingData representa valores de configuración óptimos para los elementos asociados a la instancia de Capabilities asociada. Es posible que varias instancias de SettingData de componentes se declaren como óptimas ". Mean: indica que las propiedades numéricas no nulas, no enumeradas, no enumeradas y no especificadas de la instancia de SettingData asociada representan un punto medio a lo largo de una dimensión. En el caso de las distintas combinaciones de propiedades de SettingData, se pueden declarar varias instancias de SettingData de componentes como "media". "Compatible" indica que las propiedades no clave no nulas de la instancia de SettingData del componente representan un conjunto de valores de propiedad admitidos que no están calificados de otra manera.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

**Valor predeterminado** (0)


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

**Óptimo** (1)


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

**Promedio** (2)


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

**Compatible** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> </dl>

 

