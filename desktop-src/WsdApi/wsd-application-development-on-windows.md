---
description: Aprenda a usar microsoft Web Services on Devices API (WSD) API (WSDAPI) para implementar servicios y dispositivos controlados por el cliente, y hosts de dispositivos conformes a DPWS.
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desarrollo de aplicaciones WSD en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 167cd1ad013ea387a6e33b6de449f3f84d49db13
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405788"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="1c292-103">Desarrollo de aplicaciones WSD en Windows</span><span class="sxs-lookup"><span data-stu-id="1c292-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="1c292-104">Microsoft Web Services on Devices API (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y hosts de dispositivos que se ajustan al perfil de dispositivos para servicios [web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="1c292-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="1c292-105">WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servidor (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="1c292-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="1c292-106">A menudo, el código WSDAPI para estas aplicaciones se genera mediante [WsdCodeGen](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="1c292-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="1c292-107">Algunas funciones y métodos de WSDAPI están diseñados para ser llamados solo por código generado.</span><span class="sxs-lookup"><span data-stu-id="1c292-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="1c292-108">La documentación de referencia de API indica cuándo se debe usar o implementar una función o un método solo mediante código generado.</span><span class="sxs-lookup"><span data-stu-id="1c292-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="1c292-109">El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración WsdCodeGen y código generado.</span><span class="sxs-lookup"><span data-stu-id="1c292-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="1c292-110">Para obtener más información, vea [Ejemplos de WSDAPI.](wsdapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="1c292-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="1c292-111">Si desea enumerar los dispositivos mediante el protocolo WSD y consultar los metadatos del dispositivo WSD, puede usar function [discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API en su lugar.</span><span class="sxs-lookup"><span data-stu-id="1c292-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="1c292-112">Si desea implementar un dispositivo WSD que no ejecute Windows, consulte [Desarrollo de dispositivos WSD.](wsd-device-development.md)</span><span class="sxs-lookup"><span data-stu-id="1c292-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
