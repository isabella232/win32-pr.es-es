---
title: TooManyChildren
description: TooManyChildren
ms.assetid: BF667CDC-C1F9-44B2-B64C-CD7F085CA364
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1e0eee0c29d0d5ee4cdfe66ee5b61aef4b31b32
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268849"
---
# <a name="toomanychildren"></a><span data-ttu-id="89922-103">TooManyChildren</span><span class="sxs-lookup"><span data-stu-id="89922-103">TooManyChildren</span></span>

## <a name="text"></a><span data-ttu-id="89922-104">Texto</span><span class="sxs-lookup"><span data-stu-id="89922-104">Text</span></span>

<span data-ttu-id="89922-105">Se detuvo buscando elementos del mismo nivel adicionales después de encontrar {0} elementos del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="89922-105">Stopped looking for additional siblings after finding {0} siblings.</span></span> <span data-ttu-id="89922-106">Posible árbol incorrecto</span><span class="sxs-lookup"><span data-stu-id="89922-106">Possible incorrect tree</span></span>

## <a name="type"></a><span data-ttu-id="89922-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="89922-107">Type</span></span>

<span data-ttu-id="89922-108">Advertencia</span><span class="sxs-lookup"><span data-stu-id="89922-108">Warning</span></span>

## <a name="description"></a><span data-ttu-id="89922-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="89922-109">Description</span></span>

<span data-ttu-id="89922-110">El árbol de elementos puede ser cíclico y la profundidad de árbol infinita.</span><span class="sxs-lookup"><span data-stu-id="89922-110">The element tree might be cyclic and the tree depth infinite.</span></span>

<span data-ttu-id="89922-111">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que especifica lo que parece ser una referencia circular o un bucle infinito.</span><span class="sxs-lookup"><span data-stu-id="89922-111">This issue can cause navigation problems for automated tools because they will enter what appears to be a circular reference or infinite loop.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="89922-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="89922-112">Possible causes</span></span>

-   <span data-ttu-id="89922-113">El diseño de la aplicación o el control puede ser demasiado complejo.</span><span class="sxs-lookup"><span data-stu-id="89922-113">Application or control design may be too complex.</span></span> <span data-ttu-id="89922-114">Esta advertencia puede aparecer para los controles de vista de lista que tienen un gran número de elementos.</span><span class="sxs-lookup"><span data-stu-id="89922-114">This warning might be reported for list-view controls that have a large number of items.</span></span> <span data-ttu-id="89922-115">En estos casos, normalmente puede omitir esta advertencia.</span><span class="sxs-lookup"><span data-stu-id="89922-115">In these cases, you can typically ignore this warning.</span></span>
-   <span data-ttu-id="89922-116">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="89922-116">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89922-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89922-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89922-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="89922-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




