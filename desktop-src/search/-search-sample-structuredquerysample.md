---
description: En el ejemplo de código StructuredQuerySample se muestra cómo leer líneas de la consola, analizarlas con el esquema del sistema y mostrar los árboles de condiciones resultantes.
ms.assetid: 9bb56d80-670e-4b2b-bf3f-40d0a75a89b6
title: StructuredQuerySample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64da74b56658f74b056c64c314a2986ddce45ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696285"
---
# <a name="structuredquerysample"></a><span data-ttu-id="01d16-103">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="01d16-103">StructuredQuerySample</span></span>

<span data-ttu-id="01d16-104">En el ejemplo de código StructuredQuerySample se muestra cómo leer líneas de la consola, analizarlas con el esquema del sistema y mostrar los árboles de condiciones resultantes.</span><span class="sxs-lookup"><span data-stu-id="01d16-104">The StructuredQuerySample code sample demonstrates how to read lines from the console, parse them using the system schema, and display the resulting condition trees.</span></span>

<span data-ttu-id="01d16-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="01d16-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="01d16-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d16-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="01d16-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="01d16-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="01d16-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="01d16-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01d16-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="01d16-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01d16-111">Requirements</span></span>

| <span data-ttu-id="01d16-112">Producto</span><span class="sxs-lookup"><span data-stu-id="01d16-112">Product</span></span>     | <span data-ttu-id="01d16-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="01d16-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="01d16-114">Windows</span><span class="sxs-lookup"><span data-stu-id="01d16-114">Windows</span></span>     | <span data-ttu-id="01d16-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="01d16-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="01d16-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="01d16-116">Windows SDK</span></span> | <span data-ttu-id="01d16-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="01d16-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="01d16-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-118">Downloading the Sample</span></span>

<span data-ttu-id="01d16-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="01d16-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="01d16-120">Location</span><span class="sxs-lookup"><span data-stu-id="01d16-120">Location</span></span>      | <span data-ttu-id="01d16-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="01d16-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="01d16-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="01d16-122">GitHub</span></span>        | [<span data-ttu-id="01d16-123">StructuredQuerySample</span><span class="sxs-lookup"><span data-stu-id="01d16-123">StructuredQuerySample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/StructuredQuerySample)  |

> [!NOTE]  
> <span data-ttu-id="01d16-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="01d16-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="01d16-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-125">Building the Sample</span></span>

1. <span data-ttu-id="01d16-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **StructuredQuerySample** .</span><span class="sxs-lookup"><span data-stu-id="01d16-126">Open Windows Explorer and navigate to the **StructuredQuerySample** project directory.</span></span>
2. <span data-ttu-id="01d16-127">Haga doble clic en el icono del archivo StructuredQuerySample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="01d16-127">Double-click the icon for the StructuredQuerySample.sln file to open the project in Visual Studio.</span></span>

    > [!NOTE]  
    > <span data-ttu-id="01d16-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="01d16-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="01d16-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="01d16-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="01d16-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="01d16-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="01d16-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="01d16-131">Running the Sample</span></span>

1. <span data-ttu-id="01d16-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="01d16-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="01d16-133">En el símbolo del sistema, escriba `StructuredQuerySample.exe` o, en el explorador de Windows, haga doble clic en el icono de StructuredQuerySample.exe.</span><span class="sxs-lookup"><span data-stu-id="01d16-133">At the command prompt, enter `StructuredQuerySample.exe`, or from Windows Explorer, double-click the icon for StructuredQuerySample.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="01d16-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="01d16-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="01d16-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="01d16-135">Reference</span></span>

[<span data-ttu-id="01d16-136">**ICondition**</span><span class="sxs-lookup"><span data-stu-id="01d16-136">**ICondition**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition)

[<span data-ttu-id="01d16-137">**ICondition2**</span><span class="sxs-lookup"><span data-stu-id="01d16-137">**ICondition2**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-icondition2)

[<span data-ttu-id="01d16-138">**IConditionFactory**</span><span class="sxs-lookup"><span data-stu-id="01d16-138">**IConditionFactory**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory)

[<span data-ttu-id="01d16-139">**IConditionFactory2**</span><span class="sxs-lookup"><span data-stu-id="01d16-139">**IConditionFactory2**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditionfactory2)

[<span data-ttu-id="01d16-140">**IConditionGenerator**</span><span class="sxs-lookup"><span data-stu-id="01d16-140">**IConditionGenerator**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iconditiongenerator)

[<span data-ttu-id="01d16-141">**IQueryParser**</span><span class="sxs-lookup"><span data-stu-id="01d16-141">**IQueryParser**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparser)

[<span data-ttu-id="01d16-142">**IQueryParserManager**</span><span class="sxs-lookup"><span data-stu-id="01d16-142">**IQueryParserManager**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iqueryparsermanager)

[<span data-ttu-id="01d16-143">**IQuerySolution**</span><span class="sxs-lookup"><span data-stu-id="01d16-143">**IQuerySolution**</span></span>](/windows/desktop/api/Structuredquery/nn-structuredquery-iquerysolution)

### <a name="other-samples"></a><span data-ttu-id="01d16-144">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="01d16-144">Other Samples</span></span>

[<span data-ttu-id="01d16-145">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="01d16-145">Search Code Samples</span></span>](-search-samples-ovw.md)
