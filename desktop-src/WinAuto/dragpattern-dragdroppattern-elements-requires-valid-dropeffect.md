---
title: Los elementos DragPattern/DragDropPattern requieren DropEffect válido
description: Los elementos DragPattern/DragDropPattern requieren DropEffect válido
ms.assetid: 508DD4F3-4878-4A9E-859D-06BBDA505708
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33acda19732e2ebd96182023fce9641012b50d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772702"
---
# <a name="dragpatterndragdroppattern-elements-requires-valid-dropeffect"></a><span data-ttu-id="ddd22-103">Los elementos DragPattern/DragDropPattern requieren DropEffect válido</span><span class="sxs-lookup"><span data-stu-id="ddd22-103">DragPattern/DragDropPattern elements requires valid DropEffect</span></span>

## <a name="text"></a><span data-ttu-id="ddd22-104">Texto</span><span class="sxs-lookup"><span data-stu-id="ddd22-104">Text</span></span>

<span data-ttu-id="ddd22-105">Los elementos que admiten arrastrar y colocar deben tener un conjunto ' DropEffect ' válido</span><span class="sxs-lookup"><span data-stu-id="ddd22-105">Elements that support Drag/Drop should have a valid 'DropEffect' set</span></span>

## <a name="type"></a><span data-ttu-id="ddd22-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="ddd22-106">Type</span></span>

<span data-ttu-id="ddd22-107">Error</span><span class="sxs-lookup"><span data-stu-id="ddd22-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="ddd22-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ddd22-108">Description</span></span>

<span data-ttu-id="ddd22-109">El elemento admite [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) o [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), pero no tiene un conjunto de propiedades [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) válido.</span><span class="sxs-lookup"><span data-stu-id="ddd22-109">The element supports either [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) or [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern), but does not have a valid [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property set.</span></span>

<span data-ttu-id="ddd22-110">Este problema causa problemas para las personas que dependen de un lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ddd22-110">This issue causes problems for people who rely on a screen-reader.</span></span> <span data-ttu-id="ddd22-111">El usuario no podrá saber qué efecto tiene este objeto al arrastrar.</span><span class="sxs-lookup"><span data-stu-id="ddd22-111">The user will not be able to tell what effect this object has when dragging.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ddd22-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="ddd22-112">Possible causes</span></span>

-   <span data-ttu-id="ddd22-113">El elemento, o su elemento primario, no ha creado el [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) o [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) un nombre o una etiqueta asignados de forma incorrecta.</span><span class="sxs-lookup"><span data-stu-id="ddd22-113">The element, or its parent, has not created the [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) or [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) an incorrectly assigned name or label.</span></span>
-   <span data-ttu-id="ddd22-114">Un desarrollador no es consciente de que los lectores de pantalla lean DropEffect (s).</span><span class="sxs-lookup"><span data-stu-id="ddd22-114">A developer is not aware that screen readers read DropEffect(s).</span></span>

 

 




