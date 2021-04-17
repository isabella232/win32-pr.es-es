---
description: En el ejemplo de código DSearch se muestra cómo crear una clase para que una aplicación de consola estática consulte en Windows Search mediante el ensamblado Microsoft. Search. Interop para ISearchQueryHelper.
ms.assetid: 9c09b1fe-c63e-4c6e-9c8b-f5e29cf0fe9e
title: DSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4285596a8109361accd6b3adecf80ea98074e55e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696289"
---
# <a name="dsearch"></a><span data-ttu-id="b75de-103">DSearch</span><span class="sxs-lookup"><span data-stu-id="b75de-103">DSearch</span></span>

<span data-ttu-id="b75de-104">En el ejemplo de código DSearch se muestra cómo crear una clase para que una aplicación de consola estática consulte en Windows Search mediante el ensamblado Microsoft. Search. Interop para [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span><span class="sxs-lookup"><span data-stu-id="b75de-104">The DSearch code sample demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for [**ISearchQueryHelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper).</span></span>

<span data-ttu-id="b75de-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="b75de-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="b75de-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b75de-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="b75de-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="b75de-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="b75de-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="b75de-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b75de-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="b75de-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b75de-111">Requirements</span></span>

| <span data-ttu-id="b75de-112">Producto</span><span class="sxs-lookup"><span data-stu-id="b75de-112">Product</span></span>     | <span data-ttu-id="b75de-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="b75de-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="b75de-114">Windows</span><span class="sxs-lookup"><span data-stu-id="b75de-114">Windows</span></span>     | <span data-ttu-id="b75de-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="b75de-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="b75de-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="b75de-116">Windows SDK</span></span> | <span data-ttu-id="b75de-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="b75de-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="b75de-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-118">Downloading the Sample</span></span>

<span data-ttu-id="b75de-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="b75de-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="b75de-120">Location</span><span class="sxs-lookup"><span data-stu-id="b75de-120">Location</span></span>      | <span data-ttu-id="b75de-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="b75de-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b75de-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="b75de-122">GitHub</span></span>        | [<span data-ttu-id="b75de-123">Ejemplo de DSearch</span><span class="sxs-lookup"><span data-stu-id="b75de-123">DSearch sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/DSearch)         |

> [!NOTE]  
> <span data-ttu-id="b75de-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="b75de-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="b75de-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-125">Building the Sample</span></span>

1. <span data-ttu-id="b75de-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **DSearch** .</span><span class="sxs-lookup"><span data-stu-id="b75de-126">Open Windows Explorer and navigate to the **DSearch** project directory.</span></span>
2. <span data-ttu-id="b75de-127">Haga doble clic en el icono del archivo DSearch. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b75de-127">Double-click the icon for the DSearch.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="b75de-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="b75de-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="b75de-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b75de-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="b75de-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="b75de-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="b75de-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="b75de-131">Running the Sample</span></span>

1. <span data-ttu-id="b75de-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="b75de-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="b75de-133">En el símbolo del sistema, escriba `DSearch.exe` o, en el explorador de Windows, haga doble clic en el icono de DSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="b75de-133">At the command prompt, enter `DSearch.exe`, or from Windows Explorer, double-click the icon for DSearch.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b75de-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b75de-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="b75de-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="b75de-135">Reference</span></span>

[<span data-ttu-id="b75de-136">**ISearchQueryHelper**</span><span class="sxs-lookup"><span data-stu-id="b75de-136">**ISearchQueryHelper**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)

[<span data-ttu-id="b75de-137">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="b75de-137">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="b75de-138">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="b75de-138">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

### <a name="other-samples"></a><span data-ttu-id="b75de-139">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="b75de-139">Other Samples</span></span>

[<span data-ttu-id="b75de-140">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="b75de-140">Search Code Samples</span></span>](-search-samples-ovw.md)
