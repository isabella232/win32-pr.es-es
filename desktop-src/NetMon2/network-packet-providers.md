---
description: Los proveedores de paquetes de red (NPPs) son Monitor de red componentes del sistema que recopilan el tráfico de red (tramas) de la red y los pasan a la interfaz de usuario Monitor de red y a las aplicaciones NPP.
ms.assetid: c966cd00-5cab-4fcf-ad8e-b6c4ffb0e977
title: Proveedores de paquetes de red
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8257a62e4f8b0a8434143b2fecba04d9a66c9fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913442"
---
# <a name="network-packet-providers"></a><span data-ttu-id="f537e-103">Proveedores de paquetes de red</span><span class="sxs-lookup"><span data-stu-id="f537e-103">Network Packet Providers</span></span>

<span data-ttu-id="f537e-104">Los proveedores de paquetes de red (NPPs) son Monitor de red componentes del sistema que recopilan el tráfico de red (tramas) de la red y los pasan a la interfaz de usuario Monitor de red y a [*las aplicaciones NPP*](n.md).</span><span class="sxs-lookup"><span data-stu-id="f537e-104">Network packet providers (NPPs) are Network Monitor system components that collect network traffic (frames) from the network and pass them on to the Network Monitor UI, and [*NPP applications*](n.md).</span></span>

<span data-ttu-id="f537e-105">En la ilustración siguiente se muestran dos NPPs: el NPP de NDIS proporcionado por Monitor de red y un NPP personalizado.</span><span class="sxs-lookup"><span data-stu-id="f537e-105">The following illustration shows two NPPs: the NDIS NPP provided by Network Monitor and a custom NPP.</span></span>

![NPP de NDIS proporcionado por el monitor de red y un NPP personalizado](images/npp.png)

<span data-ttu-id="f537e-107">El NPP de NDIS proporcionado por Monitor de red es Ndisnpp.dll.</span><span class="sxs-lookup"><span data-stu-id="f537e-107">The NDIS NPP provided by Network Monitor is Ndisnpp.dll.</span></span> <span data-ttu-id="f537e-108">Este NPP utiliza el controlador del sistema de Monitor de red (Nmnt.sys) para obtener los fotogramas recopilados de la red y varias interfaces COM (denominadas interfaces NPP) para pasar los fotogramas a la interfaz de usuario de Monitor de red y las aplicaciones NPP, donde se pueden mostrar y analizar.</span><span class="sxs-lookup"><span data-stu-id="f537e-108">This NPP uses the Network Monitor system driver (Nmnt.sys) to get the frames collected from the network and several COM interfaces (referred to as the NPP interfaces) to pass the frames on to the Network Monitor UI, and NPP applications, where they can be displayed and analyzed.</span></span>

<span data-ttu-id="f537e-109">Ndisnpp.dll se conecta a la capa [*NDIS*](n.md) para obtener su tráfico de red.</span><span class="sxs-lookup"><span data-stu-id="f537e-109">Ndisnpp.dll connects to the [*NDIS*](n.md) layer to obtain its network traffic.</span></span> <span data-ttu-id="f537e-110">(Los NPPs personalizados pueden omitir la capa NDIS y comunicarse directamente con el hardware de red). Tenga en cuenta que, independientemente de si un NPP usa NDIS, NPPs puede conectarse a cualquier número de tarjetas de red y que todos los NPPs deben admitir las mismas interfaces NPP.</span><span class="sxs-lookup"><span data-stu-id="f537e-110">(Custom NPPs can bypass the NDIS layer and communicate directly with the networking hardware.) Be aware that regardless of whether an NPP uses NDIS, NPPs can connect to any number of network cards and that all NPPs must support the same NPP interfaces.</span></span>

<span data-ttu-id="f537e-111">Para que una aplicación pueda empezar a capturar datos, debe:</span><span class="sxs-lookup"><span data-stu-id="f537e-111">Before an application can start to capture data, it must:</span></span>

-   <span data-ttu-id="f537e-112">Seleccione la tarjeta de interfaz de red (NIC) que conectará el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="f537e-112">Select the network interface card (NIC) that will connect the NPP to the network.</span></span>
-   <span data-ttu-id="f537e-113">Seleccione la interfaz NPP que se utilizará para capturar los fotogramas de red.</span><span class="sxs-lookup"><span data-stu-id="f537e-113">Select the NPP interface that will be used to capture the network frames.</span></span>
-   <span data-ttu-id="f537e-114">Use la interfaz seleccionada para conectarse a la NIC.</span><span class="sxs-lookup"><span data-stu-id="f537e-114">Use the selected interface to connect to the NIC.</span></span>

<span data-ttu-id="f537e-115">Para obtener más información acerca de cómo enumerar y seleccionar una tarjeta de interfaz de red, consulte [seleccionar una tarjeta de interfaz de red](selecting-a-network-interface-card.md).</span><span class="sxs-lookup"><span data-stu-id="f537e-115">For more information about how to enumerate and select a network interface card, see [Selecting a Network Interface Card](selecting-a-network-interface-card.md).</span></span>

<span data-ttu-id="f537e-116">Para obtener más información sobre las interfaces COM expuestas por NPPs, consulte [seleccionar una interfaz NPP](selecting-an-npp-interface.md).</span><span class="sxs-lookup"><span data-stu-id="f537e-116">For more information about COM interfaces exposed by NPPs, see [Selecting an NPP Interface](selecting-an-npp-interface.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f537e-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f537e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f537e-118">**IDelaydC**</span><span class="sxs-lookup"><span data-stu-id="f537e-118">**IDelaydC**</span></span>](idelaydc.md)
</dt> <dt>

[<span data-ttu-id="f537e-119">**IESP**</span><span class="sxs-lookup"><span data-stu-id="f537e-119">**IESP**</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="f537e-120">**IRTC**</span><span class="sxs-lookup"><span data-stu-id="f537e-120">**IRTC**</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="f537e-121">**IStas**</span><span class="sxs-lookup"><span data-stu-id="f537e-121">**IStats**</span></span>](istats.md)
</dt> </dl>

 

 



