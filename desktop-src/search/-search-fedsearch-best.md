---
description: En este tema se enumeran los procedimientos recomendados a través de los que puede crear un almacén de datos basado en Web que se puede buscar mediante la búsqueda federada de Windows e integrar los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.
ms.assetid: d9b62cf5-7236-4252-b88d-18120f50c62c
title: Siguientes procedimientos recomendados en la búsqueda federada de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed94f42b4470694209e37f5ede8a05d87a290d1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153975"
---
# <a name="following-best-practices-in-windows-federated-search"></a><span data-ttu-id="5c67d-103">Siguientes procedimientos recomendados en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-103">Following Best Practices in Windows Federated Search</span></span>

<span data-ttu-id="5c67d-104">En este tema se enumeran los procedimientos recomendados a través de los que puede crear un almacén de datos basado en Web que se puede buscar mediante la búsqueda federada de Windows e integrar los orígenes de datos remotos con el explorador de Windows sin tener que escribir ni implementar ningún código del lado cliente de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67d-104">This topic lists the best practices through which you can build a web-based data store that can be searched using Windows federated search, and integrates your remote data sources with Windows Explorer without having to write or deploy any Windows client-side code.</span></span>

<span data-ttu-id="5c67d-105">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="5c67d-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="5c67d-106">Prácticas recomendadas para la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-106">Best Practices for Windows Federated Search</span></span>](#best-practices-for-windows-federated-search)
-   [<span data-ttu-id="5c67d-107">Prácticas recomendadas para crear una salida RSS</span><span class="sxs-lookup"><span data-stu-id="5c67d-107">Best Practices for Creating RSS Output</span></span>](#best-practices-for-creating-rss-output)
-   [<span data-ttu-id="5c67d-108">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5c67d-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="5c67d-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c67d-109">Related topics</span></span>](#related-topics)

## <a name="best-practices-for-windows-federated-search"></a><span data-ttu-id="5c67d-110">Prácticas recomendadas para la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-110">Best Practices for Windows Federated Search</span></span>

<span data-ttu-id="5c67d-111">Los procedimientos recomendados para trabajar con [OpenSearch](https://github.com/dewitt/opensearch) en Windows 7 son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c67d-111">Best practices for working with [OpenSearch](https://github.com/dewitt/opensearch) in Windows 7 are as follows:</span></span>

-   <span data-ttu-id="5c67d-112">Admita los parámetros *{startIndex}* y *{Count}* y asegúrese de devolver siempre el número de elementos solicitados a menos que devuelva el último de los resultados.</span><span class="sxs-lookup"><span data-stu-id="5c67d-112">Support the *{startIndex}* and *{count}* parameters, and be sure to always return the number of items requested unless you are returning the last of the results.</span></span>
-   <span data-ttu-id="5c67d-113">Si conoce la extensión de nombre de archivo, asígnela a la propiedad del shell de Windows [System. FileExtension](../properties/props-system-fileextension.md) .</span><span class="sxs-lookup"><span data-stu-id="5c67d-113">If you know the file name extension, map it to the [System.FileExtension](../properties/props-system-fileextension.md) Windows Shell property.</span></span> <span data-ttu-id="5c67d-114">El uso de extensiones de nombre de archivo es una manera mejor de identificar un tipo de archivo que el tipo MIME.</span><span class="sxs-lookup"><span data-stu-id="5c67d-114">Using file name extensions is a better way to identify a file type than MIME type.</span></span>
-   <span data-ttu-id="5c67d-115">Asegúrese de que el tipo MIME o la extensión de nombre de archivo que especifique en el RSS coincide con el nombre de archivo y el tipo MIME devuelto en el encabezado HTTP por el servidor Web que hospeda el elemento cuando se solicita el contenido del elemento.</span><span class="sxs-lookup"><span data-stu-id="5c67d-115">Ensure that the MIME type or file name extension that you specify in the RSS matches the file name and MIME type returned in the HTTP header by the web server that hosts the item when the item content is requested.</span></span>
-   <span data-ttu-id="5c67d-116">Si va a devolver elementos de archivo, devuelva un tamaño de archivo siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="5c67d-116">If you are returning file items, return a file size whenever possible.</span></span> <span data-ttu-id="5c67d-117">Esto garantiza que el cuadro de diálogo progreso de la descarga sea preciso.</span><span class="sxs-lookup"><span data-stu-id="5c67d-117">This ensures that the download progress dialog box is accurate.</span></span>
-   <span data-ttu-id="5c67d-118">Compruebe que las solicitudes de elementos que van más allá del final del conjunto de resultados no devuelven resultados.</span><span class="sxs-lookup"><span data-stu-id="5c67d-118">Verify that requests for items beyond the end of the results set return no results.</span></span>
    > [!Note]  
    > <span data-ttu-id="5c67d-119">No repetir resultados.</span><span class="sxs-lookup"><span data-stu-id="5c67d-119">Do not repeat results.</span></span>

     

-   <span data-ttu-id="5c67d-120">No coloque etiquetas HTML a las que no pertenezcan.</span><span class="sxs-lookup"><span data-stu-id="5c67d-120">Do not put HTML tags where they don't belong.</span></span> <span data-ttu-id="5c67d-121">Según la especificación RSS, son válidas en el campo Descripción, pero no en el campo título.</span><span class="sxs-lookup"><span data-stu-id="5c67d-121">Per the RSS specification, they are valid in the description field, but not in the title field.</span></span>
-   <span data-ttu-id="5c67d-122">No cree contenedores para los elementos de la Página Web.</span><span class="sxs-lookup"><span data-stu-id="5c67d-122">Do not create enclosures for webpage items.</span></span> <span data-ttu-id="5c67d-123">Por ejemplo, si crea un contenedor y asigna una extensión de nombre de archivo. aspx, el explorador de Windows descarga el archivo en la memoria caché de Internet y se ejecuta desde allí.</span><span class="sxs-lookup"><span data-stu-id="5c67d-123">For example, if you create an enclosure and map a file name extension of .aspx, the file is downloaded by Windows Explorer to the Internet cache and executed from there.</span></span> <span data-ttu-id="5c67d-124">Los exploradores Web no controlan el tipo de archivo. aspx.</span><span class="sxs-lookup"><span data-stu-id="5c67d-124">Web browsers do not handle the .aspx file type.</span></span> <span data-ttu-id="5c67d-125">El usuario obtenería un cuadro **de diálogo Abrir con** o un archivo podría estar abierto por una aplicación como Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5c67d-125">The user would get an **Open with** dialog box, or the file might be opened by an application like Microsoft Visual Studio.</span></span> <span data-ttu-id="5c67d-126">Evite esto devolviendo un elemento de vínculo solo para las páginas Web.</span><span class="sxs-lookup"><span data-stu-id="5c67d-126">Avoid this by returning a link element only for webpages.</span></span>
-   <span data-ttu-id="5c67d-127">Proporcione una dirección URL de sustitución Web en el archivo. osdx con una plantilla de dirección URL con `format="text\html"` .</span><span class="sxs-lookup"><span data-stu-id="5c67d-127">Provide a web roll-over URL in the .osdx file using a URL template with `format="text\html"`.</span></span>
-   <span data-ttu-id="5c67d-128">Proporcione una dirección URL a la carpeta principal, el contenedor o la página web asignando un valor de dirección URL de elemento personalizado a la propiedad del shell de Windows [System. ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) .</span><span class="sxs-lookup"><span data-stu-id="5c67d-128">Provide a URL to the parent folder, container, or webpage by mapping a custom element URL value to the [System.ItemFolderPathDisplay](../properties/props-system-itempathdisplay.md) Windows Shell property.</span></span>

## <a name="best-practices-for-creating-rss-output"></a><span data-ttu-id="5c67d-129">Prácticas recomendadas para crear una salida RSS</span><span class="sxs-lookup"><span data-stu-id="5c67d-129">Best Practices for Creating RSS Output</span></span>

<span data-ttu-id="5c67d-130">Los procedimientos recomendados para crear la salida RSS son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="5c67d-130">Best practices for creating RSS output are as follows:</span></span>

-   <span data-ttu-id="5c67d-131">Cada elemento debe devolver una dirección URL `link` o un `enclosure` valor (o equivalente, como `media:content` )</span><span class="sxs-lookup"><span data-stu-id="5c67d-131">Each item MUST return a URL `link` or `enclosure` value (or equivalent, such as `media:content`)</span></span>
-   <span data-ttu-id="5c67d-132">No incluya etiquetas de formato HTML en el atributo de **título** , o esas etiquetas aparecerán en el título y se mostrarán en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67d-132">Do not include any HTML formatting tags in the **title** attribute, or those tags will appear in the title and be displayed in Windows Explorer.</span></span>
-   <span data-ttu-id="5c67d-133">Para el elemento **Description** :</span><span class="sxs-lookup"><span data-stu-id="5c67d-133">For the **description** element:</span></span>
    -   <span data-ttu-id="5c67d-134">Mostrar información suficiente para que el usuario sepa por qué este resultado podría ser pertinente.</span><span class="sxs-lookup"><span data-stu-id="5c67d-134">Show enough information so that the user knows why this result might be relevant.</span></span>
    -   <span data-ttu-id="5c67d-135">No incluya formato HTML.</span><span class="sxs-lookup"><span data-stu-id="5c67d-135">Do not include HTML formatting.</span></span> <span data-ttu-id="5c67d-136">El proveedor de [OpenSearch](https://github.com/dewitt/opensearch) quita el formato, lo que puede dar lugar a resultados menores que los deseados para la descripción.</span><span class="sxs-lookup"><span data-stu-id="5c67d-136">The [OpenSearch](https://github.com/dewitt/opensearch) provider removes the formatting, which might result in less than desirable results for your description.</span></span>
    -   <span data-ttu-id="5c67d-137">No incluya metadatos que ya se hayan proporcionado en otros elementos, como nombre de archivo de contenedor, tamaño, fecha de modificación, etc., porque el explorador de Windows ya muestra los metadatos.</span><span class="sxs-lookup"><span data-stu-id="5c67d-137">Do not include metadata that is already provided in other elements, such as enclosure file name, size, modified date, and so forth, because Windows Explorer already displays the metadata.</span></span> <span data-ttu-id="5c67d-138">Mostrarlo en el elemento de **Descripción** sería redundante.</span><span class="sxs-lookup"><span data-stu-id="5c67d-138">Displaying it in the **description** element would be redundant.</span></span>
-   <span data-ttu-id="5c67d-139">Para las direcciones URL de contenido o contenedor:</span><span class="sxs-lookup"><span data-stu-id="5c67d-139">For enclosure or content URLs:</span></span>
    -   <span data-ttu-id="5c67d-140">Especifique el atributo type como un tipo MIME válido.</span><span class="sxs-lookup"><span data-stu-id="5c67d-140">Specify the type attribute as a valid MIME type.</span></span>
    -   <span data-ttu-id="5c67d-141">Especifique el tamaño del archivo en bytes.</span><span class="sxs-lookup"><span data-stu-id="5c67d-141">Specify the file size in bytes.</span></span>
-   <span data-ttu-id="5c67d-142">Si va a implementar la salida RSS en .NET mediante `DateTime` , pruebe la fuente en Microsoft Internet Explorer para ver si es válida antes de implementarla en el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c67d-142">If you are implementing RSS output in .NET using `DateTime`, test your feed in Microsoft Internet Explorer to see if it is valid before deploying it to Windows Explorer.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5c67d-143">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5c67d-143">Additional Resources</span></span>

<span data-ttu-id="5c67d-144">Para obtener información adicional sobre la implementación de la Federación de búsqueda en almacenes de datos remotos mediante tecnologías de OpenSearch en Windows 7 y versiones posteriores, consulte "recursos adicionales" en [búsqueda federada en Windows](/previous-versions//dd742958(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5c67d-144">For additional information about implementing search federation to remote data stores using OpenSearch technologies in Windows 7 and later, see "Additional Resources" at [Federated Search in Windows](/previous-versions//dd742958(v=vs.85)).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c67d-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c67d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c67d-146">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-146">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="5c67d-147">Introducción con búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-147">Getting Started with Federated Search in Windows</span></span>](getting-started-with-federated-search-in-windows.md)
</dt> <dt>

[<span data-ttu-id="5c67d-148">Conexión del servicio Web en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-148">Connecting Your Web Service in Windows Federated Search</span></span>](-search-federated-search-web-service.md)
</dt> <dt>

[<span data-ttu-id="5c67d-149">Habilitación del almacén de datos en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-149">Enabling Your Data Store in Windows Federated Search</span></span>](-search-federated-search-data-store.md)
</dt> <dt>

[<span data-ttu-id="5c67d-150">Creación de un archivo de descripción de OpenSearch en Windows Federated Search</span><span class="sxs-lookup"><span data-stu-id="5c67d-150">Creating an OpenSearch Description File in Windows Federated Search</span></span>](-search-federated-search-osdx-file.md)
</dt> <dt>

[<span data-ttu-id="5c67d-151">Implementación de conectores de búsqueda en la búsqueda federada de Windows</span><span class="sxs-lookup"><span data-stu-id="5c67d-151">Deploying Search Connectors in Windows Federated Search</span></span>](-search-federated-search-deploying.md)
</dt> <dt>

[<span data-ttu-id="5c67d-152">Extender el índice</span><span class="sxs-lookup"><span data-stu-id="5c67d-152">Extending the Index</span></span>](-search-3x-wds-extidx-overview.md)
</dt> </dl>

 

 
