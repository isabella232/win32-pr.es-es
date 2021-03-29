---
title: Cambiar el ámbito o el tipo de un grupo
description: En este tema se muestra cómo cambiar el ámbito o el tipo de un grupo en dominios de modo nativo.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- agrupar AD, cambiar el ámbito o el tipo de un grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772744"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="2098a-104">Cambiar el ámbito o el tipo de un grupo</span><span class="sxs-lookup"><span data-stu-id="2098a-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="2098a-105">No se permite cambiar un tipo o ámbito de grupo en dominios de modo mixto.</span><span class="sxs-lookup"><span data-stu-id="2098a-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="2098a-106">Sin embargo, en los dominios de modo nativo se permiten las siguientes conversiones:</span><span class="sxs-lookup"><span data-stu-id="2098a-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="2098a-107">Grupo global a grupo universal: solo se permite si el grupo global no es miembro de otro grupo global.</span><span class="sxs-lookup"><span data-stu-id="2098a-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="2098a-108">Grupo local de dominio a grupo universal: el grupo local de dominio que se va a convertir no puede contener otro grupo local de dominio.</span><span class="sxs-lookup"><span data-stu-id="2098a-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="2098a-109">Grupo universal a grupo local de dominio o global: para la conversión al grupo global, el grupo universal que se está convirtiendo no puede contener usuarios o grupos globales de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="2098a-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="2098a-110">Para la conversión a un grupo local de dominio, el grupo universal que se va a convertir no puede ser miembro de ningún grupo universal o de un grupo local de dominio de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="2098a-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="2098a-111">En modo nativo, un tipo de grupo se puede convertir libremente entre grupos de seguridad y grupos de distribución.</span><span class="sxs-lookup"><span data-stu-id="2098a-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="2098a-112">Tenga en cuenta que si se usa un grupo para establecer el control de acceso, el cambio de ámbito o tipo puede afectar a las entradas de control de acceso (ACE) que contienen ese grupo.</span><span class="sxs-lookup"><span data-stu-id="2098a-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="2098a-113">El sistema de seguridad omitirá las ACE que contienen grupos que no son grupos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="2098a-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




