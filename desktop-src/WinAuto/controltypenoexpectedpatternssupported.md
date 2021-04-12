---
title: ControlTypeNoExpectedPatternsSupported
description: ControlTypeNoExpectedPatternsSupported
ms.assetid: 2C9CEFEA-8207-47A7-B100-A56CFBFB792D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c40f9f094589b312a033d6bdadf3fbf3b5020b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357163"
---
# <a name="controltypenoexpectedpatternssupported"></a><span data-ttu-id="fd069-103">ControlTypeNoExpectedPatternsSupported</span><span class="sxs-lookup"><span data-stu-id="fd069-103">ControlTypeNoExpectedPatternsSupported</span></span>

## <a name="text"></a><span data-ttu-id="fd069-104">Texto</span><span class="sxs-lookup"><span data-stu-id="fd069-104">Text</span></span>

<span data-ttu-id="fd069-105">El elemento con un ControlType de {0} debe admitir al menos uno de estos patrones: {1} pero este elemento no</span><span class="sxs-lookup"><span data-stu-id="fd069-105">Element with a ControlType of {0} should support at least one of these patterns:{1} but this element does not</span></span>

## <a name="type"></a><span data-ttu-id="fd069-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd069-106">Type</span></span>

<span data-ttu-id="fd069-107">Error</span><span class="sxs-lookup"><span data-stu-id="fd069-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="fd069-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd069-108">Description</span></span>

<span data-ttu-id="fd069-109">La compatibilidad de automatización de la interfaz de usuario del elemento no cumple con la especificación de automatización de la interfaz de usuario porque el elemento debe admitir al menos una de las listas de patrones de control proporcionadas, pero no.</span><span class="sxs-lookup"><span data-stu-id="fd069-109">The element's UI Automation support does not comply with the UI Automation specification because the element should support at least one of the provided list of control patterns, but does not.</span></span> <span data-ttu-id="fd069-110">Como resultado, es posible que este elemento no esté expuesto correctamente a las tecnologías de asistencia, lo que podría tener un impacto serio en la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="fd069-110">As a result, this element might not be properly exposed to assistive technologies, which could have a serious impact on user experience.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="fd069-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="fd069-111">Possible causes</span></span>

-   <span data-ttu-id="fd069-112">Implementación de automatización de la interfaz de usuario incompleta.</span><span class="sxs-lookup"><span data-stu-id="fd069-112">Incomplete UI Automation implementation.</span></span>
-   <span data-ttu-id="fd069-113">La propiedad ControlType no se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="fd069-113">The ControlType property is not set correctly.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd069-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd069-114">Remarks</span></span>

<span data-ttu-id="fd069-115">AccChecker registra este mensaje de error para una barra de progreso indeterminada.</span><span class="sxs-lookup"><span data-stu-id="fd069-115">AccChecker logs this error message for an indeterminate progress bar.</span></span> <span data-ttu-id="fd069-116">Puede omitir este mensaje o agregarlo a la lista de supresiones.</span><span class="sxs-lookup"><span data-stu-id="fd069-116">You can ignore this message and/or add it to the suppressions list.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd069-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd069-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd069-118">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="fd069-118">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)
</dt> <dt>

[<span data-ttu-id="fd069-119">Información general sobre tipos de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="fd069-119">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="fd069-120">Información general acerca de los patrones de control de UI Automation</span><span class="sxs-lookup"><span data-stu-id="fd069-120">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> </dl>

 

 




