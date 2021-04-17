---
description: La interfaz de adquisición de imágenes de Windows (WIA) es una API y una interfaz de controlador de dispositivo (DDI).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Acerca de la adquisición de imágenes de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105716063"
---
# <a name="about-windows-image-acquisition"></a><span data-ttu-id="5aedc-103">Acerca de la adquisición de imágenes de Windows</span><span class="sxs-lookup"><span data-stu-id="5aedc-103">About Windows Image Acquisition</span></span>

<span data-ttu-id="5aedc-104">La interfaz de adquisición de imágenes de Windows (WIA) es una API y una interfaz de controlador de dispositivo (DDI).</span><span class="sxs-lookup"><span data-stu-id="5aedc-104">The Windows Image Acquisition (WIA) interface is both an API and a device driver interface (DDI).</span></span> <span data-ttu-id="5aedc-105">La API de WIA está diseñada para permitir a las aplicaciones:</span><span class="sxs-lookup"><span data-stu-id="5aedc-105">The WIA API is designed to allow applications to:</span></span>

-   <span data-ttu-id="5aedc-106">Ejecutarse en un entorno sólido y estable.</span><span class="sxs-lookup"><span data-stu-id="5aedc-106">Run in a robust and stable environment.</span></span>
-   <span data-ttu-id="5aedc-107">Minimice los problemas de interoperabilidad.</span><span class="sxs-lookup"><span data-stu-id="5aedc-107">Minimize interoperability problems.</span></span>
-   <span data-ttu-id="5aedc-108">Enumera los dispositivos de adquisición de imágenes disponibles.</span><span class="sxs-lookup"><span data-stu-id="5aedc-108">Enumerate available image acquisition devices.</span></span>
-   <span data-ttu-id="5aedc-109">Cree conexiones a varios dispositivos simultáneamente.</span><span class="sxs-lookup"><span data-stu-id="5aedc-109">Create connections to multiple devices simultaneously.</span></span>
-   <span data-ttu-id="5aedc-110">Consultar las propiedades de los dispositivos de forma estándar y ampliable.</span><span class="sxs-lookup"><span data-stu-id="5aedc-110">Query properties of devices in a standard and expandable manner.</span></span>
-   <span data-ttu-id="5aedc-111">Adquirir datos del dispositivo mediante mecanismos de transferencia estándar y de alto rendimiento.</span><span class="sxs-lookup"><span data-stu-id="5aedc-111">Acquire device data using standard and high performance transfer mechanisms.</span></span>
-   <span data-ttu-id="5aedc-112">Mantener las propiedades de la imagen entre las transferencias de datos.</span><span class="sxs-lookup"><span data-stu-id="5aedc-112">Maintain image properties across data transfers.</span></span>
-   <span data-ttu-id="5aedc-113">Recibir una notificación de una amplia variedad de eventos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5aedc-113">Be notified of a wide variety of device events.</span></span>

<span data-ttu-id="5aedc-114">WIADDI está diseñado para minimizar la cantidad de código que un proveedor de hardware debe escribir, a la vez que mantiene la flexibilidad de crear soluciones individuales.</span><span class="sxs-lookup"><span data-stu-id="5aedc-114">The WIADDI is designed to minimize the amount of code a hardware vendor must write, while maintaining the flexibility to craft individual solutions.</span></span> <span data-ttu-id="5aedc-115">Esto se logra mediante:</span><span class="sxs-lookup"><span data-stu-id="5aedc-115">This is accomplished by:</span></span>

-   <span data-ttu-id="5aedc-116">Proporcionar una biblioteca de servicio de dispositivo estándar que realiza la mayoría de las operaciones de controlador.</span><span class="sxs-lookup"><span data-stu-id="5aedc-116">Providing a standard device service library that performs most driver operations.</span></span>
-   <span data-ttu-id="5aedc-117">Promoción de los estándares de comunicación de dispositivos de la industria para que un controlador WIA admita la mayoría de los dispositivos WIA.</span><span class="sxs-lookup"><span data-stu-id="5aedc-117">Promoting industry device communications standards so that one WIA driver supports most WIA devices.</span></span> <span data-ttu-id="5aedc-118">Por ejemplo, el protocolo de transferencia de imágenes (PTP).</span><span class="sxs-lookup"><span data-stu-id="5aedc-118">For example, Picture Transfer Protocol (PTP).</span></span>
-   <span data-ttu-id="5aedc-119">Permite que el controlador de dispositivo admita interfaces personalizadas, pero no requiere que use la biblioteca de servicio de dispositivo estándar.</span><span class="sxs-lookup"><span data-stu-id="5aedc-119">Allowing the device driver to support custom interfaces, while not requiring that it use the standard device service library.</span></span> <span data-ttu-id="5aedc-120">Sin embargo, los controladores todavía necesitan implementar las interfaces estándar de WIA.</span><span class="sxs-lookup"><span data-stu-id="5aedc-120">However, drivers still need to implement the standard WIA interfaces.</span></span>

<span data-ttu-id="5aedc-121">En esta sección se presenta una breve introducción a la interfaz WIA en las siguientes áreas:</span><span class="sxs-lookup"><span data-stu-id="5aedc-121">This section presents a brief overview of the WIA interface in the following areas:</span></span>

-   [<span data-ttu-id="5aedc-122">Arquitectura WIA</span><span class="sxs-lookup"><span data-stu-id="5aedc-122">WIA Architecture</span></span>](-wia-wia-architecture.md)
-   [<span data-ttu-id="5aedc-123">Compatibilidad de STI</span><span class="sxs-lookup"><span data-stu-id="5aedc-123">STI Compatibility</span></span>](-wia-sti-compatibility.md)
-   [<span data-ttu-id="5aedc-124">Compatibilidad con TWAIN</span><span class="sxs-lookup"><span data-stu-id="5aedc-124">TWAIN Compatibility</span></span>](-wia-twain-compatibility.md)
-   [<span data-ttu-id="5aedc-125">Administrador de dispositivos WIA</span><span class="sxs-lookup"><span data-stu-id="5aedc-125">WIA Device Manager</span></span>](-wia-wia-device-manager.md)
-   [<span data-ttu-id="5aedc-126">Biblioteca de servicio minicontrolador de WIA</span><span class="sxs-lookup"><span data-stu-id="5aedc-126">WIA Minidriver Service Library</span></span>](-wia-wia-minidriver-service-library.md)
-   [<span data-ttu-id="5aedc-127">Minicontrolador WIA</span><span class="sxs-lookup"><span data-stu-id="5aedc-127">WIA Minidriver</span></span>](-wia-wia-minidriver.md)

 

 



