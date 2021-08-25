---
title: Control de versiones (API de servidor HTTP)
description: La API del servidor HTTP versión 2.0 aplica el control de versiones con ámbito de objeto para determinar la versión de la API.
ms.assetid: 2c2d7501-85e0-44ec-aa42-01372b29266e
keywords:
- Control de versiones en la API http server versión 2.0
- API del servidor HTTP versión 2.0, control de versiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc7a84af7de439cdd13cc1e9ff66fff367370fa963882077904ad656b856511
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829701"
---
# <a name="versioning-http-server-api"></a>Control de versiones (API de servidor HTTP)

La API del servidor HTTP versión 2.0 deja obsoletas las colas de solicitudes de la versión 1.0 y las asociaciones de dirección URL con la cola de solicitudes. El control de versiones con ámbito de objeto permite a las aplicaciones proporcionar información de versión específica de la aplicación. Una aplicación puede llamar automáticamente a la versión correcta de las estructuras para el sistema operativo en el que se ejecuta.

## <a name="request-queues"></a>Colas de solicitud

A partir de la API http server 2.0, las colas de solicitudes se crean con [**HttpCreateRequestQueue,**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) lo que hace que la función [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle) de la versión 1.0 sea obsoleta. Los grupos de direcciones URL se presentan en la versión 2.0 con la [**función HttpCreateUrlGroup.**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) Las direcciones URL se agregan al grupo mediante [**HttpAddUrlToUrlGroup,**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) lo que hace que la función [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) de la versión 1.0 sea obsoleta. Los grupos de direcciones URL de la versión 2.0 no deben usarse con las colas de solicitud de la versión 1.0.

A partir de la versión 2.0, las siguientes funciones de la versión 1.0 están obsoletas y no se pueden usar con las colas de solicitudes de la versión 2.0:

-   [**HttpCreateHttpHandle**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)
-   [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)
-   [**HttpRemoveUrl**](/windows/desktop/api/Http/nf-http-httpremoveurl)

Para obtener más información sobre cómo configurar grupos de direcciones URL, vea el [tema Configuración del grupo de direcciones URL.](configuring-the-url-group.md) Para obtener más información sobre las colas de solicitudes de la versión 2.0, vea el tema [Cola de solicitudes con](named-request-queue.md) nombre.

## <a name="object-scoped-versioning"></a>Object-Scoped control de versiones

En la versión 1.0, la aplicación proporciona la versión de LA API del servidor HTTP en la llamada a [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). La información de versión solo se acepta desde la primera aplicación que llamó **a HttpInitialize** y se aplica a todas las aplicaciones de API de servidor HTTP en el mismo proceso. A partir de la API de la versión 2.0, no se usa la información de versión global proporcionada en la llamada a **HttpInitialize.** En el caso de las aplicaciones de la versión 2.0, la versión de la API del servidor HTTP se pasa en el parámetro Version cuando [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) o [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession)crean la cola de solicitudes o la sesión del servidor. Cuando la cola de solicitudes se crea con la versión 1.0 [**HttpCreateHttpHandle,**](/windows/desktop/api/Http/nf-http-httpcreatehttphandle)se marca automáticamente como versión 1.0. Las aplicaciones de la versión 1.0 y la versión 2.0 se pueden ejecutar en el mismo proceso.

Las [**estructuras HTTP REQUEST \_ y**](/previous-versions/windows/desktop/legacy/aa364545(v=vs.85)) [**HTTP \_ RESPONSE**](http-response.md) se actualizan para incluir información de autenticación en la API del servidor HTTP versión 2.0. [**HTTP \_ REQUEST \_ V1**](/windows/desktop/api/Http/ns-http-http_request_v1) y [**HTTP REQUEST \_ \_ V2**](/windows/desktop/api/Http/ns-http-http_request_v2) son específicos de la versión de la API que usa la aplicación. Sin embargo, las aplicaciones no deben usar estas estructuras directamente en su código; en su lugar, **deben usar HTTP \_ REQUEST** para obtener la versión correcta en función de la versión de la cola de solicitudes en la que se recibió la solicitud. Además, tenga en cuenta que el tamaño de la estructura **\_ DE SOLICITUD HTTP** se basa en la versión del sistema operativo en la que se compila el código.

 

 
