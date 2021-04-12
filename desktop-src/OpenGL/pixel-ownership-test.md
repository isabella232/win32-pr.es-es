---
title: Prueba de propiedad de píxeles
description: La prueba de propiedad de píxeles determina si el contexto de OpenGL actual posee el píxel en el fotogramas correspondiente a un fragmento determinado.
ms.assetid: aa9428a6-cc05-4df4-ba31-444f999006a8
keywords:
- Canalización de procesamiento de OpenGL, prueba de propiedad de píxeles
- prueba de propiedad de píxeles OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ad5ae57dbbff9f3551ecc222cd0a628193c97f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357251"
---
# <a name="pixel-ownership-test"></a><span data-ttu-id="838d7-105">Prueba de propiedad de píxeles</span><span class="sxs-lookup"><span data-stu-id="838d7-105">Pixel Ownership Test</span></span>

<span data-ttu-id="838d7-106">La prueba de propiedad de píxeles determina si el contexto de OpenGL actual posee el píxel en el fotogramas correspondiente a un fragmento determinado.</span><span class="sxs-lookup"><span data-stu-id="838d7-106">The pixel ownership test determines whether the current OpenGL context owns the pixel in the framebuffer corresponding to a particular fragment.</span></span> <span data-ttu-id="838d7-107">Si es así, el fragmento continúa con la siguiente prueba.</span><span class="sxs-lookup"><span data-stu-id="838d7-107">If so, the fragment proceeds to the next test.</span></span> <span data-ttu-id="838d7-108">De lo contrario, el sistema de ventanas determina si el fragmento se descarta o si se realizarán más operaciones de fragmento con ese fragmento.</span><span class="sxs-lookup"><span data-stu-id="838d7-108">If not, the window system determines whether the fragment is discarded or whether any further fragment operations will be performed with that fragment.</span></span> <span data-ttu-id="838d7-109">Con esta prueba, el sistema de ventanas controla el comportamiento cuando, por ejemplo, se oculta una ventana de OpenGL.</span><span class="sxs-lookup"><span data-stu-id="838d7-109">With this test, the window system controls behavior when, for example, an OpenGL window is obscured.</span></span>

 

 




