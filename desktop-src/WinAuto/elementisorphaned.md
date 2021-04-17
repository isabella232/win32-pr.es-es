---
title: ElementIsOrphaned
description: ElementIsOrphaned
ms.assetid: EB603052-2B0F-418C-947E-827453440F46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1878556af6f1954224bc9b5eadfd4d77e6e3419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704805"
---
# <a name="elementisorphaned"></a><span data-ttu-id="9802c-103">ElementIsOrphaned</span><span class="sxs-lookup"><span data-stu-id="9802c-103">ElementIsOrphaned</span></span>

## <a name="text"></a><span data-ttu-id="9802c-104">Texto</span><span class="sxs-lookup"><span data-stu-id="9802c-104">Text</span></span>

<span data-ttu-id="9802c-105">El elemento es un IAccessible huérfano en el árbol</span><span class="sxs-lookup"><span data-stu-id="9802c-105">Element is an orphaned IAccessible in the tree</span></span>

## <a name="type"></a><span data-ttu-id="9802c-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="9802c-106">Type</span></span>

<span data-ttu-id="9802c-107">Error</span><span class="sxs-lookup"><span data-stu-id="9802c-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="9802c-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="9802c-108">Description</span></span>

<span data-ttu-id="9802c-109">La dirección de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto obtenida para las coordenadas especificadas es una referencia a un elemento huérfano en el árbol de elementos.</span><span class="sxs-lookup"><span data-stu-id="9802c-109">The address of the object's [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface obtained for the given coordinates is a reference to an orphaned element in the element tree.</span></span>

<span data-ttu-id="9802c-110">Este problema es un problema para las personas que confían en un lector de pantalla y un teclado para la navegación, ya que los elementos se tratarán como invisibles y no se anunciarán al usuario.</span><span class="sxs-lookup"><span data-stu-id="9802c-110">This issue is a problem for people who rely on a screen-reader and keyboard for navigation because elements will be treated as invisible and will not be announced to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="9802c-111">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="9802c-111">Possible causes</span></span>

-   <span data-ttu-id="9802c-112">Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="9802c-112">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>
-   <span data-ttu-id="9802c-113">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="9802c-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9802c-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9802c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9802c-115">Navegación a través de la prueba de posicionamiento y la ubicación de la pantalla</span><span class="sxs-lookup"><span data-stu-id="9802c-115">Navigation Through Hit Testing and Screen Location</span></span>](navigation-through-hit-testing-and-screen-location.md)
</dt> <dt>

[<span data-ttu-id="9802c-116">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="9802c-116">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
</dt> </dl>

 

 




