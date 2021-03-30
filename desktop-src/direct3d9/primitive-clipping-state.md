---
description: Los primitivos que se encuentran parcialmente dentro (o completamente externos) el frustum de vista se pueden recortar para que solo se represente la parte visible de la primitiva.
ms.assetid: 096683a4-2d8f-49d3-b1a0-832150907f11
title: Estado de recorte primitivo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e5a305118d8db5c71e0e3cfa97132052777be68
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423152"
---
# <a name="primitive-clipping-state-direct3d-9"></a><span data-ttu-id="8909b-103">Estado de recorte primitivo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8909b-103">Primitive Clipping State (Direct3D 9)</span></span>

<span data-ttu-id="8909b-104">Los primitivos que se encuentran parcialmente dentro (o completamente externos) el [frustum de vista](viewports-and-clipping.md) se pueden recortar para que solo se represente la parte visible de la primitiva.</span><span class="sxs-lookup"><span data-stu-id="8909b-104">Primitives that lie partially inside (or completely outside) the [view frustum](viewports-and-clipping.md) can be clipped so that only the visible portion of the primitive will be rendered.</span></span> <span data-ttu-id="8909b-105">El recorte reduce la cantidad de trabajo que se realiza solo a las primitivas o partes de un primitivo que serán visibles.</span><span class="sxs-lookup"><span data-stu-id="8909b-105">Clipping reduces the amount of work that is done to only those primitives or portions of a primitive that will be visible.</span></span>

<span data-ttu-id="8909b-106">Para usar la canalización para el recorte, establezca el \_ Estado de representación de recorte de D3DRS en **true** (valor predeterminado) para habilitar el recorte o en **false** para deshabilitar el recorte de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8909b-106">To use the pipeline for clipping, set the D3DRS\_CLIPPING render state to **TRUE** (the default value) to enable clipping, or to **FALSE** to disable Direct3D clipping.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8909b-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8909b-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8909b-108">Estados de representación</span><span class="sxs-lookup"><span data-stu-id="8909b-108">Render States</span></span>](render-states.md)
</dt> </dl>

 

 



