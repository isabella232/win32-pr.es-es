---
title: Errores comunes (AD DS)
description: La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- ANUNCIOS de errores comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/11/2019
ms.locfileid: "104487251"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="26757-104">Errores comunes (AD DS)</span><span class="sxs-lookup"><span data-stu-id="26757-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="26757-105">La tabla siguiente contiene una lista de errores comunes que pueden producirse en función del ámbito del grupo que se anida.</span><span class="sxs-lookup"><span data-stu-id="26757-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="26757-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="26757-106">HRESULT</span></span></th>
<th><span data-ttu-id="26757-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="26757-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="26757-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="26757-108">0x8007001F</span></span></td>
<td><span data-ttu-id="26757-109">Error general.</span><span class="sxs-lookup"><span data-stu-id="26757-109">General failure.</span></span> <span data-ttu-id="26757-110">Este error se produce si intenta:</span><span class="sxs-lookup"><span data-stu-id="26757-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="26757-111">Agregue un grupo local de dominio a un grupo global o universal o a un grupo local de dominio de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="26757-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="26757-112">Los grupos locales de dominio solo se pueden agregar como miembros a otros grupos locales de dominio del mismo dominio.</span><span class="sxs-lookup"><span data-stu-id="26757-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="26757-113">Agregue un grupo universal a un grupo global.</span><span class="sxs-lookup"><span data-stu-id="26757-113">Add a universal group to a global group.</span></span> <span data-ttu-id="26757-114">Los grupos universales se pueden agregar a grupos locales de dominio y universales, pero no a grupos globales.</span><span class="sxs-lookup"><span data-stu-id="26757-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="26757-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="26757-115">0x8007202F</span></span></td>
<td><span data-ttu-id="26757-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="26757-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="26757-117">Este error se produce si intenta agregar un grupo de seguridad a otro grupo en un dominio que se ejecuta en modo mixto.</span><span class="sxs-lookup"><span data-stu-id="26757-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="26757-118">Los grupos de seguridad no se pueden anidar en modo mixto; los grupos de seguridad solo se pueden anidar en modo nativo.</span><span class="sxs-lookup"><span data-stu-id="26757-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




