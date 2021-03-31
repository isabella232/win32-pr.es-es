---
description: HomeProviderName
MS-HAID: WWAN\_profile\_v4.element\_HomeProviderName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: HomeProviderName
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8c80386f-a778-49ec-9439-990220d17d13
api_name:
- HomeProviderName
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5fd6613cb45871dcdd154de452035db9af5dfad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908053"
---
# <a name="span-idwwan_profile_v4element_homeprovidernamespanhomeprovidername"></a><span data-ttu-id="1c29d-103"><span id="WWAN_profile_v4.element_HomeProviderName"></span>HomeProviderName</span><span class="sxs-lookup"><span data-stu-id="1c29d-103"><span id="WWAN_profile_v4.element_HomeProviderName"></span>HomeProviderName</span></span>

<span data-ttu-id="1c29d-104">El nombre del proveedor de inicio de la SIM o el dispositivo especificados.</span><span class="sxs-lookup"><span data-stu-id="1c29d-104">The name of the home provider for the given SIM/Device.</span></span> <span data-ttu-id="1c29d-105">Para obtener más información, consulte la documentación del elemento [**HomeProviderName**](./schema-homeprovidername-mbnprofile-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="1c29d-105">For more information, see the documentation for the v1 [**HomeProviderName**](./schema-homeprovidername-mbnprofile-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1c29d-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="1c29d-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<HomeProviderName>**

## <a name="syntax"></a><span data-ttu-id="1c29d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c29d-107">Syntax</span></span>

``` syntax
<HomeProviderName>

  providerNameType

</HomeProviderName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1c29d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1c29d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1c29d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1c29d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1c29d-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1c29d-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1c29d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1c29d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1c29d-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1c29d-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1c29d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1c29d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c29d-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1c29d-114">Parent Element</span></span></th>
<th><span data-ttu-id="1c29d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c29d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c29d-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="1c29d-116"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="1c29d-117">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="1c29d-117">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="1c29d-118">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="1c29d-118">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="1c29d-119">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="1c29d-119">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="1c29d-120">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="1c29d-120">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1c29d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c29d-121">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c29d-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1c29d-122">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
