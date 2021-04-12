---
title: Características de la API del servidor HTTP
description: En este tema se admiten las características admitidas y no admitidas de la API del servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Características de la API del servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357582"
---
# <a name="http-server-api-features"></a>Características de la API del servidor HTTP

En las listas siguientes se describen las características admitidas y no admitidas de la API del servidor HTTP.

## <a name="features-supported"></a>Características admitidas

HTTP admite las siguientes características:

-   Funcionalidad de servidor de HTTP v 1.0 y v 1.1.
-   Capa de sockets seguros 3,0 (SSL) compatible con los certificados de cliente y de servidor.
-   Almacenamiento en caché de fragmentos de datos para su uso en respuestas posteriores.
-   Compatibilidad con direcciones IPv6 e IPv4.
-   Reservas de espacio de nombres URL para la seguridad de la aplicación.
-   Controladores verdaderos para todos los objetos.
-   Modelos de e/s sincrónicos y asincrónicos.
-   Compatibilidad con WOW64 en equipos que ejecutan Windows de 64 bits a partir de Windows Server 2003 con Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Características no admitidas

La API del servidor HTTP no admite la funcionalidad siguiente:

-   La API del servidor HTTP no realiza la autenticación del cliente o del servidor basándose en el contenido de los encabezados de solicitud HTTP. La aplicación debe implementar cualquier autenticación necesaria.
-   WOW64 en equipos que ejecutan Windows de 64 bits no se admite en Windows Server 2003 y Windows XP con Service Pack 2 (SP2) y versiones anteriores.
-   La API del servidor HTTP no admite el registro de solicitudes y respuestas HTTP.
-   La API del servidor HTTP no fragmenta las respuestas HTTP salientes. La aplicación debe implementar la fragmentación de la respuesta si es necesario.

 

 




