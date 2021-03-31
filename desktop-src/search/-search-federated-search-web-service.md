---
description: En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver los resultados de la búsqueda en RSS o Atom.
ms.assetid: 4c8de310-49e6-4d90-a920-0c715351c86a
title: Conexión del servicio Web en la búsqueda federada de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45632d1d3c7b820ab1f39db0896c9f2927b24ccb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153976"
---
# <a name="connecting-your-web-service-in-windows-federated-search"></a><span data-ttu-id="76d63-103">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-103">Connecting Your Web Service in Windows Federated Search</span></span>

<span data-ttu-id="76d63-104">En este tema se describen los pasos necesarios para conectar un servicio web entre el almacén de datos y la búsqueda federada de Windows y cómo enviar consultas y devolver los resultados de la búsqueda en RSS o Atom.</span><span class="sxs-lookup"><span data-stu-id="76d63-104">This topic describes the steps involved in connecting a web service between your data store and Windows Federated Search, and how to send queries and return search results in RSS or Atom.</span></span>

<span data-ttu-id="76d63-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="76d63-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="76d63-106">Conexión del servicio Web</span><span class="sxs-lookup"><span data-stu-id="76d63-106">Connect Your web Service</span></span>](#connect-your-web-service)
-   [<span data-ttu-id="76d63-107">Registrar un almacén de datos remoto existente</span><span class="sxs-lookup"><span data-stu-id="76d63-107">Register an Existing Remote Data Store</span></span>](#register-an-existing-remote-data-store)
-   [<span data-ttu-id="76d63-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="76d63-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="76d63-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76d63-109">Related topics</span></span>](#related-topics)

## <a name="connect-your-web-service"></a><span data-ttu-id="76d63-110">Conexión del servicio Web</span><span class="sxs-lookup"><span data-stu-id="76d63-110">Connect Your web Service</span></span>

<span data-ttu-id="76d63-111">**Para conectar el servicio Web del almacén de datos a la búsqueda federada, realice los pasos siguientes:**</span><span class="sxs-lookup"><span data-stu-id="76d63-111">**To connect the web service of your data store to federated search, perform the following steps:**</span></span>

1.  <span data-ttu-id="76d63-112">Cree un archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="76d63-112">Create an .osdx file.</span></span>
2.  <span data-ttu-id="76d63-113">Proporcione el archivo. osdx a los usuarios para que puedan agregar el servicio a petición abriendo el archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="76d63-113">Supply the .osdx file to users so that they can add the service on demand by opening the .osdx file.</span></span>
3.  <span data-ttu-id="76d63-114">Genere un conector de búsqueda e impleméntelo activamente en su empresa.</span><span class="sxs-lookup"><span data-stu-id="76d63-114">Generate a search connector and actively deploy it in your enterprise.</span></span>

## <a name="register-an-existing-remote-data-store"></a><span data-ttu-id="76d63-115">Registrar un almacén de datos remoto existente</span><span class="sxs-lookup"><span data-stu-id="76d63-115">Register an Existing Remote Data Store</span></span>

<span data-ttu-id="76d63-116">Un usuario registra un nuevo almacén de datos remoto con la búsqueda federada de Windows abriendo un archivo de descripción de OpenSearch (. osdx).</span><span class="sxs-lookup"><span data-stu-id="76d63-116">A user registers a new remote data store with Windows Federated Search by opening an OpenSearch Description (.osdx) file.</span></span> <span data-ttu-id="76d63-117">Cuando el usuario lo hace, se producen los siguientes eventos:</span><span class="sxs-lookup"><span data-stu-id="76d63-117">When the user does so, the following events occur:</span></span>

1.  <span data-ttu-id="76d63-118">Se crea un archivo. searchconnector-MS (conector de búsqueda) en la carpeta búsquedas de Windows (% userprofile%/searches).</span><span class="sxs-lookup"><span data-stu-id="76d63-118">A .searchconnector-ms file (search connector) is created in the Windows Searches folder (%userprofile%/Searches).</span></span>
2.  <span data-ttu-id="76d63-119">Se crea un acceso directo al archivo. searchconnector-MS en la carpeta links (% userprofile%/links).</span><span class="sxs-lookup"><span data-stu-id="76d63-119">A shortcut to the .searchconnector-ms file is created in the Links folder (%userprofile%/Links).</span></span>
3.  <span data-ttu-id="76d63-120">Aparece un acceso directo en el panel **Favoritos** de navegación del explorador de Windows, lo que permite al usuario navegar al nuevo almacén de datos y consultar el servicio Web.</span><span class="sxs-lookup"><span data-stu-id="76d63-120">A shortcut appears in the Windows Explorer navigation **Favorites** pane, enabling the user to navigate into the new data store, and query the web service.</span></span>

> [!Note]  
> <span data-ttu-id="76d63-121">Un almacén de datos que ya tiene un servicio Web de [OpenSearch](https://github.com/dewitt/opensearch) compatible con la búsqueda federada de Windows se puede Agregar al explorador de Windows cuando un usuario abre un archivo. osdx.</span><span class="sxs-lookup"><span data-stu-id="76d63-121">A data store that already has an [OpenSearch](https://github.com/dewitt/opensearch) web service that is compatible with Windows Federated Search can be added to Windows Explorer when a user opens an .osdx file.</span></span>

 

## <a name="additional-resources"></a><span data-ttu-id="76d63-122">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="76d63-122">Additional Resources</span></span>

<span data-ttu-id="76d63-123">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="76d63-123">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76d63-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76d63-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76d63-125">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-125">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="76d63-126">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-126">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="76d63-127">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-127">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="76d63-128">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="76d63-128">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="76d63-129">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-129">Following Best Practices in Windows Federated Search</span></span>](-search-fedsearch-best.md)
</dt> <dt>

[<span data-ttu-id="76d63-130">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="76d63-130">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> </dl>

 

 
