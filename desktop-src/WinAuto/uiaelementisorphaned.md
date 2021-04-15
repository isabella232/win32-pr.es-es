---
title: UiaElementIsOrphaned
description: UiaElementIsOrphaned
ms.assetid: F85F08E7-5A9C-4F08-B680-8B251D51168A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ec0861a586fd5275a674d9ef8ba6a0e72364b2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714187"
---
# <a name="uiaelementisorphaned"></a><span data-ttu-id="08e25-103">UiaElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="08e25-103">UiaElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="08e25-104">Texto</span><span class="sxs-lookup"><span data-stu-id="08e25-104">Text</span></span>

<span data-ttu-id="08e25-105">El elemento es un AutomationElement huérfano en el árbol</span><span class="sxs-lookup"><span data-stu-id="08e25-105">Element is an orphaned AutomationElement in the tree</span></span>

## <a name="type"></a><span data-ttu-id="08e25-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="08e25-106">Type</span></span>

<span data-ttu-id="08e25-107">Error</span><span class="sxs-lookup"><span data-stu-id="08e25-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="08e25-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="08e25-108">Description</span></span>

<span data-ttu-id="08e25-109">La dirección de la interfaz [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del objeto obtenida para las coordenadas dadas es una referencia a un elemento huérfano en el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="08e25-109">The address of the object's [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="08e25-110">Este problema es un problema para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se tratarán como invisibles y no se anunciarán al usuario.</span><span class="sxs-lookup"><span data-stu-id="08e25-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="08e25-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="08e25-111">Possible causes</span></span>

-   <span data-ttu-id="08e25-112">Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="08e25-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="08e25-113">Implementación de automatización de la interfaz de usuario incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="08e25-113">An incorrect or invalid UI Automation implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08e25-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08e25-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08e25-115">**IUIAutomationElement.ElementFromPoint**</span><span class="sxs-lookup"><span data-stu-id="08e25-115">**IUIAutomationElement.ElementFromPoint**</span></span>](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomation-elementfrompoint)
</dt> </dl>

 

 




