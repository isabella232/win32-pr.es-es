---
description: La siguiente funcionalidad se ha agregado a la infraestructura de gráficos de Microsoft DirectX (DXGI) 1,5, para admitir la especificación y la duplicación más flexibles de los formatos de salida.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Mejoras en DXGI 1,5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 58df3ef78781437ee033530a2ed2179bb9a132d8
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/06/2021
ms.locfileid: "104361984"
---
# <a name="dxgi-15-improvements"></a><span data-ttu-id="f07ac-103">Mejoras en DXGI 1,5</span><span class="sxs-lookup"><span data-stu-id="f07ac-103">DXGI 1.5 Improvements</span></span>

<span data-ttu-id="f07ac-104">La siguiente funcionalidad se ha agregado a la infraestructura de gráficos de Microsoft DirectX (DXGI) 1,5, para admitir la especificación y la duplicación más flexibles de los formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="f07ac-104">The following functionality has been added to Microsoft DirectX Graphics Infrastructure (DXGI) 1.5, to support more flexible specifying and duplication of output formats.</span></span>

## <a name="high-dynamic-range-and-wide-color-gamut"></a><span data-ttu-id="f07ac-105">Gama de colores alto y ancho dinámico</span><span class="sxs-lookup"><span data-stu-id="f07ac-105">High Dynamic Range and Wide Color Gamut</span></span>

<span data-ttu-id="f07ac-106">Consulte [uso de DirectX con altas pantallas de rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md).</span><span class="sxs-lookup"><span data-stu-id="f07ac-106">Refer to [Using DirectX with high dynamic range displays and advanced color](../direct3darticles/high-dynamic-range.md).</span></span>

## <a name="variable-refresh-rate-displays"></a><span data-ttu-id="f07ac-107">Se muestra la frecuencia de actualización de variables</span><span class="sxs-lookup"><span data-stu-id="f07ac-107">Variable refresh rate displays</span></span>

<span data-ttu-id="f07ac-108">Consulte [frecuencia de actualización de variables](variable-refresh-rate-displays.md).</span><span class="sxs-lookup"><span data-stu-id="f07ac-108">Refer to [Variable refresh rate displays](variable-refresh-rate-displays.md).</span></span>

## <a name="duplicating-output"></a><span data-ttu-id="f07ac-109">Duplicar salida</span><span class="sxs-lookup"><span data-stu-id="f07ac-109">Duplicating output</span></span>

<span data-ttu-id="f07ac-110">Se ha agregado una sola interfaz, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), con un único método, [**DUPLICATEOUTPUT1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), a DXGI 1,5 para proporcionar una versión de rendimiento más flexible y superior del método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original.</span><span class="sxs-lookup"><span data-stu-id="f07ac-110">A single interface, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), with a single method, [**DuplicateOutput1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), has been added to DXGI 1.5 to provide a more flexible and higher performance version of the original [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) method.</span></span> <span data-ttu-id="f07ac-111">**DuplicateOutput1** permite especificar una lista de formatos admitidos para las superficies de pantalla completa que pueden ser devueltas por el objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) y permite capturar contenido de HDR y WCG.</span><span class="sxs-lookup"><span data-stu-id="f07ac-111">**DuplicateOutput1** allows specifying a list of supported formats for fullscreen surfaces that can be returned by the [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) object, and enables capturing HDR and WCG content.</span></span>

## <a name="offering-and-reclaiming-resources"></a><span data-ttu-id="f07ac-112">Oferta y recuperación de recursos</span><span class="sxs-lookup"><span data-stu-id="f07ac-112">Offering and Reclaiming Resources</span></span>

<span data-ttu-id="f07ac-113">Los métodos actualizados [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) y [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) se han agregado a una nueva interfaz, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), para permitir que se anule la confirmación de memoria además de descartar los recursos.</span><span class="sxs-lookup"><span data-stu-id="f07ac-113">Updated methods [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) and [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) have been added to a new interface, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), to allow de-committing of memory in addition to discarding resources.</span></span> <span data-ttu-id="f07ac-114">Al optar por la nueva marca de recursos de la oferta de DXGI, permitir marca de [**\_ \_ \_ \_ \_ desconfirmación**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) significa que los nuevos resultados de la reclamación deben ser controlados correctamente.</span><span class="sxs-lookup"><span data-stu-id="f07ac-114">Opting in to the new [**DXGI\_OFFER\_RESOURCE\_FLAG\_ALLOW\_DECOMMIT**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) flag means the new reclaim results must be properly handled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f07ac-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f07ac-115">Related topics</span></span>

[<span data-ttu-id="f07ac-116">Guía de programación para DXGI</span><span class="sxs-lookup"><span data-stu-id="f07ac-116">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
