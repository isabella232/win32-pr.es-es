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
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="f011e-118">Creación dinámica del documento ServiceInfo</span><span class="sxs-lookup"><span data-stu-id="f011e-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="f011e-119">Puede usar ASP para crear el documento de ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="f011e-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="f011e-120">Esto puede proporcionar mayor flexibilidad en la tienda en línea mediante las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f011e-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="f011e-121">Generar dinámicamente el nombre de host para las direcciones URL.</span><span class="sxs-lookup"><span data-stu-id="f011e-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="f011e-122">Cambiar las direcciones URL para la localización en función de los parámetros de configuración regional y Geoid.</span><span class="sxs-lookup"><span data-stu-id="f011e-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="f011e-123">Anexar dinámicamente los parámetros de cadena de consulta de la dirección URL de ServiceInfo a otras direcciones URL, como la dirección URL de la página de navegación.</span><span class="sxs-lookup"><span data-stu-id="f011e-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="f011e-124">En el ejemplo de código siguiente se muestra una página ASP simple que crea dinámicamente un documento ServiceInfo:</span><span class="sxs-lookup"><span data-stu-id="f011e-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


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



<span data-ttu-id="f011e-125">En el código de ejemplo anterior se usa ASP para recuperar el nombre de host del servidor Web y crear dinámicamente las direcciones URL en el documento.</span><span class="sxs-lookup"><span data-stu-id="f011e-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="f011e-126">El código también recupera el parámetro de cadena de consulta de *configuración regional* de la solicitud ServiceInfo y lo anexa a la dirección URL de la página navegar.</span><span class="sxs-lookup"><span data-stu-id="f011e-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f011e-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f011e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f011e-128">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="f011e-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f011e-129">**Navegación para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="f011e-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="f011e-130">**Documento ServiceInfo para una tienda en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="f011e-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="f011e-131">**Documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="f011e-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="f011e-132">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="f011e-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




