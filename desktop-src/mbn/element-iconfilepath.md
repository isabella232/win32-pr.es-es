---
description: ICONFilePath
MS-HAID: WWAN\_profile\_v4.element\_ICONFilePath
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: ICONFilePath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 273f8a48cb099c95aaa0b54d438e06b3e1f0bb63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720356"
---
# <a name="span-idwwan_profile_v4element_iconfilepathspaniconfilepath"></a><span data-ttu-id="266a4-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span><span class="sxs-lookup"><span data-stu-id="266a4-103"><span id="WWAN_profile_v4.element_ICONFilePath"></span>ICONFilePath</span></span>

<span data-ttu-id="266a4-104">La ruta de acceso al archivo de icono para la conexión.</span><span class="sxs-lookup"><span data-stu-id="266a4-104">The path to the icon file for the connection.</span></span> <span data-ttu-id="266a4-105">La interfaz de usuario de la conexión del sistema operativo muestra el icono cuando se realiza una conexión con este perfil.</span><span class="sxs-lookup"><span data-stu-id="266a4-105">The operating system connection user interface displays the icon when a connection is made using this profile.</span></span>

<span data-ttu-id="266a4-106">Para obtener más información sobre el uso de este elemento, consulte la documentación de la versión 1 de [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span><span class="sxs-lookup"><span data-stu-id="266a4-106">For more details on using this element, see the v1 documentation for [**ICONFilePath**](./schema-iconfilepath-mbnprofile-element.md).</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="266a4-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="266a4-107">Element hierarchy</span></span>

[<MBNProfileExt>](element-mbnprofileext.md)  
**<ICONFilePath>**

## <a name="syntax"></a><span data-ttu-id="266a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="266a4-108">Syntax</span></span>

``` syntax
<ICONFilePath>

  iconFileType

</ICONFilePath>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="266a4-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="266a4-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="266a4-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="266a4-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="266a4-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="266a4-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="266a4-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="266a4-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="266a4-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="266a4-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="266a4-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="266a4-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="266a4-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="266a4-115">Parent Element</span></span></th>
<th><span data-ttu-id="266a4-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="266a4-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="266a4-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span><span class="sxs-lookup"><span data-stu-id="266a4-117"><a href="element-mbnprofileext.md">MBNProfileExt</a></span></span></td>
<td><p><span data-ttu-id="266a4-118">El elemento <strong>MBNProfileExt</strong> es una extensión del elemento MBNProfile anterior.</span><span class="sxs-lookup"><span data-stu-id="266a4-118">The <strong>MBNProfileExt</strong> element is an extension of the earlier MBNProfile element.</span></span> <span data-ttu-id="266a4-119">Identifica un perfil de banda ancha móvil con un conjunto de opciones más completo que el elemento MBNProfile.</span><span class="sxs-lookup"><span data-stu-id="266a4-119">It identifies a Mobile Broadband profile with a richer set of options than the MBNProfile element.</span></span></p>
<p><span data-ttu-id="266a4-120">Puede haber más de un elemento MbnProfileExt en un perfil, que describe la configuración del perfil para un conjunto determinado de condiciones de funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="266a4-120">There can be more than one MbnProfileExt element in a profile, describing profile settings for a particular set of operating conditions.</span></span> <span data-ttu-id="266a4-121">Use el elemento secundario <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> de <strong>MBNProfileExt</strong> para especificar qué condiciones de funcionamiento convierten un perfil determinado en el perfil activo.</span><span class="sxs-lookup"><span data-stu-id="266a4-121">Use the <a href="element-profileconditionedon.md"><strong>ProfileConditionedOn</strong></a> child element of <strong>MBNProfileExt</strong> to specify which operating conditions make a particular profile the active profile.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="266a4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="266a4-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="266a4-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="266a4-123">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
