---
title: API de UPnP
description: El entorno UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y PC.
ms.assetid: 1dc05d6e-19ae-45e2-82c2-d3b63b16bf9d
keywords:
- UPnP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022ede01a62230194969d7789e0ace70f960debb
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "104149705"
---
# <a name="upnp-apis"></a><span data-ttu-id="fa0df-104">API de UPnP</span><span class="sxs-lookup"><span data-stu-id="fa0df-104">UPnP APIs</span></span>

## <a name="purpose"></a><span data-ttu-id="fa0df-105">Propósito</span><span class="sxs-lookup"><span data-stu-id="fa0df-105">Purpose</span></span>

<span data-ttu-id="fa0df-106">El entorno UPnP permite redes dinámicas de dispositivos inteligentes, dispositivos inalámbricos y PC.</span><span class="sxs-lookup"><span data-stu-id="fa0df-106">The UPnP  framework enables dynamic networking of intelligent appliances, wireless devices, and PCs.</span></span> <span data-ttu-id="fa0df-107">Existen dos API para trabajar con dispositivos certificados con UPnP:</span><span class="sxs-lookup"><span data-stu-id="fa0df-107">There are two APIs for working with UPnP-certified devices:</span></span>

-   <span data-ttu-id="fa0df-108">La API de punto de control, que consta de un conjunto de interfaces COM que se usan para buscar y controlar dispositivos.</span><span class="sxs-lookup"><span data-stu-id="fa0df-108">The Control Point API, which consists of a set of COM interfaces used to find and control devices.</span></span>
-   <span data-ttu-id="fa0df-109">La API del host del dispositivo, que consta de un conjunto de interfaces COM que se usan para implementar dispositivos hospedados por un equipo.</span><span class="sxs-lookup"><span data-stu-id="fa0df-109">The Device Host API, which consists of a set of COM interfaces used to implement devices that are hosted by a computer.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="fa0df-110">Donde sea aplicable</span><span class="sxs-lookup"><span data-stu-id="fa0df-110">Where applicable</span></span>

<span data-ttu-id="fa0df-111">La API de punto de control permite a los desarrolladores escribir aplicaciones que busquen y controlen dispositivos certificados para UPnP.</span><span class="sxs-lookup"><span data-stu-id="fa0df-111">The Control Point API enables developers to write applications that search for and control UPnP-certified devices.</span></span> <span data-ttu-id="fa0df-112">La API del host del dispositivo permite a los desarrolladores implementar la funcionalidad de los dispositivos certificados con UPnP y usar el host del dispositivo para administrar las funciones de detección, descripción, control, presentación y eventos de un dispositivo certificado con UPnP.</span><span class="sxs-lookup"><span data-stu-id="fa0df-112">The Device Host API enables developers to implement the functionality of UPnP-certified devices, and use the device host to manage the discovery, description, control, presentation, and eventing functions of a UPnP-certified device.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="fa0df-113">Audiencia de desarrolladores</span><span class="sxs-lookup"><span data-stu-id="fa0df-113">Developer audience</span></span>

<span data-ttu-id="fa0df-114">Los desarrolladores que usan las API del punto de control y las API de host del dispositivo deben estar familiarizados con la arquitectura del dispositivo UPnP.</span><span class="sxs-lookup"><span data-stu-id="fa0df-114">Developers using the Control Point APIs and Device Host APIs must be familiar with the UPnP device architecture.</span></span> <span data-ttu-id="fa0df-115">Para obtener más información, consulte la [documentación de implementación de UPnP](https://openconnectivity.org/resources/upnpresources.zip) y el foro de [UPnP](https://openconnectivity.org/).</span><span class="sxs-lookup"><span data-stu-id="fa0df-115">For more information, see the [UPnP Implementation Documentation](https://openconnectivity.org/resources/upnpresources.zip) and the [UPnP Forum](https://openconnectivity.org/).</span></span>

<span data-ttu-id="fa0df-116">Los desarrolladores que usan las API de host del dispositivo deben estar familiarizados con las interfaces de Active Template Library (ATL) y COM.</span><span class="sxs-lookup"><span data-stu-id="fa0df-116">Developers who are using the Device Host APIs should be familiar with the Active Template Library (ATL) and COM interfaces.</span></span>

<span data-ttu-id="fa0df-117">Las API de punto de control y las API de host de dispositivo se usan en una gran variedad de aplicaciones, desde scripts incrustados en páginas HTML hasta programas de C++ y Microsoft Visual Basic completos.</span><span class="sxs-lookup"><span data-stu-id="fa0df-117">The Control Point APIs and Device Host APIs are used by a variety of applications, from scripts embedded in HTML pages to full-fledged C++ and Microsoft Visual Basic programs.</span></span>

<span data-ttu-id="fa0df-118">Solo la API del punto de control admite Visual Basic Scripting Edition (VBScript).</span><span class="sxs-lookup"><span data-stu-id="fa0df-118">Only the Control Point API supports Visual Basic Scripting Edition (VBScript).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="fa0df-119">Requisitos de tiempo de ejecución</span><span class="sxs-lookup"><span data-stu-id="fa0df-119">Run-time requirements</span></span>

<span data-ttu-id="fa0df-120">La API de punto de control se usa en equipos que ejecutan Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional y Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="fa0df-120">The Control Point API is used on computers running Microsoft Windows Millennium Edition, Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="fa0df-121">La API del host del dispositivo se usa en equipos que ejecutan Windows XP, Windows XP Professional y Windows CE .NET.</span><span class="sxs-lookup"><span data-stu-id="fa0df-121">The Device Host API is used on computers running Windows XP, Windows XP Professional, and Windows CE .NET.</span></span>

<span data-ttu-id="fa0df-122">Para obtener información más específica acerca de los sistemas operativos que admiten una función determinada, consulte "requisitos" en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="fa0df-122">For more specific information about which operating systems support a particular function, refer to "Requirements" in the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="fa0df-123">En esta sección</span><span class="sxs-lookup"><span data-stu-id="fa0df-123">In this section</span></span>



| <span data-ttu-id="fa0df-124">Tema</span><span class="sxs-lookup"><span data-stu-id="fa0df-124">Topic</span></span>                                                                                          | <span data-ttu-id="fa0df-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa0df-125">Description</span></span>                                                                                        |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa0df-126">Información general sobre la arquitectura de UPnP</span><span class="sxs-lookup"><span data-stu-id="fa0df-126">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)<br/>            | <span data-ttu-id="fa0df-127">Información general y fondo.</span><span class="sxs-lookup"><span data-stu-id="fa0df-127">General information and background.</span></span><br/>                                                     |
| [<span data-ttu-id="fa0df-128">Información general sobre puntos de control</span><span class="sxs-lookup"><span data-stu-id="fa0df-128">Control Point Overview</span></span>](control-point-api.md)<br/>                                     | <span data-ttu-id="fa0df-129">Información general sobre la API de punto de control.</span><span class="sxs-lookup"><span data-stu-id="fa0df-129">General information about the Control Point API.</span></span><br/>                                        |
| [<span data-ttu-id="fa0df-130">Uso de la API de punto de control</span><span class="sxs-lookup"><span data-stu-id="fa0df-130">Using the Control Point API</span></span>](using-the-control-point-api-with-upnp-technology.md)<br/> | <span data-ttu-id="fa0df-131">Código de ejemplo que muestra cómo desarrollar aplicaciones que controlan dispositivos certificados para UPnP.</span><span class="sxs-lookup"><span data-stu-id="fa0df-131">Sample code that shows how to develop applications that control UPnP-certified devices.</span></span><br/> |
| [<span data-ttu-id="fa0df-132">Referencia de API de punto de control</span><span class="sxs-lookup"><span data-stu-id="fa0df-132">Control Point API Reference</span></span>](control-point-api-with-upnp-technology-reference.md)<br/> | <span data-ttu-id="fa0df-133">Documentación de interfaces, métodos y eventos de componentes de punto de control.</span><span class="sxs-lookup"><span data-stu-id="fa0df-133">Documentation of Control Point component interfaces, methods, and events.</span></span><br/>               |
| [<span data-ttu-id="fa0df-134">Introducción a la API de host de dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa0df-134">Device Host API Overview</span></span>](device-host-api.md)<br/>                                     | <span data-ttu-id="fa0df-135">Información general sobre la API del host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa0df-135">General information about the Device Host API.</span></span><br/>                                          |
| [<span data-ttu-id="fa0df-136">Uso de la API del host del dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa0df-136">Using the Device Host API</span></span>](using-the-device-host-api-with-upnp-technology.md)<br/>     | <span data-ttu-id="fa0df-137">Código de ejemplo que muestra cómo desarrollar una aplicación para dispositivos certificados para UPnP.</span><span class="sxs-lookup"><span data-stu-id="fa0df-137">Sample code that shows how to develop an application for UPnP-certified devices.</span></span><br/>        |
| [<span data-ttu-id="fa0df-138">Referencia de API de host de dispositivo</span><span class="sxs-lookup"><span data-stu-id="fa0df-138">Device Host API Reference</span></span>](device-host-api-with-upnp-technology-reference.md)<br/>     | <span data-ttu-id="fa0df-139">Documentación de interfaces, métodos y eventos del componente host del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fa0df-139">Documentation of Device Host component interfaces, methods, and events.</span></span><br/>                 |



 

 

 





