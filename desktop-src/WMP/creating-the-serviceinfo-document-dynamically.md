---
title: Creación dinámica del documento ServiceInfo
description: Creación dinámica del documento ServiceInfo
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Reproductor de Windows Media en línea, crear el documento ServiceInfo
- online stores,creating ServiceInfo document
- type 1 online stores,creating ServiceInfo document
- tipo 2 tiendas en línea, crear documento ServiceInfo
- Reproductor de Windows Media en línea, crear dinámicamente el documento ServiceInfo
- tiendas en línea, crear dinámicamente el documento ServiceInfo
- tiendas en línea de tipo 1, crear dinámicamente un documento ServiceInfo
- tipo 2 tiendas en línea, crear dinámicamente el documento ServiceInfo
- Reproductor de Windows Media tiendas en línea,documento ServiceInfo
- tiendas en línea,documento ServiceInfo
- type 1 online stores,ServiceInfo document
- tiendas en línea de tipo 2, documento ServiceInfo
- crear dinámicamente el documento ServiceInfo
- creación de un documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3883487d072af57174a1f40f2fcef05d3290917b473a95bf723c34d793c5ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340995"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a>Creación dinámica del documento ServiceInfo

Puede usar ASP para crear el documento ServiceInfo. Esto puede proporcionar una mayor flexibilidad en su tienda en línea mediante las técnicas siguientes:

-   Generación dinámica del nombre de host para las direcciones URL.
-   Cambiar las direcciones URL para la localización en función de los parámetros de configuración regional y geoid.
-   Anexar dinámicamente parámetros de cadena de consulta desde la dirección URL de ServiceInfo a otras direcciones URL, como la dirección URL de la página de navegación.

En el código de ejemplo siguiente se muestra una página ASP simple que crea dinámicamente un documento ServiceInfo:


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



El código de ejemplo anterior usa ASP para recuperar el nombre de host del servidor web y crear dinámicamente las direcciones URL del documento. El código también recupera el parámetro de cadena de consulta de configuración *regional* de la solicitud ServiceInfo y lo anexa a la dirección URL de la página de navegación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Información común a los almacenes en línea de tipo 1 y 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Navegación para tiendas en línea de tipo 2**](navigation-for-type-2-online-stores.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 1**](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Documento ServiceInfo para una tienda en línea de tipo 2**](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Documento ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 




