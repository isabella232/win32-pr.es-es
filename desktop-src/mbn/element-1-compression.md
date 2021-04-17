---
description: ModemDMConfigProfile \/ ... \/ Compresión (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Compresión
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8dc3acd6-5997-47a5-bd30-899569b9aad9
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a40c9d68dbe9e619afa3a1bc18bd2d14cfcb3cfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652419"
---
# <a name="span-idwwan_profile_v4element_1_compressionspanmodemdmconfigprofilecompression-v4"></a><span data-ttu-id="d1eb1-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile \/ ... \/ Compresión (v4)</span><span class="sxs-lookup"><span data-stu-id="d1eb1-103"><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile\/...\/Compression (v4)</span></span>

<span data-ttu-id="d1eb1-104">Especifica si se usará la compresión en el vínculo de datos para el encabezado y la transferencia de datos.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-104">Specifies whether compression will be used at the data link for header and data transfer.</span></span>

<span data-ttu-id="d1eb1-105">Para obtener más información, consulte la documentación del elemento [**Compression**](./schema-compression-contexttype-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-105">For more information, see the documentation for the v1 [**Compression**](./schema-compression-contexttype-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="d1eb1-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="d1eb1-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a><span data-ttu-id="d1eb1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1eb1-107">Syntax</span></span>

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="d1eb1-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="d1eb1-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="d1eb1-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="d1eb1-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="d1eb1-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="d1eb1-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="d1eb1-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="d1eb1-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="d1eb1-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="d1eb1-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1eb1-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="d1eb1-114">Parent Element</span></span></th>
<th><span data-ttu-id="d1eb1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d1eb1-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1eb1-116"><a href="element-1-context.md">Contexto</a></span><span class="sxs-lookup"><span data-stu-id="d1eb1-116"><a href="element-1-context.md">Context</a></span></span></td>
<td><p><span data-ttu-id="d1eb1-117">Especifica los parámetros necesarios para establecer una conexión de datos.</span><span class="sxs-lookup"><span data-stu-id="d1eb1-117">Specifies the parameters required to establish a data connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="d1eb1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1eb1-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1eb1-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d1eb1-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
