---
description: Introducción a la arquitectura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Introducción a la arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912889"
---
# <a name="architecture-overview"></a><span data-ttu-id="8fff1-103">Introducción a la arquitectura</span><span class="sxs-lookup"><span data-stu-id="8fff1-103">Architecture Overview</span></span>

<span data-ttu-id="8fff1-104">La arquitectura de WPD puede dividirse en tres procesos.</span><span class="sxs-lookup"><span data-stu-id="8fff1-104">The WPD architecture can be divided into three processes.</span></span> <span data-ttu-id="8fff1-105">Dentro de estos procesos se encuentran los tres componentes principales de WPD: la API, el serializador y el controlador.</span><span class="sxs-lookup"><span data-stu-id="8fff1-105">Within these processes are the three primary components of WPD: the API, the serializer, and the driver.</span></span> <span data-ttu-id="8fff1-106">En la ilustración siguiente se muestran los procesos y los componentes que constituyen la arquitectura de WPD.</span><span class="sxs-lookup"><span data-stu-id="8fff1-106">The following illustration depicts the processes and components that constitute the WPD architecture.</span></span>

![Ilustración en la que se muestran los componentes de API, serializador y controlador de WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a><span data-ttu-id="8fff1-108">La interfaz de programación de aplicaciones de WPD</span><span class="sxs-lookup"><span data-stu-id="8fff1-108">The WPD Application Programming Interface</span></span>

<span data-ttu-id="8fff1-109">La API de WPD se implementa como un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="8fff1-109">The WPD API is implemented as an in-proc COM server.</span></span> <span data-ttu-id="8fff1-110">La API usa las API estándar de Microsoft Win32 para comunicarse con el controlador de WPD adecuado.</span><span class="sxs-lookup"><span data-stu-id="8fff1-110">The API uses standard Microsoft Win32 APIs to communicate with the appropriate WPD driver.</span></span> <span data-ttu-id="8fff1-111">Un componente denominado serializador de WPD lo usan los objetos de la API y el controlador para empaquetar o desempaquetar los parámetros de los búferes del marco de trabajo de controladores de modo de usuario (UMDF) de Windows Driver Foundation (WDF).</span><span class="sxs-lookup"><span data-stu-id="8fff1-111">A component called the WPD serializer is used by both API objects and the driver to pack or unpack parameters to or from Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) buffers.</span></span>

## <a name="the-wpd-serializer"></a><span data-ttu-id="8fff1-112">El serializador de WPD</span><span class="sxs-lookup"><span data-stu-id="8fff1-112">The WPD Serializer</span></span>

<span data-ttu-id="8fff1-113">El serializador de WPD se implementa como un servidor COM en proceso.</span><span class="sxs-lookup"><span data-stu-id="8fff1-113">The WPD serializer is implemented as an in-proc COM server.</span></span> <span data-ttu-id="8fff1-114">La API de WPD usa el serializador para empaquetar comandos y parámetros en los búferes de mensajes que se envían al controlador.</span><span class="sxs-lookup"><span data-stu-id="8fff1-114">The WPD API uses the serializer to pack commands and parameters into message buffers that are sent to the driver.</span></span> <span data-ttu-id="8fff1-115">El controlador usa el serializador para desempaquetar estos búferes de mensajes para su procesamiento.</span><span class="sxs-lookup"><span data-stu-id="8fff1-115">The driver uses the serializer to unpack these message buffers for processing.</span></span> <span data-ttu-id="8fff1-116">El controlador también usa el serializador para empaquetar datos y parámetros en búferes de respuesta que se devuelven a la API de WPD, y la API de WPD usa el serializador para desempaquetar estos búferes de respuesta y volver a los llamadores.</span><span class="sxs-lookup"><span data-stu-id="8fff1-116">The driver also uses the serializer to pack data and parameters into response buffers that are returned to the WPD API, and the WPD API uses the serializer to unpack these response buffers to return to callers.</span></span>

## <a name="wpd-driver"></a><span data-ttu-id="8fff1-117">Controlador de WPD</span><span class="sxs-lookup"><span data-stu-id="8fff1-117">WPD Driver</span></span>

<span data-ttu-id="8fff1-118">El controlador WPD se implementa como un controlador estándar de controlador de modo de usuario (UMDF) de Windows Driver Foundation (WDF).</span><span class="sxs-lookup"><span data-stu-id="8fff1-118">The WPD driver is implemented as a standard Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) driver.</span></span> <span data-ttu-id="8fff1-119">Los controladores de WPD se hospedan en UMDF en un proceso independiente denominado host de controlador.</span><span class="sxs-lookup"><span data-stu-id="8fff1-119">WPD drivers are hosted by UMDF in a separate process called the Driver Host.</span></span>

<span data-ttu-id="8fff1-120">El controlador recibe mensajes desde el reflector UMDF (esto no se muestra en el diagrama, ya que el modo en que se reciben los búferes no es importante para el controlador).</span><span class="sxs-lookup"><span data-stu-id="8fff1-120">The driver receives messages from the UMDF reflector (this is not shown in the diagram, since how the buffers are received is not important to the driver.</span></span> <span data-ttu-id="8fff1-121">Consulte la documentación de UMDF para obtener más información).</span><span class="sxs-lookup"><span data-stu-id="8fff1-121">See UMDF documentation for more information).</span></span> <span data-ttu-id="8fff1-122">El controlador implementa un controlador de código de control de e/s (IOCL) específico de WPD para procesar los mensajes de WPD recibidos por la API de WPD.</span><span class="sxs-lookup"><span data-stu-id="8fff1-122">The driver implements a WPD-specific I/O Control code (IOCL) handler to process WPD messages received by the WPD API.</span></span> <span data-ttu-id="8fff1-123">El controlador usa el serializador de WPD para desempaquetar los comandos y parámetros de estos búferes de mensajes y para empaquetar la respuesta en el búfer de retorno.</span><span class="sxs-lookup"><span data-stu-id="8fff1-123">The driver uses the WPD serializer to unpack commands and parameters from these message buffers, and to pack the response into the return buffer.</span></span>

<span data-ttu-id="8fff1-124">Los controladores de WPD pueden comunicarse con sus dispositivos pasando por un controlador de modo kernel, al que normalmente se tiene acceso a través de operaciones de archivo Win32 (es decir, CreateFile, ReadFile, WriteFile, etc.).</span><span class="sxs-lookup"><span data-stu-id="8fff1-124">WPD drivers may communicate with their devices by going through a kernel-mode driver, typically accessed via Win32 file operations (that is, CreateFile, ReadFile, WriteFile, and so on).</span></span> <span data-ttu-id="8fff1-125">En el caso de los buses comunes, Microsoft proporcionará controladores de kernel estándar para que los usen los proveedores, lo que permitirá a los proveedores enviar una solución de controladores solo en modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="8fff1-125">For the common buses, Microsoft will provide standard kernel drivers for vendors to use, which will allow vendors to ship a user-mode-only driver solution.</span></span> <span data-ttu-id="8fff1-126">Además, en el caso de los dispositivos de protocolo de transferencia de medios (MTP) y de clase de almacenamiento masivo (MSC), Microsoft proporcionará controladores de clase de WPD.</span><span class="sxs-lookup"><span data-stu-id="8fff1-126">In addition, for Media Transfer Protocol (MTP) and Mass Storage Class (MSC) devices, Microsoft will provide WPD class drivers.</span></span>

<span data-ttu-id="8fff1-127">Para obtener más información acerca de los controladores de WPD, consulte la documentación del controlador de dispositivos portátiles de Windows en el kit de controladores de Windows.</span><span class="sxs-lookup"><span data-stu-id="8fff1-127">For more information about WPD drivers, see the Windows Portable Devices Driver documentation in the Windows Driver Kit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8fff1-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8fff1-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8fff1-129">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="8fff1-129">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



