---
description: Proporciona un vínculo entre la instancia de funciones de la característica de conmutador Ethernet y la configuración mínima, máxima, incremental y predeterminada de un recurso.
ms.assetid: 5abd8b2a-9f72-4875-be5c-ce5a2f526e9a
title: Msvm_FeatureSettingsDefineCapabilities (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FeatureSettingsDefineCapabilities
- Msvm_FeatureSettingsDefineCapabilities.GroupComponent
- Msvm_FeatureSettingsDefineCapabilities.PartComponent
- Msvm_FeatureSettingsDefineCapabilities.PropertyPolicy
- Msvm_FeatureSettingsDefineCapabilities.ValueRole
- Msvm_FeatureSettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ec91a73931458cb6f7e07a7cfc23e71e4665fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666617"
---
# <a name="msvm_featuresettingsdefinecapabilities-class"></a>MSVM \_ FeatureSettingsDefineCapabilities (clase)

Proporciona un vínculo entre la instancia de funciones de la característica de conmutador Ethernet y la configuración mínima, máxima, incremental y predeterminada de un recurso.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FeatureSettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  Msvm_EthernetSwitchFeatureCapabilities REF GroupComponent;
  Msvm_FeatureSettingData                REF PartComponent;
  uint16                                     PropertyPolicy = 0;
  uint16                                     ValueRole = 3;
  uint16                                     ValueRange = 0;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ FeatureSettingsDefineCapabilities** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ FeatureSettingsDefineCapabilities** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa las capacidades de la característica de conmutador Ethernet. Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa la configuración del recurso. Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica si las propiedades que no son **null** y que no son de clave del **PartComponent** se tratan de forma independiente o como un conjunto correlacionado. Por ejemplo, se podría definir un conjunto independiente de propiedades máximas, pero no hay ninguna relación entre cada propiedad. Por otro lado, es posible que sea necesario definir varios conjuntos correlacionados de propiedades máximas cuando los valores máximos de cada uno de ellos dependan de algunos de los otros.

Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).

<dl> <dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independiente** (0)
</dt> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlacionado** (1)
</dt> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Indica una mayor semántica en la interpretación de todas las propiedades no clave no **nulas** de los datos de configuración.

Los valores siguientes solo se evalúan con respecto a las propiedades numéricas no **nulas**, no enumeradas, que no son de clave, y no son booleanas de los datos de configuración. Cada propiedad de ese conjunto debe ser comparable matemáticamente a otras instancias de esa propiedad.

Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).



| Value                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Punto**</dt> <dt>0</dt> </dl>                     | Esta instancia de datos de configuración proporciona un único conjunto de valores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <dt>**Mínimo**</dt> <dt>1</dt> </dl>         | Estos datos de configuración proporcionan valores mínimos para las propiedades evaluadas. Cuando se usa con **PropertyPolicy** = "independiente", solo se debe especificar una configuración de este tipo por cada instancia de datos de configuración concreta para cualquier funcionalidad. A menos que esté restringido por un valor máximo en el mismo conjunto de propiedades, también se considera que todos los valores que se comparan por encima de los valores especificados son compatibles con la instancia de Capabilities asociada. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <dt>**Máximo**</dt> <dt>2</dt> </dl>         | Estos datos de configuración proporcionan los valores máximos para las propiedades evaluadas. Cuando se usa con **PropertyPolicy** = "independiente", solo se debe especificar una configuración de este tipo por cada instancia de datos de configuración concreta para cualquier funcionalidad. A menos que esté restringido por un valor mínimo en el mismo conjunto de propiedades, también se considera que todos los valores que se comparan por debajo de los valores especificados son compatibles con la instancia de Capabilities asociada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <dt>**Incrementos**</dt> <dt>3</dt> </dl> | Estos datos de configuración proporcionan valores de incremento para las propiedades evaluadas. En el caso de las capacidades asociadas, si una propiedad evaluada no tiene actualmente valores mínimos o máximos correspondientes, la propiedad no tiene ningún efecto. De lo contrario, para cada propiedad evaluada, su valor (*x*) debe estar entre *MinimumValue* y *MaximumValue*, de forma inclusiva, y debe tener la propiedad de que el resultado de *MaximumValue* menos *x* y el resultado de *x* menos *MinimumValue* son un entero múltiplo del *incremento*. Si no se especifica *MinimumValue* o *MaximumValue* y el otro es, el valor que falta se debe suponer que es el valor más bajo o más alto admitido para el tipo de datos de la propiedad. Además, si se especifican *MinimumValue* y *MaximumValue* para una propiedad evaluada, el resultado de *MaximumValue* menos *MinimumValue* debe ser un entero múltiplo del *incremento*. <br/> |



 

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Especifica la semántica adicional en la interpretación de las propiedades no clave no **nulas** de los datos de configuración. Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).



| Value                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <dt>**Valor predeterminado**</dt> <dt>0</dt> </dl>         | Los valores de propiedad de los datos de configuración se usarán como valores predeterminados, cuando se crea una nueva instancia de datos de configuración para los elementos cuyas capacidades están definidas por las capacidades asociadas. En las instancias de los datos de configuración, para propiedades particulares que tienen el mismo propósito semántico, se debe especificar como valor predeterminado como máximo una instancia de datos de configuración de este tipo.<br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <dt>**Óptimo**</dt> <dt>1</dt> </dl>         | La instancia de datos de configuración representa valores de configuración óptimos para los elementos asociados a las capacidades asociadas. Las instancias de datos de configuración de varios componentes se pueden declarar como óptimas.<br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <dt>**Promedio**</dt> <dt>2</dt> </dl>                     | Las propiedades numéricas no **nulas**, sin clave, no enumeradas y no booleanas de la instancia de datos de configuración asociada representan un promedio de punto a lo largo de alguna dimensión. En el caso de distintas combinaciones de propiedades de datos de configuración, es posible que varias instancias de datos de configuración de componentes se declaren como **media**. <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <dt>**Compatible**</dt> <dt>3</dt> </dl> | Las propiedades que no son **null** y que no son de clave de los datos de configuración representan un conjunto de valores de propiedad admitidos que no están calificados de otra manera. <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

