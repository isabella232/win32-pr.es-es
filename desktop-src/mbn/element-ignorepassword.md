---
description: MBNProfileExt \/ ... \/ IgnorePassword (v4)
MS-HAID: WWAN\_profile\_v4.element\_IgnorePassword
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IgnorePassword
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc73050a01f6f0f9799290ba267b8ecaaee1003a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275513"
---
# <a name="span-idwwan_profile_v4element_ignorepasswordspanmbnprofileextignorepassword-v4"></a><span data-ttu-id="59753-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>MBNProfileExt \/ ... \/ IgnorePassword (v4)</span><span class="sxs-lookup"><span data-stu-id="59753-103"><span id="WWAN_profile_v4.element_IgnorePassword"></span>MBNProfileExt\/...\/IgnorePassword (v4)</span></span>

<span data-ttu-id="59753-104">Especifica cómo se administran las contraseñas al actualizar perfiles.</span><span class="sxs-lookup"><span data-stu-id="59753-104">Specifies how passwords are handled when upgrading profiles.</span></span>

<span data-ttu-id="59753-105">Si se establece en **true** y existe un perfil con el mismo nombre en el momento de la operación de actualización, se tomará la contraseña de ese perfil y se almacenará en el nuevo perfil.</span><span class="sxs-lookup"><span data-stu-id="59753-105">If set to **TRUE** and a profile with the same name exists at the time of the update operation, then the password from that profile will be taken and stored in the new profile.</span></span>

<span data-ttu-id="59753-106">Para obtener más información, consulte la documentación del elemento [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="59753-106">For more details, see the documentation for the v1 [**IgnorePassword**](./schema-ignorepassword-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="59753-107">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="59753-107">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<IgnorePassword\>**

## <a name="syntax"></a><span data-ttu-id="59753-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="59753-108">Syntax</span></span>

``` syntax
<IgnorePassword>

  boolean

</IgnorePassword>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="59753-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="59753-109"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="59753-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="59753-110"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="59753-111">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="59753-111">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="59753-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="59753-112"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="59753-113">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="59753-113">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="59753-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="59753-114"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="59753-115">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="59753-115">Parent Element</span></span></th>
<th><span data-ttu-id="59753-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="59753-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="59753-117"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="59753-117"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="59753-118">Credenciales de inicio de sesión para una conexión.</span><span class="sxs-lookup"><span data-stu-id="59753-118">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="59753-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59753-119">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="59753-120">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="59753-120">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
