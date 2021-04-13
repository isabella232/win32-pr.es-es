---
title: Administración del tamaño del paquete
description: Administración del tamaño del paquete
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- SDK de Windows Media Format, administrar tamaños de paquetes
- SDK de Windows Media Format, tamaños de paquete
- perfiles, tamaños de paquete
- perfiles, administración de tamaños de paquetes
- paquetes, tamaños
- paquetes, interfaz IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420450"
---
# <a name="managing-packet-size"></a><span data-ttu-id="c72c1-110">Administración del tamaño del paquete</span><span class="sxs-lookup"><span data-stu-id="c72c1-110">Managing Packet Size</span></span>

<span data-ttu-id="c72c1-111">El escritor está diseñado para administrar el tamaño de los paquetes internamente.</span><span class="sxs-lookup"><span data-stu-id="c72c1-111">The writer is designed to manage the size of packets internally.</span></span> <span data-ttu-id="c72c1-112">Sin embargo, puede que tenga requisitos específicos para su aplicación que llamen a un control manual sobre el tamaño de los paquetes en los archivos ASF que escriba.</span><span class="sxs-lookup"><span data-stu-id="c72c1-112">However, you may have specific requirements for your application that call for some manual control over the size of packets in the ASF files that you write.</span></span> <span data-ttu-id="c72c1-113">El SDK de Windows Media Format proporciona dos interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) y [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , que le permiten controlar el tamaño máximo y mínimo de los paquetes.</span><span class="sxs-lookup"><span data-stu-id="c72c1-113">The Windows Media Format SDK provides two interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) and [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) that enable you to control the maximum and minimum size of packets.</span></span>

<span data-ttu-id="c72c1-114">Ambas interfaces de tamaño de paquete se exponen en el objeto de perfil.</span><span class="sxs-lookup"><span data-stu-id="c72c1-114">Both packet size interfaces are exposed in the profile object.</span></span> <span data-ttu-id="c72c1-115">También están disponibles para el objeto lector.</span><span class="sxs-lookup"><span data-stu-id="c72c1-115">They are also available to the reader object.</span></span> <span data-ttu-id="c72c1-116">Al igual que con otras interfaces relacionadas con perfiles, el lector solo puede tener acceso a los métodos de lectura.</span><span class="sxs-lookup"><span data-stu-id="c72c1-116">As with other profile-related interfaces, the reader can access only the reading methods.</span></span>

<span data-ttu-id="c72c1-117">El tamaño de los paquetes tiene algún efecto en el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c72c1-117">The size of packets has some effect on performance.</span></span> <span data-ttu-id="c72c1-118">En general, cuanto menor es el tamaño del paquete, más se fragmentan los datos en un archivo.</span><span class="sxs-lookup"><span data-stu-id="c72c1-118">In general, the smaller the packet size, the more fragmented the data is within a file.</span></span> <span data-ttu-id="c72c1-119">Cuanto más se fragmenta un archivo, menos eficaz será reconstruirlo.</span><span class="sxs-lookup"><span data-stu-id="c72c1-119">The more fragmented a file is, the less efficient it will be to reconstruct it.</span></span> <span data-ttu-id="c72c1-120">En un escenario de streaming, esto puede no ser una consideración importante, ya que el proceso de lectura de un archivo de un origen de Internet suele ser ineficaz.</span><span class="sxs-lookup"><span data-stu-id="c72c1-120">In a streaming scenario, this may not be an important consideration, as the process of reading a file from an Internet source is generally inefficient.</span></span> <span data-ttu-id="c72c1-121">No obstante, cuando se trabaja con un archivo de forma local, esto podría ser una consideración.</span><span class="sxs-lookup"><span data-stu-id="c72c1-121">When dealing with a file locally however, this might be a consideration.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c72c1-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c72c1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c72c1-123">**Interfaz IWMPacketSize**</span><span class="sxs-lookup"><span data-stu-id="c72c1-123">**IWMPacketSize Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[<span data-ttu-id="c72c1-124">**Interfaz IWMPacketSize2**</span><span class="sxs-lookup"><span data-stu-id="c72c1-124">**IWMPacketSize2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[<span data-ttu-id="c72c1-125">**Trabajar con perfiles**</span><span class="sxs-lookup"><span data-stu-id="c72c1-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




