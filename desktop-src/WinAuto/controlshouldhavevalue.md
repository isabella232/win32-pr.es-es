---
title: ControlShouldHaveValue
description: ControlShouldHaveValue
ms.assetid: 90C37CC5-21D2-4D26-B6D9-2C95C52127BF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b078712319ffcfde386df519837ba467ca2fcf4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268938"
---
# <a name="controlshouldhavevalue"></a><span data-ttu-id="e8d16-103">ControlShouldHaveValue</span><span class="sxs-lookup"><span data-stu-id="e8d16-103">ControlShouldHaveValue</span></span>

## <a name="text"></a><span data-ttu-id="e8d16-104">Texto</span><span class="sxs-lookup"><span data-stu-id="e8d16-104">Text</span></span>

<span data-ttu-id="e8d16-105">Un control con el rol de {0} debe tener un valor, pero \_ no se implementa Get accValue</span><span class="sxs-lookup"><span data-stu-id="e8d16-105">A control with role of {0} should have a value but get\_accValue is not implemented</span></span>

## <a name="type"></a><span data-ttu-id="e8d16-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="e8d16-106">Type</span></span>

<span data-ttu-id="e8d16-107">Error</span><span class="sxs-lookup"><span data-stu-id="e8d16-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="e8d16-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e8d16-108">Description</span></span>

<span data-ttu-id="e8d16-109">Un elemento no proporciona un valor según lo previsto según el rol de MSAA asignado, lo que implica que el elemento no tiene implementado el método [**Get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) .</span><span class="sxs-lookup"><span data-stu-id="e8d16-109">An element does not supply a value as expected based on the assigned MSAA role, implying that the element does not have the [**get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) method implemented.</span></span> <span data-ttu-id="e8d16-110">Por ejemplo, los siguientes roles de MSAA deben proporcionar un valor.</span><span class="sxs-lookup"><span data-stu-id="e8d16-110">For example, the following MSAA roles should all supply a value.</span></span>

-   <span data-ttu-id="e8d16-111">\_cuadro combinado de sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-111">ROLE\_SYSTEM\_COMBOBOX</span></span>
-   <span data-ttu-id="e8d16-112">\_IPAddress del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-112">ROLE\_SYSTEM\_IPADDRESS</span></span>
-   <span data-ttu-id="e8d16-113">\_vínculo del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-113">ROLE\_SYSTEM\_LINK</span></span>
-   <span data-ttu-id="e8d16-114">\_OUTLINEITEM del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-114">ROLE\_SYSTEM\_OUTLINEITEM</span></span>
-   <span data-ttu-id="e8d16-115">\_PROGRESSBAR del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-115">ROLE\_SYSTEM\_PROGRESSBAR</span></span>
-   <span data-ttu-id="e8d16-116">\_control deslizante del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-116">ROLE\_SYSTEM\_SLIDER</span></span>
-   <span data-ttu-id="e8d16-117">\_SPINBUTTON del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-117">ROLE\_SYSTEM\_SPINBUTTON</span></span>
-   <span data-ttu-id="e8d16-118">\_barra de desplazamiento del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-118">ROLE\_SYSTEM\_SCROLLBAR</span></span>
-   <span data-ttu-id="e8d16-119">\_texto del sistema de roles \_</span><span class="sxs-lookup"><span data-stu-id="e8d16-119">ROLE\_SYSTEM\_TEXT</span></span>

<span data-ttu-id="e8d16-120">Este problema es un problema para las personas que usan un lector de pantalla y un teclado para la navegación porque un elemento que tiene un valor intrínseco debe ser capaz de notificar ese valor a un usuario.</span><span class="sxs-lookup"><span data-stu-id="e8d16-120">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because an element that has an intrinsic value must be able to report that value to a user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e8d16-121">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="e8d16-121">Possible causes</span></span>

<span data-ttu-id="e8d16-122">El elemento o su elemento primario tiene un rol de MSAA establecido incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="e8d16-122">The element or its parent has an MSAA role set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8d16-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e8d16-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8d16-124">**IAccessible:: get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="e8d16-124">**IAccessible::get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[<span data-ttu-id="e8d16-125">**Roles de objeto**</span><span class="sxs-lookup"><span data-stu-id="e8d16-125">**Object Roles**</span></span>](object-roles.md)
</dt> </dl>

 

 




