---
description: En el ejemplo de código IFilterSample se muestra cómo crear una clase base de IFilter para implementar la interfaz IFilter.
ms.assetid: 4c0df747-627d-4937-a117-d43137d5d081
title: IFilterSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10f66bf32c4abe25038aa6b2a3b6d879ba65cf7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696288"
---
# <a name="ifiltersample"></a><span data-ttu-id="95c3f-103">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="95c3f-103">IFilterSample</span></span>

<span data-ttu-id="95c3f-104">En el ejemplo de código IFilterSample se muestra cómo crear una clase base de IFilter para implementar la interfaz [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) .</span><span class="sxs-lookup"><span data-stu-id="95c3f-104">The IFilterSample code sample demonstrates how to create an IFilter base class for implementing the [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) interface.</span></span>

<span data-ttu-id="95c3f-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="95c3f-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="95c3f-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c3f-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="95c3f-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="95c3f-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="95c3f-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="95c3f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95c3f-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="95c3f-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95c3f-111">Requirements</span></span>

| <span data-ttu-id="95c3f-112">Producto</span><span class="sxs-lookup"><span data-stu-id="95c3f-112">Product</span></span>     | <span data-ttu-id="95c3f-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="95c3f-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="95c3f-114">Windows</span><span class="sxs-lookup"><span data-stu-id="95c3f-114">Windows</span></span>     | <span data-ttu-id="95c3f-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="95c3f-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="95c3f-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="95c3f-116">Windows SDK</span></span> | <span data-ttu-id="95c3f-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="95c3f-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="95c3f-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-118">Downloading the Sample</span></span>

<span data-ttu-id="95c3f-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="95c3f-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="95c3f-120">Location</span><span class="sxs-lookup"><span data-stu-id="95c3f-120">Location</span></span>      | <span data-ttu-id="95c3f-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="95c3f-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="95c3f-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="95c3f-122">GitHub</span></span>        | [<span data-ttu-id="95c3f-123">IFilterSample</span><span class="sxs-lookup"><span data-stu-id="95c3f-123">IFilterSample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)          |

> [!NOTE]  
> <span data-ttu-id="95c3f-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="95c3f-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="95c3f-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-125">Building the Sample</span></span>

1. <span data-ttu-id="95c3f-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **FilterBase** .</span><span class="sxs-lookup"><span data-stu-id="95c3f-126">Open Windows Explorer and navigate to the **FilterBase** project directory.</span></span>
2. <span data-ttu-id="95c3f-127">Haga doble clic en el icono del archivo FilterBase. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="95c3f-127">Double-click the icon for the FilterBase.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="95c3f-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="95c3f-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="95c3f-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="95c3f-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="95c3f-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="95c3f-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="95c3f-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95c3f-131">Running the Sample</span></span>

1. <span data-ttu-id="95c3f-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="95c3f-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="95c3f-133">En el símbolo del sistema, escriba `FilterBase.exe` o, en el explorador de Windows, haga doble clic en el icono de FilterBase.exe.</span><span class="sxs-lookup"><span data-stu-id="95c3f-133">At the command prompt, enter `FilterBase.exe`, or from Windows Explorer, double-click the icon for FilterBase.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95c3f-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95c3f-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="95c3f-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="95c3f-135">Reference</span></span>

[<span data-ttu-id="95c3f-136">**Imaging**</span><span class="sxs-lookup"><span data-stu-id="95c3f-136">**IFilter**</span></span>](/windows/win32/api/filter/nn-filter-ifilter)

### <a name="conceptual"></a><span data-ttu-id="95c3f-137">Conceptual</span><span class="sxs-lookup"><span data-stu-id="95c3f-137">Conceptual</span></span>

[<span data-ttu-id="95c3f-138">Desarrollar controladores de filtro</span><span class="sxs-lookup"><span data-stu-id="95c3f-138">Developing Filter Handlers</span></span>](-search-ifilter-conceptual.md)

### <a name="other-samples"></a><span data-ttu-id="95c3f-139">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="95c3f-139">Other Samples</span></span>

[<span data-ttu-id="95c3f-140">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="95c3f-140">Search Code Samples</span></span>](-search-samples-ovw.md)
