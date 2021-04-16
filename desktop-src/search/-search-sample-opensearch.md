---
description: En el ejemplo de código OpenSearch se muestra cómo crear un servicio de búsqueda federado mediante el protocolo OpenSearch y un archivo de descriptor de OpenSearch (. osdx) (un conector de búsqueda).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423727"
---
# <a name="opensearch"></a><span data-ttu-id="464b6-103">OpenSearch</span><span class="sxs-lookup"><span data-stu-id="464b6-103">OpenSearch</span></span>

<span data-ttu-id="464b6-104">En el ejemplo de código OpenSearch se muestra cómo crear un servicio de búsqueda federado mediante el protocolo [OpenSearch](https://github.com/dewitt/opensearch) y un archivo de descriptor de OpenSearch (. osdx) (un conector de búsqueda).</span><span class="sxs-lookup"><span data-stu-id="464b6-104">The OpenSearch code sample demonstrates how to create a federated search service using the [OpenSearch](https://github.com/dewitt/opensearch) protocol, and an OpenSearch Descriptor (.osdx) file (a search connector).</span></span>

<span data-ttu-id="464b6-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="464b6-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="464b6-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="464b6-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="464b6-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="464b6-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="464b6-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-109">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="464b6-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="464b6-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="464b6-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="464b6-111">Requirements</span></span>



| <span data-ttu-id="464b6-112">Producto</span><span class="sxs-lookup"><span data-stu-id="464b6-112">Product</span></span>     | <span data-ttu-id="464b6-113">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="464b6-113">Minimum Product Version</span></span> |
|-------------|-------------------------|
| <span data-ttu-id="464b6-114">Windows</span><span class="sxs-lookup"><span data-stu-id="464b6-114">Windows</span></span>     | <span data-ttu-id="464b6-115">Windows 7</span><span class="sxs-lookup"><span data-stu-id="464b6-115">Windows 7</span></span>               |
| <span data-ttu-id="464b6-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="464b6-116">Windows SDK</span></span> | <span data-ttu-id="464b6-117">7.0</span><span class="sxs-lookup"><span data-stu-id="464b6-117">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="464b6-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-118">Downloading the Sample</span></span>

<span data-ttu-id="464b6-119">Este ejemplo está disponible en las siguientes ubicaciones.</span><span class="sxs-lookup"><span data-stu-id="464b6-119">This sample is available in the following locations.</span></span>



| <span data-ttu-id="464b6-120">Location</span><span class="sxs-lookup"><span data-stu-id="464b6-120">Location</span></span>      | <span data-ttu-id="464b6-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="464b6-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="464b6-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="464b6-122">GitHub</span></span>  | [<span data-ttu-id="464b6-123">Ejemplo de OpenSearch</span><span class="sxs-lookup"><span data-stu-id="464b6-123">OpenSearch sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> <span data-ttu-id="464b6-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="464b6-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

 

## <a name="building-the-sample"></a><span data-ttu-id="464b6-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-125">Building the Sample</span></span>

<span data-ttu-id="464b6-126">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="464b6-126">To build the sample from the Command Prompt:</span></span>

1.  <span data-ttu-id="464b6-127">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="464b6-127">Open the Command Prompt window and navigate to the **AdventureSearch** project directory.</span></span> 
2.  <span data-ttu-id="464b6-128">Escriba `msbuild AdventureSearch.sln`.</span><span class="sxs-lookup"><span data-stu-id="464b6-128">Enter `msbuild AdventureSearch.sln`.</span></span>

<span data-ttu-id="464b6-129">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="464b6-129">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="464b6-130">Abra el explorador de Windows y navegue hasta el directorio del proyecto **AdventureSearch** .</span><span class="sxs-lookup"><span data-stu-id="464b6-130">Open Windows Explorer and navigate to the **AdventureSearch** project directory.</span></span>
2.  <span data-ttu-id="464b6-131">Haga doble clic en el icono del archivo AdventureSearch. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="464b6-131">Double-click the icon for the AdventureSearch.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="464b6-132">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="464b6-132">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="464b6-133">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="464b6-133">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="464b6-134">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="464b6-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="464b6-135">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="464b6-135">Running the Sample</span></span>

1.  <span data-ttu-id="464b6-136">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="464b6-136">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="464b6-137">En el símbolo del sistema, escriba `AdventureSearch.exe` o, en el explorador de Windows, haga doble clic en el icono de AdventureSearch.exe.</span><span class="sxs-lookup"><span data-stu-id="464b6-137">At the command prompt, enter `AdventureSearch.exe`, or from Windows Explorer, double-click the icon for AdventureSearch.exe.</span></span>
3.  <span data-ttu-id="464b6-138">En el símbolo del sistema, escriba `GetOSDX.exe` o, en el explorador de Windows, haga doble clic en el icono de GetOSDX.exe.</span><span class="sxs-lookup"><span data-stu-id="464b6-138">At the command prompt, enter `GetOSDX.exe`, or from Windows Explorer, double-click the icon for GetOSDX.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="464b6-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="464b6-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="464b6-140">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="464b6-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="464b6-141">Información general sobre el esquema de Descripción del conector de búsqueda</span><span class="sxs-lookup"><span data-stu-id="464b6-141">Overview of the Search Connector Description Schema</span></span>](search-sconn-desc-schema-entry.md)
</dt> <dt>

<span data-ttu-id="464b6-142">**Vista**</span><span class="sxs-lookup"><span data-stu-id="464b6-142">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="464b6-143">Búsqueda federada en Windows</span><span class="sxs-lookup"><span data-stu-id="464b6-143">Federated Search in Windows</span></span>](-search-federated-search-overview.md)
</dt> <dt>

[<span data-ttu-id="464b6-144">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="464b6-144">Search Code Samples</span></span>](-search-samples-ovw.md)
</dt> <dt>

<span data-ttu-id="464b6-145">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="464b6-145">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="464b6-146">Esquema de descripción de biblioteca</span><span class="sxs-lookup"><span data-stu-id="464b6-146">Library Description Schema</span></span>](../shell/library-schema-entry.md)
</dt> </dl>

 

 
