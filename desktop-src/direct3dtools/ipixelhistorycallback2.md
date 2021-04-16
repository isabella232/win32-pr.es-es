---
description: Devolución de llamada para devolver intersecciones del historial de píxeles (nivel de llamada de dibujo) y primitivas (nivel de triángulo) en dos resultados diferentes.
MS-HAID: vspixengine.IPixelHistoryCallback2
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixelHistoryCallback2
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 0111482E-B66A-4763-8890-85B1711F38B2
api_name:
- IPixelHistoryCallback2
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 473f3540ad9c6a16659a6e43c3aa31eef706ec59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537323"
---
# <a name="span-idvspixengineipixelhistorycallback2spanipixelhistorycallback2-interface"></a><span data-ttu-id="ccadf-103"><span id="vspixengine.ipixelhistorycallback2"></span>Interfaz IPixelHistoryCallback2</span><span class="sxs-lookup"><span data-stu-id="ccadf-103"><span id="vspixengine.ipixelhistorycallback2"></span>IPixelHistoryCallback2 interface</span></span>

<span data-ttu-id="ccadf-104">Devolución de llamada para devolver intersecciones del historial de píxeles (nivel de llamada de dibujo) y primitivas (nivel de triángulo) en dos resultados diferentes.</span><span class="sxs-lookup"><span data-stu-id="ccadf-104">Callback to return pixel history intersections (draw call level) and primitives (triangle level) in two different results.</span></span>

## <a name="members"></a><span data-ttu-id="ccadf-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="ccadf-105">Members</span></span>

<span data-ttu-id="ccadf-106">La interfaz **IPixelHistoryCallback2** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ccadf-106">The **IPixelHistoryCallback2** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ccadf-107">**IPixelHistoryCallback2** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ccadf-107">**IPixelHistoryCallback2** also has these types of members:</span></span>

-   [<span data-ttu-id="ccadf-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="ccadf-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ccadf-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="ccadf-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ccadf-110">La interfaz **IPixelHistoryCallback2** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="ccadf-110">The **IPixelHistoryCallback2** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ccadf-111">Método</span><span class="sxs-lookup"><span data-stu-id="ccadf-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ccadf-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="ccadf-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ccadf-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ccadf-113"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-intersectionscallback-dword-pixelhistoryintersection-arr"><strong>IntersectionsCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ccadf-114">Devolución de llamada que notifica al host la información de intersección del historial de píxeles devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="ccadf-114">A callback that notifies the host of pixel history intersection information returned by the assocaited request.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ccadf-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="ccadf-115"><a href="/windows/desktop/direct3dtools/ipixelhistorycallback2-primitivescallback-dword-pixelhistoryoperation-arr"><strong>PrimitivesCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ccadf-116">Devolución de llamada que notifica al host la información de la operación primitiva del historial de píxeles devuelta por la solicitud asociada.</span><span class="sxs-lookup"><span data-stu-id="ccadf-116">A callback that notifies the host of pixel history primitive operation information returned by the associated request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ccadf-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccadf-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ccadf-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ccadf-118">Header</span></span></p></td><td><span data-ttu-id="ccadf-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ccadf-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
