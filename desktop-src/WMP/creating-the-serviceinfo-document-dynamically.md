---
title: Creación dinámica del documento ServiceInfo
description: Creación dinámica del documento ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player tiendas en línea, crear documento ServiceInfo
- tiendas en línea, crear documento ServiceInfo
- tipo 1 tiendas en línea, crear documento ServiceInfo
- tipo 2 tiendas en línea, crear documento ServiceInfo
- Windows Media Player tiendas en línea, creación dinámica de documentos de ServiceInfo
- tiendas en línea, creación dinámica de documentos de ServiceInfo
- tipo 1 tiendas en línea, creación dinámica del documento ServiceInfo
- tipo 2 tiendas en línea, creación dinámica del documento ServiceInfo
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- creación dinámica del documento ServiceInfo
- creación de un documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993939"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Creación dinámica del documento ServiceInfo

Puede usar ASP para crear el documento de ServiceInfo. Esto puede proporcionar mayor flexibilidad en la tienda en línea mediante las técnicas siguientes:

-   Generar dinámicamente el nombre de host para las direcciones URL.
-   Cambiar las direcciones URL para la localización en función de los parámetros de configuración regional y Geoid.
-   Anexar dinámicamente los parámetros de cadena de consulta de la dirección URL de ServiceInfo a otras direcciones URL, como la dirección URL de la página de navegación.

En el ejemplo de código siguiente se muestra una página ASP simple que crea dinámicamente un documento ServiceInfo:


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



En el código de ejemplo anterior se usa ASP para recuperar el nombre de host del servidor Web y crear dinámicamente las direcciones URL en el documento. El código también recupera el parámetro de cadena de consulta de *configuración regional* de la solicitud ServiceInfo y lo anexa a la dirección URL de la página navegar.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común para las tiendas en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navegación para las tiendas en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




