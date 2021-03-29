---
title: Documento ServiceInfo para una tienda en línea de tipo 2
description: Documento ServiceInfo para una tienda en línea de tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075867"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="094dc-107">Documento ServiceInfo para una tienda en línea de tipo 2</span><span class="sxs-lookup"><span data-stu-id="094dc-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="094dc-108">Los proveedores de tiendas en línea de tipo 2 deben proporcionar a Microsoft la dirección URL de un documento XML que describa la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="094dc-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="094dc-109">Windows Media Player 10 y Windows Media Player 11 Use este documento para determinar cómo configurar la interfaz de usuario para hospedar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="094dc-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="094dc-110">En Windows Media Player 10, el documento ServiceInfo proporciona lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="094dc-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="094dc-111">Información sobre cómo configurar los paneles de tareas que Windows Media Player muestra cuando la tienda en línea está activa.</span><span class="sxs-lookup"><span data-stu-id="094dc-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="094dc-112">Una tienda en línea puede tener uno, dos o tres paneles de tareas.</span><span class="sxs-lookup"><span data-stu-id="094dc-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="094dc-113">Información utilizada para configurar los botones del panel de tareas, como el texto del botón, el color del botón y la información sobre herramientas de los botones.</span><span class="sxs-lookup"><span data-stu-id="094dc-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="094dc-114">Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="094dc-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="094dc-115">Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="094dc-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="094dc-116">Información sobre cómo el programa de instalación de Windows Media Player debe configurar la primera tienda en línea que el usuario ve.</span><span class="sxs-lookup"><span data-stu-id="094dc-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="094dc-117">En Windows Media Player 11, el documento ServiceInfo proporciona lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="094dc-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="094dc-118">Información utilizada para configurar el botón para la pestaña tiendas en línea, como el texto del botón y la información sobre herramientas para el botón.</span><span class="sxs-lookup"><span data-stu-id="094dc-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="094dc-119">Direcciones URL para las imágenes que Windows Media Player muestra para identificar la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="094dc-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="094dc-120">Direcciones URL de páginas web, proporcionadas por la tienda en línea, que Windows Media Player hospeda en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="094dc-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="094dc-121">Al empezar a desarrollar la tienda en línea, debe proporcionar a Microsoft la dirección URL del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="094dc-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="094dc-122">Durante la fase de desarrollo, la tienda en línea aparecerá en Windows Media Player solo cuando se establezca una clave del registro especial.</span><span class="sxs-lookup"><span data-stu-id="094dc-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="094dc-123">Una vez publicada la tienda en línea, el escenario ususal es que Windows Media Player recupera el documento ServiceInfo de la web automáticamente.</span><span class="sxs-lookup"><span data-stu-id="094dc-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="094dc-124">En algunos casos, sin embargo, Windows Media Player recupera el documento ServiceInfo del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="094dc-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="094dc-125">Para obtener más información, consulte [configuración de la tienda en línea inicial](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="094dc-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="094dc-126">Cuando Windows Media Player recupera el documento ServiceInfo de la web, anexa una cadena de consulta a la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="094dc-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="094dc-127">La cadena de consulta contiene parámetros que proporcionan información sobre la configuración regional del usuario y la versión de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="094dc-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="094dc-128">Puede crear documentos de ServiceInfo estáticos o dinámicos.</span><span class="sxs-lookup"><span data-stu-id="094dc-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="094dc-129">Un documento de ServiceInfo estático tiene una extensión de nombre de archivo. Xml.</span><span class="sxs-lookup"><span data-stu-id="094dc-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="094dc-130">Un documento de ServiceInfo dinámico es una página ASP y tiene una extensión de nombre de archivo. asp o. aspx.</span><span class="sxs-lookup"><span data-stu-id="094dc-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="094dc-131">No todos los elementos disponibles para su uso en el documento ServiceInfo se pueden usar en cada tienda en línea y algunos elementos son opcionales para todas las tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="094dc-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="094dc-132">Para obtener información acerca de los tipos de tiendas en línea que puede crear y las características disponibles para cada tipo, consulte [Windows Media Player tiendas en línea](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="094dc-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="094dc-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="094dc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="094dc-134">**Acerca de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="094dc-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="094dc-135">**Creación dinámica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="094dc-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="094dc-136">**Ejemplo de documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="094dc-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="094dc-137">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="094dc-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




