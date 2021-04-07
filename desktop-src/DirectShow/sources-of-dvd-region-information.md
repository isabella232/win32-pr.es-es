---
description: Orígenes de información de la región de DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Orígenes de información de la región de DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002383"
---
# <a name="sources-of-dvd-region-information"></a><span data-ttu-id="7e4c0-103">Orígenes de información de la región de DVD</span><span class="sxs-lookup"><span data-stu-id="7e4c0-103">Sources of DVD Region Information</span></span>

<span data-ttu-id="7e4c0-104">Hay tres orígenes de información de la región de DVD que funcionan conjuntamente para determinar la región de reproducción de DVD en un equipo Windows.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-104">There are three sources of DVD region information that work together to determine the region for DVD playback on a Windows PC.</span></span>

-   <span data-ttu-id="7e4c0-105">Título del DVD.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-105">DVD Title.</span></span> <span data-ttu-id="7e4c0-106">La mayoría de los títulos de DVD se marcan para una región específica.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-106">Most DVD titles are marked for a specific region.</span></span> <span data-ttu-id="7e4c0-107">Algunos títulos se pueden reproducir en una sola región, algunos se pueden reproducir en varias regiones y otros pueden reproducirse en todas las regiones.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-107">Some titles can be played in only one region, some can be played in multiple regions, and others can be played all regions.</span></span> <span data-ttu-id="7e4c0-108">Las regiones 1 a 6 se definieron en la especificación de DVD-Video original.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-108">Regions 1 through 6 were defined in the original DVD-Video specification.</span></span> <span data-ttu-id="7e4c0-109">La región 7 no está definida actualmente.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-109">Region 7 is currently undefined.</span></span> <span data-ttu-id="7e4c0-110">La región 8 se agregó en 1999 para lugares especiales, como aviones.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-110">Region 8 was added in 1999 for special venues, such as airplanes.</span></span> <span data-ttu-id="7e4c0-111">Los discos DVD-ROM (los que no tienen ninguna zona de vídeo) no deben contener ninguna codificación de región.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-111">DVD-ROM discs (those with no video zone) should not contain any region coding.</span></span>
-   <span data-ttu-id="7e4c0-112">Unidad de DVD-ROM.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-112">DVD-ROM Drive.</span></span> <span data-ttu-id="7e4c0-113">Hay dos tipos de unidades de DVD-ROM: las unidades RPC Phase 1 (RPC1) y las unidades RPC Phase 2 (RPC2).</span><span class="sxs-lookup"><span data-stu-id="7e4c0-113">There are two types of DVD-ROM drives: RPC Phase 1 (RPC1) drives and RPC Phase 2 (RPC2) drives.</span></span> <span data-ttu-id="7e4c0-114">Las unidades RPC1 no tienen compatibilidad integrada con hardware para la administración de regiones.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-114">RPC1 drives do not have built-in hardware support for region management.</span></span> <span data-ttu-id="7e4c0-115">Para estas unidades, Windows mantiene la información del recuento de cambios de la región y la región se puede cambiar una sola vez.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-115">For these drives, Windows maintains the region change count information and the region can be changed only once.</span></span> <span data-ttu-id="7e4c0-116">Las unidades RPC2 mantienen la información de recuento de cambios de la región en hardware y, en general, la región de dichas unidades puede cambiarse hasta cinco veces.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-116">RPC2 drives maintain the region change count information in hardware and in general the region of such drives can be changed up to 5 times.</span></span>
-   <span data-ttu-id="7e4c0-117">Descodificador de DVD.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-117">DVD Decoder.</span></span> <span data-ttu-id="7e4c0-118">Algunos descodificadores de DVD, hardware o software, se establecen para una región específica.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-118">Some DVD decoders, hardware or software, are set for a specific region.</span></span> <span data-ttu-id="7e4c0-119">En general, el usuario no puede cambiar la región del descodificador.</span><span class="sxs-lookup"><span data-stu-id="7e4c0-119">In general, the user cannot change the decoder's region.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e4c0-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7e4c0-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e4c0-121">Compatibilidad de cambio de región de DVD en Windows</span><span class="sxs-lookup"><span data-stu-id="7e4c0-121">DVD Region Change Support in Windows</span></span>](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



