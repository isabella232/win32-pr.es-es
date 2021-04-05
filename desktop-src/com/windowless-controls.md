---
title: Controles sin ventana
description: Controles sin ventana
ms.assetid: 1759e5db-423c-44cc-b901-f50046c91956
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762c839067f32a5ac182ccd6b48bfb81c1c68f13
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419170"
---
# <a name="windowless-controls"></a><span data-ttu-id="f5851-103">Controles sin ventana</span><span class="sxs-lookup"><span data-stu-id="f5851-103">Windowless Controls</span></span>

<span data-ttu-id="f5851-104">La especificación de controles ActiveX 96 incluye una definición de controles sin ventanas.</span><span class="sxs-lookup"><span data-stu-id="f5851-104">The ActiveX Controls 96 specification includes a definition for windowless controls.</span></span> <span data-ttu-id="f5851-105">Estos controles no funcionan en su propia ventana y requieren un contenedor para ofrecer una ventana compartida en la que el control puede dibujarse, vea el SDK de ActiveX.</span><span class="sxs-lookup"><span data-stu-id="f5851-105">Such controls do not operate in their own window and require a container to offer a shared window into which the control may draw, see the ActiveX SDK.</span></span> <span data-ttu-id="f5851-106">Los controles sin ventana están diseñados para ser compatibles con los contenedores de control más antiguos creando su propia ventana en esa situación, los contenedores de control sin ventana deben hospedar controles en ventanas de la forma tradicional sin problemas.</span><span class="sxs-lookup"><span data-stu-id="f5851-106">Windowless controls are designed to be compatible with older control containers by creating their own window in that situation, windowless control containers should host windowed controls in the traditional way with no problem.</span></span> <span data-ttu-id="f5851-107">Sin embargo, puede ser útil para que un contenedor distinga los controles que pueden funcionar en un modo sin ventanas, por lo que se define una categoría de componente adecuada.</span><span class="sxs-lookup"><span data-stu-id="f5851-107">It may however be useful for a container to distinguish those controls that can operate in a windowless mode, so an appropriate component category is defined.</span></span>

<span data-ttu-id="f5851-108">CATId-{1D06B600-3AE3-11cf-87B9-00AA006C8166} CATId \_ WindowlessObject</span><span class="sxs-lookup"><span data-stu-id="f5851-108">CATID - {1D06B600-3AE3-11cf-87B9-00AA006C8166} CATID\_WindowlessObject</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5851-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f5851-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5851-110">Categorías del componente</span><span class="sxs-lookup"><span data-stu-id="f5851-110">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

 




