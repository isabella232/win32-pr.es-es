---
description: En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907746"
---
# <a name="wssql"></a><span data-ttu-id="37f25-103">WSSQL</span><span class="sxs-lookup"><span data-stu-id="37f25-103">WSSQL</span></span>

<span data-ttu-id="37f25-104">En el ejemplo de código WSSQL se muestra cómo comunicarse entre Microsoft OLE DB y Windows Search a través de Lenguaje de consulta estructurado (SQL).</span><span class="sxs-lookup"><span data-stu-id="37f25-104">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through Structured Query Language (SQL).</span></span>

<span data-ttu-id="37f25-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="37f25-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="37f25-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f25-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="37f25-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="37f25-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="37f25-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="37f25-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37f25-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="37f25-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37f25-111">Requirements</span></span>

| <span data-ttu-id="37f25-112">Producto</span><span class="sxs-lookup"><span data-stu-id="37f25-112">Product</span></span>     | <span data-ttu-id="37f25-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="37f25-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="37f25-114">Windows</span><span class="sxs-lookup"><span data-stu-id="37f25-114">Windows</span></span>     | <span data-ttu-id="37f25-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="37f25-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="37f25-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="37f25-116">Windows SDK</span></span> | <span data-ttu-id="37f25-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="37f25-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="37f25-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-118">Downloading the Sample</span></span>

<span data-ttu-id="37f25-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="37f25-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="37f25-120">Location</span><span class="sxs-lookup"><span data-stu-id="37f25-120">Location</span></span>      | <span data-ttu-id="37f25-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="37f25-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="37f25-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="37f25-122">GitHub</span></span>        | [<span data-ttu-id="37f25-123">Ejemplo de WSSQL</span><span class="sxs-lookup"><span data-stu-id="37f25-123">WSSQL sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> <span data-ttu-id="37f25-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="37f25-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="37f25-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-125">Building the Sample</span></span>

1. <span data-ttu-id="37f25-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **WSSQL** .</span><span class="sxs-lookup"><span data-stu-id="37f25-126">Open Windows Explorer and navigate to the **WSSQL** project directory.</span></span>
2. <span data-ttu-id="37f25-127">Haga doble clic en el icono del archivo WSSQL. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="37f25-127">Double-click the icon for the WSSQL.sln file to open the project in Visual Studio.</span></span>
    > [!NOTE]  
    > <span data-ttu-id="37f25-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="37f25-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="37f25-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="37f25-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="37f25-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="37f25-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="37f25-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="37f25-131">Running the Sample</span></span>

1. <span data-ttu-id="37f25-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="37f25-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="37f25-133">En el símbolo del sistema, escriba `WSSQL.exe` o, en el explorador de Windows, haga doble clic en el icono de WSSQL.exe.</span><span class="sxs-lookup"><span data-stu-id="37f25-133">At the command prompt, enter `WSSQL.exe`, or from Windows Explorer, double-click the icon for WSSQL.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="37f25-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="37f25-134">Related topics</span></span>

### <a name="conceptual"></a><span data-ttu-id="37f25-135">Conceptual</span><span class="sxs-lookup"><span data-stu-id="37f25-135">Conceptual</span></span>

[<span data-ttu-id="37f25-136">Usar la sintaxis SQL de búsqueda de Windows</span><span class="sxs-lookup"><span data-stu-id="37f25-136">Using Windows Search SQL Syntax</span></span>](-search-sql-windowssearch-entry.md)

[<span data-ttu-id="37f25-137">Información general del lenguaje de consulta</span><span class="sxs-lookup"><span data-stu-id="37f25-137">General Query Language Information</span></span>](-search-sql-generalqueryinfo.md)

[<span data-ttu-id="37f25-138">Información general sobre la programación de OLE DB</span><span class="sxs-lookup"><span data-stu-id="37f25-138">OLE DB Programming Overview</span></span>](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a><span data-ttu-id="37f25-139">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="37f25-139">Other Samples</span></span>

[<span data-ttu-id="37f25-140">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="37f25-140">Search Code Samples</span></span>](-search-samples-ovw.md)
