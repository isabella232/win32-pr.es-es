---
title: Combinación
description: La mezcla combina los valores R, G, B y A de un fragmento con los almacenados en el fotogramas en la ubicación correspondiente.
ms.assetid: 02a78ce3-bb0a-4e9c-a2b1-6da8e95bcee5
keywords:
- Canalización de procesamiento de OpenGL, fusión
- combinación de OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0fe7cd2893700d8015148fcc5c25707d19676c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357088"
---
# <a name="blending"></a><span data-ttu-id="a76e4-105">Combinación</span><span class="sxs-lookup"><span data-stu-id="a76e4-105">Blending</span></span>

<span data-ttu-id="a76e4-106">La mezcla combina los valores R, G, B y A de un fragmento con los almacenados en el fotogramas en la ubicación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="a76e4-106">Blending combines a fragment's R, G, B, and A values with those stored in the framebuffer at the corresponding location.</span></span> <span data-ttu-id="a76e4-107">La combinación, que solo se realiza en el modo RGBA, depende del valor alfa del fragmento y del píxel almacenado actualmente correspondiente; también puede depender de los valores RGB.</span><span class="sxs-lookup"><span data-stu-id="a76e4-107">The blending, which is performed only in RGBA mode, depends on the alpha value of the fragment and that of the corresponding currently stored pixel; it may also depend on the RGB values.</span></span> <span data-ttu-id="a76e4-108">Puede controlar la fusión con [**glBlendFunc**](glblendfunc.md), con el que se indican los factores de fusión de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="a76e4-108">You control blending with [**glBlendFunc**](glblendfunc.md), with which you indicate the source and destination blending factors.</span></span>

 

 




