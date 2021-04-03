---
description: Acceso a las superficies de DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Acceso a las superficies de DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906830"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="d87fb-103">Acceso a las superficies de DirectDraw</span><span class="sxs-lookup"><span data-stu-id="d87fb-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="d87fb-104">Los objetos de ejemplo multimedia que proporcionan los filtros de la VMR a los de nivel superior admiten la interfaz [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) .</span><span class="sxs-lookup"><span data-stu-id="d87fb-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="d87fb-105">Para obtener la interfaz, llame a QueryInterface en la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) y especifique IID \_ IVMRSurface.</span><span class="sxs-lookup"><span data-stu-id="d87fb-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="d87fb-106">Los filtros ascendentes pueden usar los métodos de IVMRSurface para tener acceso y manipular la superficie que ha creado el VMR.</span><span class="sxs-lookup"><span data-stu-id="d87fb-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d87fb-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d87fb-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d87fb-108">Usar la VMR para desarrolladores de filtros de DirectShow</span><span class="sxs-lookup"><span data-stu-id="d87fb-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



