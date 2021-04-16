---
description: La aplicación puede usar el búfer de estarcido para componer imágenes 2D o 3D en una escena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composición (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696132"
---
# <a name="compositing-direct3d-9"></a><span data-ttu-id="98e03-103">Composición (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="98e03-103">Compositing (Direct3D 9)</span></span>

<span data-ttu-id="98e03-104">La aplicación puede usar el búfer de estarcido para componer imágenes 2D o 3D en una escena 3D.</span><span class="sxs-lookup"><span data-stu-id="98e03-104">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="98e03-105">Se utiliza una máscara en el búfer de estarcido para tapabar un área de la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="98e03-105">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="98e03-106">La información de 2D almacenada, como texto o mapas de bits, se puede escribir en el área ocluidos.</span><span class="sxs-lookup"><span data-stu-id="98e03-106">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="98e03-107">Como alternativa, la aplicación puede representar primitivos 3D adicionales en la región enmascarada de estarcido de la superficie de destino de representación.</span><span class="sxs-lookup"><span data-stu-id="98e03-107">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="98e03-108">Incluso puede representar una escena completa.</span><span class="sxs-lookup"><span data-stu-id="98e03-108">It can even render an entire scene.</span></span>

<span data-ttu-id="98e03-109">A menudo, los juegos componen varias escenas 3D juntas.</span><span class="sxs-lookup"><span data-stu-id="98e03-109">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="98e03-110">Por ejemplo, los juegos de conducción suelen mostrar un reflejo de la vista trasera.</span><span class="sxs-lookup"><span data-stu-id="98e03-110">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="98e03-111">El reflejo contiene la vista de la escena 3D detrás del controlador.</span><span class="sxs-lookup"><span data-stu-id="98e03-111">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="98e03-112">En esencia, es una segunda escena 3D compuesta con la vista hacia delante del controlador.</span><span class="sxs-lookup"><span data-stu-id="98e03-112">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98e03-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98e03-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98e03-114">Técnicas de búfer de estarcido</span><span class="sxs-lookup"><span data-stu-id="98e03-114">Stencil Buffer Techniques</span></span>](stencil-buffer-techniques.md)
</dt> </dl>

 

 



