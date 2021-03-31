---
title: TabbedToUnknownElement
description: TabbedToUnknownElement
ms.assetid: B0447B19-E281-4D30-8ED8-FC0EE13571C8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 612476d81779c882eeca807a9c3b82c41594f218
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418549"
---
# <a name="tabbedtounknownelement"></a><span data-ttu-id="1c4cf-103">TabbedToUnknownElement</span><span class="sxs-lookup"><span data-stu-id="1c4cf-103">TabbedToUnknownElement</span></span>

## <a name="text"></a><span data-ttu-id="1c4cf-104">Texto</span><span class="sxs-lookup"><span data-stu-id="1c4cf-104">Text</span></span>

<span data-ttu-id="1c4cf-105">La tabulación ha pasado a un elemento fuera del HWND de destino.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-105">Tabbing has gone to an element outside the target hwnd.</span></span>

## <a name="type"></a><span data-ttu-id="1c4cf-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="1c4cf-106">Type</span></span>

<span data-ttu-id="1c4cf-107">Error</span><span class="sxs-lookup"><span data-stu-id="1c4cf-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="1c4cf-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c4cf-108">Description</span></span>

<span data-ttu-id="1c4cf-109">El uso de la navegación con el teclado estándar (TAB o Mayús + Tab) hace que el foco se desplace fuera del HWND del destino de la comprobación.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-109">Using standard keyboard navigation (Tab or Shift+Tab) causes focus to shift outside the HWND of the verification target.</span></span>

<span data-ttu-id="1c4cf-110">AccChecker sube el árbol de elementos hasta el HWND de nivel superior para el destino de comprobación elegido antes de ejecutar cualquier tarea de comprobación.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-110">AccChecker moves up the element tree to the top-level HWND for the chosen verification target before running any verification tasks.</span></span> <span data-ttu-id="1c4cf-111">Esto reduce el número de errores falsos generados si un HWND elegido para la comprobación forma parte de un área cliente más compleja.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-111">This reduces the number of spurious errors generated if an HWND chosen for verification is part of a more complex client area.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="1c4cf-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="1c4cf-112">Possible causes</span></span>

-   <span data-ttu-id="1c4cf-113">El destino de la comprobación no requiere una implementación de tabulación para proporcionar toda la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-113">The verification target doesn't require a tabbing implementation to provide full functionality.</span></span>
-   <span data-ttu-id="1c4cf-114">Interacción del usuario durante la comprobación, por ejemplo, al mover el foco a un HWND no objetivo, se interfiere con el proceso de comprobación.</span><span class="sxs-lookup"><span data-stu-id="1c4cf-114">User interaction during verification, such as moving focus to a non-target HWND, interfered with the verification process.</span></span>

 

 




