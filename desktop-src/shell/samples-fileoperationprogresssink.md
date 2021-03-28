---
description: Muestra cómo usar los métodos de la interfaz IFileOperationProgressSink para supervisar los detalles de las acciones de la interfaz IFileOperation.
title: Receptor de progreso de operación de archivo
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 196ABB75-1FE0-44f5-9060-59AAB4231567
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 60e3bde90da36a6122608b463b28df670f0d2a8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082815"
---
# <a name="file-operation-progress-sink"></a><span data-ttu-id="95537-103">Receptor de progreso de operación de archivo</span><span class="sxs-lookup"><span data-stu-id="95537-103">File Operation Progress Sink</span></span>

<span data-ttu-id="95537-104">Muestra cómo usar los métodos de la interfaz [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) para supervisar los detalles de las acciones de la interfaz [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) .</span><span class="sxs-lookup"><span data-stu-id="95537-104">Demonstrates how to use the [**IFileOperationProgressSink**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperationprogresssink) interface methods for monitoring the details of [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) interface actions.</span></span>

<span data-ttu-id="95537-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="95537-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="95537-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95537-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="95537-107">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="95537-108">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-108">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="95537-109">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-109">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="95537-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="95537-110">Requirements</span></span>



| <span data-ttu-id="95537-111">Producto</span><span class="sxs-lookup"><span data-stu-id="95537-111">Product</span></span>                                | <span data-ttu-id="95537-112">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="95537-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="95537-113">Windows</span><span class="sxs-lookup"><span data-stu-id="95537-113">Windows</span></span>                                | <span data-ttu-id="95537-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95537-114">Windows Vista</span></span>           |
| <span data-ttu-id="95537-115">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="95537-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="95537-116">6.1</span><span class="sxs-lookup"><span data-stu-id="95537-116">6.1</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="95537-117">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-117">Downloading the Sample</span></span>

| <span data-ttu-id="95537-118">Ubicación</span><span class="sxs-lookup"><span data-stu-id="95537-118">Location</span></span>      | <span data-ttu-id="95537-119">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="95537-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95537-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="95537-120">GitHub</span></span>  | [<span data-ttu-id="95537-121">Ejemplo de FileOperationProgressSink</span><span class="sxs-lookup"><span data-stu-id="95537-121">FileOperationProgressSink sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/FileOperationProgressSink) |

## <a name="building-the-sample"></a><span data-ttu-id="95537-122">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-122">Building the Sample</span></span>

<span data-ttu-id="95537-123">Para compilar el ejemplo desde la ventana del símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="95537-123">To build the sample from the command prompt window:</span></span>

1.  <span data-ttu-id="95537-124">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **FileOperationProgressSink** .</span><span class="sxs-lookup"><span data-stu-id="95537-124">Open the command prompt window and navigate to the **FileOperationProgressSink** project directory.</span></span>
2.  <span data-ttu-id="95537-125">Escriba `msbuild FileOperationProgressSinkSample.sln`.</span><span class="sxs-lookup"><span data-stu-id="95537-125">Enter `msbuild FileOperationProgressSinkSample.sln`.</span></span>

<span data-ttu-id="95537-126">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="95537-126">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="95537-127">Abra el explorador de Windows y navegue hasta el directorio del proyecto **FilesInUse** .</span><span class="sxs-lookup"><span data-stu-id="95537-127">Open Windows Explorer and navigate to the **FilesInUse** project directory.</span></span> <span data-ttu-id="95537-128">Por ejemplo, la ruta de instalación predeterminada completa es `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample` .</span><span class="sxs-lookup"><span data-stu-id="95537-128">For example, the full default installation path is `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppPlatform\FileOperationProgressSinkSample`.</span></span>
2.  <span data-ttu-id="95537-129">Haga doble clic en el icono del archivo FileOperationProgressSinkSample. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="95537-129">Double-click the icon for the FileOperationProgressSinkSample.sln file to open the project in Visual Studio.</span></span>
    > [!Note]  
    > <span data-ttu-id="95537-130">La extensión de nombre de archivo. sln no se muestra en configuración de carpeta predeterminada.</span><span class="sxs-lookup"><span data-stu-id="95537-130">The .sln file name extension is not shown under default folder settings.</span></span> <span data-ttu-id="95537-131">En esa situación, puede identificarse por su icono único o por su descripción de tipo, "Microsoft Visual Studio solución".</span><span class="sxs-lookup"><span data-stu-id="95537-131">In that situation, it can be identified by its unique icon or by its type description, "Microsoft Visual Studio Solution".</span></span>

     

3.  <span data-ttu-id="95537-132">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="95537-132">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="95537-133">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="95537-133">Running the Sample</span></span>

1.  <span data-ttu-id="95537-134">Desplácese hasta el directorio que contiene el nuevo ejecutable, mediante la ventana del símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="95537-134">Navigate to the directory that contains the new executable, using the command prompt window or Windows Explorer.</span></span>
2.  <span data-ttu-id="95537-135">En el símbolo del sistema, escriba `FileOperationProgressSinkSample.exe` o, en el explorador de Windows, haga doble clic en el icono de FileOperationProgressSinkSample.exe.</span><span class="sxs-lookup"><span data-stu-id="95537-135">At the command prompt, enter `FileOperationProgressSinkSample.exe`, or from Windows Explorer, double-click the icon for FileOperationProgressSinkSample.exe.</span></span>

 

 



