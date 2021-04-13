---
title: ElementHasNoName
description: ElementHasNoName
ms.assetid: 893A758F-BD34-4ABE-A99E-8CABE33966E0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc9af7e1ad0a62f35edb88102b68bfa6de3d5c28
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357768"
---
# <a name="elementhasnoname"></a><span data-ttu-id="fb3b7-103">ElementHasNoName</span><span class="sxs-lookup"><span data-stu-id="fb3b7-103">ElementHasNoName</span></span>

## <a name="text"></a><span data-ttu-id="fb3b7-104">Texto</span><span class="sxs-lookup"><span data-stu-id="fb3b7-104">Text</span></span>

<span data-ttu-id="fb3b7-105">El elemento no tiene nombre</span><span class="sxs-lookup"><span data-stu-id="fb3b7-105">Element has no name</span></span>

## <a name="type"></a><span data-ttu-id="fb3b7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb3b7-106">Type</span></span>

<span data-ttu-id="fb3b7-107">Error</span><span class="sxs-lookup"><span data-stu-id="fb3b7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="fb3b7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb3b7-108">Description</span></span>

<span data-ttu-id="fb3b7-109">Un elemento no tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-109">An element does not have a name.</span></span> <span data-ttu-id="fb3b7-110">Por ejemplo, el elemento no tiene accName implementado y se devuelve una cadena vacía cuando se usa el método [**Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) para recuperar el nombre de MSAA del elemento.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-110">For example, the element does not have accName implemented and an empty string is returned when the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method is used to retrieve the MSAA name of the element.</span></span>

<span data-ttu-id="fb3b7-111">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque un elemento podría identificarse incorrectamente al usuario.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might be incorrectly identified to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fb3b7-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="fb3b7-112">Possible causes</span></span>

-   <span data-ttu-id="fb3b7-113">El elemento o su elemento primario no tiene nombre o etiqueta.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-113">The element or its parent has no name or label.</span></span>
-   <span data-ttu-id="fb3b7-114">Al elemento se le asigna un [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) que sugiere que el elemento tiene un nombre.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-114">The element is assigned an [**accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) that suggests the element have a name.</span></span>
-   <span data-ttu-id="fb3b7-115">El elemento que tiene el foco no debe recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-115">The element that has focus should not receive focus.</span></span> <span data-ttu-id="fb3b7-116">Por ejemplo, una etiqueta o un control deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-116">For example, a label or a disabled control.</span></span>
-   <span data-ttu-id="fb3b7-117">Un control invisible ha recibido el foco.</span><span class="sxs-lookup"><span data-stu-id="fb3b7-117">An invisible control has received focus.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fb3b7-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb3b7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb3b7-119">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="fb3b7-119">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="fb3b7-120">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="fb3b7-120">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




