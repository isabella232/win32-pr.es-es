---
description: La siguiente funcionalidad se ha agregado a Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.5, para admitir una especificación y duplicación más flexibles de los formatos de salida.
ms.assetid: DD7401E1-9991-48D8-AD23-4D34238EA4AF
title: Mejoras de DXGI 1.5
ms.topic: article
ms.date: 03/05/2021
ms.openlocfilehash: 52661018941f84a14f45c112ba7ed68800d0cf0f2fb69f7a1d3333651fb17787
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987135"
---
# <a name="dxgi-15-improvements"></a>Mejoras de DXGI 1.5

La siguiente funcionalidad se ha agregado a Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.5, para admitir una especificación y duplicación más flexibles de los formatos de salida.

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Alto rango dinámico y gama de colores anchos

Consulte Using DirectX with high dynamic range displays and advanced color (Uso de [DirectX con pantallas de alto rango dinámico y color avanzado).](../direct3darticles/high-dynamic-range.md)

## <a name="variable-refresh-rate-displays"></a>Se muestra la frecuencia de actualización variable

Consulte Variable [refresh rate (Velocidad de actualización variable) para ver](variable-refresh-rate-displays.md).

## <a name="duplicating-output"></a>Duplicación de la salida

Se ha agregado una única interfaz, [**IDXGIOutput5,**](/windows/win32/api/DXGI1_5/nn-dxgi1_5-idxgioutput5)con un único método, [**DuplicateOutput1,**](/windows/win32/api/DXGI1_5/nf-dxgi1_5-idxgioutput5-duplicateoutput1)a DXGI 1.5 para proporcionar una versión de rendimiento más flexible y superior del método [**DuplicateOutput**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput) original. **DuplicateOutput1** permite especificar una lista de formatos admitidos para superficies de pantalla completa que puede devolver el objeto [**IDXGIOutputDuplication**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutputduplication) y permite capturar contenido de HDR y WCG.

## <a name="offering-and-reclaiming-resources"></a>Oferta y reclamación de recursos

Se han [**agregado los métodos actualizados OfferResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-offerresources1) y [**ReclaimResources1**](/windows/win32/api/dxgi1_5/nf-dxgi1_5-idxgidevice4-reclaimresources1) a una nueva interfaz, [**IDXGIDevice4,**](/windows/win32/api/dxgi1_5/nn-dxgi1_5-idxgidevice4)para permitir la desatención de memoria, además de descartar los recursos. Si se opta por la nueva [**marca ALLOW \_ \_ \_ \_ \_ DECOMMIT de DXGI OFFER RESOURCE FLAG,**](/windows/win32/api/dxgi1_5/ne-dxgi1_5-dxgi_offer_resource_flags) los resultados de la nueva reclamación deben controlarse correctamente.

## <a name="related-topics"></a>Temas relacionados

[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
