---
title: Anidar en modo mixto
description: En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Anidar en AD en modo mixto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903102"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="62002-104">Anidar en modo mixto</span><span class="sxs-lookup"><span data-stu-id="62002-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="62002-105">En este tema se enumeran las restricciones de los grupos de seguridad en un dominio de modo mixto.</span><span class="sxs-lookup"><span data-stu-id="62002-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="62002-106">Los grupos de seguridad en un dominio de modo mixto tienen las siguientes restricciones:</span><span class="sxs-lookup"><span data-stu-id="62002-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="62002-107">No se pueden crear grupos universales en dominios de modo mixto porque el ámbito universal solo es compatible con dominios de modo nativo de Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="62002-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="62002-108">Un grupo global puede contener cuentas del mismo dominio al que pertenece el grupo.</span><span class="sxs-lookup"><span data-stu-id="62002-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="62002-109">Un grupo global no puede contener grupos universales, ningún grupo global o una cuenta de otro dominio.</span><span class="sxs-lookup"><span data-stu-id="62002-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="62002-110">Un grupo local de dominio puede contener grupos y cuentas globales de cualquier dominio o bosque.</span><span class="sxs-lookup"><span data-stu-id="62002-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="62002-111">Un grupo local de dominio no puede contener ningún otro grupo local de dominio.</span><span class="sxs-lookup"><span data-stu-id="62002-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="62002-112">Tenga en cuenta que los grupos de distribución se pueden anidar según las reglas de anidamiento del modo nativo.</span><span class="sxs-lookup"><span data-stu-id="62002-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




