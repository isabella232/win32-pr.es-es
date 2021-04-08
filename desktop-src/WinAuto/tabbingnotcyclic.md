---
title: TabbingNotCyclic
description: TabbingNotCyclic
ms.assetid: F6BCC613-1EA1-438C-AC09-8A282870E021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08fd2e9f6613e07840f432b646c1bdc06a34b5f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077975"
---
# <a name="tabbingnotcyclic"></a><span data-ttu-id="46a6a-103">TabbingNotCyclic</span><span class="sxs-lookup"><span data-stu-id="46a6a-103">TabbingNotCyclic</span></span>

## <a name="text"></a><span data-ttu-id="46a6a-104">Texto</span><span class="sxs-lookup"><span data-stu-id="46a6a-104">Text</span></span>

<span data-ttu-id="46a6a-105">El tabulador de esta aplicación no es cíclico.</span><span class="sxs-lookup"><span data-stu-id="46a6a-105">The tabbing in this application is not cyclic.</span></span> <span data-ttu-id="46a6a-106">Los tiempos de tabulación hacia delante o hacia atrás {0} no vuelven al mismo control.</span><span class="sxs-lookup"><span data-stu-id="46a6a-106">Tabbing forwards or backwards {0} times doesn't come back to the same control.</span></span>

## <a name="type"></a><span data-ttu-id="46a6a-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="46a6a-107">Type</span></span>

<span data-ttu-id="46a6a-108">Error</span><span class="sxs-lookup"><span data-stu-id="46a6a-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="46a6a-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="46a6a-109">Description</span></span>

<span data-ttu-id="46a6a-110">Cuando se usa la navegación de teclado estándar (TAB o Mayús + Tab), no es posible atravesar el árbol de elementos del destino de comprobación hasta que el elemento inicial se convierta en el elemento final (con el mismo número de pulsaciones de teclas) invirtiendo la dirección del recorrido.</span><span class="sxs-lookup"><span data-stu-id="46a6a-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to traverse the element tree of the verification target until the starting element becomes the ending element (using the same number of keystrokes) by reversing the direction of traversal.</span></span> <span data-ttu-id="46a6a-111">Por ejemplo, la tabulación hacia delante (tabulación) x veces desde el elemento a (0) hasta el elemento A (x) y, a continuación, la tabulación hacia atrás (Mayús + Tab) x veces no da lugar a que el elemento A (0) vuelva a obtener el foco.</span><span class="sxs-lookup"><span data-stu-id="46a6a-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times does not result in element A(0) regaining focus.</span></span>

<span data-ttu-id="46a6a-112">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque no hay ninguna manera predecible de volver a un control una vez que se ha visitado.</span><span class="sxs-lookup"><span data-stu-id="46a6a-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there is no predictable way to return to a control after it has been visited.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="46a6a-113">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="46a6a-113">Possible causes</span></span>

-   <span data-ttu-id="46a6a-114">El elemento o su elemento primario es un control personalizado que no implementa el tabulador correctamente.</span><span class="sxs-lookup"><span data-stu-id="46a6a-114">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="46a6a-115">Por ejemplo, la propiedad estado de MSAA no se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="46a6a-115">For example, the MSAA State property isn't set correctly.</span></span>
-   <span data-ttu-id="46a6a-116">Algunas aplicaciones, como el Bloc de notas, muestran este comportamiento de forma inconsistente.</span><span class="sxs-lookup"><span data-stu-id="46a6a-116">Some applications, such as the Notepad, exhibit this behavior innately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="46a6a-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46a6a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46a6a-118">Directrices para el diseño de la interfaz de usuario de teclado</span><span class="sxs-lookup"><span data-stu-id="46a6a-118">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 