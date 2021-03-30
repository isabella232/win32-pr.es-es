---
description: En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y se muestran dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907747"
---
# <a name="wsoledb"></a><span data-ttu-id="08fc7-103">WSOleDB</span><span class="sxs-lookup"><span data-stu-id="08fc7-103">WSOleDB</span></span>

<span data-ttu-id="08fc7-104">En el ejemplo de código WSOleDB se muestra Active Template Library (ATL) OLE DB el acceso a las aplicaciones de Windows Search y se muestran dos métodos adicionales para recuperar los resultados de la búsqueda de Windows.</span><span class="sxs-lookup"><span data-stu-id="08fc7-104">The WSOleDB code sample demonstrates Active Template Library (ATL) OLE DB access to Windows Search applications, and demonstrates two additional methods for retrieving results from Windows Search.</span></span>

<span data-ttu-id="08fc7-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="08fc7-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="08fc7-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08fc7-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="08fc7-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="08fc7-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="08fc7-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="08fc7-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08fc7-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="08fc7-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08fc7-111">Requirements</span></span>

| <span data-ttu-id="08fc7-112">Producto</span><span class="sxs-lookup"><span data-stu-id="08fc7-112">Product</span></span>     | <span data-ttu-id="08fc7-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="08fc7-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="08fc7-114">Windows</span><span class="sxs-lookup"><span data-stu-id="08fc7-114">Windows</span></span>     | <span data-ttu-id="08fc7-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="08fc7-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="08fc7-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="08fc7-116">Windows SDK</span></span> | <span data-ttu-id="08fc7-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="08fc7-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="08fc7-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-118">Downloading the Sample</span></span>

<span data-ttu-id="08fc7-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="08fc7-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="08fc7-120">Location</span><span class="sxs-lookup"><span data-stu-id="08fc7-120">Location</span></span>      | <span data-ttu-id="08fc7-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="08fc7-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="08fc7-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="08fc7-122">GitHub</span></span>        | [<span data-ttu-id="08fc7-123">Ejemplo de WSOleDB</span><span class="sxs-lookup"><span data-stu-id="08fc7-123">WSOleDB sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> <span data-ttu-id="08fc7-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="08fc7-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="08fc7-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-125">Building the Sample</span></span>

1. <span data-ttu-id="08fc7-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **WSOleDB** .</span><span class="sxs-lookup"><span data-stu-id="08fc7-126">Open Windows Explorer and navigate to the **WSOleDB** project directory.</span></span>
2. <span data-ttu-id="08fc7-127">Haga doble clic en el icono del archivo WSOleDB. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="08fc7-127">Double-click the icon for the WSOleDB.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="08fc7-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="08fc7-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="08fc7-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="08fc7-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="08fc7-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="08fc7-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="08fc7-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="08fc7-131">Running the Sample</span></span>

1. <span data-ttu-id="08fc7-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="08fc7-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="08fc7-133">En el símbolo del sistema, escriba `WSOleDB.exe` o, en el explorador de Windows, haga doble clic en el icono de WSOleDB.exe.</span><span class="sxs-lookup"><span data-stu-id="08fc7-133">At the command prompt, enter `WSOleDB.exe`, or from Windows Explorer, double-click the icon for WSOleDB.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08fc7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="08fc7-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="08fc7-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="08fc7-135">Reference</span></span>

[<span data-ttu-id="08fc7-136">**ISearchCatalogManager**</span><span class="sxs-lookup"><span data-stu-id="08fc7-136">**ISearchCatalogManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[<span data-ttu-id="08fc7-137">**ISearchCatalogManager2**</span><span class="sxs-lookup"><span data-stu-id="08fc7-137">**ISearchCatalogManager2**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[<span data-ttu-id="08fc7-138">**ISearchManager**</span><span class="sxs-lookup"><span data-stu-id="08fc7-138">**ISearchManager**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[<span data-ttu-id="08fc7-139">**IPropertyStore**</span><span class="sxs-lookup"><span data-stu-id="08fc7-139">**IPropertyStore**</span></span>](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a><span data-ttu-id="08fc7-140">Conceptual</span><span class="sxs-lookup"><span data-stu-id="08fc7-140">Conceptual</span></span>

[<span data-ttu-id="08fc7-141">Información general sobre la programación de OLE DB</span><span class="sxs-lookup"><span data-stu-id="08fc7-141">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="08fc7-142">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="08fc7-142">Other Samples</span></span>

[<span data-ttu-id="08fc7-143">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="08fc7-143">Search Code Samples</span></span>](-search-samples-ovw.md)
