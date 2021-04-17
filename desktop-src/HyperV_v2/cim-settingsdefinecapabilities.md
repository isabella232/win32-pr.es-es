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
# <a name="cim_settingsdefinecapabilities-class"></a><span data-ttu-id="c819c-103">\_Clase SettingsDefineCapabilities de CIM</span><span class="sxs-lookup"><span data-stu-id="c819c-103">CIM\_SettingsDefineCapabilities class</span></span>

<span data-ttu-id="c819c-104">Representa una asociación entre las propiedades de una instancia de [**\_ SettingData de CIM**](cim-settingdata.md) y una instancia de [**\_ funciones de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="c819c-104">Represents an association between properties of a [**CIM\_SettingData**](cim-settingdata.md) instance and a [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="c819c-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c819c-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="c819c-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c819c-106">Members</span></span>

<span data-ttu-id="c819c-107">La clase **CIM \_ SettingsDefineCapabilities** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c819c-107">The **CIM\_SettingsDefineCapabilities** class has these types of members:</span></span>

-   [<span data-ttu-id="c819c-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c819c-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c819c-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c819c-109">Properties</span></span>

<span data-ttu-id="c819c-110">La clase **CIM \_ SettingsDefineCapabilities** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c819c-110">The **CIM\_SettingsDefineCapabilities** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c819c-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="c819c-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c819c-112">Tipo de datos **: \_ capacidades de CIM**</span><span class="sxs-lookup"><span data-stu-id="c819c-112">Data type: **CIM\_Capabilities**</span></span>
</dt> <dt>

<span data-ttu-id="c819c-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c819c-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c819c-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="c819c-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c819c-115">Referencia a la instancia [**de \_ funcionalidades de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="c819c-115">A reference to the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="c819c-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="c819c-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c819c-117">Tipo de datos **: \_ SettingData de CIM**</span><span class="sxs-lookup"><span data-stu-id="c819c-117">Data type: **CIM\_SettingData**</span></span>
</dt> <dt>

<span data-ttu-id="c819c-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c819c-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c819c-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="c819c-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="c819c-120">Referencia a la instancia [**de \_ SettingData de CIM**](cim-settingdata.md) utilizada para definir la instancia de [**\_ capacidades de CIM**](cim-capabilities.md) .</span><span class="sxs-lookup"><span data-stu-id="c819c-120">A reference to the [**CIM\_SettingData**](cim-settingdata.md) instance used to define the [**CIM\_Capabilities**](cim-capabilities.md) instance.</span></span>

</dd> <dt>

<span data-ttu-id="c819c-121">**PropertyPolicy**</span><span class="sxs-lookup"><span data-stu-id="c819c-121">**PropertyPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c819c-122">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c819c-122">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c819c-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c819c-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c819c-124">Calificadores: [**obligatorio**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**ValueRole**","**\_ SettingsDefineCapabilities CIM**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="c819c-124">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**ValueRole**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="c819c-125">Indica si las propiedades que no son NULL y que no son de clave de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) asociada se tratan de forma independiente o como un conjunto correlacionado.</span><span class="sxs-lookup"><span data-stu-id="c819c-125">Indicates whether the non-null, non-key properties of the associated [**CIM\_SettingData**](cim-settingdata.md) instance are treated independently or as a correlated set.</span></span> <span data-ttu-id="c819c-126">Por ejemplo, se puede definir un conjunto independiente de propiedades máximas cuando no hay ninguna relación entre cada propiedad.</span><span class="sxs-lookup"><span data-stu-id="c819c-126">For instance, an independent set of maximum properties might be defined when there is no relationship between each property.</span></span> <span data-ttu-id="c819c-127">En cambio, es posible que sea necesario definir varios conjuntos correlacionados de propiedades máximas si los valores máximos de cada uno de ellos dependen de algunos de los demás.</span><span class="sxs-lookup"><span data-stu-id="c819c-127">In contrast, several correlated sets of maximum properties might need to be defined when the maximum values of each are dependent on some of the others.</span></span>

<dt>

<span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span>

<span data-ttu-id="c819c-128">**Independiente** (0)</span><span class="sxs-lookup"><span data-stu-id="c819c-128">**Independent** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Correlated"></span><span id="correlated"></span><span id="CORRELATED"></span>

<span data-ttu-id="c819c-129">**Correlacionado** (1)</span><span class="sxs-lookup"><span data-stu-id="c819c-129">**Correlated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c819c-130">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c819c-130">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c819c-131">**ValueRange**</span><span class="sxs-lookup"><span data-stu-id="c819c-131">**ValueRange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c819c-132">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c819c-132">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c819c-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c819c-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c819c-134">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**\_ SettingsDefineCapabilities CIM**.**ValueRole**")</span><span class="sxs-lookup"><span data-stu-id="c819c-134">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRole**")</span></span>
</dt> </dl>

<span data-ttu-id="c819c-135">Indica el tipo de intervalo de valores utilizado por las propiedades de las propiedades no NULL y no clave de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c819c-135">Indicates the type of value range used by properties of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="c819c-136">**Punto** (0)</span><span class="sxs-lookup"><span data-stu-id="c819c-136">**Point** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Minimums"></span><span id="minimums"></span><span id="MINIMUMS"></span>

<span data-ttu-id="c819c-137">**Mínimo** (1)</span><span class="sxs-lookup"><span data-stu-id="c819c-137">**Minimums** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Maximums"></span><span id="maximums"></span><span id="MAXIMUMS"></span>

<span data-ttu-id="c819c-138">**Máximos** (2)</span><span class="sxs-lookup"><span data-stu-id="c819c-138">**Maximums** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Increments"></span><span id="increments"></span><span id="INCREMENTS"></span>

<span data-ttu-id="c819c-139">**Incrementos** (3)</span><span class="sxs-lookup"><span data-stu-id="c819c-139">**Increments** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c819c-140">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c819c-140">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c819c-141">**ValueRole**</span><span class="sxs-lookup"><span data-stu-id="c819c-141">**ValueRole**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c819c-142">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="c819c-142">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="c819c-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c819c-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c819c-144">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ SettingsDefineCapabilities**.**PropertyPolicy**","**\_ SettingsDefineCapabilities CIM**.**ValueRange**")</span><span class="sxs-lookup"><span data-stu-id="c819c-144">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_SettingsDefineCapabilities**.**PropertyPolicy**", "**CIM\_SettingsDefineCapabilities**.**ValueRange**")</span></span>
</dt> </dl>

<span data-ttu-id="c819c-145">La semántica adicional para la interpretación de las propiedades no clave no nulas de la instancia de [**\_ SettingData de CIM**](cim-settingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="c819c-145">The additional semantics for the interpretation of the non-null, non-key properties of the [**CIM\_SettingData**](cim-settingdata.md) instance.</span></span>

<span data-ttu-id="c819c-146">"Default" indica que los valores de propiedad de la instancia de SettingData del componente se utilizarán como valores predeterminados, cuando se crea una nueva instancia de SettingData para los elementos cuyas funciones están definidas por la instancia de funcionalidades asociada.</span><span class="sxs-lookup"><span data-stu-id="c819c-146">"Default" indicates that property values of the component SettingData instance will be used as default values, when a new SettingData instance is created for elements whose capabilities are defined by the associated Capabilities instance.</span></span>

<span data-ttu-id="c819c-147">En las instancias de settingdata, para propiedades particulares que tienen el mismo propósito semántico, como máximo, se especificará como valor predeterminado una instancia de settingdata como predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c819c-147">Across instances of settingdata, for particular properties having the same semantic purpose, at most one such settingdata instance shall be specified as a default.</span></span>

<span data-ttu-id="c819c-148">"Optimal" indica que la instancia de SettingData representa valores de configuración óptimos para los elementos asociados a la instancia de Capabilities asociada.</span><span class="sxs-lookup"><span data-stu-id="c819c-148">"Optimal" indicates that the SettingData instance represents optimal setting values for elements associated with the associated capabilities instance.</span></span> <span data-ttu-id="c819c-149">Es posible que varias instancias de SettingData de componentes se declaren como óptimas ". Mean: indica que las propiedades numéricas no nulas, no enumeradas, no enumeradas y no especificadas de la instancia de SettingData asociada representan un punto medio a lo largo de una dimensión.</span><span class="sxs-lookup"><span data-stu-id="c819c-149">Multiple component SettingData instances may be declared as optimal."Mean" indicates that the non-null, non-key, non-enumerated, non-boolean, numeric properties of the associated SettingData instance represents an average point along some dimension.</span></span> <span data-ttu-id="c819c-150">En el caso de las distintas combinaciones de propiedades de SettingData, se pueden declarar varias instancias de SettingData de componentes como "media".</span><span class="sxs-lookup"><span data-stu-id="c819c-150">For different combinations of SettingData properties, multiple component SettingData instances may be declared as "Mean".</span></span> <span data-ttu-id="c819c-151">"Compatible" indica que las propiedades no clave no nulas de la instancia de SettingData del componente representan un conjunto de valores de propiedad admitidos que no están calificados de otra manera.</span><span class="sxs-lookup"><span data-stu-id="c819c-151">"Supported" indicates that the non-null, non-key properties of the Component SettingData instance represents a set of supported property values that are not otherwise qualified.</span></span>

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span data-ttu-id="c819c-152">**Valor predeterminado** (0)</span><span class="sxs-lookup"><span data-stu-id="c819c-152">**Default** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Optimal"></span><span id="optimal"></span><span id="OPTIMAL"></span>

<span data-ttu-id="c819c-153">**Óptimo** (1)</span><span class="sxs-lookup"><span data-stu-id="c819c-153">**Optimal** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Mean"></span><span id="mean"></span><span id="MEAN"></span>

<span data-ttu-id="c819c-154">**Promedio** (2)</span><span class="sxs-lookup"><span data-stu-id="c819c-154">**Mean** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>

<span data-ttu-id="c819c-155">**Compatible** (3)</span><span class="sxs-lookup"><span data-stu-id="c819c-155">**Supported** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="c819c-156">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="c819c-156">**DMTF Reserved** (..)</span></span>


<span data-ttu-id="c819c-157"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="c819c-157"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="c819c-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c819c-158">Requirements</span></span>



| <span data-ttu-id="c819c-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="c819c-159">Requirement</span></span> | <span data-ttu-id="c819c-160">Value</span><span class="sxs-lookup"><span data-stu-id="c819c-160">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c819c-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c819c-161">Minimum supported client</span></span><br/> | <span data-ttu-id="c819c-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="c819c-162">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="c819c-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c819c-163">Minimum supported server</span></span><br/> | <span data-ttu-id="c819c-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c819c-164">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="c819c-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c819c-165">Namespace</span></span><br/>                | <span data-ttu-id="c819c-166">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="c819c-166">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="c819c-167">MOF</span><span class="sxs-lookup"><span data-stu-id="c819c-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c819c-168"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c819c-168"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c819c-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c819c-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c819c-170"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c819c-170"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c819c-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="c819c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c819c-172">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="c819c-172">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

