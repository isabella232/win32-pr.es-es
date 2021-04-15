---
description: IsAdditionalPdpContextProfile
MS-HAID: WWAN\_profile\_v3.element\_IsAdditionalPdpContextProfile
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IsAdditionalPdpContextProfile
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169aa9a34a561f65eed5dfc315e7711ef6bb9bf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360270"
---
# <a name="span-idwwan_profile_v3element_isadditionalpdpcontextprofilespanisadditionalpdpcontextprofile"></a><span data-ttu-id="841f2-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span><span class="sxs-lookup"><span data-stu-id="841f2-103"><span id="WWAN_profile_v3.element_IsAdditionalPdpContextProfile"></span>IsAdditionalPdpContextProfile</span></span>

<span data-ttu-id="841f2-104">El elemento **IsAdditionalPdpContextProfile** contiene un **valor booleano** que es **true** si se trata de un perfil "PDP adicional (Protocolo de datos de paquetes)" y **false**, de lo contrario,.</span><span class="sxs-lookup"><span data-stu-id="841f2-104">The **IsAdditionalPdpContextProfile** element contains a **boolean** that is **true** if this is an "additional PDP (Packet Data Protocol) context" profile and **false**, otherwise.</span></span> <span data-ttu-id="841f2-105">El valor predeterminado es **false**.</span><span class="sxs-lookup"><span data-stu-id="841f2-105">Default is **false**.</span></span>

<span data-ttu-id="841f2-106">Un perfil de "contexto PDP adicional" es un perfil que no se activa a través del puerto predeterminado del adaptador físico y establecer este elemento en true garantiza que este perfil no se muestre de forma inapropiada en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="841f2-106">An "additional PDP context" profile is a profile that does not get activated over the physical adapter default port, and setting this element to true ensures that this profile is not displayed inappropriately in the user interface.</span></span>

<span data-ttu-id="841f2-107">Tenga en cuenta que si este elemento está establecido en true, también debe cumplirse lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="841f2-107">Note that if this element is set to true, then the following must also be true.</span></span>

-   <span data-ttu-id="841f2-108">El elemento [**IsDefault**](./schema-isdefault-mbnprofile-element.md) no debe especificarse o establecerse en **false** para que el perfil sea válido.</span><span class="sxs-lookup"><span data-stu-id="841f2-108">The [**IsDefault**](./schema-isdefault-mbnprofile-element.md) element must be unspecified or set to **false** for the profile to be valid.</span></span>
-   <span data-ttu-id="841f2-109">El elemento [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) debe estar sin especificar o establecerse en **manual** para que el perfil sea válido.</span><span class="sxs-lookup"><span data-stu-id="841f2-109">The [**ConnectionMode**](./schema-connectionmode-mbnprofile-element.md) element must be unspecified or set to **manual** for the profile to be valid.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="841f2-110">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="841f2-110">Element hierarchy</span></span>

**<IsAdditionalPdpContextProfile>**

## <a name="syntax"></a><span data-ttu-id="841f2-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="841f2-111">Syntax</span></span>

``` syntax
<IsAdditionalPdpContextProfile>

  boolean

</IsAdditionalPdpContextProfile>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="841f2-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="841f2-112"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="841f2-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="841f2-113"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="841f2-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="841f2-114">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="841f2-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="841f2-115"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="841f2-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="841f2-116">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="841f2-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="841f2-117"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<span data-ttu-id="841f2-118">Es posible que este elemento externo (documento) no esté incluido en otros elementos.</span><span class="sxs-lookup"><span data-stu-id="841f2-118">This outermost (document) element may not be contained by any other elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="841f2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="841f2-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="841f2-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="841f2-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v3</p></td>
</tr>
</tbody>
</table>

 

 
