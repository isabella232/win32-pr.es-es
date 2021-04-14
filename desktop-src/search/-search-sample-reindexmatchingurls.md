---
description: 'En el ejemplo de código ReindexMatchingUrls se muestra cómo proporcionar tres maneras de especificar los archivos que se van a volver a indizar: las direcciones URL que coinciden con un tipo de archivo, un tipo MIME o una cláusula WHERE especificada.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497068"
---
# <a name="reindexmatchingurls"></a><span data-ttu-id="ac375-103">ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="ac375-103">ReindexMatchingUrls</span></span>

<span data-ttu-id="ac375-104">En el ejemplo de código ReindexMatchingUrls se muestra cómo proporcionar tres maneras de especificar los archivos que se van a volver a indizar: las direcciones URL que coinciden con un tipo de archivo, un tipo MIME o una cláusula WHERE especificada.</span><span class="sxs-lookup"><span data-stu-id="ac375-104">The ReindexMatchingUrls code sample demonstrates how to provide three ways to specify the files to re-index: URLs that match a file type, mime type, or a specified WHERE clause.</span></span>

<span data-ttu-id="ac375-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="ac375-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="ac375-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac375-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="ac375-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="ac375-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="ac375-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="ac375-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac375-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="ac375-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ac375-111">Requirements</span></span>

| <span data-ttu-id="ac375-112">Producto</span><span class="sxs-lookup"><span data-stu-id="ac375-112">Product</span></span>     | <span data-ttu-id="ac375-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="ac375-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="ac375-114">Windows</span><span class="sxs-lookup"><span data-stu-id="ac375-114">Windows</span></span>     | <span data-ttu-id="ac375-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="ac375-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="ac375-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="ac375-116">Windows SDK</span></span> | <span data-ttu-id="ac375-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="ac375-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="ac375-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-118">Downloading the Sample</span></span>

<span data-ttu-id="ac375-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="ac375-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="ac375-120">Location</span><span class="sxs-lookup"><span data-stu-id="ac375-120">Location</span></span>      | <span data-ttu-id="ac375-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="ac375-121">Path URL</span></span>                                                                      |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="ac375-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="ac375-122">GitHub</span></span>  | [<span data-ttu-id="ac375-123">Ejemplo de ReindexMatchingUrls</span><span class="sxs-lookup"><span data-stu-id="ac375-123">ReindexMatchingUrls sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> <span data-ttu-id="ac375-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="ac375-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="ac375-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-125">Building the Sample</span></span>

1. <span data-ttu-id="ac375-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **ReindexMatchingUrls** .</span><span class="sxs-lookup"><span data-stu-id="ac375-126">Open Windows Explorer and navigate to the **ReindexMatchingUrls** project directory.</span></span> <span data-ttu-id="ac375-127">Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .</span><span class="sxs-lookup"><span data-stu-id="ac375-127">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls`.</span></span>
2. <span data-ttu-id="ac375-128">Haga doble clic en el icono del archivo REINDEX. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="ac375-128">Double-click the icon for the Reindex.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="ac375-129">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="ac375-129">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="ac375-130">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="ac375-130">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="ac375-131">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="ac375-131">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="ac375-132">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ac375-132">Running the Sample</span></span>

1. <span data-ttu-id="ac375-133">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="ac375-133">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="ac375-134">En el símbolo del sistema, escriba `Reindex.exe` o, en el explorador de Windows, haga doble clic en el icono de Reindex.exe.</span><span class="sxs-lookup"><span data-stu-id="ac375-134">At the command prompt, enter `Reindex.exe`, or from Windows Explorer, double-click the icon for Reindex.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac375-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac375-135">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="ac375-136">Referencia</span><span class="sxs-lookup"><span data-stu-id="ac375-136">Reference</span></span>

[<span data-ttu-id="ac375-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="ac375-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="ac375-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="ac375-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="ac375-139">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="ac375-139">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="ac375-140">**ISearchPersistentItemsChangedSink**</span><span class="sxs-lookup"><span data-stu-id="ac375-140">**ISearchPersistentItemsChangedSink**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[<span data-ttu-id="ac375-141">**ISearchViewChangedSink**</span><span class="sxs-lookup"><span data-stu-id="ac375-141">**ISearchViewChangedSink**</span></span>](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[<span data-ttu-id="ac375-142">**PRIORIZAr \_ marcas**</span><span class="sxs-lookup"><span data-stu-id="ac375-142">**PRIORITIZE\_FLAGS**</span></span>](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a><span data-ttu-id="ac375-143">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="ac375-143">Other Samples</span></span>

[<span data-ttu-id="ac375-144">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="ac375-144">Search Code Samples</span></span>](-search-samples-ovw.md)
