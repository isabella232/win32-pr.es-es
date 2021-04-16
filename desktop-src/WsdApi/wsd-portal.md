---
description: La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al perfil de dispositivos para servicios web (DPWS).
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Servicios web en dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d8b5812983e7102093234458c94b475bb6a503
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696778"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="728de-103">Servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="728de-103">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="728de-104">Propósito</span><span class="sxs-lookup"><span data-stu-id="728de-104">Purpose</span></span>

<span data-ttu-id="728de-105">La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="728de-105">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="728de-106">WSDAPI usa [WS-Discovery para la](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) detección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="728de-106">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="728de-107">WSDAPI se puede usar para el desarrollo de implementaciones de cliente y de servicio.</span><span class="sxs-lookup"><span data-stu-id="728de-107">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="728de-108">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="728de-108">Where applicable</span></span>

<span data-ttu-id="728de-109">Servicios web en dispositivos permite a un cliente detectar y tener acceso a un dispositivo remoto y sus servicios asociados a través de una red.</span><span class="sxs-lookup"><span data-stu-id="728de-109">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="728de-110">Admite la detección de dispositivos, la descripción, el control y los eventos.</span><span class="sxs-lookup"><span data-stu-id="728de-110">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="728de-111">Los desarrolladores pueden crear proxies de cliente de WSDAPI y códigos auxiliares correspondientes para los hosts de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="728de-111">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="728de-112">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="728de-112">Developer audience</span></span>

<span data-ttu-id="728de-113">La documentación de servicios web en dispositivos está pensada para programadores de C/C++ y proveedores de dispositivos que crean productos conformes a DPWS.</span><span class="sxs-lookup"><span data-stu-id="728de-113">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="728de-114">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="728de-114">Run-time requirements</span></span>

<span data-ttu-id="728de-115">Las aplicaciones cliente que usan WSDAPI se admiten a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="728de-115">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="728de-116">En esta sección</span><span class="sxs-lookup"><span data-stu-id="728de-116">In this section</span></span>



| <span data-ttu-id="728de-117">Tema</span><span class="sxs-lookup"><span data-stu-id="728de-117">Topic</span></span>                                                                                  | <span data-ttu-id="728de-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="728de-118">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="728de-119">Acerca de los servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="728de-119">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="728de-120">Información general y arquitectónica sobre los servicios web en los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="728de-120">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="728de-121">Uso de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="728de-121">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="728de-122">Información sobre la generación de código, la configuración de aplicaciones y la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="728de-122">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="728de-123">Referencia de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="728de-123">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="728de-124">Documentación de referencia de la API servicios web en dispositivos.</span><span class="sxs-lookup"><span data-stu-id="728de-124">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="728de-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="728de-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="728de-126">Blog de dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="728de-126">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

