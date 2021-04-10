---
title: TabbingNotSymmetric
description: TabbingNotSymmetric
ms.assetid: 1E14ED9F-27C1-4054-B0A6-702167222196
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc19efbbbce0f299044726466dd8f87b133fc26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149391"
---
# <a name="tabbingnotsymmetric"></a><span data-ttu-id="e0813-103">TabbingNotSymmetric</span><span class="sxs-lookup"><span data-stu-id="e0813-103">TabbingNotSymmetric</span></span>

## <a name="text"></a><span data-ttu-id="e0813-104">Texto</span><span class="sxs-lookup"><span data-stu-id="e0813-104">Text</span></span>

<span data-ttu-id="e0813-105">Al tabular hacia atrás y hacia delante no se produce el mismo elemento.</span><span class="sxs-lookup"><span data-stu-id="e0813-105">Tabbing backwards and forwards does not yield the same element.</span></span> <span data-ttu-id="e0813-106">Esperado {0} pero recibido {1}</span><span class="sxs-lookup"><span data-stu-id="e0813-106">Expected {0} but received {1}</span></span>

## <a name="type"></a><span data-ttu-id="e0813-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="e0813-107">Type</span></span>

<span data-ttu-id="e0813-108">Error</span><span class="sxs-lookup"><span data-stu-id="e0813-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="e0813-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0813-109">Description</span></span>

<span data-ttu-id="e0813-110">Cuando se usa la navegación de teclado estándar (TAB o Mayús + Tab), no es posible repetir la ruta de acceso del recorrido a través del árbol de elementos del destino de la comprobación si se invierte la dirección de recorrido.</span><span class="sxs-lookup"><span data-stu-id="e0813-110">When using standard keyboard navigation (Tab or Shift+Tab), it isn't possible to repeat the path of traversal through the element tree of the verification target if the direction of traversal is reversed.</span></span> <span data-ttu-id="e0813-111">Por ejemplo, la tabulación hacia delante (tabulación) x veces desde el elemento a (0) hasta el elemento a (x) y, a continuación, la tabulación hacia atrás (Mayús + Tab) x veces hace que el elemento A (0) vuelva a obtener el foco a través de un conjunto diferente de elementos intermedios.</span><span class="sxs-lookup"><span data-stu-id="e0813-111">For example, tabbing forward (Tab) x times from element A(0) to element A(x) and then tabbing backward (Shift+Tab) x times results in element A(0) regaining focus through a different set of intermediate elements.</span></span>

<span data-ttu-id="e0813-112">Este problema causa problemas para las personas que confían en un lector de pantalla y un teclado para la navegación porque los elementos de recorrido aparecen errático e imprevisibles.</span><span class="sxs-lookup"><span data-stu-id="e0813-112">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because traversing elements appears erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="e0813-113">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="e0813-113">Possible causes</span></span>

-   <span data-ttu-id="e0813-114">Varios elementos o sus elementos primarios son controles personalizados que no implementan el tabulador correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0813-114">Multiple elements or their parents are custom controls that don't implement tabbing correctly.</span></span> <span data-ttu-id="e0813-115">Por ejemplo, la propiedad estado de MSAA no se ha establecido correctamente.</span><span class="sxs-lookup"><span data-stu-id="e0813-115">For example, the MSAA State property is not set correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e0813-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0813-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0813-117">Directrices para el diseño de la interfaz de usuario de teclado</span><span class="sxs-lookup"><span data-stu-id="e0813-117">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 