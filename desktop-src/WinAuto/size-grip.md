---
title: Control de tamaño (referencia de elementos de interfaz de usuario de MSAA)
description: El control de tamaño es un puntero especial del mouse en la esquina inferior derecha de una ventana que permite al usuario hacer clic y arrastrar el control de tamaño para cambiar el tamaño de la ventana.
ms.assetid: 886b27b3-e88d-47a1-85f3-a55bd14c7a7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fb7180a8936aff46903257e6be8ca4ab7f0e5b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779669"
---
# <a name="size-grip-msaa-ui-element-reference"></a><span data-ttu-id="09bfe-103">Control de tamaño (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="09bfe-103">Size Grip (MSAA UI Element Reference)</span></span>

<span data-ttu-id="09bfe-104">El control de tamaño es un puntero especial del mouse en la esquina inferior derecha de una ventana que permite al usuario hacer clic y arrastrar el control de tamaño para cambiar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="09bfe-104">The size grip is a special mouse pointer in the lower-right corner of a window that allows a user to click and drag the size grip to resize the window.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="09bfe-105">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="09bfe-105">IAccessible Methods</span></span>

<span data-ttu-id="09bfe-106">El control de tamaño admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="09bfe-106">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="09bfe-107">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="09bfe-107">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="09bfe-108">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="09bfe-108">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="09bfe-109">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="09bfe-109">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="09bfe-110">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="09bfe-110">IAccessible Properties</span></span>

<span data-ttu-id="09bfe-111">El control de tamaño admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="09bfe-111">The size grip supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="09bfe-112">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09bfe-112">Property</span></span>                                                                   | <span data-ttu-id="09bfe-113">Comentarios</span><span class="sxs-lookup"><span data-stu-id="09bfe-113">Comments</span></span>                                                                                                                                                               |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09bfe-114">**obtener \_ accDescription**</span><span class="sxs-lookup"><span data-stu-id="09bfe-114">**get\_accDescription**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdescription) | <span data-ttu-id="09bfe-115">La propiedad **Description** es "se puede usar para cambiar el ancho y el alto de una ventana".</span><span class="sxs-lookup"><span data-stu-id="09bfe-115">The **Description** property is "Can be used to resize a window's width and height".</span></span>                                                                                   |
| [<span data-ttu-id="09bfe-116">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="09bfe-116">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)               | <span data-ttu-id="09bfe-117">La propiedad **Name** es "size Box".</span><span class="sxs-lookup"><span data-stu-id="09bfe-117">The **Name** property is "Size box".</span></span>                                                                                                                                   |
| [<span data-ttu-id="09bfe-118">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="09bfe-118">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)           | <span data-ttu-id="09bfe-119">Ventana que contiene el control de tamaño.</span><span class="sxs-lookup"><span data-stu-id="09bfe-119">The window that contains the size grip.</span></span>                                                                                                                                |
| [<span data-ttu-id="09bfe-120">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="09bfe-120">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)               | <span data-ttu-id="09bfe-121">La propiedad **role** es [**el \_ \_ control del sistema de funciones**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="09bfe-121">The **Role** property is [**ROLE\_SYSTEM\_GRIP**](object-roles.md).</span></span>                                                                                  |
| [<span data-ttu-id="09bfe-122">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="09bfe-122">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)             | <span data-ttu-id="09bfe-123">El valor de la propiedad **State** es cero, lo que significa que el objeto es visible o que el [**sistema de estado es \_ \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="09bfe-123">The value for the **State** property is zero, which means the object is visible, or [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="09bfe-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="09bfe-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="09bfe-125">IAccessible</span><span class="sxs-lookup"><span data-stu-id="09bfe-125">IAccessible</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




