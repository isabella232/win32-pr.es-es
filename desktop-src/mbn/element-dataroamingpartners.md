---
description: DataRoamingPartners
MS-HAID: WWAN\_profile\_v4.element\_DataRoamingPartners
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: DataRoamingPartners
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: c29edf9c-4e70-4b8f-8c71-0ec8a9fad60d
api_name:
- DataRoamingPartners
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f6df58bc0765b5254645c45270f8145f5d10d422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715091"
---
# <a name="span-idwwan_profile_v4element_dataroamingpartnersspandataroamingpartners"></a><span data-ttu-id="ee969-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span><span class="sxs-lookup"><span data-stu-id="ee969-103"><span id="WWAN_profile_v4.element_DataRoamingPartners"></span>DataRoamingPartners</span></span>

<span data-ttu-id="ee969-104">Especifica una lista de proveedores de red preferidos en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="ee969-104">Specifies a list of preferred network providers when roaming.</span></span>

<span data-ttu-id="ee969-105">Para obtener más información, consulte la documentación del elemento [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="ee969-105">For details, see the documentation for the v1 [**DataRoamingPartners**](./schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="ee969-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="ee969-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<DataRoamingPartners>**

## <a name="syntax"></a><span data-ttu-id="ee969-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee969-107">Syntax</span></span>

``` syntax
<DataRoamingPartners>

  <!-- Child elements -->
  Provider+

</DataRoamingPartners>
```

### <a name="key"></a><span data-ttu-id="ee969-108">Clave</span><span class="sxs-lookup"><span data-stu-id="ee969-108">Key</span></span>

<span data-ttu-id="ee969-109">`+`   requerido (uno o varios)</span><span class="sxs-lookup"><span data-stu-id="ee969-109">`+`   required (one or more)</span></span>

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="ee969-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="ee969-110"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="ee969-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="ee969-111"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="ee969-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="ee969-112">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="ee969-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="ee969-113"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee969-114">Elemento secundario</span><span class="sxs-lookup"><span data-stu-id="ee969-114">Child Element</span></span></th>
<th><span data-ttu-id="ee969-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee969-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee969-116"><a href="element-provider.md">Proveedor</a></span><span class="sxs-lookup"><span data-stu-id="ee969-116"><a href="element-provider.md">Provider</a></span></span></td>
<td><p><span data-ttu-id="ee969-117">Especifica un proveedor de red preferido en una lista de proveedores que se usarán en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="ee969-117">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span></p>
<p><span data-ttu-id="ee969-118">El valor de este elemento es una instancia del tipo complejo de <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> de v1.</span><span class="sxs-lookup"><span data-stu-id="ee969-118">The value of this element is an instance of the v1 <a href="../mbn/schema-providertype-complextype.md"><strong>providerType</strong></a> complex type.</span></span></p></td>
</tr>
</tbody>
</table>

 

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="ee969-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="ee969-119"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ee969-120">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="ee969-120">Parent Element</span></span></th>
<th><span data-ttu-id="ee969-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee969-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ee969-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="ee969-122"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="ee969-123">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="ee969-123">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="ee969-124">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="ee969-124">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="ee969-125">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="ee969-125">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="ee969-126">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="ee969-126">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="ee969-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee969-127">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee969-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee969-128">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
