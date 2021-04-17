---
description: De forma predeterminada, el sistema tiene todas las excepciones FP desactivadas.
ms.assetid: efbea036-de9c-4f92-865a-494161da375e
title: Excepciones de punto flotante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a4db92a13a0215bb372db12d30bb11a749a0fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659305"
---
# <a name="floating-point-exceptions"></a><span data-ttu-id="21c33-103">Excepciones de punto flotante</span><span class="sxs-lookup"><span data-stu-id="21c33-103">Floating-Point Exceptions</span></span>

<span data-ttu-id="21c33-104">De forma predeterminada, el sistema tiene todas las excepciones FP desactivadas.</span><span class="sxs-lookup"><span data-stu-id="21c33-104">By default, the system has all FP exceptions turned off.</span></span> <span data-ttu-id="21c33-105">Por lo tanto, los cálculos generan NAN o infinito, en lugar de una excepción.</span><span class="sxs-lookup"><span data-stu-id="21c33-105">Therefore, computations result in NAN or INFINITY, rather than an exception.</span></span> <span data-ttu-id="21c33-106">Antes de poder interceptar las excepciones de punto flotante (FP) mediante el control de excepciones estructurado, debe llamar a la función de biblioteca en tiempo de ejecución de C de [ \_ controlfp \_ s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) para activar todas las excepciones FP posibles.</span><span class="sxs-lookup"><span data-stu-id="21c33-106">Before you can trap floating-point (FP) exceptions using structured exception handling, you must call the [\_controlfp\_s](/previous-versions/visualstudio/visual-studio-2010/c9676k6h(v=vs.100)) C run-time library function to turn on all possible FP exceptions.</span></span> <span data-ttu-id="21c33-107">Para capturar solo determinadas excepciones, use solo las marcas que corresponden a las excepciones que se van a capturar.</span><span class="sxs-lookup"><span data-stu-id="21c33-107">To trap only particular exceptions, use only the flags that correspond to the exceptions to be trapped.</span></span> <span data-ttu-id="21c33-108">Tenga en cuenta que cualquier controlador de errores de FP debe llamar a [ \_ clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) como su primera instrucción FP.</span><span class="sxs-lookup"><span data-stu-id="21c33-108">Note that any handler for FP errors should call [\_clearfp](/cpp/c-runtime-library/reference/clear87-clearfp?view=vs-2019) as its first FP instruction.</span></span> <span data-ttu-id="21c33-109">Esta función borra las excepciones de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="21c33-109">This function clears floating-point exceptions.</span></span>

 

 
