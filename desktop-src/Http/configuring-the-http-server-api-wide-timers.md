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
# <a name="configuring-the-http-server-api-wide-timers"></a>Configuración de los temporizadores de gran nivel de API de servidor HTTP

Los temporizadores **HeaderWait** y **IDLECONNECTION** de la API del servidor HTTP se configuran mediante una llamada a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) de la versión 1,0. El parámetro *ConfigId* se establece en **HttpServiceConfigTimeout** y el parámetro *pConfigInformation* especifica la estructura del [**\_ \_ \_ \_ conjunto de tiempo de espera de configuración del servicio http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contiene el temporizador establecido y el valor para el temporizador.

La configuración de los tiempos de espera de la API del servidor HTTP requiere privilegios administrativos, pero no los consulta. Estas configuraciones se establecen para todas las aplicaciones del equipo y se conservan cuando se reinicia el servicio HTTP o se reinicia el equipo. Para consultar los tiempos de espera de API de servidor HTTP existentes, la aplicación llama a [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




