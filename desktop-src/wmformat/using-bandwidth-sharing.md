---
title: Uso del uso compartido de ancho de banda
description: Uso del uso compartido de ancho de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- SDK de Windows Media Format, uso compartido de ancho de banda
- uso compartido de ancho de banda, acerca de
- perfiles, uso compartido de ancho de banda
- flujos, uso compartido de ancho de banda
- uso compartido de ancho de banda, interfaz IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420457"
---
# <a name="using-bandwidth-sharing"></a><span data-ttu-id="7fdf7-108">Uso del uso compartido de ancho de banda</span><span class="sxs-lookup"><span data-stu-id="7fdf7-108">Using Bandwidth Sharing</span></span>

<span data-ttu-id="7fdf7-109">Puede usar objetos de uso compartido de ancho de banda para especificar que determinados flujos, cuando se combinan, no utilicen más ancho de banda de lo especificado.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-109">You can use bandwidth sharing objects to specify that certain streams, when combined, will not use more bandwidth than specified.</span></span> <span data-ttu-id="7fdf7-110">El escritor no genera ni comprueba la información de un objeto de uso compartido de ancho de banda ni lo usa el lector para nada.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-110">The information in a bandwidth sharing object is not generated or verified by the writer nor used by the reader for anything.</span></span>

<span data-ttu-id="7fdf7-111">Cuando se escribe un archivo que tiene información de uso compartido de ancho de banda en su perfil, los datos se almacenan en la sección de encabezado.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-111">When a file is written that has bandwidth sharing information in its profile, the data is stored in its header section.</span></span> <span data-ttu-id="7fdf7-112">Puede usar la interfaz [**IWMProfile**](iwmprofile.md) en el lector para comprobar la información de uso compartido del ancho de banda cuando se reproduzca el archivo.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-112">You can use the [**IWMProfile**](iwmprofile.md) interface in the reader to check for bandwidth sharing information when the file is played.</span></span>

<span data-ttu-id="7fdf7-113">Cada objeto de uso compartido de ancho de banda se define con dos valores.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-113">Each bandwidth sharing object is defined by two settings.</span></span> <span data-ttu-id="7fdf7-114">El primero es el ancho de banda, tal y como se define en un ancho de banda y una ventana de búfer.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-114">First is the bandwidth, as defined by a bandwidth and a buffer window.</span></span> <span data-ttu-id="7fdf7-115">La segunda opción es un tipo de uso compartido de ancho de banda, que puede ser exclusivo o parcial.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-115">The second setting is a bandwidth sharing type, which can be either exclusive or partial.</span></span> <span data-ttu-id="7fdf7-116">El uso compartido de ancho de banda exclusivo significa que las secuencias constituyentes se reproducen de una en una, mientras que parcial significa que las secuencias se entregan al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="7fdf7-116">Exclusive bandwidth sharing means that the constituent streams are played back one at a time, while partial means the streams are delivered concurrently.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fdf7-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7fdf7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fdf7-118">**Interfaz IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-118">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="7fdf7-119">**IWMProfile3::AddBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-119">**IWMProfile3::AddBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="7fdf7-120">**IWMProfile3::CreateNewBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-120">**IWMProfile3::CreateNewBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="7fdf7-121">**IWMProfile3::GetBandwidthSharing**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-121">**IWMProfile3::GetBandwidthSharing**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[<span data-ttu-id="7fdf7-122">**IWMProfile3::GetBandwidthSharingCount**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-122">**IWMProfile3::GetBandwidthSharingCount**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[<span data-ttu-id="7fdf7-123">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="7fdf7-123">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




