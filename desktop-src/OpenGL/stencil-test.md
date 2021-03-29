---
title: Prueba de estarcido
description: La prueba de la galería de símbolos descarta condicionalmente un fragmento según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia.
ms.assetid: 967be1e5-a9a2-45cc-aae7-c33cc257ade1
keywords:
- Canalización de procesamiento de OpenGL, prueba de estarcido
- Galería de símbolos de prueba OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e285c3dfb1591c5ed3d95969024d2350a7517a79
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779465"
---
# <a name="stencil-test"></a><span data-ttu-id="6e569-105">Prueba de estarcido</span><span class="sxs-lookup"><span data-stu-id="6e569-105">Stencil Test</span></span>

<span data-ttu-id="6e569-106">La prueba de la galería de símbolos descarta condicionalmente un fragmento según el resultado de una comparación entre el valor del búfer de estarcido y un valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="6e569-106">The stencil test conditionally discards a fragment based on the outcome of a comparison between the value in the stencil buffer and a reference value.</span></span> <span data-ttu-id="6e569-107">La función [**glStencilFunc**](glstencilfunc.md) especifica la función de comparación y el valor de referencia.</span><span class="sxs-lookup"><span data-stu-id="6e569-107">The [**glStencilFunc**](glstencilfunc.md) function specifies the comparison function and the reference value.</span></span> <span data-ttu-id="6e569-108">Si el fragmento supera o no la prueba de estarcido, el valor del búfer de estarcido se modifica según las instrucciones especificadas con [**glStencilOp**](glstencilop.md).</span><span class="sxs-lookup"><span data-stu-id="6e569-108">Whether the fragment passes or fails the stencil test, the value in the stencil buffer is modified according to the instructions specified with [**glStencilOp**](glstencilop.md).</span></span>

 

 




