---
description: MBNProfileExt \/ ... \/ Contraseña (v4)
MS-HAID: WWAN\_profile\_v4.element\_Password
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Contraseña
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5d8816c7-a3be-4a9c-a3e0-5c12230dc06f
api_name:
- Password
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c90b2481aa503b7b616d21fca24917b960a92dc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275509"
---
# <a name="span-idwwan_profile_v4element_passwordspanmbnprofileextpassword-v4"></a><span data-ttu-id="1cc5d-103"><span id="WWAN_profile_v4.element_Password"></span>MBNProfileExt \/ ... \/ Contraseña (v4)</span><span class="sxs-lookup"><span data-stu-id="1cc5d-103"><span id="WWAN_profile_v4.element_Password"></span>MBNProfileExt\/...\/Password (v4)</span></span>

<span data-ttu-id="1cc5d-104">Especifica la contraseña que se usa para autenticar a un usuario.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-104">Specifies the password used to authenticate a user.</span></span>

<span data-ttu-id="1cc5d-105">Para obtener más información, consulte la documentación del elemento de [**contraseña**](./schema-password-userlogoncred-element.md) v1.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-105">For more information, see the documentation for the v1 [**Password**](./schema-password-userlogoncred-element.md) element.</span></span>

## <a name="element-hierarchy"></a><span data-ttu-id="1cc5d-106">Jerarquía de elemento</span><span class="sxs-lookup"><span data-stu-id="1cc5d-106">Element hierarchy</span></span>

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;[\<UserLogonCred\>](element-1-userlogoncred.md)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**\<Password\>**

## <a name="syntax"></a><span data-ttu-id="1cc5d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc5d-107">Syntax</span></span>

``` syntax
<Password>

  string

</Password>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span data-ttu-id="1cc5d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos y elementos</span><span class="sxs-lookup"><span data-stu-id="1cc5d-108"><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attributes and Elements</span></span>

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span data-ttu-id="1cc5d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos</span><span class="sxs-lookup"><span data-stu-id="1cc5d-109"><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>

<span data-ttu-id="1cc5d-110">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-110">None.</span></span>

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span data-ttu-id="1cc5d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos secundarios</span><span class="sxs-lookup"><span data-stu-id="1cc5d-111"><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Child Elements</span></span>

<span data-ttu-id="1cc5d-112">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-112">None.</span></span>

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span data-ttu-id="1cc5d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos primarios</span><span class="sxs-lookup"><span data-stu-id="1cc5d-113"><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Parent Elements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1cc5d-114">Elemento primario</span><span class="sxs-lookup"><span data-stu-id="1cc5d-114">Parent Element</span></span></th>
<th><span data-ttu-id="1cc5d-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="1cc5d-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1cc5d-116"><a href="element-userlogoncred.md">UserLogonCred</a></span><span class="sxs-lookup"><span data-stu-id="1cc5d-116"><a href="element-userlogoncred.md">UserLogonCred</a></span></span></td>
<td><p><span data-ttu-id="1cc5d-117">Credenciales de inicio de sesión para una conexión.</span><span class="sxs-lookup"><span data-stu-id="1cc5d-117">Logon credentials for a connection.</span></span></p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a><span data-ttu-id="1cc5d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc5d-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1cc5d-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1cc5d-119">Namespace</span></span></p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
