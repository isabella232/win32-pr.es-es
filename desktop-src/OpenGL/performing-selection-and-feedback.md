---
title: Realización de una selección y comentarios
description: Realización de una selección y comentarios
ms.assetid: 908114b3-ac0e-4fd5-ad28-137e6af7ffc7
keywords:
- OpenGL, selección
- OpenGL, comentarios
- OpenGL, representación
- modo de selección OpenGL
- modo de comentarios OpenGL
- modo de representación OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be13ae103d33039c996851582823c23c30316731
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357102"
---
# <a name="performing-selection-and-feedback"></a><span data-ttu-id="51ddf-109">Realización de una selección y comentarios</span><span class="sxs-lookup"><span data-stu-id="51ddf-109">Performing Selection and Feedback</span></span>

<span data-ttu-id="51ddf-110">Selección, comentarios y representación son modos de operación mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="51ddf-110">Selection, feedback, and rendering are mutually exclusive modes of operation.</span></span> <span data-ttu-id="51ddf-111">La representación es el modo predeterminado y normal durante el cual se generan fragmentos mediante la rasterización.</span><span class="sxs-lookup"><span data-stu-id="51ddf-111">Rendering is the normal, default mode during which fragments are produced by rasterization.</span></span>

<span data-ttu-id="51ddf-112">En los modos de selección y de comentarios, no se generan fragmentos; por lo tanto, no se produce ninguna modificación de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="51ddf-112">In selection and feedback modes, no fragments are produced; therefore, no framebuffer modification occurs.</span></span> <span data-ttu-id="51ddf-113">En el modo de selección, puede determinar qué primitivos se van a dibujar en alguna región de una ventana. en el modo de comentarios, la información acerca de los primitivos que se van a rasterizar se revierte a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="51ddf-113">In selection mode, you can determine which primitives will be drawn into some region of a window; in feedback mode, information about primitives that will be rasterized is fed back to the application.</span></span>

<span data-ttu-id="51ddf-114">Puede seleccionar uno de estos tres modos con [**glRenderMode**](glrendermode.md).</span><span class="sxs-lookup"><span data-stu-id="51ddf-114">You select among these three modes with [**glRenderMode**](glrendermode.md).</span></span>

-   [<span data-ttu-id="51ddf-115">Selección</span><span class="sxs-lookup"><span data-stu-id="51ddf-115">Selection</span></span>](selection.md)
-   [<span data-ttu-id="51ddf-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="51ddf-116">Feedback</span></span>](feedback.md)
-   [<span data-ttu-id="51ddf-117">Selección y referencia de comentarios</span><span class="sxs-lookup"><span data-stu-id="51ddf-117">Selection and Feedback Reference</span></span>](selection-and-feedback-reference.md)

 

 




