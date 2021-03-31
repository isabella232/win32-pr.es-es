---
title: Control de versiones (API de servidor HTTP)
description: La API del servidor HTTP versión 2,0 aplica el control de versiones del ámbito del objeto para determinar la versión de la API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Control de versiones en la API del servidor HTTP versión 2,0
- Servidor HTTP versión 2,0 API, control de versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5221ff7a93bb24e7e0b8a1b9f7c2399012cdbe95
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149795"
---
# <a name="versioning-http-server-api"></a>Control de versiones (API de servidor HTTP)

La API del servidor HTTP versión 2,0 hace que las colas de solicitudes de la versión 1,0 y las asociaciones de direcciones URL queden obsoletas con la cola de solicitudes. El control de versiones de ámbito de objeto permite a las aplicaciones proporcionar información de versión específica de la aplicación. Una aplicación puede llamar automáticamente a la versión correcta de las estructuras para el sistema operativo en el que se está ejecutando.

## <a name="request-queues"></a>Solicitar colas

A partir de la versión 2,0 de la API del servidor HTTP, las colas de solicitudes se crean con [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) , lo que permite que la versión 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) esté obsoleta. Los grupos de direcciones URL se introducen en la versión 2,0 con la función [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) . Las direcciones URL se agregan al grupo mediante [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) , lo que hace que la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) de la versión 1,0 sea obsoleta. Los grupos de direcciones URL de la versión 2,0 no deben usarse con colas de solicitudes de la versión 1,0.

A partir de la versión 2,0, las siguientes funciones de la versión 1,0 están obsoletas y no se pueden usar con las colas de solicitudes de la versión 2,0:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Para obtener más información sobre la configuración de grupos de direcciones URL, vea el tema [configurar el grupo de direcciones URL](configuring-the-url-group.md) . Para obtener más información sobre las colas de solicitudes de la versión 2,0, vea el tema [cola de solicitudes con nombre](named-request-queue.md) .

## <a name="object-scoped-versioning"></a>Control de versiones de Object-Scoped

En la versión 1,0, la aplicación proporciona la versión de la API del servidor HTTP en la llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). La información de versión solo se acepta desde la primera aplicación que llamó a **HttpInitialize** y se aplica a todas las aplicaciones de API de servidor http en el mismo proceso. A partir de la versión 2,0 de la API, no se utiliza la información de versión global suministrada en la llamada a **HttpInitialize** . En el caso de las aplicaciones de la versión 2,0, la versión de la API del servidor HTTP se pasa en el parámetro de versión cuando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) o [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession)crea la cola de solicitudes o la sesión del servidor. Cuando se crea la cola de solicitudes con la versión 1,0 [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle), se marca automáticamente como la versión 1,0. Las aplicaciones de la versión 1,0 y la versión 2,0 se pueden ejecutar en el mismo proceso.

Las estructuras de [**\_ solicitud HTTP**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) y [**\_ respuesta http**](http-response.md) se actualizan para incluir información de autenticación en la API del servidor http versión 2,0. [**Http \_ Las solicitudes \_ v1**](/windows/desktop/api/Http/ns-http-http_request_v1) y [**http \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) son específicas de la versión de la API usada por la aplicación. Sin embargo, las aplicaciones no deben usar estas estructuras directamente en su código; en su lugar, deben utilizar la **\_ solicitud HTTP** para obtener la versión correcta en función de la versión de la cola de solicitudes en la que se recibió la solicitud. Además, tenga en cuenta que el tamaño de la estructura de la **\_ solicitud HTTP** se basa en la versión del sistema operativo en el que se compila el código.

 

 
