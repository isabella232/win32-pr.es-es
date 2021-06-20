---
description: Obtenga información sobre cómo implementar servicios web en dispositivos (WSD). Comprenda su propósito, cuando sea aplicable, el público desarrollador y los requisitos en tiempo de ejecución.
ms.assetid: 590e0b0b-763c-44fb-a49f-606415f57b26
title: Servicios web en dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 267f8dba0fd56c383dd3cecabb3c00959aa0d90c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405758"
---
# <a name="web-services-on-devices"></a><span data-ttu-id="6fb00-104">Servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="6fb00-104">Web Services on Devices</span></span>

## <a name="purpose"></a><span data-ttu-id="6fb00-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="6fb00-105">Purpose</span></span>

<span data-ttu-id="6fb00-106">Microsoft Web Services on Devices API (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y hosts de dispositivos que se ajustan al perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="6fb00-106">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="6fb00-107">WSDAPI usa [WS-Discovery para](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) la detección de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6fb00-107">WSDAPI uses [WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf) for device discovery.</span></span>

<span data-ttu-id="6fb00-108">WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servicio.</span><span class="sxs-lookup"><span data-stu-id="6fb00-108">WSDAPI may be used for the development of both client and service implementations.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6fb00-109">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="6fb00-109">Where applicable</span></span>

<span data-ttu-id="6fb00-110">Servicios web en dispositivos permite que un cliente detecte y acceda a un dispositivo remoto y sus servicios asociados a través de una red.</span><span class="sxs-lookup"><span data-stu-id="6fb00-110">Web Services on Devices allows a client to discover and access a remote device and its associated services across a network.</span></span> <span data-ttu-id="6fb00-111">Admite la detección, descripción, control y eventos de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6fb00-111">It supports device discovery, description, control, and eventing.</span></span> <span data-ttu-id="6fb00-112">Los desarrolladores pueden crear servidores proxy de cliente de WSDAPI y los códigos auxiliares correspondientes para los hosts de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6fb00-112">Developers can create WSDAPI client proxies and corresponding stubs for device hosts.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6fb00-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="6fb00-113">Developer audience</span></span>

<span data-ttu-id="6fb00-114">La documentación de Servicios web en dispositivos está pensada para programadores de C/C++ y proveedores de dispositivos que crean productos compatibles con DPWS.</span><span class="sxs-lookup"><span data-stu-id="6fb00-114">The Web Services on Devices documentation is intended for C/C++ programmers and device vendors creating DPWS-compliant products.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6fb00-115">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="6fb00-115">Run-time requirements</span></span>

<span data-ttu-id="6fb00-116">Las aplicaciones cliente que usan WSDAPI se admiten a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="6fb00-116">Client applications that use WSDAPI are supported starting with Windows Vista and Windows Server 2008.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6fb00-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="6fb00-117">In this section</span></span>



| <span data-ttu-id="6fb00-118">Tema</span><span class="sxs-lookup"><span data-stu-id="6fb00-118">Topic</span></span>                                                                                  | <span data-ttu-id="6fb00-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="6fb00-119">Description</span></span>                                                                                  |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fb00-120">Acerca de los servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="6fb00-120">About Web Services on Devices</span></span>](about-web-services-for-devices.md)<br/>         | <span data-ttu-id="6fb00-121">Arquitectura e información general sobre servicios web en dispositivos.</span><span class="sxs-lookup"><span data-stu-id="6fb00-121">Architectural and general information about Web Services on Devices.</span></span><br/>              |
| [<span data-ttu-id="6fb00-122">Uso de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="6fb00-122">Using Web Services on Devices</span></span>](using-web-services-on-devices.md)<br/>          | <span data-ttu-id="6fb00-123">Información sobre la generación de código, la configuración de aplicaciones y la solución de problemas.</span><span class="sxs-lookup"><span data-stu-id="6fb00-123">Information about generating code, configuring applications, and troubleshooting.</span></span><br/> |
| [<span data-ttu-id="6fb00-124">Referencia de servicios web en dispositivos</span><span class="sxs-lookup"><span data-stu-id="6fb00-124">Web Services on Devices Reference</span></span>](web-services-for-devices-reference.md)<br/> | <span data-ttu-id="6fb00-125">Documentación de referencia de Web Services on Devices API.</span><span class="sxs-lookup"><span data-stu-id="6fb00-125">Reference documentation for the Web Services on Devices API.</span></span><br/>                      |



 

## <a name="related-topics"></a><span data-ttu-id="6fb00-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6fb00-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6fb00-127">Blog de Dan Driscoll</span><span class="sxs-lookup"><span data-stu-id="6fb00-127">Dan Driscoll's Blog</span></span>](/archive/blogs/dandris/)
</dt> </dl>

 

