---
title: Los elementos DragPattern/DragDropPattern requieren el nombre
description: Los elementos DragPattern/DragDropPattern requieren el nombre
ms.assetid: DEF58FB2-5830-4162-87D0-40DEC1237529
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc60eeca59f4754f9c160696cdfa2556c36a5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704565"
---
# <a name="dragpatterndragdroppattern-elements-requires-name"></a><span data-ttu-id="fa9fd-103">Los elementos DragPattern/DragDropPattern requieren el nombre</span><span class="sxs-lookup"><span data-stu-id="fa9fd-103">DragPattern/DragDropPattern elements requires Name</span></span>

## <a name="text"></a><span data-ttu-id="fa9fd-104">Texto</span><span class="sxs-lookup"><span data-stu-id="fa9fd-104">Text</span></span>

<span data-ttu-id="fa9fd-105">Los elementos que admiten arrastrar y colocar deben tener un conjunto ' name ' válido</span><span class="sxs-lookup"><span data-stu-id="fa9fd-105">Elements that support Drag/Drop should have a valid 'Name' set</span></span>

## <a name="type"></a><span data-ttu-id="fa9fd-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fa9fd-106">Type</span></span>

<span data-ttu-id="fa9fd-107">Error</span><span class="sxs-lookup"><span data-stu-id="fa9fd-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="fa9fd-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa9fd-108">Description</span></span>

<span data-ttu-id="fa9fd-109">El elemento admite [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), pero no tiene un conjunto de nombres válido.</span><span class="sxs-lookup"><span data-stu-id="fa9fd-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid Name set.</span></span>

<span data-ttu-id="fa9fd-110">Este problema causa problemas para las personas que dependen de un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="fa9fd-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="fa9fd-111">El usuario no podrá indicar cuál es el objeto, ya que la lectura de pantalla no leerá un nombre válido para distinguir lo que es este elemento al arrastrar.</span><span class="sxs-lookup"><span data-stu-id="fa9fd-111">The user will not be able to tell what this object is since the screen read will not read out a valid name to distinguish what this element is when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fa9fd-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="fa9fd-112">Possible causes</span></span>

-   <span data-ttu-id="fa9fd-113">El elemento, o su elemento primario, tiene un nombre o una etiqueta asignados incorrectamente.</span><span class="sxs-lookup"><span data-stu-id="fa9fd-113">The element, or its parent, has an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="fa9fd-114">Un desarrollador no es consciente de que los lectores de pantalla leen los nombres y los tipos de control.</span><span class="sxs-lookup"><span data-stu-id="fa9fd-114">A developer is not aware that screen readers read names and control types.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fa9fd-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa9fd-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa9fd-116">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="fa9fd-116">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="fa9fd-117">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="fa9fd-117">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="fa9fd-118">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fa9fd-118">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="fa9fd-119">**IUIAutomationElement::CurrentName**</span><span class="sxs-lookup"><span data-stu-id="fa9fd-119">**IUIAutomationElement::CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




