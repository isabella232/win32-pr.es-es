---
title: Proceso cruzado y uso compartido de dispositivos entre recursos en mosaico
description: Los grupos de mosaicos se pueden compartir con otros procesos, al igual que los recursos tradicionales.
ms.assetid: CADE009E-A71E-4ACA-A549-EFCE81F8EAD1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f69c88ec7e56a0ad3f67ca7d219352261af9d60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268381"
---
# <a name="tiled-resource-cross-process-and-device-sharing"></a><span data-ttu-id="b2f2b-103">Proceso cruzado y uso compartido de dispositivos entre recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="b2f2b-103">Tiled resource cross process and device sharing</span></span>

<span data-ttu-id="b2f2b-104">Los grupos de mosaicos se pueden compartir con otros procesos, al igual que los recursos tradicionales.</span><span class="sxs-lookup"><span data-stu-id="b2f2b-104">Tile pools can be shared with other processes just like traditional resources.</span></span> <span data-ttu-id="b2f2b-105">Los recursos en mosaico que hacen referencia a los grupos de mosaicos no se pueden compartir entre dispositivos y procesos.</span><span class="sxs-lookup"><span data-stu-id="b2f2b-105">Tiled resources that reference tile pools can't be shared across devices and processes.</span></span> <span data-ttu-id="b2f2b-106">Sin embargo, los procesos independientes pueden crear sus propios recursos en mosaico que se asignan a los grupos de mosaicos que se comparten entre esos recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="b2f2b-106">But separate processes can create their own tiled resources that map to tile pools that are shared between those tiled resources.</span></span>

<span data-ttu-id="b2f2b-107">No se puede cambiar el tamaño de los grupos de mosaicos compartidos.</span><span class="sxs-lookup"><span data-stu-id="b2f2b-107">Shared tile pools can't be resized.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b2f2b-108">En esta sección</span><span class="sxs-lookup"><span data-stu-id="b2f2b-108">In this section</span></span>



| <span data-ttu-id="b2f2b-109">Tema</span><span class="sxs-lookup"><span data-stu-id="b2f2b-109">Topic</span></span>                                                                                                                   | <span data-ttu-id="b2f2b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b2f2b-110">Description</span></span>                                                                     |
|-------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="b2f2b-111">Formatos de estarcido no compatibles con recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="b2f2b-111">Stencil formats not supported with tiled resources</span></span>](stencil-formats-not-supported-with-tiled-resources.md)<br/> | <span data-ttu-id="b2f2b-112">Los formatos que contienen la galería de símbolos no se admiten con recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="b2f2b-112">Formats that contain stencil aren't supported with tiled resources.</span></span> <br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b2f2b-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b2f2b-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2f2b-114">Crear recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="b2f2b-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 





