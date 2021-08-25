---
title: Configuración de los temporizadores anchos de LA API del servidor HTTP
description: Configuración de los temporizadores anchos de LA API del servidor HTTP
ms.assetid: 34f80bac-a7c5-4949-9c15-ed63a3582e26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0eb5fc40bedd51884830893673b3bae2341a21110fa2c3b33878dba7a4aef0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047355"
---
# <a name="configuring-the-http-server-api-wide-timers"></a>Configuración de los temporizadores anchos de LA API del servidor HTTP

Los temporizadores **HeaderWait** e **IdleConnection** de la API del servidor HTTP se configuran mediante una llamada a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) de la versión 1.0. El *parámetro ConfigId* se establece en **HttpServiceConfigTimeout** y el parámetro *pConfigInformation* especifica la estructura [**HTTP SERVICE CONFIG TIMEOUT \_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set) que contiene el temporizador establecido y el valor del temporizador.

La configuración de los tiempos de espera para toda la API del servidor HTTP requiere privilegios administrativos, pero la consulta no. Estas configuraciones se establecen para todas las aplicaciones del equipo y se conservan cuando se reinicia el servicio HTTP o se reinicia el equipo. Para consultar los tiempos de espera existentes de la API del servidor HTTP, la aplicación llama a [**HttpQueryServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpqueryserviceconfiguration).

 

 




