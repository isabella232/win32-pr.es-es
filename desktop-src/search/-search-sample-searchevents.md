---
description: En el ejemplo de código SearchEvents se muestra cómo priorizar eventos de indización.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696284"
---
# <a name="searchevents"></a><span data-ttu-id="1fc56-103">SearchEvents</span><span class="sxs-lookup"><span data-stu-id="1fc56-103">SearchEvents</span></span>

<span data-ttu-id="1fc56-104">En el ejemplo de código SearchEvents se muestra cómo priorizar eventos de indización.</span><span class="sxs-lookup"><span data-stu-id="1fc56-104">The SearchEvents code sample demonstrates how to prioritize indexing events.</span></span>

<span data-ttu-id="1fc56-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="1fc56-105">This topic contains the following sections.</span></span>

- [<span data-ttu-id="1fc56-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc56-106">Requirements</span></span>](#requirements)
- [<span data-ttu-id="1fc56-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-107">Downloading the Sample</span></span>](#downloading-the-sample)
- [<span data-ttu-id="1fc56-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-108">Building the Sample</span></span>](#building-the-sample)
- [<span data-ttu-id="1fc56-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-109">Running the Sample</span></span>](#running-the-sample)
- [<span data-ttu-id="1fc56-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fc56-110">Related topics</span></span>](#related-topics)

## <a name="requirements"></a><span data-ttu-id="1fc56-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc56-111">Requirements</span></span>

| <span data-ttu-id="1fc56-112">Producto</span><span class="sxs-lookup"><span data-stu-id="1fc56-112">Product</span></span>     | <span data-ttu-id="1fc56-113">Versión del producto</span><span class="sxs-lookup"><span data-stu-id="1fc56-113">Product Version</span></span>          |
|-------------|--------------------------|
| <span data-ttu-id="1fc56-114">Windows</span><span class="sxs-lookup"><span data-stu-id="1fc56-114">Windows</span></span>     | <span data-ttu-id="1fc56-115">Windows 7, 8.1 o 10</span><span class="sxs-lookup"><span data-stu-id="1fc56-115">Windows 7, 8.1, or 10</span></span>    |
| <span data-ttu-id="1fc56-116">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="1fc56-116">Windows SDK</span></span> | <span data-ttu-id="1fc56-117">7,0 o superior</span><span class="sxs-lookup"><span data-stu-id="1fc56-117">7.0 or greater</span></span>           |

## <a name="downloading-the-sample"></a><span data-ttu-id="1fc56-118">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-118">Downloading the Sample</span></span>

<span data-ttu-id="1fc56-119">Este ejemplo está disponible en la siguiente ubicación.</span><span class="sxs-lookup"><span data-stu-id="1fc56-119">This sample is available in the following location.</span></span>

| <span data-ttu-id="1fc56-120">Location</span><span class="sxs-lookup"><span data-stu-id="1fc56-120">Location</span></span>      | <span data-ttu-id="1fc56-121">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="1fc56-121">Path URL</span></span>                                                                  |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="1fc56-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="1fc56-122">GitHub</span></span>        | [<span data-ttu-id="1fc56-123">Ejemplo de SearchEvents</span><span class="sxs-lookup"><span data-stu-id="1fc56-123">SearchEvents sample</span></span>](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> <span data-ttu-id="1fc56-124">En todas las versiones de Windows, incluido Windows 7, se recomienda descargar los ejemplos directamente desde GitHub para obtener la versión más actualizada.</span><span class="sxs-lookup"><span data-stu-id="1fc56-124">For all versions of Windows, including Windows 7, it is recommended to download the samples directly from GitHub for the most up to date version.</span></span>

## <a name="building-the-sample"></a><span data-ttu-id="1fc56-125">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-125">Building the Sample</span></span>

1. <span data-ttu-id="1fc56-126">Abra el explorador de Windows y navegue hasta el directorio del proyecto **SearchEvents** .</span><span class="sxs-lookup"><span data-stu-id="1fc56-126">Open Windows Explorer and navigate to the **SearchEvents** project directory.</span></span>
2. <span data-ttu-id="1fc56-127">Haga doble clic en el icono del archivo Eventing. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1fc56-127">Double-click the icon for the Eventing.sln file to open the project in Visual Studio.</span></span>
  
    > [!NOTE]  
    > <span data-ttu-id="1fc56-128">El archivo sln se creó con una versión anterior de Visual Studio, por lo que será necesario actualizarlo si está ejecutando Visual Studio 2012 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1fc56-128">The sln file was created under an older version of Visual Studio, thus upgrading it will be required if you are running Visual Studio 2012 or newer.</span></span> <span data-ttu-id="1fc56-129">Esto no afectará al comportamiento del ejemplo.</span><span class="sxs-lookup"><span data-stu-id="1fc56-129">This will not impact the sample's behavior.</span></span>

3. <span data-ttu-id="1fc56-130">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="1fc56-130">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="1fc56-131">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="1fc56-131">Running the Sample</span></span>

1. <span data-ttu-id="1fc56-132">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="1fc56-132">Navigate to the directory that contains the new executable, using the Command Prompt window or Windows Explorer.</span></span>
2. <span data-ttu-id="1fc56-133">En el símbolo del sistema, escriba `Eventing.exe` o, en el explorador de Windows, haga doble clic en el icono de Eventing.exe.</span><span class="sxs-lookup"><span data-stu-id="1fc56-133">At the command prompt, enter `Eventing.exe`, or from Windows Explorer, double-click the icon for Eventing.exe.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fc56-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1fc56-134">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="1fc56-135">Referencia</span><span class="sxs-lookup"><span data-stu-id="1fc56-135">Reference</span></span>

[<span data-ttu-id="1fc56-136">**IRowsetEvents**</span><span class="sxs-lookup"><span data-stu-id="1fc56-136">**IRowsetEvents**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[<span data-ttu-id="1fc56-137">**IRowsetPrioritization**</span><span class="sxs-lookup"><span data-stu-id="1fc56-137">**IRowsetPrioritization**</span></span>](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[<span data-ttu-id="1fc56-138">**nivel de prioridad \_**</span><span class="sxs-lookup"><span data-stu-id="1fc56-138">**PRIORITY\_LEVEL**</span></span>](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[<span data-ttu-id="1fc56-139">**ROWSETEVENT \_ ITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="1fc56-139">**ROWSETEVENT\_ITEMSTATE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[<span data-ttu-id="1fc56-140">**\_tipo ROWSETEVENT**</span><span class="sxs-lookup"><span data-stu-id="1fc56-140">**ROWSETEVENT\_TYPE**</span></span>](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a><span data-ttu-id="1fc56-141">Otros ejemplos</span><span class="sxs-lookup"><span data-stu-id="1fc56-141">Other Samples</span></span>

[<span data-ttu-id="1fc56-142">Ejemplos de código de búsqueda</span><span class="sxs-lookup"><span data-stu-id="1fc56-142">Search Code Samples</span></span>](-search-samples-ovw.md)
