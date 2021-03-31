---
title: FirstChildLastChildMismatch
description: FirstChildLastChildMismatch
ms.assetid: 98726C1A-DC43-4FC7-8ECA-628F63D0AFE3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37fedb7e23ce2ac2a7f9c51c9db9e06e59ead515
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418887"
---
# <a name="firstchildlastchildmismatch"></a><span data-ttu-id="d615e-103">FirstChildLastChildMismatch</span><span class="sxs-lookup"><span data-stu-id="d615e-103">FirstChildLastChildMismatch</span></span>

## <a name="text"></a><span data-ttu-id="d615e-104">Texto</span><span class="sxs-lookup"><span data-stu-id="d615e-104">Text</span></span>

<span data-ttu-id="d615e-105">Al navegar llamando {0} desde el nodo probado y, a continuación, llamando repetidamente a {1} , finalizamos en el siguiente elemento secundario: {2} .</span><span class="sxs-lookup"><span data-stu-id="d615e-105">When navigating by calling {0} from the tested node, and then repeatedly calling {1}, we finished at the following child: {2}.</span></span> <span data-ttu-id="d615e-106">Esto no coincidía con el resultado de llamar a {3} en el nodo probado, que produjo: {4} .</span><span class="sxs-lookup"><span data-stu-id="d615e-106">This did not match the result of calling {3} on the tested node, which yielded: {4}.</span></span> <span data-ttu-id="d615e-107">En su lugar, el elemento secundario debe notificar como elemento primario el nodo de prueba.</span><span class="sxs-lookup"><span data-stu-id="d615e-107">Instead, the child should report as its parent the testing node.</span></span>

## <a name="type"></a><span data-ttu-id="d615e-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="d615e-108">Type</span></span>

<span data-ttu-id="d615e-109">Error</span><span class="sxs-lookup"><span data-stu-id="d615e-109">Error</span></span>

## <a name="description"></a><span data-ttu-id="d615e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="d615e-110">Description</span></span>

<span data-ttu-id="d615e-111">Hay un problema al desplazarse entre los elementos secundarios de un elemento.</span><span class="sxs-lookup"><span data-stu-id="d615e-111">There is a problem when navigating between element’s children.</span></span> <span data-ttu-id="d615e-112">1.</span><span class="sxs-lookup"><span data-stu-id="d615e-112">1.</span></span> <span data-ttu-id="d615e-113">Implementación de automatización de la interfaz de usuario incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="d615e-113">An incorrect or invalid UI Automation implementation.</span></span>

<span data-ttu-id="d615e-114">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="d615e-114">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="d615e-115">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="d615e-115">Possible causes</span></span>

<span data-ttu-id="d615e-116">Implementación de automatización de la interfaz de usuario incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="d615e-116">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d615e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d615e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d615e-118">**IUIAutomationElement::GetCachedParent**</span><span class="sxs-lookup"><span data-stu-id="d615e-118">**IUIAutomationElement::GetCachedParent**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcachedparent)
</dt> <dt>

[<span data-ttu-id="d615e-119">**IUIAutomationTreeWalker**</span><span class="sxs-lookup"><span data-stu-id="d615e-119">**IUIAutomationTreeWalker**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtreewalker)
</dt> </dl>

 

 




