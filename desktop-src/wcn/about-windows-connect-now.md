---
title: Acerca de Windows Connect Now
description: Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para puntos de acceso de red y dispositivos (por ejemplo, impresoras, cámaras y PCs) para conectarse y cambiar la configuración.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149546"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="40b56-103">Acerca de Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="40b56-103">About Windows Connect Now</span></span>

<span data-ttu-id="40b56-104">Windows Connect Now (WCN) proporciona un mecanismo sencillo y seguro para puntos de acceso de red y dispositivos (por ejemplo, impresoras, cámaras y PCs) para conectarse y cambiar la configuración.</span><span class="sxs-lookup"><span data-stu-id="40b56-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="40b56-105">Esta API es la implementación de Microsoft del protocolo Wi-Fi de configuración simple (/Wi-Fi) de configuración protegida (WPS), que creó Wi-Fi Alliance como una solución para redes domésticas y pequeñas empresas.</span><span class="sxs-lookup"><span data-stu-id="40b56-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="40b56-106">Esta tecnología no está pensada para escenarios empresariales.</span><span class="sxs-lookup"><span data-stu-id="40b56-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="40b56-107">El nombre de la especificación cambió entre la versión 1.0 h y la versión 2.</span><span class="sxs-lookup"><span data-stu-id="40b56-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="40b56-108">La especificación h de la versión 1.0 se llamaba Wi-Fi instalación protegida (WPS).</span><span class="sxs-lookup"><span data-stu-id="40b56-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="40b56-109">A partir de la especificación de la versión 2, la especificación se denomina Wi-Fi configuración simple (WSC).</span><span class="sxs-lookup"><span data-stu-id="40b56-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="40b56-110">En nuestra documentación, los términos WPS y WSC se usan indistintamente a menos que se indique.</span><span class="sxs-lookup"><span data-stu-id="40b56-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="40b56-111">Windows Connect ahora permite que las aplicaciones busquen dispositivos compatibles con WCN mediante la [API de detección de funciones](/previous-versions/windows/desktop/fundisc/fd-portal).</span><span class="sxs-lookup"><span data-stu-id="40b56-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="40b56-112">El ámbito de una búsqueda se puede restringir a un SSID específico, un estado, una categoría o incluso ampliarse para incluir todos los dispositivos compatibles con WCN.</span><span class="sxs-lookup"><span data-stu-id="40b56-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="40b56-113">Una vez que se encuentran los dispositivos, la API de WCN permite la comunicación con el dispositivo compatible con WCN con el fin de facilitar la configuración o la conectividad.</span><span class="sxs-lookup"><span data-stu-id="40b56-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 