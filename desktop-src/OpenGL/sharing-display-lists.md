---
title: Compartir listas de visualización
description: Cuando se crea un contexto de representación, tiene su propio espacio de lista de presentación.
ms.assetid: 8ace5684-a27b-4d6e-a80b-58a0b7064879
keywords:
- OpenGL en Windows, compartir listas de visualización
- compartir listas de visualización OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d8d012e8e04455f76ca5d7bfe74229ac0b0ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357618"
---
# <a name="sharing-display-lists"></a><span data-ttu-id="402be-105">Compartir listas de visualización</span><span class="sxs-lookup"><span data-stu-id="402be-105">Sharing Display Lists</span></span>

<span data-ttu-id="402be-106">Cuando se crea un contexto de representación, tiene su propio espacio de lista de presentación.</span><span class="sxs-lookup"><span data-stu-id="402be-106">When you create a rendering context, it has its own display-list space.</span></span> <span data-ttu-id="402be-107">La función [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) permite a un contexto de representación compartir el espacio de la lista de presentación de otro contexto de representación.</span><span class="sxs-lookup"><span data-stu-id="402be-107">The [**wglShareLists**](/windows/desktop/api/wingdi/nf-wingdi-wglsharelists) function enables a rendering context to share the display-list space of another rendering context.</span></span> <span data-ttu-id="402be-108">Cualquier número de contextos de representación puede compartir un solo espacio de lista de presentación.</span><span class="sxs-lookup"><span data-stu-id="402be-108">Any number of rendering contexts can share a single display-list space.</span></span>

 

 




