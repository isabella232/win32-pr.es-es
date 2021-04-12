---
title: ElementsChildHasDifferentParent
description: ElementsChildHasDifferentParent
ms.assetid: 2347A33C-8FBD-4C30-8B40-9CB35F121C8E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ea0f0ec7708f91d407f1fa7a55fa59a813234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357767"
---
# <a name="elementschildhasdifferentparent"></a><span data-ttu-id="4c80b-103">ElementsChildHasDifferentParent</span><span class="sxs-lookup"><span data-stu-id="4c80b-103">ElementsChildHasDifferentParent</span></span>

## <a name="text"></a><span data-ttu-id="4c80b-104">Texto</span><span class="sxs-lookup"><span data-stu-id="4c80b-104">Text</span></span>

<span data-ttu-id="4c80b-105">El elemento secundario del elemento ( {0} ) tiene distintos elementos primarios ( {1} ) que</span><span class="sxs-lookup"><span data-stu-id="4c80b-105">Element's child({0}) has different parent({1}) than element</span></span>

## <a name="type"></a><span data-ttu-id="4c80b-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4c80b-106">Type</span></span>

<span data-ttu-id="4c80b-107">Error</span><span class="sxs-lookup"><span data-stu-id="4c80b-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="4c80b-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4c80b-108">Description</span></span>

<span data-ttu-id="4c80b-109">Este error indica que, cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en los elementos secundarios del elemento de destino, los elementos secundarios no informan de un elemento primario coherente.</span><span class="sxs-lookup"><span data-stu-id="4c80b-109">This error indicates that, when [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the children of the target element, the children do not report a consistent parent.</span></span>

![un ejemplo de los elementos secundarios de un elemento que informa de un elemento primario incoherente](images/accchecker-inconsistent-parent.png)

<span data-ttu-id="4c80b-111">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="4c80b-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="4c80b-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="4c80b-112">Possible causes</span></span>

<span data-ttu-id="4c80b-113">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="4c80b-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c80b-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c80b-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c80b-115">**AccessibleChildren**</span><span class="sxs-lookup"><span data-stu-id="4c80b-115">**AccessibleChildren**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren)
</dt> </dl>

 

 




