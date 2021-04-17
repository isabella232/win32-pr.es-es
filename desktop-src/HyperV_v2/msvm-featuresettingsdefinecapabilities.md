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
# <a name="msvm_featuresettingsdefinecapabilities-class"></a><span data-ttu-id="41803-103">MSVM \_ FeatureSettingsDefineCapabilities (clase)</span><span class="sxs-lookup"><span data-stu-id="41803-103">Msvm\_FeatureSettingsDefineCapabilities class</span></span>

<span data-ttu-id="41803-104">Proporciona un vínculo entre la instancia de funciones de la característica de conmutador Ethernet y la configuración mínima, máxima, incremental y predeterminada de un recurso.</span><span class="sxs-lookup"><span data-stu-id="41803-104">Provides a link between the Ethernet switch feature capabilities instance and the minimum, maximum, incremental, and default settings for a resource.</span></span>

<span data-ttu-id="41803-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="41803-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="41803-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41803-106">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="41803-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="41803-107">Members</span></span>

<span data-ttu-id="41803-108">La clase **MSVM \_ FeatureSettingsDefineCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="41803-108">The **Msvm\_FeatureSettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="41803-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41803-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="41803-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="41803-110">Properties</span></span>

<span data-ttu-id="41803-111">La clase **MSVM \_ FeatureSettingsDefineCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="41803-111">The **Msvm\_FeatureSettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="41803-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="41803-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41803-113">Tipo de datos: **[ **MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="41803-113">Data type: **[**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md)**</span></span>
</dt> <dt>

<span data-ttu-id="41803-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41803-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41803-115">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="41803-115">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="41803-116">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) que representa las capacidades de la característica de conmutador Ethernet.</span><span class="sxs-lookup"><span data-stu-id="41803-116">A reference to an instance of the [**Msvm\_EthernetSwitchFeatureCapabilities**](msvm-ethernetswitchfeaturecapabilities.md) class that represents the Ethernet switch feature capabilities.</span></span> <span data-ttu-id="41803-117">Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="41803-117">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="41803-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="41803-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41803-119">Tipo de datos: **[ **MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="41803-119">Data type: **[**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="41803-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41803-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41803-121">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="41803-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="41803-122">Referencia a una instancia de la clase [**MSVM \_ FeatureSettingData**](msvm-featuresettingdata.md) que representa la configuración del recurso.</span><span class="sxs-lookup"><span data-stu-id="41803-122">A reference to an instance of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represents the resource settings.</span></span> <span data-ttu-id="41803-123">Esta propiedad se hereda del [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component).</span><span class="sxs-lookup"><span data-stu-id="41803-123">This property is inherited from [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component).</span></span>

</dd> <dt>

<span data-ttu-id="41803-124">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="41803-124">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41803-125">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41803-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41803-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41803-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="41803-127">Especifica si las propiedades que no son **null** y que no son de clave del **PartComponent** se tratan de forma independiente o como un conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="41803-127">Specifies whether the non-**Null**, non-key properties of the **PartComponent** are treated independently or as a correlated set.</span></span> <span data-ttu-id="41803-128">Por ejemplo, se podría definir un conjunto independiente de propiedades máximas, pero no hay ninguna relación entre cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="41803-128">For example, an independent set of maximum properties might be defined, yet there is no relationship between each property.</span></span> <span data-ttu-id="41803-129">Por otro lado, es posible que sea necesario definir varios conjuntos correlacionados de propiedades máximas cuando los valores máximos de cada uno de ellos dependan de algunos de los otros.</span><span class="sxs-lookup"><span data-stu-id="41803-129">On the other hand, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<span data-ttu-id="41803-130">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41803-130">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="41803-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independiente** (0)</span><span class="sxs-lookup"><span data-stu-id="41803-131"><span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>**Independent** (0)</span></span>
</dt> <dt>

<span data-ttu-id="41803-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlacionado** (1)</span><span class="sxs-lookup"><span data-stu-id="41803-132"><span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>**Correlated** (1)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="41803-133">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="41803-133">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41803-134">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41803-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41803-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41803-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41803-136">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="41803-136">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41803-137">Indica una mayor semántica en la interpretación de todas las propiedades no clave no **nulas** de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="41803-137">Indicates further semantics on the interpretation of all non-**Null**, non-key properties of the setting data.</span></span>

<span data-ttu-id="41803-138">Los valores siguientes solo se evalúan con respecto a las propiedades numéricas no **nulas**, no enumeradas, que no son de clave, y no son booleanas de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="41803-138">The values below are only evaluated against non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the setting data.</span></span> <span data-ttu-id="41803-139">Cada propiedad de ese conjunto debe ser comparable matemáticamente a otras instancias de esa propiedad.</span><span class="sxs-lookup"><span data-stu-id="41803-139">Each property of that set must be mathematically comparable to other instances of that property.</span></span>

<span data-ttu-id="41803-140">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41803-140">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="41803-141">Value</span><span class="sxs-lookup"><span data-stu-id="41803-141">Value</span></span>                                                                                                                                                                                                                                   | <span data-ttu-id="41803-142">Significado</span><span class="sxs-lookup"><span data-stu-id="41803-142">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="41803-143"><dt>**Punto**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="41803-143"><dt>**Point**</dt> <dt>0</dt></span></span> </dl>                     | <span data-ttu-id="41803-144">Esta instancia de datos de configuración proporciona un único conjunto de valores.</span><span class="sxs-lookup"><span data-stu-id="41803-144">This setting data instance provides a single set of values.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span><dl> <span data-ttu-id="41803-145"><dt>**Mínimo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41803-145"><dt>**Minimums**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="41803-146">Estos datos de configuración proporcionan valores mínimos para las propiedades evaluadas.</span><span class="sxs-lookup"><span data-stu-id="41803-146">This setting data provides minimum values for evaluated properties.</span></span> <span data-ttu-id="41803-147">Cuando se usa con **PropertyPolicy** = "independiente", solo se debe especificar una configuración de este tipo por cada instancia de datos de configuración concreta para cualquier funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="41803-147">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="41803-148">A menos que esté restringido por un valor máximo en el mismo conjunto de propiedades, también se considera que todos los valores que se comparan por encima de los valores especificados son compatibles con la instancia de Capabilities asociada.</span><span class="sxs-lookup"><span data-stu-id="41803-148">Unless restricted by a Maximums value on the same set of properties, all values that compare higher than the specified values are also considered to be supported by the associated capabilities instance.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span><dl> <span data-ttu-id="41803-149"><dt>**Máximo**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41803-149"><dt>**Maximums**</dt> <dt>2</dt></span></span> </dl>         | <span data-ttu-id="41803-150">Estos datos de configuración proporcionan los valores máximos para las propiedades evaluadas.</span><span class="sxs-lookup"><span data-stu-id="41803-150">This setting data provides maximum values for evaluated properties.</span></span> <span data-ttu-id="41803-151">Cuando se usa con **PropertyPolicy** = "independiente", solo se debe especificar una configuración de este tipo por cada instancia de datos de configuración concreta para cualquier funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="41803-151">When used with **PropertyPolicy** = "Independent", only one such setting per particular setting data instance must be specified for any capabilities.</span></span> <span data-ttu-id="41803-152">A menos que esté restringido por un valor mínimo en el mismo conjunto de propiedades, también se considera que todos los valores que se comparan por debajo de los valores especificados son compatibles con la instancia de Capabilities asociada.</span><span class="sxs-lookup"><span data-stu-id="41803-152">Unless restricted by a Minimums value on the same set of properties, all values that compare lower than the specified values are also considered to be supported by the associated capabilities instance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span><dl> <span data-ttu-id="41803-153"><dt>**Incrementos**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="41803-153"><dt>**Increments**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="41803-154">Estos datos de configuración proporcionan valores de incremento para las propiedades evaluadas.</span><span class="sxs-lookup"><span data-stu-id="41803-154">This setting data provides increment values for evaluated properties.</span></span> <span data-ttu-id="41803-155">En el caso de las capacidades asociadas, si una propiedad evaluada no tiene actualmente valores mínimos o máximos correspondientes, la propiedad no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="41803-155">For the associated capabilities, if an evaluated property currently has no corresponding Minimums or Maximums values, then the property has no affect.</span></span> <span data-ttu-id="41803-156">De lo contrario, para cada propiedad evaluada, su valor (*x*) debe estar entre *MinimumValue* y *MaximumValue*, de forma inclusiva, y debe tener la propiedad de que el resultado de *MaximumValue* menos *x* y el resultado de *x* menos *MinimumValue* son un entero múltiplo del *incremento*.</span><span class="sxs-lookup"><span data-stu-id="41803-156">Otherwise, for each evaluated property, its value (*x*) must be between the *MinimumValue* and *MaximumValue*, inclusively, and must have the property that both the result of *MaximumValue* minus *x* and the result of *x* minus *MinimumValue* are each an integer multiple of the *Increment*.</span></span> <span data-ttu-id="41803-157">Si no se especifica *MinimumValue* o *MaximumValue* y el otro es, el valor que falta se debe suponer que es el valor más bajo o más alto admitido para el tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="41803-157">If either *MinimumValue* or *MaximumValue* is not specified and the other is, then the missing value must be respectively assumed to be the lowest or highest supported value for the property's data type.</span></span> <span data-ttu-id="41803-158">Además, si se especifican *MinimumValue* y *MaximumValue* para una propiedad evaluada, el resultado de *MaximumValue* menos *MinimumValue* debe ser un entero múltiplo del *incremento*.</span><span class="sxs-lookup"><span data-stu-id="41803-158">Additionally, if both a *MinimumValue* and a *MaximumValue* are specified for an evaluated property, then the result of *MaximumValue* minus *MinimumValue* must be an integer multiple of the *Increment*.</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="41803-159">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="41803-159">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41803-160">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="41803-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="41803-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="41803-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="41803-162">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="41803-162">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="41803-163">Especifica la semántica adicional en la interpretación de las propiedades no clave no **nulas** de los datos de configuración.</span><span class="sxs-lookup"><span data-stu-id="41803-163">Specifies further semantics on the interpretation of the non-**Null**, non-key properties of the setting data.</span></span> <span data-ttu-id="41803-164">Esta propiedad se hereda de [**\_ SettingsDefineCapabilities CIM**](/previous-versions//cc136913(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="41803-164">This property is inherited from [**CIM\_SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).</span></span>



| <span data-ttu-id="41803-165">Value</span><span class="sxs-lookup"><span data-stu-id="41803-165">Value</span></span>                                                                                                                                                                                                                               | <span data-ttu-id="41803-166">Significado</span><span class="sxs-lookup"><span data-stu-id="41803-166">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Default"></span><span id="default"></span><span id="DEFAULT"></span><dl> <span data-ttu-id="41803-167"><dt>**Valor predeterminado**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="41803-167"><dt>**Default**</dt> <dt>0</dt></span></span> </dl>         | <span data-ttu-id="41803-168">Los valores de propiedad de los datos de configuración se usarán como valores predeterminados, cuando se crea una nueva instancia de datos de configuración para los elementos cuyas capacidades están definidas por las capacidades asociadas.</span><span class="sxs-lookup"><span data-stu-id="41803-168">The property values of the setting data will be used as default values, when a new setting data instance is created for elements whose capabilities are defined by the associated capabilities.</span></span> <span data-ttu-id="41803-169">En las instancias de los datos de configuración, para propiedades particulares que tienen el mismo propósito semántico, se debe especificar como valor predeterminado como máximo una instancia de datos de configuración de este tipo.</span><span class="sxs-lookup"><span data-stu-id="41803-169">Across instances of the setting data, for particular properties having the same semantic purpose, at most one such setting data instance must be specified as a default.</span></span><br/> |
| <span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span><dl> <span data-ttu-id="41803-170"><dt>**Óptimo**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41803-170"><dt>**Optimal**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="41803-171">La instancia de datos de configuración representa valores de configuración óptimos para los elementos asociados a las capacidades asociadas.</span><span class="sxs-lookup"><span data-stu-id="41803-171">The setting data instance represents optimal setting values for elements associated with the associated capabilities.</span></span> <span data-ttu-id="41803-172">Las instancias de datos de configuración de varios componentes se pueden declarar como óptimas.</span><span class="sxs-lookup"><span data-stu-id="41803-172">Multiple component setting data instances may be declared as optimal.</span></span><br/>                                                                                                                                                                              |
| <span id="Mean"></span><span id="mean"></span><span id="MEAN"></span><dl> <span data-ttu-id="41803-173"><dt>**Promedio**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41803-173"><dt>**Mean**</dt> <dt>2</dt></span></span> </dl>                     | <span data-ttu-id="41803-174">Las propiedades numéricas no **nulas**, sin clave, no enumeradas y no booleanas de la instancia de datos de configuración asociada representan un promedio de punto a lo largo de alguna dimensión.</span><span class="sxs-lookup"><span data-stu-id="41803-174">The non-**Null**, non-key, non-enumerated, non-Boolean, numeric properties of the associated setting data instance represents an average point along some dimension.</span></span> <span data-ttu-id="41803-175">En el caso de distintas combinaciones de propiedades de datos de configuración, es posible que varias instancias de datos de configuración de componentes se declaren como **media**.</span><span class="sxs-lookup"><span data-stu-id="41803-175">For different combinations of setting data properties, multiple component setting data instances may be declared as **Mean**.</span></span> <br/>                                                                      |
| <span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span><dl> <span data-ttu-id="41803-176"><dt>**Compatible**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="41803-176"><dt>**Supported**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="41803-177">Las propiedades que no son **null** y que no son de clave de los datos de configuración representan un conjunto de valores de propiedad admitidos que no están calificados de otra manera.</span><span class="sxs-lookup"><span data-stu-id="41803-177">The non-**Null**, non-key properties of the setting data represents a set of supported property values that are not otherwise qualified.</span></span> <br/>                                                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41803-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41803-178">Requirements</span></span>



| <span data-ttu-id="41803-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="41803-179">Requirement</span></span> | <span data-ttu-id="41803-180">Value</span><span class="sxs-lookup"><span data-stu-id="41803-180">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41803-181">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41803-181">Minimum supported client</span></span><br/> | <span data-ttu-id="41803-182">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="41803-182">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="41803-183">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41803-183">Minimum supported server</span></span><br/> | <span data-ttu-id="41803-184">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="41803-184">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="41803-185">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="41803-185">Namespace</span></span><br/>                | <span data-ttu-id="41803-186">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="41803-186">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="41803-187">MOF</span><span class="sxs-lookup"><span data-stu-id="41803-187">MOF</span></span><br/>                      | <dl> <span data-ttu-id="41803-188"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="41803-188"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="41803-189">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="41803-189">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41803-190"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="41803-190"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

