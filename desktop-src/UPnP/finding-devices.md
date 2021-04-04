---
title: Búsqueda de dispositivos
description: La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse y dejar la red en cualquier momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076187"
---
# <a name="finding-devices"></a><span data-ttu-id="527d0-103">Búsqueda de dispositivos</span><span class="sxs-lookup"><span data-stu-id="527d0-103">Finding Devices</span></span>

<span data-ttu-id="527d0-104">La arquitectura de UPnP es una arquitectura de red dinámica que permite a los dispositivos unirse y dejar la red en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="527d0-104">The UPnP architecture is a dynamic network architecture that allows devices to join and leave the network at any time.</span></span> <span data-ttu-id="527d0-105">Debido a esta arquitectura dinámica, las aplicaciones no pueden confiar en que los dispositivos basados en UPnP específicos estén disponibles en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="527d0-105">Because of this dynamic architecture, applications cannot rely on specific UPnP-based devices to be available at any given time.</span></span> <span data-ttu-id="527d0-106">Por este motivo, las aplicaciones (o los puntos de control) buscan en la red los dispositivos que coinciden mejor con los criterios especificados.</span><span class="sxs-lookup"><span data-stu-id="527d0-106">For this reason, applications (or control points) search the network to find devices that most closely match specified criteria.</span></span> <span data-ttu-id="527d0-107">Las aplicaciones también esperan mensajes de anuncios de dispositivo que indican que se han agregado nuevos dispositivos a la red.</span><span class="sxs-lookup"><span data-stu-id="527d0-107">Applications also wait for device advertisement messages that indicate new devices have been added to the network.</span></span>

<span data-ttu-id="527d0-108">Estos son los criterios de búsqueda válidos para dispositivos basados en UPnP:</span><span class="sxs-lookup"><span data-stu-id="527d0-108">The following are valid search criteria for UPnP-based devices:</span></span>

-   <span data-ttu-id="527d0-109">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="527d0-109">Device type</span></span>
-   <span data-ttu-id="527d0-110">Tipo de servicio</span><span class="sxs-lookup"><span data-stu-id="527d0-110">Service type</span></span>
-   <span data-ttu-id="527d0-111">Nombre único del dispositivo (UDN)</span><span class="sxs-lookup"><span data-stu-id="527d0-111">Unique device name (UDN)</span></span>
-   <span data-ttu-id="527d0-112">Todos los dispositivos raíz</span><span class="sxs-lookup"><span data-stu-id="527d0-112">All root devices</span></span>

<span data-ttu-id="527d0-113">Las búsquedas de tipo de dispositivo y tipo de servicio se usan normalmente para buscar una clase de dispositivos con características comunes.</span><span class="sxs-lookup"><span data-stu-id="527d0-113">The device type and service type searches are typically used to find a class of devices with common characteristics.</span></span> <span data-ttu-id="527d0-114">La búsqueda de UDN se usa para buscar un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="527d0-114">The UDN search is used to find a specific device.</span></span>

<span data-ttu-id="527d0-115">Para buscar dispositivos, una aplicación debe crear primero instancias del objeto de buscador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="527d0-115">To search for devices, an application must first instantiate the Device Finder object.</span></span> <span data-ttu-id="527d0-116">Este objeto expone la interfaz [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; sus métodos realizan las búsquedas descritas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="527d0-116">This object exposes the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface; its methods perform the previously described searches.</span></span>

<span data-ttu-id="527d0-117">En las secciones siguientes se describe el proceso de búsqueda de dispositivos:</span><span class="sxs-lookup"><span data-stu-id="527d0-117">The following sections describe the process of finding devices:</span></span>

-   [<span data-ttu-id="527d0-118">Crear el buscador de dispositivos</span><span class="sxs-lookup"><span data-stu-id="527d0-118">Creating the Device Finder</span></span>](creating-the-device-finder.md)
-   [<span data-ttu-id="527d0-119">Búsqueda asincrónica</span><span class="sxs-lookup"><span data-stu-id="527d0-119">Asynchronous Searching</span></span>](asynchronous-searching.md)
-   [<span data-ttu-id="527d0-120">Búsqueda sincrónica</span><span class="sxs-lookup"><span data-stu-id="527d0-120">Synchronous Searching</span></span>](synchronous-searching.md)
-   [<span data-ttu-id="527d0-121">Colecciones de dispositivos devueltas por búsquedas sincrónicas</span><span class="sxs-lookup"><span data-stu-id="527d0-121">Device Collections Returned By Synchronous Searches</span></span>](device-collections-returned-by-synchronous-searches.md)

 

 




