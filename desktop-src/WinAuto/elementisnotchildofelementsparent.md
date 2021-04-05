---
title: ElementIsNotChildOfElementsParent
description: ElementIsNotChildOfElementsParent
ms.assetid: DFD5CC2A-B5F4-49F2-B3EF-2CD447A575E2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a3d62a6ae656bffffca442ed3cbb9b85be8dc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419188"
---
# <a name="elementisnotchildofelementsparent"></a><span data-ttu-id="0506e-103">ElementIsNotChildOfElementsParent</span><span class="sxs-lookup"><span data-stu-id="0506e-103">ElementIsNotChildOfElementsParent</span></span>

## <a name="text"></a><span data-ttu-id="0506e-104">Texto</span><span class="sxs-lookup"><span data-stu-id="0506e-104">Text</span></span>

<span data-ttu-id="0506e-105">El elemento no es un elemento secundario del elemento primario</span><span class="sxs-lookup"><span data-stu-id="0506e-105">Element is not a child of it's parent</span></span>

## <a name="type"></a><span data-ttu-id="0506e-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="0506e-106">Type</span></span>

<span data-ttu-id="0506e-107">Error</span><span class="sxs-lookup"><span data-stu-id="0506e-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="0506e-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="0506e-108">Description</span></span>

<span data-ttu-id="0506e-109">Cuando se llama a [**Get \_ accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) en el elemento secundario devuelto por [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (mediante las \_ constantes de navegación NAVDIR FIRSTCHILD o NAVDIR \_ LASTCHILD), el elemento primario devuelto no coincide con el elemento primario especificado en la llamada **accNavigate** .</span><span class="sxs-lookup"><span data-stu-id="0506e-109">When [**get\_accParent**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent) is called on the child element returned by [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) (using either the NAVDIR\_FIRSTCHILD or NAVDIR\_LASTCHILD navigation constants), the parent element returned does not match the parent element specified in the **accNavigate** call.</span></span>

<span data-ttu-id="0506e-110">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="0506e-110">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="0506e-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="0506e-111">Possible causes</span></span>

<span data-ttu-id="0506e-112">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="0506e-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0506e-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0506e-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0506e-114">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="0506e-114">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> <dt>

[<span data-ttu-id="0506e-115">**IAccessible:: get \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="0506e-115">**IAccessible::get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)
</dt> </dl>

 

 




