---
title: Configuración de los temporizadores de gran nivel de API de servidor HTTP
description: Configuración de los temporizadores de gran nivel de API de servidor HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae91abb1c89419e99fa13273cd55b0783df3906a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268815"
---
# <a name="configuring-the-http-server-api-wide-timers"></a><span data-ttu-id="55dc8-103">Configuración de los temporizadores de gran nivel de API de servidor HTTP</span><span class="sxs-lookup"><span data-stu-id="55dc8-103">Configuring the HTTP Server API Wide Timers</span></span>

<span data-ttu-id="55dc8-104">Los temporizadores **HeaderWait** y **IDLECONNECTION** de la API del servidor HTTP se configuran mediante una llamada a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) de la versión 1,0.</span><span class="sxs-lookup"><span data-stu-id="55dc8-104">The HTTP Server API-wide **HeaderWait** and **IdleConnection** timers are configured by calling the version 1.0 [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) function.</span></span> <span data-ttu-id="55dc8-105">El parámetro *ConfigId* se establece en **HttpServiceConfigTimeout** y el parámetro *pConfigInformation* especifica la estructura del [**\_ \_ \_ \_ conjunto de tiempo de espera de configuración del servicio http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contiene el temporizador establecido y el valor para el temporizador.</span><span class="sxs-lookup"><span data-stu-id="55dc8-105">The *ConfigId* parameter is set to **HttpServiceConfigTimeout** and the *pConfigInformation* parameter specifies the [**HTTP\_SERVICE\_CONFIG\_TIMEOUT\_SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) structure that contains the timer that is set and the value for the timer.</span></span>

<span data-ttu-id="55dc8-106">La configuración de los tiempos de espera de la API del servidor HTTP requiere privilegios administrativos, pero no los consulta.</span><span class="sxs-lookup"><span data-stu-id="55dc8-106">Configuring the HTTP Server API-wide timeouts requires administrative privileges, however querying them does not.</span></span> <span data-ttu-id="55dc8-107">Estas configuraciones se establecen para todas las aplicaciones del equipo y se conservan cuando se reinicia el servicio HTTP o se reinicia el equipo.</span><span class="sxs-lookup"><span data-stu-id="55dc8-107">These configurations are set for all applications on the computer and they persist when the HTTP service is restarted or the computer is restarted.</span></span> <span data-ttu-id="55dc8-108">Para consultar los tiempos de espera de API de servidor HTTP existentes, la aplicación llama a [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span><span class="sxs-lookup"><span data-stu-id="55dc8-108">To query existing HTTP Server API-wide timeouts, the application calls [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).</span></span>

 

 




