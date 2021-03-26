---
description: Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo incrustado en la vista previa en miniatura de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o Active la ventana de la aplicación.
title: Ejemplo de barra de herramientas de miniaturas de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e61208f15772a43138e6cd7a38fd6327445bdfa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985822"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a><span data-ttu-id="78cf7-103">Ejemplo de barra de herramientas de miniaturas de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="78cf7-103">Taskbar Thumbnail Toolbar Sample</span></span>

<span data-ttu-id="78cf7-104">Muestra una barra de herramientas en miniatura, un control de barra de herramientas activo incrustado en la vista previa en miniatura de una ventana, que se usa para proporcionar acceso a los comandos clave de una ventana sin hacer que el usuario restaure o Active la ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="78cf7-104">Demonstrates a thumbnail toolbar, an active toolbar control embedded in a window's thumbnail preview, used to provide access to a window's key commands without making the user restore or activate the application's window.</span></span>

<span data-ttu-id="78cf7-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="78cf7-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="78cf7-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="78cf7-106">Description</span></span>](#description)
-   [<span data-ttu-id="78cf7-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78cf7-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="78cf7-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="78cf7-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="78cf7-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="78cf7-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78cf7-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="78cf7-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="78cf7-112">Description</span></span>

<span data-ttu-id="78cf7-113">En este ejemplo se muestra cómo proporcionar una barra de herramientas simple a una vista previa en miniatura de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="78cf7-113">This sample shows how to provide a simple toolbar to a taskbar thumbnail preview.</span></span> <span data-ttu-id="78cf7-114">La barra de herramientas consta de tres botones.</span><span class="sxs-lookup"><span data-stu-id="78cf7-114">The toolbar consists of three buttons.</span></span> <span data-ttu-id="78cf7-115">Al hacer clic en un botón, se muestra una ventana para confirmar que se activó el botón.</span><span class="sxs-lookup"><span data-stu-id="78cf7-115">Clicking a button displays a window to confirm that the button was activated.</span></span> <span data-ttu-id="78cf7-116">Se muestran las siguientes API:</span><span class="sxs-lookup"><span data-stu-id="78cf7-116">The following APIs are demonstrated:</span></span>

-   [<span data-ttu-id="78cf7-117">**ITaskbarList3:: ThumbBarAddButtons**</span><span class="sxs-lookup"><span data-stu-id="78cf7-117">**ITaskbarList3::ThumbBarAddButtons**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [<span data-ttu-id="78cf7-118">**ITaskbarList3:: ThumbBarSetImageList**</span><span class="sxs-lookup"><span data-stu-id="78cf7-118">**ITaskbarList3::ThumbBarSetImageList**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   <span data-ttu-id="78cf7-119">Estructura [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton)</span><span class="sxs-lookup"><span data-stu-id="78cf7-119">[**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) structure</span></span>

## <a name="requirements"></a><span data-ttu-id="78cf7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78cf7-120">Requirements</span></span>



| <span data-ttu-id="78cf7-121">Producto</span><span class="sxs-lookup"><span data-stu-id="78cf7-121">Product</span></span>                                | <span data-ttu-id="78cf7-122">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="78cf7-122">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="78cf7-123">Windows</span><span class="sxs-lookup"><span data-stu-id="78cf7-123">Windows</span></span>                                | <span data-ttu-id="78cf7-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="78cf7-124">Windows 7</span></span>               |
| <span data-ttu-id="78cf7-125">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="78cf7-125">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="78cf7-126">7.0</span><span class="sxs-lookup"><span data-stu-id="78cf7-126">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="78cf7-127">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-127">Downloading the Sample</span></span>

| <span data-ttu-id="78cf7-128">Ubicación</span><span class="sxs-lookup"><span data-stu-id="78cf7-128">Location</span></span>      | <span data-ttu-id="78cf7-129">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="78cf7-129">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78cf7-130">GitHub</span><span class="sxs-lookup"><span data-stu-id="78cf7-130">GitHub</span></span>  | [<span data-ttu-id="78cf7-131">Ejemplo de TaskbarThumbnailToolbar</span><span class="sxs-lookup"><span data-stu-id="78cf7-131">TaskbarThumbnailToolbar sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a><span data-ttu-id="78cf7-132">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-132">Building the Sample</span></span>

<span data-ttu-id="78cf7-133">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="78cf7-133">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="78cf7-134">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="78cf7-134">Open the command prompt window and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="78cf7-135">Escriba `msbuild ThumbnailToolbar.sln`.</span><span class="sxs-lookup"><span data-stu-id="78cf7-135">Enter `msbuild ThumbnailToolbar.sln`.</span></span>

<span data-ttu-id="78cf7-136">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="78cf7-136">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="78cf7-137">Abra el explorador de Windows y navegue hasta el directorio del proyecto **TaskbarThumbnailToolbar** .</span><span class="sxs-lookup"><span data-stu-id="78cf7-137">Open Windows Explorer and navigate to the **TaskbarThumbnailToolbar** project directory.</span></span>
2.  <span data-ttu-id="78cf7-138">Haga doble clic en el icono del archivo ThumbnailToolbar. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="78cf7-138">Double-click the icon for the ThumbnailToolbar.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="78cf7-139">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="78cf7-139">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="78cf7-140">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="78cf7-140">Running the Sample</span></span>

1.  <span data-ttu-id="78cf7-141">Navegue hasta el directorio que contiene el nuevo archivo ejecutable (por ejemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug` ), mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="78cf7-141">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="78cf7-142">Si usa la línea de comandos, escriba `ThumbnailToolbar.exe` .</span><span class="sxs-lookup"><span data-stu-id="78cf7-142">If using the command line, enter `ThumbnailToolbar.exe`.</span></span>
    -   <span data-ttu-id="78cf7-143">Si usa el explorador de Windows, haga doble clic en el icono de ThumbnailToolbar.exe.</span><span class="sxs-lookup"><span data-stu-id="78cf7-143">If using Windows Explorer, double-click the icon for ThumbnailToolbar.exe.</span></span>

    <span data-ttu-id="78cf7-144">Se abrirá una nueva ventana con un botón de la barra de tareas asociado.</span><span class="sxs-lookup"><span data-stu-id="78cf7-144">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="78cf7-145">Mantenga el cursor sobre el botón de la barra de tareas **ThumbnailToolbar** para que se muestre la vista previa.</span><span class="sxs-lookup"><span data-stu-id="78cf7-145">Hover the cursor over the **ThumbnailToolbar** taskbar button so that the preview displays.</span></span> <span data-ttu-id="78cf7-146">Haga clic en uno de los tres botones (verde, amarillo, rojo) que se muestra en la barra de herramientas de la vista previa.</span><span class="sxs-lookup"><span data-stu-id="78cf7-146">Click one of the three buttons (green, yellow, red) shown in the preview's toolbar.</span></span>
3.  <span data-ttu-id="78cf7-147">Elija **salir** en el menú **archivo** de la ventana para finalizar el programa.</span><span class="sxs-lookup"><span data-stu-id="78cf7-147">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78cf7-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="78cf7-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78cf7-149">Extensiones de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="78cf7-149">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



