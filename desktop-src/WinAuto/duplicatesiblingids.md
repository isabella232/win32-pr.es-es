---
title: DuplicateSiblingIDs
description: DuplicateSiblingIDs
ms.assetid: 942385A4-BD14-4046-9ABC-110B32D96BB6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27ba2ccca45234bb49fc782c5522b4e446d77a2c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704809"
---
# <a name="duplicatesiblingids"></a><span data-ttu-id="779a1-103">DuplicateSiblingIDs</span><span class="sxs-lookup"><span data-stu-id="779a1-103">DuplicateSiblingIDs</span></span>

## <a name="text"></a><span data-ttu-id="779a1-104">Texto</span><span class="sxs-lookup"><span data-stu-id="779a1-104">Text</span></span>

<span data-ttu-id="779a1-105">El ID. de automatización duplicado \\ "" producirá {0} \\ ambigüedad entre los elementos.</span><span class="sxs-lookup"><span data-stu-id="779a1-105">Duplicate Automation ID \\"{0}\\" will cause ambiguity between elements.</span></span>

## <a name="type"></a><span data-ttu-id="779a1-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="779a1-106">Type</span></span>

<span data-ttu-id="779a1-107">Error</span><span class="sxs-lookup"><span data-stu-id="779a1-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="779a1-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="779a1-108">Description</span></span>

<span data-ttu-id="779a1-109">Un elemento tiene el mismo ID. de automatización que otro elemento.</span><span class="sxs-lookup"><span data-stu-id="779a1-109">An element has the same Automation ID as another element.</span></span>

<span data-ttu-id="779a1-110">Este problema puede producir problemas de automatización que impiden que el código de prueba haga referencia al elemento correcto.</span><span class="sxs-lookup"><span data-stu-id="779a1-110">This issue can cause automation problems that prevent test code from referencing the correct element.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="779a1-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="779a1-111">Possible causes</span></span>

-   <span data-ttu-id="779a1-112">Los elementos relacionados tienen el mismo identificador de automatización.</span><span class="sxs-lookup"><span data-stu-id="779a1-112">Sibling elements have the same Automation ID.</span></span>
-   <span data-ttu-id="779a1-113">Implementación incorrecta de la propiedad AutomationId AutomationId.</span><span class="sxs-lookup"><span data-stu-id="779a1-113">Incorrect implementation of the UIA AutomationId property.</span></span>

## <a name="related-topics"></a><span data-ttu-id="779a1-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="779a1-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="779a1-115">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="779a1-115">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="779a1-116">**IUIAutomationElement.CurrentAutomationId**</span><span class="sxs-lookup"><span data-stu-id="779a1-116">**IUIAutomationElement.CurrentAutomationId**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentautomationid)
</dt> </dl>

 

 




