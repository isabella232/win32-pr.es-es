---
description: Proveedor
MS-HAID: WWAN\_profile\_v4.element\_Provider
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Proveedor
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a701c4dd-967f-4f03-ada4-d34059f5a1e4
api_name:
- Provider
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7b4658e51f6f137795a935121dc90c047cf047
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497380"
---
# <a name="span-idwwan_profile_v4element_providerspanprovider"></a><span data-ttu-id="a3cac-103"><span id="WWAN_profile_v4.element_Provider"></span>Proveedor</span><span class="sxs-lookup"><span data-stu-id="a3cac-103"><span id="WWAN_profile_v4.element_Provider"></span>Provider</span></span>

<span data-ttu-id="a3cac-104">Especifica un proveedor de red preferido en una lista de proveedores que se usarán en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="a3cac-104">Specifies one preferred network provider in a list of providers to be used when roaming.</span></span>

<span data-ttu-id="a3cac-105">El valor de este elemento es una instancia del tipo complejo de [**providerType**](./schema-providertype-complextype.md) de v1.</span><span class="sxs-lookup"><span data-stu-id="a3cac-105">The value of this element is an instance of the v1 [**providerType**](./schema-providertype-complextype.md) complex type.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="a3cac-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="a3cac-106">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
[<DataRoamingPartners>](element-dataroamingpartners.md)  
**<Provider>**

## <a name="syntax"></a><span data-ttu-id="a3cac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3cac-107">Syntax</span></span>

``` syntax
<Provider>

  providerType

</Provider>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="a3cac-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="a3cac-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="a3cac-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="a3cac-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="a3cac-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3cac-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="a3cac-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="a3cac-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="a3cac-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="a3cac-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="a3cac-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="a3cac-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a3cac-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="a3cac-114">Parent Element</span></span></th>
<th><span data-ttu-id="a3cac-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3cac-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a3cac-116"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span><span class="sxs-lookup"><span data-stu-id="a3cac-116"><a href="element-dataroamingpartners.md">DataRoamingPartners</a></span></span></td>
<td><p><span data-ttu-id="a3cac-117">Especifica una lista de proveedores de red preferidos en itinerancia.</span><span class="sxs-lookup"><span data-stu-id="a3cac-117">Specifies a list of preferred network providers when roaming.</span></span></p>
<p><span data-ttu-id="a3cac-118">Para obtener más información, consulte la documentación del elemento <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> v1.</span><span class="sxs-lookup"><span data-stu-id="a3cac-118">For details, see the documentation for the v1 <a href="../mbn/schema-dataroamingpartners-mbnprofile-element.md"><strong>DataRoamingPartners</strong></a> element.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="a3cac-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3cac-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3cac-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3cac-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
