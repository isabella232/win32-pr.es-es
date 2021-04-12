---
title: AccessibleObjectFromPointReturnedNullIAccessible
description: AccessibleObjectFromPointReturnedNullIAccessible
ms.assetid: DF786659-8ADC-4EB0-A606-8B80C139691A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c5807fa04f69271f2a2d38e7014b1cd17d4eaa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357670"
---
# <a name="accessibleobjectfrompointreturnednulliaccessible"></a><span data-ttu-id="ad514-103">AccessibleObjectFromPointReturnedNullIAccessible</span><span class="sxs-lookup"><span data-stu-id="ad514-103">AccessibleObjectFromPointReturnedNullIAccessible</span></span>

## <a name="text"></a><span data-ttu-id="ad514-104">Texto</span><span class="sxs-lookup"><span data-stu-id="ad514-104">Text</span></span>

<span data-ttu-id="ad514-105">AccessibleObjectFromPoint ( {0} , {1} ) devolvió null</span><span class="sxs-lookup"><span data-stu-id="ad514-105">AccessibleObjectFromPoint({0}, {1}) returned null</span></span>

## <a name="type"></a><span data-ttu-id="ad514-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad514-106">Type</span></span>

<span data-ttu-id="ad514-107">Error</span><span class="sxs-lookup"><span data-stu-id="ad514-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ad514-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ad514-108">Description</span></span>

<span data-ttu-id="ad514-109">La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del elemento de la interfaz de usuario obtenida para las coordenadas dadas es NULL.</span><span class="sxs-lookup"><span data-stu-id="ad514-109">The address of the UI element's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is NULL.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ad514-110">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="ad514-110">Possible causes</span></span>

-   <span data-ttu-id="ad514-111">Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="ad514-111">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="ad514-112">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="ad514-112">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad514-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ad514-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad514-114">Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla</span><span class="sxs-lookup"><span data-stu-id="ad514-114">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="ad514-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="ad514-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




