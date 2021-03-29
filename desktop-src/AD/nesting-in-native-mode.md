---
title: Anidar en modo nativo
description: En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio de modo nativo.
ms.assetid: 7992ef2d-9dcf-4087-b09a-35235b23e499
ms.tgt_platform: multiple
keywords:
- Anidar en AD en modo nativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69dba115bb705fe706a049e85136475c6d5b3a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903101"
---
# <a name="nesting-in-native-mode"></a><span data-ttu-id="447ef-104">Anidar en modo nativo</span><span class="sxs-lookup"><span data-stu-id="447ef-104">Nesting in Native Mode</span></span>

<span data-ttu-id="447ef-105">En la lista siguiente se describe lo que puede incluirse en un grupo que existe en un dominio de modo nativo.</span><span class="sxs-lookup"><span data-stu-id="447ef-105">The following list describes what can be contained in a group that exists in a native-mode domain.</span></span> <span data-ttu-id="447ef-106">Esta misma lista también se aplica a los grupos de distribución en dominios de modo mixto.</span><span class="sxs-lookup"><span data-stu-id="447ef-106">This same list also applies to distribution groups in mixed-mode domains.</span></span> <span data-ttu-id="447ef-107">El ámbito del Grupo determina las reglas de contención.</span><span class="sxs-lookup"><span data-stu-id="447ef-107">The scope of the group determines these containment rules.</span></span>

-   <span data-ttu-id="447ef-108">Un grupo universal puede contener otros grupos universales, grupos globales y cuentas de cualquier dominio del bosque en el que reside este grupo universal.</span><span class="sxs-lookup"><span data-stu-id="447ef-108">A universal group can contain other universal groups, global groups and accounts from any domain within the forest in which this Universal Group resides.</span></span>
-   <span data-ttu-id="447ef-109">Un grupo global puede contener otros grupos y cuentas globales del mismo dominio al que pertenece el grupo.</span><span class="sxs-lookup"><span data-stu-id="447ef-109">A global group can contain other global groups and accounts from the same domain that the group belongs to.</span></span> <span data-ttu-id="447ef-110">Un grupo global no puede contener grupos universales ni cualquier grupo o cuenta global de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="447ef-110">A global group cannot contain any universal groups, or any global group or account from another domain.</span></span>
-   <span data-ttu-id="447ef-111">Un grupo local de dominio puede contener grupos universales, grupos globales y cuentas de cualquier dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="447ef-111">A domain local group can contain universal groups, global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="447ef-112">Un grupo local de dominio también puede contener otros grupos locales de dominio del mismo dominio al que pertenece el grupo.</span><span class="sxs-lookup"><span data-stu-id="447ef-112">A domain local group can also contain other domain local groups from the same domain that the group belongs to.</span></span> <span data-ttu-id="447ef-113">Un grupo local de dominio no puede contener otros grupos locales de dominio de ningún otro dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="447ef-113">A domain local group cannot contain other domain local groups from any other domain or forest.</span></span>

 

 




