---
title: Acerca de Bluetooth
description: Bluetooth es un protocolo estándar del sector que habilita la conectividad inalámbrica para una multitud de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos de mano.
ms.assetid: 424168a1-e55c-4947-9a80-8594b4d83bbd
keywords:
- Bluetooth Bluetooth, descrito
- Bluetooth Bluetooth, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b704bb3245adcd75948f7f9fbb411697c7c45f0
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077363"
---
# <a name="about-bluetooth"></a><span data-ttu-id="bd341-105">Acerca de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="bd341-105">About Bluetooth</span></span>

<span data-ttu-id="bd341-106">Bluetooth es un protocolo estándar del sector que habilita la conectividad inalámbrica para una multitud de dispositivos, incluidos equipos, impresoras, teléfonos móviles y dispositivos de mano.</span><span class="sxs-lookup"><span data-stu-id="bd341-106">Bluetooth is an industry-standard protocol that enables wireless connectivity for a multitude of devices, including computers, printers, mobile phones, and handheld devices.</span></span>

<span data-ttu-id="bd341-107">Las características clave de Bluetooth incluyen:</span><span class="sxs-lookup"><span data-stu-id="bd341-107">Key Bluetooth features include:</span></span>

-   <span data-ttu-id="bd341-108">Un protocolo inalámbrico de bajo coste y bajo consumo de energía con soporte técnico estándar del sector y aceptación mundial.</span><span class="sxs-lookup"><span data-stu-id="bd341-108">A low-cost, low-power consumption wireless protocol with industry-standard support and worldwide acceptance.</span></span>
-   <span data-ttu-id="bd341-109">Una interfaz de programación definida y familiar que los desarrolladores pueden usar para desarrollar o migrar aplicaciones rápidamente.</span><span class="sxs-lookup"><span data-stu-id="bd341-109">A defined and familiar programming interface that developers can use to quickly develop or port applications.</span></span>
-   <span data-ttu-id="bd341-110">Un sitio web oficial y una organización cooperativa en todo el sector que explica, promueve y normaliza la tecnología Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bd341-110">An official Web site and an industry-wide cooperative organization that explains, promotes, and standardizes Bluetooth technology.</span></span> <span data-ttu-id="bd341-111">Para obtener más información, vea [www.Bluetooth.com](https://www.bluetooth.com/).</span><span class="sxs-lookup"><span data-stu-id="bd341-111">For more information, see [www.bluetooth.com](https://www.bluetooth.com/).</span></span>

<span data-ttu-id="bd341-112">Bluetooth en Windows proporciona servicios principales que son similares a los expuestos por el protocolo de control de transmisión (la parte TCP de TCP/IP).</span><span class="sxs-lookup"><span data-stu-id="bd341-112">Bluetooth on Windows provides core services that are similar to those exposed by Transmission Control Protocol (the TCP part of TCP/IP).</span></span> <span data-ttu-id="bd341-113">Como muchos protocolos y servicios de red, la conectividad Bluetooth y la transferencia de datos se programan a través de llamadas a funciones de Windows Sockets, mediante las técnicas de programación de Windows Sockets comunes y las extensiones de Bluetooth específicas.</span><span class="sxs-lookup"><span data-stu-id="bd341-113">Like many networking protocols and services, Bluetooth connectivity and data transfer are programmed through Windows Sockets function calls, using common Windows Sockets programming techniques and specific Bluetooth extensions.</span></span> <span data-ttu-id="bd341-114">Sin embargo, dado que existen diferencias significativas entre una red cableada, fija y una red ad hoc inalámbrica, Bluetooth proporciona extensiones como detección de servicio/dispositivo y notificación que permiten que las aplicaciones funcionen correctamente en el entorno inalámbrico.</span><span class="sxs-lookup"><span data-stu-id="bd341-114">However, because significant differences exist between a wired, fixed network and a wireless ad-hoc network, Bluetooth provides extensions such as service/device discovery and notification that enable applications to operate properly in the wireless environment.</span></span> <span data-ttu-id="bd341-115">Estas extensiones también disponen de la forma de portabilidad simple a tecnologías similares, como IrDA, o transportes inalámbricos futuros.</span><span class="sxs-lookup"><span data-stu-id="bd341-115">These extensions also pave the way for simple porting to similar technologies, such as IrDA, or future wireless transports.</span></span>

<span data-ttu-id="bd341-116">Microsoft ofrece compatibilidad con Bluetooth en Windows XP con Service Pack 1 (SP1) y versiones posteriores, en Windows XP Embedded con Service Pack 2 y en Windows CE.</span><span class="sxs-lookup"><span data-stu-id="bd341-116">Microsoft provides support for Bluetooth on Windows XP with Service Pack 1 (SP1) and later, on Windows XP Embedded with Service Pack 2, and on Windows CE.</span></span> <span data-ttu-id="bd341-117">Las aplicaciones Bluetooth que se ejecutan en Windows XP deben poder ejecutarse en una imagen de tiempo de ejecución basada en Windows XP Embedded que incluye las dependencias requeridas.</span><span class="sxs-lookup"><span data-stu-id="bd341-117">Bluetooth applications that run on Windows XP should be able to run on a Windows XP Embedded-based run-time image that includes the required dependencies.</span></span> <span data-ttu-id="bd341-118">Para obtener más información acerca de Windows XP Embedded, consulte la documentación de la ayuda de Windows XP Embedded en MSDN.</span><span class="sxs-lookup"><span data-stu-id="bd341-118">For more information about Windows XP Embedded, see the Windows XP Embedded Help documentation on MSDN.</span></span> <span data-ttu-id="bd341-119">Para obtener más información acerca de la programación de Windows CE, consulte el SDK de Windows CE.</span><span class="sxs-lookup"><span data-stu-id="bd341-119">For more information about Windows CE programming, consult the Windows CE SDK.</span></span>

<span data-ttu-id="bd341-120">Microsoft proporciona dos métodos para programar Bluetooth en Windows:</span><span class="sxs-lookup"><span data-stu-id="bd341-120">Microsoft provides two approaches for programming Bluetooth on Windows:</span></span>

-   <span data-ttu-id="bd341-121">Usar la interfaz de Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="bd341-121">Using the Windows Sockets interface</span></span>
-   <span data-ttu-id="bd341-122">Administración directa de dispositivos mediante interfaces Bluetooth que no son de socket</span><span class="sxs-lookup"><span data-stu-id="bd341-122">Managing devices directly by using nonsocket Bluetooth interfaces</span></span>

<span data-ttu-id="bd341-123">En esta sección se proporciona información general sobre ambos enfoques en los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="bd341-123">This section provides overview information about both of these approaches in the following topics.</span></span> <span data-ttu-id="bd341-124">Para obtener más información sobre el uso de elementos de la API de Windows Sockets para programar Bluetooth, consulte [programación de Bluetooth con Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="bd341-124">For more information about using Windows Sockets API elements to program Bluetooth, see [Bluetooth Programming with Windows Sockets](bluetooth-programming-with-windows-sockets.md).</span></span>



| <span data-ttu-id="bd341-125">Sección</span><span class="sxs-lookup"><span data-stu-id="bd341-125">Section</span></span>                                                                                | <span data-ttu-id="bd341-126">Contenido</span><span class="sxs-lookup"><span data-stu-id="bd341-126">Content</span></span>                                                           |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="bd341-127">Compatibilidad de Windows Sockets con Bluetooth</span><span class="sxs-lookup"><span data-stu-id="bd341-127">Windows Sockets Support for Bluetooth</span></span>](windows-sockets-support-for-bluetooth.md)     | <span data-ttu-id="bd341-128">Describe la relación entre Bluetooth y Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="bd341-128">Describes the relationship between Bluetooth and Windows Sockets.</span></span> |
| [<span data-ttu-id="bd341-129">Administración de dispositivos y servicios Bluetooth</span><span class="sxs-lookup"><span data-stu-id="bd341-129">Managing Bluetooth Devices and Services</span></span>](managing-bluetooth-devices-and-services.md) | <span data-ttu-id="bd341-130">Describe cómo administrar dispositivos y servicios Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="bd341-130">Describes how to manage Bluetooth devices and services.</span></span>           |



 

 

 




