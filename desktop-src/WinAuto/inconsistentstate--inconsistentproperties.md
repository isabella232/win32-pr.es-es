---
title: InconsistentState, InconsistentProperties
description: InconsistentState, InconsistentProperties
ms.assetid: 82A2ECA8-0155-402A-A745-B97D3F633643
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5522025eff8aecbdf0f4313c0052afebd4a17958
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774263"
---
# <a name="inconsistentstate-inconsistentproperties"></a><span data-ttu-id="1ac64-103">InconsistentState, InconsistentProperties</span><span class="sxs-lookup"><span data-stu-id="1ac64-103">InconsistentState, InconsistentProperties</span></span>

## <a name="text"></a><span data-ttu-id="1ac64-104">Texto</span><span class="sxs-lookup"><span data-stu-id="1ac64-104">Text</span></span>

<span data-ttu-id="1ac64-105">Un control tiene Estados/propiedades incoherentes {0} y {1}</span><span class="sxs-lookup"><span data-stu-id="1ac64-105">A control has states/properties that are inconsistent {0} and {1}</span></span>

## <a name="type"></a><span data-ttu-id="1ac64-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1ac64-106">Type</span></span>

<span data-ttu-id="1ac64-107">Error</span><span class="sxs-lookup"><span data-stu-id="1ac64-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="1ac64-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1ac64-108">Description</span></span>

<span data-ttu-id="1ac64-109">Un elemento informa de los Estados de MSAA incoherentes o en conflicto o de las propiedades de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1ac64-109">An element is reporting inconsistent or conflicting MSAA states or UI Automation properties.</span></span> <span data-ttu-id="1ac64-110">Por ejemplo, cuando el método [**Get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) devuelve cualquiera de las siguientes combinaciones.</span><span class="sxs-lookup"><span data-stu-id="1ac64-110">For example, when the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method returns any of the following combinations.</span></span>

-   <span data-ttu-id="1ac64-111">Sistema \_ \_ de estado expandido y sistema de estado \_ \_ contraído</span><span class="sxs-lookup"><span data-stu-id="1ac64-111">STATE\_SYSTEM\_EXPANDED and STATE\_SYSTEM\_COLLAPSED</span></span>
-   <span data-ttu-id="1ac64-112">\_Sistema \_ de estado seleccionado y no \_ seleccionable del sistema de estado \_</span><span class="sxs-lookup"><span data-stu-id="1ac64-112">STATE\_SYSTEM\_SELECTED and not STATE\_SYSTEM\_SELECTABLE</span></span>
-   <span data-ttu-id="1ac64-113">\_Sistema \_ de estado centrado y sin \_ sistema de estado \_ enfocable</span><span class="sxs-lookup"><span data-stu-id="1ac64-113">STATE\_SYSTEM\_FOCUSED and not STATE\_SYSTEM\_FOCUSABLE</span></span>

<span data-ttu-id="1ac64-114">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque es posible que se notifique al usuario un estado incorrecto del elemento.</span><span class="sxs-lookup"><span data-stu-id="1ac64-114">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="1ac64-115">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="1ac64-115">Possible causes</span></span>

<span data-ttu-id="1ac64-116">El elemento o su elemento primario tiene un estado de MSAA establecido incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="1ac64-116">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ac64-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ac64-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac64-118">**IAccessible:: get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="1ac64-118">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="1ac64-119">**Constantes de estado de objeto**</span><span class="sxs-lookup"><span data-stu-id="1ac64-119">**Object State Constants**</span></span>](object-state-constants.md)
</dt> <dt>

[<span data-ttu-id="1ac64-120">Estados y propiedades</span><span class="sxs-lookup"><span data-stu-id="1ac64-120">States and Properties</span></span>](uiauto-msaa.md)
</dt> </dl>

 

 




