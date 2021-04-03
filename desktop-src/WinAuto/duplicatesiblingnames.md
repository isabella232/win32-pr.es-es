---
title: DuplicateSiblingNames
description: DuplicateSiblingNames
ms.assetid: 4E9FFD16-EAC0-4778-8DEB-D179E2197411
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aed5a7caeadc34519988fe8a4a1f12ec4e05ce13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780047"
---
# <a name="duplicatesiblingnames"></a><span data-ttu-id="5e43c-103">DuplicateSiblingNames</span><span class="sxs-lookup"><span data-stu-id="5e43c-103">DuplicateSiblingNames</span></span>

## <a name="text"></a><span data-ttu-id="5e43c-104">Texto</span><span class="sxs-lookup"><span data-stu-id="5e43c-104">Text</span></span>

<span data-ttu-id="5e43c-105">El nombre del mismo nivel y el rol \\ "" duplicados {0} \\ provocarán ambigüedades entre los elementos.</span><span class="sxs-lookup"><span data-stu-id="5e43c-105">Duplicate sibling Name+Role \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="5e43c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="5e43c-106">Type</span></span>

<span data-ttu-id="5e43c-107">Error</span><span class="sxs-lookup"><span data-stu-id="5e43c-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="5e43c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="5e43c-108">Description</span></span>

<span data-ttu-id="5e43c-109">Un elemento tiene el mismo nombre y role/ControlType como otro elemento.</span><span class="sxs-lookup"><span data-stu-id="5e43c-109">An element has the same Name and Role/ControlType as another element.</span></span>

<span data-ttu-id="5e43c-110">Este problema puede causar confusión, ya que los lectores de pantalla leerán el mismo texto para todos los elementos con el mismo nombre y rol/ControlType.</span><span class="sxs-lookup"><span data-stu-id="5e43c-110">This issue can cause confusion because screen readers will read the same text for all the elements with the same Name and Role/ControlType.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="5e43c-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="5e43c-111">Possible causes</span></span>

-   <span data-ttu-id="5e43c-112">El nombre del elemento contiene el texto role/ControlType.</span><span class="sxs-lookup"><span data-stu-id="5e43c-112">Element’s name contain Role/ControlType text.</span></span>
-   <span data-ttu-id="5e43c-113">El nombre del elemento o el nombre de su elemento primario no está establecido o no se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="5e43c-113">Element’s name or the name of its parent is not set or is set incorrectly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e43c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e43c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e43c-115">**IAccessible:: get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="5e43c-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="5e43c-116">Propiedad Name</span><span class="sxs-lookup"><span data-stu-id="5e43c-116">Name Property</span></span>](name-property.md)
</dt> <dt>

[<span data-ttu-id="5e43c-117">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5e43c-117">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="5e43c-118">**IUIAutomationElement.CurrentName**</span><span class="sxs-lookup"><span data-stu-id="5e43c-118">**IUIAutomationElement.CurrentName**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname)
</dt> </dl>

 

 




