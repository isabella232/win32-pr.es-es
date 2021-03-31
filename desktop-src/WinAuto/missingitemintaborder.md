---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103791788"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="4aff5-103">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="4aff5-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="4aff5-104">Texto</span><span class="sxs-lookup"><span data-stu-id="4aff5-104">Text</span></span>

<span data-ttu-id="4aff5-105">Este elemento parece ser tabulable, pero no está en el orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="4aff5-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="4aff5-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="4aff5-106">Type</span></span>

<span data-ttu-id="4aff5-107">Error</span><span class="sxs-lookup"><span data-stu-id="4aff5-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="4aff5-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="4aff5-108">Description</span></span>

<span data-ttu-id="4aff5-109">No se puede tener acceso A un elemento enfocable mediante la navegación de teclado estándar (TAB o Mayús + Tab).</span><span class="sxs-lookup"><span data-stu-id="4aff5-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="4aff5-110">Por ejemplo, el elemento no se ha marcado como una posición de tabulación o se le ha asignado un índice de tabulación.</span><span class="sxs-lookup"><span data-stu-id="4aff5-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="4aff5-111">Este problema causa problemas para las personas que usan un lector de pantalla y un teclado para la navegación porque:</span><span class="sxs-lookup"><span data-stu-id="4aff5-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="4aff5-112">El elemento no es reconocible.</span><span class="sxs-lookup"><span data-stu-id="4aff5-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="4aff5-113">Si el elemento es un elemento secundario de un control de lista personalizado, es posible que falten las claves que indican que se puede navegar por el elemento secundario mediante las teclas de dirección o de página.</span><span class="sxs-lookup"><span data-stu-id="4aff5-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="4aff5-114">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="4aff5-114">Possible causes</span></span>

-   <span data-ttu-id="4aff5-115">El rol MSAA del elemento o su elemento primario no se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="4aff5-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="4aff5-116">Por ejemplo, si todos los elementos de lista de un control de vista de lista no se exponen a través de MSAA como el sistema de rol \_ \_ ListItem, se produce un error en la comprobación porque no se puede obtener acceso a los elementos de la lista mediante la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="4aff5-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="4aff5-117">El elemento o su elemento primario es un control personalizado que no implementa el tabulador correctamente.</span><span class="sxs-lookup"><span data-stu-id="4aff5-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="4aff5-118">Por ejemplo, la propiedad estado de MSAA nunca se establece en estado de \_ foco del sistema \_ .</span><span class="sxs-lookup"><span data-stu-id="4aff5-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="4aff5-119">Se seleccionó un elemento que actúa como contenedor de otros elementos para la comprobación pero no admite la navegación por el teclado.</span><span class="sxs-lookup"><span data-stu-id="4aff5-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="4aff5-120">Por ejemplo, no se puede tener acceso a una barra de herramientas y a sus elementos secundarios mediante la tecla TAB.</span><span class="sxs-lookup"><span data-stu-id="4aff5-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4aff5-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4aff5-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4aff5-122">Directrices para el diseño de la interfaz de usuario de teclado</span><span class="sxs-lookup"><span data-stu-id="4aff5-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 