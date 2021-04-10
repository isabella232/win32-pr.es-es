---
description: Devoluciones de llamada utilizadas para ver las texturas.
MS-HAID: vspixengine.IPixEngine5Callbacks
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interfaz IPixEngine5Callbacks
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F87F00ED-C816-49A3-926B-28E3C8330EA2
api_name:
- IPixEngine5Callbacks
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 80f00a0d7e2e3478114d94480e01e31add63ef90
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152403"
---
# <a name="span-idvspixengineipixengine5callbacksspanipixengine5callbacks-interface"></a><span data-ttu-id="e71c7-103"><span id="vspixengine.ipixengine5callbacks"></span>Interfaz IPixEngine5Callbacks</span><span class="sxs-lookup"><span data-stu-id="e71c7-103"><span id="vspixengine.ipixengine5callbacks"></span>IPixEngine5Callbacks interface</span></span>

<span data-ttu-id="e71c7-104">Devoluciones de llamada utilizadas para ver las texturas.</span><span class="sxs-lookup"><span data-stu-id="e71c7-104">Callbacks used for viewing textures.</span></span>

## <a name="members"></a><span data-ttu-id="e71c7-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="e71c7-105">Members</span></span>

<span data-ttu-id="e71c7-106">La interfaz **IPixEngine5Callbacks** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e71c7-106">The **IPixEngine5Callbacks** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e71c7-107">**IPixEngine5Callbacks** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e71c7-107">**IPixEngine5Callbacks** also has these types of members:</span></span>

-   [<span data-ttu-id="e71c7-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="e71c7-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e71c7-109"><span id="methods"></span>Métodos</span><span class="sxs-lookup"><span data-stu-id="e71c7-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e71c7-110">La interfaz **IPixEngine5Callbacks** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e71c7-110">The **IPixEngine5Callbacks** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e71c7-111">Método</span><span class="sxs-lookup"><span data-stu-id="e71c7-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e71c7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e71c7-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e71c7-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-113"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-freetexturecomplete"><strong>FreeTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-114">Función de devolución de llamada que se usa para notificar al host cuando se ha liberado una textura.</span><span class="sxs-lookup"><span data-stu-id="e71c7-114">A callback function used to notify the host when a texture has been freed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e71c7-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-115"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadhistogramcomplete-pixenginehistogram-ptr"><strong>LoadHistogramComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-116">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga del histograma.</span><span class="sxs-lookup"><span data-stu-id="e71c7-116">A callback function used to notify the host when a histogram load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e71c7-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-117"><a href="/previous-versions/windows/desktop/legacy/mt432759(v=vs.85)"><strong>LoadTextureFromFileComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-118">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de textura.</span><span class="sxs-lookup"><span data-stu-id="e71c7-118">A callback function used to notify the host when a texture load has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e71c7-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-119"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-loadtextureslicecomplete-pixenginetextureslicedescriptor-pixenginehistogram-ptr"><strong>LoadTextureSliceComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-120">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una carga de segmento de textura.</span><span class="sxs-lookup"><span data-stu-id="e71c7-120">A callback function used to notify the host when a texture slice load has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e71c7-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-121"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-readtexelvaluecomplete-uint-bstr-arr-double-arr"><strong>ReadTexelValueComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-122">Función de devolución de llamada que se usa para notificar al host cuando se ha completado un valor de textura leído.</span><span class="sxs-lookup"><span data-stu-id="e71c7-122">A callback function used to notify the host when a texel value read has been completed.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="e71c7-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-123"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-rendertexturecomplete"><strong>RenderTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-124">Función de devolución de llamada que se usa para notificar al host cuando se ha completado una representación de textura.</span><span class="sxs-lookup"><span data-stu-id="e71c7-124">A callback function used to notify the host when a texture render has been completed.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e71c7-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span><span class="sxs-lookup"><span data-stu-id="e71c7-125"><a href="/windows/desktop/direct3dtools/ipixengine5callbacks-savetexturecomplete"><strong>SaveTextureComplete</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e71c7-126">Una función de devolución de llamada que se usa para notificar al host cuando se ha completado el guardado de una textura.</span><span class="sxs-lookup"><span data-stu-id="e71c7-126">A callback function used to notify the host when saving a texture has been completed.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e71c7-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e71c7-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e71c7-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e71c7-128">Header</span></span></p></td><td><span data-ttu-id="e71c7-129">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e71c7-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
