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
# <a name="dxgi-15-improvements"></a>Mejoras en DXGI 1,5

La siguiente funcionalidad se ha agregado a la infraestructura de gráficos de Microsoft DirectX (DXGI) 1,5, para admitir la especificación y la duplicación más flexibles de los formatos de salida.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Gama de colores alto y ancho dinámico

Consulte [uso de DirectX con altas pantallas de rango dinámico y color avanzado](../direct3darticles/high-dynamic-range.md).

## <a name="variable-refresh-rate-displays"></a>Se muestra la frecuencia de actualización de variables

Consulte [frecuencia de actualización de variables](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicar salida

Se ha agregado una sola interfaz, [**IDXGIOutput5**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5), con un único método, [**DUPLICATEOUTPUT1**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1), a DXGI 1,5 para proporcionar una versión de rendimiento más flexible y superior del método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original. **DuplicateOutput1** permite especificar una lista de formatos admitidos para las superficies de pantalla completa que pueden ser devueltas por el objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) y permite capturar contenido de HDR y WCG.

## <a name="offering-and-reclaiming-resources"></a>Oferta y recuperación de recursos

Los métodos actualizados [**OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) y [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) se han agregado a una nueva interfaz, [**IDXGIDevice4**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4), para permitir que se anule la confirmación de memoria además de descartar los recursos. Al optar por la nueva marca de recursos de la oferta de DXGI, permitir marca de [**\_ \_ \_ \_ \_ desconfirmación**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) significa que los nuevos resultados de la reclamación deben ser controlados correctamente.

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
