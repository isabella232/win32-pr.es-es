---
description: Formatos de píxeles de rango dinámico altos
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formatos de píxeles de rango dinámico altos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911941"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="2e8b4-103">Formatos de píxeles de rango dinámico altos</span><span class="sxs-lookup"><span data-stu-id="2e8b4-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="2e8b4-104">Los códecs deben usar formatos de píxeles de Windows Imaging Component (WIC) que conserven todo el intervalo dinámico de los datos del sensor subyacente.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="2e8b4-105">GUID \_ WICPixelFormat48bppRGB es un formato típico de 16 bits por canal de punto fijo que se puede usar.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="2e8b4-106">También se pueden usar otros formatos de precisión más altos.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="2e8b4-107">Para habilitar la compatibilidad total con la canalización de representación acelerada de la unidad de procesamiento de gráficos (GPU) de Windows Presentation Foundation, Microsoft recomienda la compatibilidad con un formato de píxel de punto flotante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="2e8b4-108">Formatos de píxeles de alto color: con Windows 7, se han agregado dos nuevos formatos de píxel de WIC para admitir los nuevos formatos de presentación de color alto.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="2e8b4-109">Estos son: GUID \_ WICPixelFormat32bppRGBA1010102 y GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="2e8b4-110">El formato de alto color Float de 16 bits por canal (BPC) es compatible con el \_ formato de píxel WICPixelFormat64bppRGBAHalf de GUID existente.</span><span class="sxs-lookup"><span data-stu-id="2e8b4-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e8b4-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2e8b4-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2e8b4-112">**Vista**</span><span class="sxs-lookup"><span data-stu-id="2e8b4-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2e8b4-113">Información general sobre componentes de Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="2e8b4-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="2e8b4-114">Instrucciones de WIC para formatos de imagen RAW de cámara</span><span class="sxs-lookup"><span data-stu-id="2e8b4-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="2e8b4-115">Cómo escribir un códec de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="2e8b4-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



