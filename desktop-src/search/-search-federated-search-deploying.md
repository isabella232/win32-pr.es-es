---
description: En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (. osdx), cómo implementar un archivo. osdx y cómo realizar un seguimiento del uso del servicio de OpenSearch.
ms.assetid: 9db0f970-4e17-492b-ab75-a8b0f8011d0a
title: Implementación de conectores de búsqueda en Windows Federated Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a870169cd6cca3537327a8631a15d61da78eb6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497081"
---
# <a name="deploying-search-connectors-in-windows-federated-search"></a><span data-ttu-id="1ee26-103">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-103">Deploying Search Connectors in Windows Federated Search</span></span>

<span data-ttu-id="1ee26-104">En este tema se explica cómo un usuario registra un nuevo almacén de datos remoto con búsqueda federada abriendo un archivo de descripción de OpenSearch (. osdx), cómo implementar un archivo. osdx y cómo realizar un seguimiento del uso del servicio de [OpenSearch](https://github.com/dewitt/opensearch) .</span><span class="sxs-lookup"><span data-stu-id="1ee26-104">This topic explains how a user registers a new remote data store with federated search by opening an OpenSearch Description (.osdx) file, how to deploy an .osdx file, and how to track usage of your [OpenSearch](https://github.com/dewitt/opensearch) service.</span></span>

<span data-ttu-id="1ee26-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1ee26-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="1ee26-106">El archivo. searchconnector-MS (conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="1ee26-106">The .searchconnector-ms (Search Connector) File</span></span>](#the-searchconnector-ms-search-connector-file)
-   [<span data-ttu-id="1ee26-107">Métodos de implementación</span><span class="sxs-lookup"><span data-stu-id="1ee26-107">Deployment Methods</span></span>](#deployment-methods)
    -   [<span data-ttu-id="1ee26-108">Implementación de extracción</span><span class="sxs-lookup"><span data-stu-id="1ee26-108">Pull Deployment</span></span>](#pull-deployment)
    -   [<span data-ttu-id="1ee26-109">Implementación de extracción</span><span class="sxs-lookup"><span data-stu-id="1ee26-109">Push Deployment</span></span>](#push-deployment)
-   [<span data-ttu-id="1ee26-110">Seguimiento del uso</span><span class="sxs-lookup"><span data-stu-id="1ee26-110">Tracking Usage</span></span>](#tracking-usage)
-   [<span data-ttu-id="1ee26-111">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1ee26-111">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="1ee26-112">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ee26-112">Related topics</span></span>](#related-topics)

## <a name="the-searchconnector-ms-search-connector-file"></a><span data-ttu-id="1ee26-113">El archivo. searchconnector-MS (conector de búsqueda)</span><span class="sxs-lookup"><span data-stu-id="1ee26-113">The .searchconnector-ms (Search Connector) File</span></span>

<span data-ttu-id="1ee26-114">Simplemente abrir el archivo. osdx que describe cómo conectarse al servicio Web y cómo asignar cualquier elemento personalizado en el XML de RSS o Atom registra el nuevo almacén de datos remotos con la búsqueda federada.</span><span class="sxs-lookup"><span data-stu-id="1ee26-114">Merely opening the .osdx file that describes how to connect to the web service and how to map any custom elements in your RSS or Atom XML registers your new remote data store with federated search.</span></span> <span data-ttu-id="1ee26-115">Un almacén de datos que ya tiene un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) compatible con búsqueda federada se puede Agregar al explorador de Windows cuando un usuario abre un archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="1ee26-115">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with federated search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

<span data-ttu-id="1ee26-116">Una vez que haya dado el archivo. osdx a su usuario y el usuario abra el archivo. osdx, se producirán los siguientes eventos.</span><span class="sxs-lookup"><span data-stu-id="1ee26-116">After you have given the .osdx to your user and the user opens the .osdx file, the following events occur.</span></span>

1.  <span data-ttu-id="1ee26-117">Se crea un archivo. searchconnector-MS en la carpeta **búsquedas de Windows** (% userprofile%/searches).</span><span class="sxs-lookup"><span data-stu-id="1ee26-117">A .searchconnector-ms file is created in the **Windows Searches** folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="1ee26-118">Se crea un acceso directo al archivo. searchconnector-MS en la carpeta **Links** (% userprofile%/links).</span><span class="sxs-lookup"><span data-stu-id="1ee26-118">A shortcut to the .searchconnector-ms file is created in the **Links** folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="1ee26-119">Aparece un acceso directo en el panel **Favoritos** de navegación del explorador de Windows, lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio Web.</span><span class="sxs-lookup"><span data-stu-id="1ee26-119">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store and query the web service.</span></span>

## <a name="deployment-methods"></a><span data-ttu-id="1ee26-120">Métodos de implementación</span><span class="sxs-lookup"><span data-stu-id="1ee26-120">Deployment Methods</span></span>

<span data-ttu-id="1ee26-121">Hay dos maneras de implementar conectores de búsqueda: implementación de extracción e implementación de inserción.</span><span class="sxs-lookup"><span data-stu-id="1ee26-121">There are two ways to deploy search connectors, pull deployment and push deployment.</span></span>

### <a name="pull-deployment"></a><span data-ttu-id="1ee26-122">Implementación de extracción</span><span class="sxs-lookup"><span data-stu-id="1ee26-122">Pull Deployment</span></span>

<span data-ttu-id="1ee26-123">La implementación de extracción describe cualquier tipo de implementación en la que el usuario final toma la iniciativa para instalar los conectores de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1ee26-123">Pull deployment describes any type of deployment in which the end user takes the initiative to install the search connectors.</span></span> <span data-ttu-id="1ee26-124">Los métodos comunes de implementación de extracción son:</span><span class="sxs-lookup"><span data-stu-id="1ee26-124">Common methods of pull deployment are:</span></span>

-   <span data-ttu-id="1ee26-125">Adjuntar el archivo. osdx en un correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="1ee26-125">Attaching the .osdx file in an email.</span></span>
-   <span data-ttu-id="1ee26-126">Publicar el archivo en una página web.</span><span class="sxs-lookup"><span data-stu-id="1ee26-126">Posting the file on a webpage.</span></span>
-   <span data-ttu-id="1ee26-127">Proporcionar un vínculo dinámico en el sitio de la intranet; por ejemplo, uno que genera archivos. osdx personalizados basados en las opciones del usuario o en el ámbito actual dentro del sitio.</span><span class="sxs-lookup"><span data-stu-id="1ee26-127">Providing a dynamic link on your intranet site; for example, one that generates custom .osdx files based on user choices or the current scope within the site.</span></span>

<span data-ttu-id="1ee26-128">Para que el archivo se descargue cuando el usuario hace clic en el vínculo en el explorador, el servidor Web que hospeda el servicio Web debe estar configurado para proporcionar el archivo. osdx como un archivo.</span><span class="sxs-lookup"><span data-stu-id="1ee26-128">For the file to be downloaded when the user clicks the link in their browser, the web server hosting the web service must be configured to deliver the .osdx as a file.</span></span> <span data-ttu-id="1ee26-129">Por lo tanto, debe configurar los tipos MIME en el servidor web para tratar los archivos. osdx como `"application/opensearchdescription+xml"` .</span><span class="sxs-lookup"><span data-stu-id="1ee26-129">Hence, you must configure the MIME Types on the web server to treat .osdx files as `"application/opensearchdescription+xml"`.</span></span> <span data-ttu-id="1ee26-130">Opcionalmente, puede usar el icono proporcionado por Microsoft para identificar el vínculo del conector de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1ee26-130">Optionally, you can use the icon supplied by Microsoft to identify search connector link.</span></span>

### <a name="push-deployment"></a><span data-ttu-id="1ee26-131">Implementación de extracción</span><span class="sxs-lookup"><span data-stu-id="1ee26-131">Push Deployment</span></span>

<span data-ttu-id="1ee26-132">La implementación de inserciones describe cualquier tipo de implementación que no dependa de la iniciativa del usuario para instalar los conectores de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="1ee26-132">Push deployment describes any type of deployment that does not depend on user initiative to install the search connectors.</span></span> <span data-ttu-id="1ee26-133">Los métodos comunes de implementación de la instalación de extracción son:</span><span class="sxs-lookup"><span data-stu-id="1ee26-133">Common methods of push deployment are:</span></span>

-   <span data-ttu-id="1ee26-134">Preferencias de directiva de grupo (GPP)</span><span class="sxs-lookup"><span data-stu-id="1ee26-134">Group Policy Preferences (GPP)</span></span>
-   <span data-ttu-id="1ee26-135">Script de inicio de sesión</span><span class="sxs-lookup"><span data-stu-id="1ee26-135">Logon script</span></span>
-   <span data-ttu-id="1ee26-136">Perfiles móviles</span><span class="sxs-lookup"><span data-stu-id="1ee26-136">Roaming profiles</span></span>
-   <span data-ttu-id="1ee26-137">Creación de imágenes</span><span class="sxs-lookup"><span data-stu-id="1ee26-137">Imaging</span></span>

## <a name="tracking-usage"></a><span data-ttu-id="1ee26-138">Seguimiento del uso</span><span class="sxs-lookup"><span data-stu-id="1ee26-138">Tracking Usage</span></span>

<span data-ttu-id="1ee26-139">Para realizar un seguimiento del uso del servicio de [OpenSearch](https://github.com/dewitt/opensearch) por los usuarios que buscan en el explorador de Windows, filtre los archivos de registro del servidor web para esta cadena de agente de usuario: `Windows-Search+(Windows+NT+6.1)` .</span><span class="sxs-lookup"><span data-stu-id="1ee26-139">To track the usage of your [OpenSearch](https://github.com/dewitt/opensearch) service by users searching from Windows Explorer, filter your web server log files for this user agent string: `Windows-Search+(Windows+NT+6.1)`.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ee26-140">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="1ee26-140">Additional Resources</span></span>

<span data-ttu-id="1ee26-141">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1ee26-141">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1ee26-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1ee26-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ee26-143">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="1ee26-144">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-144">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="1ee26-145">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-145">Connecting Your web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="1ee26-146">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-146">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="1ee26-147">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="1ee26-147">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="1ee26-148">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="1ee26-148">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> </dl>

 

 
