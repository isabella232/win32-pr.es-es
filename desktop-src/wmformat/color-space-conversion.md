---
title: Conversión de espacio de colores
description: Conversión de espacio de colores
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- SDK de Windows Media Format, conversión de espacio de colores
- Advanced Systems Format (ASF), conversión de espacio de colores
- ASF (formato de sistemas avanzados), conversión de espacio de colores
- conversión de espacio de colores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268765"
---
# <a name="color-space-conversion"></a><span data-ttu-id="ed981-107">Conversión de espacio de colores</span><span class="sxs-lookup"><span data-stu-id="ed981-107">Color Space Conversion</span></span>

<span data-ttu-id="ed981-108">A menudo hay una diferencia entre la profundidad de color del formato de vídeo comprimido en el perfil y el formato de entrada.</span><span class="sxs-lookup"><span data-stu-id="ed981-108">There is often a difference between the color depth of the compressed video format in the profile and the input format.</span></span> <span data-ttu-id="ed981-109">Cuando esto sucede, el vídeo de origen se debe convertir para ajustarse al espacio de colores del destino.</span><span class="sxs-lookup"><span data-stu-id="ed981-109">When this happens, the source video must be converted to conform to the color space of the destination.</span></span> <span data-ttu-id="ed981-110">El escritor controla este proceso y se comunica con un convertidor de espacio de colores interno.</span><span class="sxs-lookup"><span data-stu-id="ed981-110">The writer handles this process, communicating with an internal color-space converter.</span></span>

<span data-ttu-id="ed981-111">El lector también se comunica con el convertidor de espacio de colores para reconciliar las diferencias entre el formato comprimido y el formato de salida.</span><span class="sxs-lookup"><span data-stu-id="ed981-111">The reader also communicates with the color-space converter to reconcile any difference between the compressed format and the output format.</span></span>

<span data-ttu-id="ed981-112">Como con todas las transformaciones realizadas en los datos, la conversión entre profundidades de color puede reducir la calidad del resultado.</span><span class="sxs-lookup"><span data-stu-id="ed981-112">As with all transforms performed on data, converting between color depths can reduce the quality of the output.</span></span> <span data-ttu-id="ed981-113">Cuando sea posible, debe usar los formatos de entrada y salida con la misma profundidad de color que el formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="ed981-113">When possible, you should use input and output formats with the same color depth as the compressed format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed981-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ed981-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed981-115">**Características de escritura de archivos**</span><span class="sxs-lookup"><span data-stu-id="ed981-115">**File Writing Features**</span></span>](file-writing-features.md)
</dt> <dt>

[<span data-ttu-id="ed981-116">**Trabajar con entradas**</span><span class="sxs-lookup"><span data-stu-id="ed981-116">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> <dt>

[<span data-ttu-id="ed981-117">**Trabajar con salidas**</span><span class="sxs-lookup"><span data-stu-id="ed981-117">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




