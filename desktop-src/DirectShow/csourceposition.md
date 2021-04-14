---
description: CSourcePosition es una clase abstracta para implementar la interfaz IMediaPosition en un filtro de origen.
ms.assetid: 838d2efd-6870-4412-98e2-fb2628e14bf3
title: Clase CSourcePosition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourcePosition
api_type:
- COM
api_location: ''
ms.openlocfilehash: 0b88289381641edcef5922557862729acbb81f54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659263"
---
# <a name="csourceposition-class"></a><span data-ttu-id="5748b-103">Clase CSourcePosition</span><span class="sxs-lookup"><span data-stu-id="5748b-103">CSourcePosition class</span></span>

<span data-ttu-id="5748b-104">`CSourcePosition` es una clase abstracta para implementar la interfaz [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) en un filtro de origen.</span><span class="sxs-lookup"><span data-stu-id="5748b-104">`CSourcePosition` is an abstract class for implementing the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface on a source filter.</span></span>

<span data-ttu-id="5748b-105">Esta clase está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="5748b-105">This class is obsolete.</span></span> <span data-ttu-id="5748b-106">Si el filtro de origen es buscable, debe exponer la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) en lugar de **IMediaPosition**.</span><span class="sxs-lookup"><span data-stu-id="5748b-106">If your source filter is seekable, it should expose the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface instead of **IMediaPosition**.</span></span> <span data-ttu-id="5748b-107">Puede usar la clase base [**CSourceSeeking**](csourceseeking.md) para este propósito.</span><span class="sxs-lookup"><span data-stu-id="5748b-107">You can use the [**CSourceSeeking**](csourceseeking.md) base class for this purpose.</span></span>

 

 



