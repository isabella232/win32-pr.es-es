---
description: La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al perfil de dispositivos para servicios web (DPWS).
ms.assetid: 88de8dea-56d5-4bfc-8837-03da81b7d0f9
title: Desarrollo de aplicaciones WSD en Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e33976a1903c87ffb6c577cd5a451a3b772a67a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716123"
---
# <a name="wsd-application-development-on-windows"></a><span data-ttu-id="ce107-103">Desarrollo de aplicaciones WSD en Windows</span><span class="sxs-lookup"><span data-stu-id="ce107-103">WSD Application Development on Windows</span></span>

<span data-ttu-id="ce107-104">La API de servicios Web de Microsoft en dispositivos (WSDAPI) admite la implementación de dispositivos y servicios controlados por el cliente, y los hosts de dispositivo que se ajustan al [Perfil de dispositivos para servicios web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span><span class="sxs-lookup"><span data-stu-id="ce107-104">The Microsoft Web Services on Devices API (WSDAPI) supports the implementation of client-controlled devices and services, and device hosts conforming to the [Devices Profile for Web Services](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS).</span></span> <span data-ttu-id="ce107-105">WSDAPI se puede usar para el desarrollo de implementaciones de cliente y servidor (dispositivo).</span><span class="sxs-lookup"><span data-stu-id="ce107-105">WSDAPI may be used for the development of both client and server (device) implementations.</span></span>

<span data-ttu-id="ce107-106">Con bastante frecuencia, el código de WSDAPI para estas aplicaciones se genera mediante [WsdCodeGen](web-services-for-devices-code-generator.md).</span><span class="sxs-lookup"><span data-stu-id="ce107-106">Quite often, WSDAPI code for these applications is generated using [WsdCodeGen](web-services-for-devices-code-generator.md).</span></span> <span data-ttu-id="ce107-107">Algunas funciones y métodos WSDAPI están diseñados para ser llamados únicamente por parte del código generado.</span><span class="sxs-lookup"><span data-stu-id="ce107-107">Some WSDAPI functions and methods are intended to be called only by generated code.</span></span> <span data-ttu-id="ce107-108">La documentación de referencia de la API indica cuándo debe usarse o implementarse una función o un método solo por código generado.</span><span class="sxs-lookup"><span data-stu-id="ce107-108">The API reference documentation indicates when a function or method should be used or implemented only by generated code.</span></span>

<span data-ttu-id="ce107-109">El Windows SDK incluye algunos archivos WSDL de ejemplo, archivos de configuración de WsdCodeGen y código generado.</span><span class="sxs-lookup"><span data-stu-id="ce107-109">The Windows SDK includes some sample WSDL files, WsdCodeGen configuration files, and generated code.</span></span> <span data-ttu-id="ce107-110">Para obtener más información, vea [ejemplos de WSDAPI](wsdapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ce107-110">For more information, see [WSDAPI Samples](wsdapi-samples.md).</span></span>

<span data-ttu-id="ce107-111">Si desea enumerar los dispositivos con el protocolo WSD y consultar los metadatos del dispositivo WSD, puede usar la API de [detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="ce107-111">If you want to enumerate devices using the WSD protocol and query WSD device metadata, you can use the [Function Discovery](/previous-versions/windows/desktop/fundisc/fd-portal) API instead.</span></span>

<span data-ttu-id="ce107-112">Si desea implementar un dispositivo WSD que no ejecuta Windows, consulte el desarrollo de [dispositivos WSD](wsd-device-development.md).</span><span class="sxs-lookup"><span data-stu-id="ce107-112">If you want to implement a WSD device that does not run Windows, see [WSD Device Development](wsd-device-development.md).</span></span>
