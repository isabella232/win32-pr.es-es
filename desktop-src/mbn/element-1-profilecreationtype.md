---
description: ProfileCreationType (en ModemDMConfigProfile)
MS-HAID: WWAN\_profile\_v4.element\_1\_ProfileCreationType
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ProfileCreationType (en ModemDMConfigProfile)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b755840d0308ec2d7a7bba5896b0cf67b7b61198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907923"
---
# <a name="span-idwwan_profile_v4element_1_profilecreationtypespanprofilecreationtype-in-modemdmconfigprofile"></a><span data-ttu-id="3e390-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (en ModemDMConfigProfile)</span><span class="sxs-lookup"><span data-stu-id="3e390-103"><span id="WWAN_profile_v4.element_1_ProfileCreationType"></span>ProfileCreationType (in ModemDMConfigProfile)</span></span>

<span data-ttu-id="3e390-104">Especifica cómo se creó este perfil de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="3e390-104">Specifies how this modem DM profile was created.</span></span>

<span data-ttu-id="3e390-105">Este valor se usa para decidir si un usuario puede eliminar el perfil.</span><span class="sxs-lookup"><span data-stu-id="3e390-105">This value is used to decide whether a user can delete the profile.</span></span> <span data-ttu-id="3e390-106">Los usuarios solo pueden eliminar perfiles de **UserProvisioned** .</span><span class="sxs-lookup"><span data-stu-id="3e390-106">Users can only delete **UserProvisioned** profiles.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3e390-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="3e390-107">Element hierarchy</span></span>

[<ModemDMConfigProfile>](element-modemdmconfigprofile.md)  
**<ProfileCreationType>**

## <a name="syntax"></a><span data-ttu-id="3e390-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e390-108">Syntax</span></span>

``` syntax
<ProfileCreationType>

  "UserProvisioned" | "AdminProvisioned" | "OperatorProvisioned" | "DeviceProvisioned"

</ProfileCreationType>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3e390-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3e390-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3e390-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="3e390-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3e390-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3e390-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3e390-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3e390-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3e390-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3e390-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3e390-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3e390-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e390-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3e390-115">Parent Element</span></span></th>
<th><span data-ttu-id="3e390-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3e390-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e390-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span><span class="sxs-lookup"><span data-stu-id="3e390-117"><a href="element-modemdmconfigprofile.md">ModemDMConfigProfile</a></span></span></td>
<td><p><span data-ttu-id="3e390-118">Perfil de configuración de DM de módem.</span><span class="sxs-lookup"><span data-stu-id="3e390-118">Modem DM configuration profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="related-elements"></a><span data-ttu-id="3e390-119">Elementos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e390-119">Related elements</span></span>

<span data-ttu-id="3e390-120">Los elementos siguientes tienen el mismo nombre que este, pero contenido o atributos diferentes:</span><span class="sxs-lookup"><span data-stu-id="3e390-120">The following elements have the same name as this one, but different content or attributes:</span></span>

-   <span data-ttu-id="3e390-121">**[ProfileCreationType (en MBNProfileExt)](element-profilecreationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="3e390-121">**[ProfileCreationType (in MBNProfileExt)](element-profilecreationtype.md)**</span></span>

## <a name="requirements"></a><span data-ttu-id="3e390-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e390-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e390-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e390-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 



