---
description: ModemDMConfigProfile \/ ... \/ Nombre de usuario (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_UserName
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: UserName
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 1b43a275-cdbd-44e6-adc6-121aa935447e
api_name:
- UserName
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5e31cd6bdb4e623ee7bbb57fb02cbbbbbcd393f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154204"
---
# <a name="span-idwwan_profile_v4element_1_usernamespanmodemdmconfigprofileusername-v4"></a><span data-ttu-id="3f01e-103"><span id="WWAN_profile_v4.element_1_UserName"></span>ModemDMConfigProfile \/ ... \/ Nombre de usuario (v4)</span><span class="sxs-lookup"><span data-stu-id="3f01e-103"><span id="WWAN_profile_v4.element_1_UserName"></span>ModemDMConfigProfile\/...\/UserName (v4)</span></span>

<span data-ttu-id="3f01e-104">El nombre de usuario que se usará para el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="3f01e-104">The user name to use for logon.</span></span>

<span data-ttu-id="3f01e-105">Para obtener más información, consulte la documentación del elemento de [**nombre de usuario**](./schema-username-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="3f01e-105">For more details, see the documentation for the v1 [**UserName**](./schema-username-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="3f01e-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="3f01e-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<UserName\>**

## <a name="syntax"></a><span data-ttu-id="3f01e-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f01e-107">Syntax</span></span>

``` syntax
<UserName>

  nameType

</UserName>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="3f01e-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="3f01e-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="3f01e-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="3f01e-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="3f01e-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f01e-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="3f01e-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="3f01e-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="3f01e-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="3f01e-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="3f01e-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="3f01e-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3f01e-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="3f01e-114">Parent Element</span></span></th>
<th><span data-ttu-id="3f01e-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="3f01e-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3f01e-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="3f01e-116"><a href="element-1-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="3f01e-117">Credenciales de inicio de sesión para una conexión.</span><span class="sxs-lookup"><span data-stu-id="3f01e-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="3f01e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f01e-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3f01e-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f01e-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
