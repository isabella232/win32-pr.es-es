---
description: Per-Pixel combinación alfa
ms.assetid: 68661dc5-1423-47b2-a0df-858e5eb7f02b
title: Per-Pixel combinación alfa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df7e67084ae19df4a1aab81474dc8a9b1a313b9d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686339"
---
# <a name="per-pixel-alpha-blending"></a><span data-ttu-id="20ba6-103">Per-Pixel combinación alfa</span><span class="sxs-lookup"><span data-stu-id="20ba6-103">Per-Pixel Alpha Blending</span></span>

<span data-ttu-id="20ba6-104">Se han definido cuatro subtipos de medios para la combinación alfa por píxel.</span><span class="sxs-lookup"><span data-stu-id="20ba6-104">Four media subtypes have been defined for per-pixel alpha blending.</span></span> <span data-ttu-id="20ba6-105">Estos subtipos solo se admiten cuando el VMR está en modo de mezcla.</span><span class="sxs-lookup"><span data-stu-id="20ba6-105">These subtypes are only supported when the VMR is in mixing mode.</span></span> <span data-ttu-id="20ba6-106">VMR rechazará la conexión si no está en modo de mezcla cuando un filtro de nivel superior intenta conectarse utilizando uno de estos subtipos.</span><span class="sxs-lookup"><span data-stu-id="20ba6-106">The VMR will reject the connection if it is not in mixing mode when an upstream filter attempts to connect using one of these subtypes.</span></span> <span data-ttu-id="20ba6-107">Estos subtipos se definen en UUID. h:</span><span class="sxs-lookup"><span data-stu-id="20ba6-107">These subtypes are defined in uuids.h:</span></span>

-   <span data-ttu-id="20ba6-108">MEDIASUBTYPE \_ ARGB1555</span><span class="sxs-lookup"><span data-stu-id="20ba6-108">MEDIASUBTYPE\_ARGB1555</span></span>
-   <span data-ttu-id="20ba6-109">MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="20ba6-109">MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="20ba6-110">MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="20ba6-110">MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="20ba6-111">MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="20ba6-111">MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="20ba6-112">Para obtener más información, vea subtipos de [vídeo RGB sin comprimir](uncompressed-rgb-video-subtypes.md) y [**subtipos de vídeo YUV**](yuv-video-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="20ba6-112">For more information, see [Uncompressed RGB Video Subtypes](uncompressed-rgb-video-subtypes.md) and [**YUV Video Subtypes**](yuv-video-subtypes.md).</span></span>

 

 



