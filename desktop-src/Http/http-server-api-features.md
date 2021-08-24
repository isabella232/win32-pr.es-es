---
title: Características de LA API del servidor HTTP
description: En este tema se admiten y no se admiten características de la API de servidor HTTP.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- Características de LA API del servidor HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0eaf567d4576618b07ef5ad8dec91b360f37ab46eb820ff52e2bca896ca91a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014783"
---
# <a name="http-server-api-features"></a>Características de LA API del servidor HTTP

En las listas siguientes se describen las características admitidas y no admitidas de la API de servidor HTTP.

## <a name="features-supported"></a>Características admitidas

HTTP admite las siguientes características:

-   Funcionalidad del servidor HTTP v1.0 y v1.1.
-   Capa de sockets seguros 3.0 (SSL) con compatibilidad con certificados de cliente y servidor.
-   Almacenamiento en caché de fragmentos de datos para su uso en respuestas posteriores.
-   Compatibilidad con el direccionamiento IPv6 e IPv4.
-   Reservas de espacios de nombres de dirección URL para la seguridad de la aplicación.
-   Identificadores true para todos los objetos.
-   Modelos de E/S sincrónicos y asincrónicos.
-   Compatibilidad con WOW64 en equipos que se ejecutan en equipos de 64 bits Windows a partir de Windows Server 2003 con Service Pack 1 (SP1).

## <a name="features-not-supported"></a>Características no admitidas

La API del servidor HTTP no admite la funcionalidad siguiente:

-   La API del servidor HTTP no realiza la autenticación de cliente o servidor en función del contenido de los encabezados de solicitud HTTP. La aplicación debe implementar cualquier autenticación necesaria.
-   WOW64 en equipos que se ejecutan en Windows de 64 bits no se admite en Windows Server 2003 y Windows XP con Service Pack 2 (SP2) y versiones anteriores.
-   La API del servidor HTTP no admite el registro de solicitudes y respuestas HTTP.
-   La API del servidor HTTP no fragmenta las respuestas HTTP salientes. La aplicación debe implementar la fragmentación de respuesta si es necesario.

 

 




