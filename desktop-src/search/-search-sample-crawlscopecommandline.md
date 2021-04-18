---
description: En el ejemplo de código CrawlScopeCommandLine se muestra cómo definir las opciones de la línea de comandos para las operaciones de indización del administrador de ámbito de rastreo (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715013"
---
# <a name="crawlscopecommandline"></a><span data-ttu-id="04da4-103">CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="04da4-103">CrawlScopeCommandLine</span></span>

<span data-ttu-id="04da4-104">En el ejemplo de código CrawlScopeCommandLine se muestra cómo definir las opciones de la línea de comandos para las operaciones de indización del administrador de ámbito de rastreo (CSM).</span><span class="sxs-lookup"><span data-stu-id="04da4-104">The CrawlScopeCommandLine code sample demonstrates how to define command line options for Crawl Scope Manager (CSM) indexing operations.</span></span>

<span data-ttu-id="04da4-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="04da4-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="04da4-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04da4-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="04da4-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="04da4-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="04da4-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="04da4-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04da4-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="04da4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="04da4-111">Requirements</span></span>

| <span data-ttu-id="04da4-112">Producto</span><span class="sxs-lookup"><span data-stu-id="04da4-112">Product</span></span>     | <span data-ttu-id="04da4-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="04da4-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="04da4-114">Windows</span><span class="sxs-lookup"><span data-stu-id="04da4-114">Windows</span></span>     | <span data-ttu-id="04da4-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="04da4-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="04da4-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="04da4-116">Windows SDK</span></span> | <span data-ttu-id="04da4-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="04da4-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="04da4-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-118">Downloading the Sample</span></span>

<span data-ttu-id="04da4-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="04da4-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="04da4-120">Location</span><span class="sxs-lookup"><span data-stu-id="04da4-120">Location</span></span> | <span data-ttu-id="04da4-121">Ruta de acceso o dirección URL</span><span class="sxs-lookup"><span data-stu-id="04da4-121">Path or URL</span></span>                                                                |
|----------|----------------------------------------------------------------------------|
| <span data-ttu-id="04da4-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="04da4-122">GitHub</span></span>   |    [<span data-ttu-id="04da4-123">Ejemplo de CrawlScopeCommandLine</span><span class="sxs-lookup"><span data-stu-id="04da4-123">CrawlScopeCommandLine sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> <span data-ttu-id="04da4-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="04da4-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="04da4-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-125">Building the Sample</span></span>

1. <span data-ttu-id="04da4-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **CrawlScopeCommandLine** .</span><span class="sxs-lookup"><span data-stu-id="04da4-126">Open Windows Explorer and navigate to the **CrawlScopeCommandLine** project directory.</span></span>
2. <span data-ttu-id="04da4-127">Haga doble clic en el icono del archivo csmcmd. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="04da4-127">Double-click the icon for the csmcmd.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="04da4-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="04da4-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="04da4-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="04da4-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="04da4-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="04da4-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="04da4-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="04da4-131">Running the Sample</span></span>

1. <span data-ttu-id="04da4-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="04da4-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="04da4-133">En el símbolo del sistema, escriba `csmcmd.exe` o, en el explorador de Windows, haga doble clic en el icono de csmcmd.exe.</span><span class="sxs-lookup"><span data-stu-id="04da4-133">At the command prompt, enter `csmcmd.exe`, or from Windows Explorer, double-click the icon for csmcmd.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="04da4-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="04da4-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="04da4-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="04da4-135">Reference</span></span>

[<span data-ttu-id="04da4-136">**IEnumSearchRoots**</span><span class="sxs-lookup"><span data-stu-id="04da4-136">**IEnumSearchRoots**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[<span data-ttu-id="04da4-137">**IEnumSearchScopeRules**</span><span class="sxs-lookup"><span data-stu-id="04da4-137">**IEnumSearchScopeRules**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[<span data-ttu-id="04da4-138">**ISearchCrawlScopeManager**</span><span class="sxs-lookup"><span data-stu-id="04da4-138">**ISearchCrawlScopeManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[<span data-ttu-id="04da4-139">**ISearchCrawlScopeManager2**</span><span class="sxs-lookup"><span data-stu-id="04da4-139">**ISearchCrawlScopeManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[<span data-ttu-id="04da4-140">**ISearchRoot**</span><span class="sxs-lookup"><span data-stu-id="04da4-140">**ISearchRoot**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[<span data-ttu-id="04da4-141">**ISearchScopeRule**</span><span class="sxs-lookup"><span data-stu-id="04da4-141">**ISearchScopeRule**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[<span data-ttu-id="04da4-142">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="04da4-142">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="04da4-143">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="04da4-143">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="04da4-144">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="04da4-144">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a><span data-ttu-id="04da4-145">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="04da4-145">Other Samples</span></span>

[<span data-ttu-id="04da4-146">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="04da4-146">Search Code Samples</span></span>](-search-samples-ovw.md)
