---
title: Espacio de direcciones disponible para los recursos en mosaico
description: En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2019
ms.locfileid: "103784864"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="fbd7b-103">Espacio de direcciones disponible para los recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="fbd7b-103">Address space available for tiled resources</span></span>

<span data-ttu-id="fbd7b-104">En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.</span><span class="sxs-lookup"><span data-stu-id="fbd7b-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="fbd7b-105">En los sistemas operativos de 64 bits, hay disponible al menos 40 bits de espacio de direcciones virtuales (1 terabyte).</span><span class="sxs-lookup"><span data-stu-id="fbd7b-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="fbd7b-106">En el caso de los sistemas operativos de 32 bits, el espacio de direcciones es de 32 bits (4 GB).</span><span class="sxs-lookup"><span data-stu-id="fbd7b-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="fbd7b-107">En el caso de los sistemas ARM de 32 bits, se puede producir un error en la creación de recursos en mosaico individuales si la asignación usaría más de 27 bits de espacio de direcciones (128 MB).</span><span class="sxs-lookup"><span data-stu-id="fbd7b-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="fbd7b-108">Esto incluye cualquier relleno oculto en el espacio de direcciones que el hardware puede usar para los mapas de caracteres, el relleno de mosaico empaquetado y, posiblemente, el relleno de las dimensiones de superficie a potencias de 2.</span><span class="sxs-lookup"><span data-stu-id="fbd7b-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="fbd7b-109">En los sistemas de gráficos con una tabla de páginas independiente para la unidad de procesamiento de gráficos (GPU), la mayor parte de este espacio de direcciones estará disponible para los recursos de GPU que realiza la aplicación, aunque las asignaciones de GPU realizadas por el controlador de pantalla caben en el mismo espacio.</span><span class="sxs-lookup"><span data-stu-id="fbd7b-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="fbd7b-110">En los sistemas futuros con una tabla de páginas compartida entre la CPU y la GPU, el espacio de direcciones disponible se comparte entre todas las asignaciones de CPU y GPU en un proceso.</span><span class="sxs-lookup"><span data-stu-id="fbd7b-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbd7b-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fbd7b-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbd7b-112">Parámetros de creación de recursos en mosaico</span><span class="sxs-lookup"><span data-stu-id="fbd7b-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




