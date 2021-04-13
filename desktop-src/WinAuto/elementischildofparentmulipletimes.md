---
title: ElementIsChildOfParentMulipleTimes
description: ElementIsChildOfParentMulipleTimes
ms.assetid: B966ABE0-5109-4DAD-8125-EB4A3B3A5F61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da27c66027f7948dfa794c85dace015565d636c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269468"
---
# <a name="elementischildofparentmulipletimes"></a><span data-ttu-id="9e9f3-103">ElementIsChildOfParentMulipleTimes</span><span class="sxs-lookup"><span data-stu-id="9e9f3-103">ElementIsChildOfParentMulipleTimes</span></span>

## <a name="text"></a><span data-ttu-id="9e9f3-104">Texto</span><span class="sxs-lookup"><span data-stu-id="9e9f3-104">Text</span></span>

<span data-ttu-id="9e9f3-105">El accParent del elemento es ( {0} ), pero el elemento original es una {1} hora secundaria</span><span class="sxs-lookup"><span data-stu-id="9e9f3-105">Element's accParent is ({0}), but original element is a child {1} times</span></span>

## <a name="type"></a><span data-ttu-id="9e9f3-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9e9f3-106">Type</span></span>

<span data-ttu-id="9e9f3-107">Error</span><span class="sxs-lookup"><span data-stu-id="9e9f3-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9e9f3-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e9f3-108">Description</span></span>

<span data-ttu-id="9e9f3-109">Cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento de destino, notifica que es un elemento secundario del mismo elemento primario varias veces.</span><span class="sxs-lookup"><span data-stu-id="9e9f3-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the target element, it reports being a child of the same parent multiple times.</span></span>

<span data-ttu-id="9e9f3-110">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="9e9f3-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9e9f3-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="9e9f3-111">Possible causes</span></span>

<span data-ttu-id="9e9f3-112">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="9e9f3-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e9f3-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e9f3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e9f3-114">**IAccessible:: get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="9e9f3-114">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




