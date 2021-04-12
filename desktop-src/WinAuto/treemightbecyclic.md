---
title: TreeMightBeCyclic
description: TreeMightBeCyclic
ms.assetid: 9A997949-A1A2-448C-9739-BE176621F1B4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9647f4429ba17226f342a8dceb3c51b033d08b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359022"
---
# <a name="treemightbecyclic"></a><span data-ttu-id="ba0df-103">TreeMightBeCyclic</span><span class="sxs-lookup"><span data-stu-id="ba0df-103">TreeMightBeCyclic</span></span>

## <a name="text"></a><span data-ttu-id="ba0df-104">Texto</span><span class="sxs-lookup"><span data-stu-id="ba0df-104">Text</span></span>

<span data-ttu-id="ba0df-105">El árbol tiene {0} niveles de profundidad.</span><span class="sxs-lookup"><span data-stu-id="ba0df-105">Tree is {0} levels deep.</span></span> <span data-ttu-id="ba0df-106">Esto podría indicar que el árbol de accesibilidad es cíclico y, por tanto, parecería infinito.</span><span class="sxs-lookup"><span data-stu-id="ba0df-106">This might indicate that the accessibility tree is cyclic, and thus it would appear to be infinite.</span></span>

## <a name="type"></a><span data-ttu-id="ba0df-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="ba0df-107">Type</span></span>

<span data-ttu-id="ba0df-108">Error</span><span class="sxs-lookup"><span data-stu-id="ba0df-108">Error</span></span>

## <a name="description"></a><span data-ttu-id="ba0df-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba0df-109">Description</span></span>

<span data-ttu-id="ba0df-110">El árbol de elementos es cíclico y la profundidad del árbol puede ser infinita.</span><span class="sxs-lookup"><span data-stu-id="ba0df-110">The element tree is cyclic and the tree depth might be infinite.</span></span>

<span data-ttu-id="ba0df-111">Este problema causa problemas para las personas que usan un lector de pantalla y un teclado para la navegación porque no habrá ningún límite aparente en el recorrido de los elementos de la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="ba0df-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because there will be no apparent limit to the traversal of elements in the target application.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="ba0df-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="ba0df-112">Possible causes</span></span>

<span data-ttu-id="ba0df-113">Varios elementos, o sus elementos primarios, son controles personalizados que no implementan el tabulador correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba0df-113">Multiple elements, or their parents, are custom controls that do not implement tabbing correctly.</span></span> <span data-ttu-id="ba0df-114">Por ejemplo, la propiedad [Estado](state-property.md) de MSAA no se actualiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="ba0df-114">For example, the MSAA [State](state-property.md) property is not updated correctly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba0df-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ba0df-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba0df-116">Directrices para el diseño de la interfaz de usuario de teclado</span><span class="sxs-lookup"><span data-stu-id="ba0df-116">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> <dt>

[<span data-ttu-id="ba0df-117">Directrices de interacción de la experiencia del usuario de Windows: teclado</span><span class="sxs-lookup"><span data-stu-id="ba0df-117">Windows User Experience Interaction Guidelines - Keyboard</span></span>](https://msdn.microsoft.com/library/bb545460.aspx#guidelines)
</dt> </dl>

 

 