---
title: Bosques
description: Un bosque es un conjunto de uno o más árboles de dominio que no forman un espacio de nombres contiguo.
ms.assetid: b7beb305-0022-477a-85bf-779821202b26
ms.tgt_platform: multiple
keywords:
- bosques Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc84fca35ce90b20582bd62a675e6cf8d0285f7e
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995084"
---
# <a name="forests"></a><span data-ttu-id="e2a5e-104">Bosques</span><span class="sxs-lookup"><span data-stu-id="e2a5e-104">Forests</span></span>

<span data-ttu-id="e2a5e-105">Un [*bosque*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) es un conjunto de uno o más árboles de dominio que no forman un espacio de nombres contiguo.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-105">A [*forest*](/previous-versions/windows/desktop/legacy/ms681904(v=vs.85)) is a set of one or more domain trees that do not form a contiguous namespace.</span></span> <span data-ttu-id="e2a5e-106">Todos los árboles de un bosque comparten un esquema, una configuración y un catálogo global comunes.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-106">All trees in a forest share a common schema, configuration, and global catalog.</span></span> <span data-ttu-id="e2a5e-107">Todos los árboles de un bosque determinado confían en la confianza de acuerdo con las relaciones de confianza de Kerberos jerárquicas transitivas.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-107">All trees in a given forest exchange trust according to transitive hierarchical Kerberos trust relationships.</span></span> <span data-ttu-id="e2a5e-108">A diferencia de los árboles, un bosque no requiere un nombre distinto.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-108">Unlike trees, a forest does not require a distinct name.</span></span> <span data-ttu-id="e2a5e-109">Un bosque existe como un conjunto de objetos de referencias cruzadas y relaciones de confianza de Kerberos que reconocen los árboles de miembros.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-109">A forest exists as a set of cross-reference objects and Kerberos trust relationships recognized by the member trees.</span></span> <span data-ttu-id="e2a5e-110">Los árboles de un bosque forman una jerarquía para los fines de la confianza Kerberos; el nombre del árbol situado en la raíz del árbol de confianza hace referencia a un bosque determinado.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-110">Trees in a forest form a hierarchy for the purposes of Kerberos trust; the tree name at the root of the trust tree refers to a given forest.</span></span>

<span data-ttu-id="e2a5e-111">En la ilustración siguiente se muestra un bosque de espacios de nombres no contiguos.</span><span class="sxs-lookup"><span data-stu-id="e2a5e-111">The following figure shows a forest of noncontiguous namespaces.</span></span>

![bosque de espacios de nombres no contiguos](images/forests.png)

 

 