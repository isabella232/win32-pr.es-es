---
description: Muestra las superposiciones de los iconos de la barra de tareas y las barras de progreso.
title: Ejemplo de estado periférico de la barra de tareas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997889"
---
# <a name="taskbar-peripheral-status-sample"></a><span data-ttu-id="85871-103">Ejemplo de estado periférico de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="85871-103">Taskbar Peripheral Status Sample</span></span>

<span data-ttu-id="85871-104">Muestra las superposiciones de los iconos de la barra de tareas y las barras de progreso.</span><span class="sxs-lookup"><span data-stu-id="85871-104">Demonstrates taskbar icon overlays and progress bars.</span></span>

<span data-ttu-id="85871-105">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="85871-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="85871-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="85871-106">Description</span></span>](#description)
-   [<span data-ttu-id="85871-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85871-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="85871-108">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="85871-109">Compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="85871-110">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-110">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="85871-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85871-111">Related topics</span></span>](#related-topics)

## <a name="description"></a><span data-ttu-id="85871-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="85871-112">Description</span></span>

<span data-ttu-id="85871-113">Este ejemplo crea un botón de la barra de tareas de ejemplo en el que se muestra el uso de [**ITaskbarList3:: SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) permitiéndole aplicar varias superposiciones elegidas en un menú.</span><span class="sxs-lookup"><span data-stu-id="85871-113">This sample creates an example taskbar button on which it demonstrates the use of [**ITaskbarList3::SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) by allowing you to apply various overlays chosen from a menu.</span></span>

<span data-ttu-id="85871-114">El ejemplo también proporciona la opción de simular un indicador de progreso en el botón, mostrando el uso de [**ITaskbarList3:: SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) y [**ITaskbarList3:: SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) al mostrar en primer lugar un indicador de progreso indeterminado (TBPF \_ indeterminado) y, a continuación, un indicador proporcional normal (TBPF \_ normal).</span><span class="sxs-lookup"><span data-stu-id="85871-114">The sample also provides the option of simulating a progress indicator on the button, demonstrating the use of [**ITaskbarList3::SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) and [**ITaskbarList3::SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) by showing at first an indeterminate progress indicator (TBPF\_INDETERMINATE), and then a normal proportional indicator (TBPF\_NORMAL).</span></span>

## <a name="requirements"></a><span data-ttu-id="85871-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="85871-115">Requirements</span></span>



| <span data-ttu-id="85871-116">Producto</span><span class="sxs-lookup"><span data-stu-id="85871-116">Product</span></span>                                | <span data-ttu-id="85871-117">Versión mínima del producto</span><span class="sxs-lookup"><span data-stu-id="85871-117">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="85871-118">Windows</span><span class="sxs-lookup"><span data-stu-id="85871-118">Windows</span></span>                                | <span data-ttu-id="85871-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85871-119">Windows 7</span></span>               |
| <span data-ttu-id="85871-120">Kit de desarrollo de software de Windows (SDK)</span><span class="sxs-lookup"><span data-stu-id="85871-120">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="85871-121">7.0</span><span class="sxs-lookup"><span data-stu-id="85871-121">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="85871-122">Descargar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-122">Downloading the Sample</span></span>

| <span data-ttu-id="85871-123">Ubicación</span><span class="sxs-lookup"><span data-stu-id="85871-123">Location</span></span>      | <span data-ttu-id="85871-124">URL de ruta de acceso</span><span class="sxs-lookup"><span data-stu-id="85871-124">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85871-125">GitHub</span><span class="sxs-lookup"><span data-stu-id="85871-125">GitHub</span></span>  | [<span data-ttu-id="85871-126">Ejemplo de TaskBarPeripheralStatus</span><span class="sxs-lookup"><span data-stu-id="85871-126">TaskBarPeripheralStatus sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a><span data-ttu-id="85871-127">Generar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-127">Building the Sample</span></span>

<span data-ttu-id="85871-128">Para compilar el ejemplo desde el símbolo del sistema:</span><span class="sxs-lookup"><span data-stu-id="85871-128">To build the sample from the command prompt:</span></span>

1.  <span data-ttu-id="85871-129">Abra la ventana del símbolo del sistema y navegue hasta el directorio del proyecto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="85871-129">Open the command prompt window and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="85871-130">Escriba `msbuild PeripheralStatus.sln`.</span><span class="sxs-lookup"><span data-stu-id="85871-130">Enter `msbuild PeripheralStatus.sln`.</span></span>

<span data-ttu-id="85871-131">Para compilar el ejemplo mediante Microsoft Visual Studio (preferido):</span><span class="sxs-lookup"><span data-stu-id="85871-131">To build the sample using Microsoft Visual Studio (preferred):</span></span>

1.  <span data-ttu-id="85871-132">Abra el explorador de Windows y navegue hasta el directorio del proyecto **TaskbarPeripheralStatus** .</span><span class="sxs-lookup"><span data-stu-id="85871-132">Open Windows Explorer and navigate to the **TaskbarPeripheralStatus** project directory.</span></span>
2.  <span data-ttu-id="85871-133">Haga doble clic en el icono del archivo PeripheralStatus. sln para abrir el proyecto en Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="85871-133">Double-click the icon for the PeripheralStatus.sln file to open the project in Visual Studio.</span></span>
3.  <span data-ttu-id="85871-134">En el menú **compilar** , seleccione **compilar solución**.</span><span class="sxs-lookup"><span data-stu-id="85871-134">From the **Build** menu, select **Build Solution**.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="85871-135">Ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="85871-135">Running the Sample</span></span>

1.  <span data-ttu-id="85871-136">Navegue hasta el directorio que contiene el nuevo archivo ejecutable (por ejemplo, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug` ), mediante el símbolo del sistema o el explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="85871-136">Navigate to the directory that contains the new executable file (for instance, `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`), using the command prompt or Windows Explorer.</span></span>

    -   <span data-ttu-id="85871-137">Si usa la línea de comandos, escriba `PeripheralStatus.exe` .</span><span class="sxs-lookup"><span data-stu-id="85871-137">If using the command line, enter `PeripheralStatus.exe`.</span></span>
    -   <span data-ttu-id="85871-138">Si usa el explorador de Windows, haga doble clic en el icono de PeripheralStatus.exe.</span><span class="sxs-lookup"><span data-stu-id="85871-138">If using Windows Explorer, double-click the icon for PeripheralStatus.exe.</span></span>

    <span data-ttu-id="85871-139">Se abrirá una nueva ventana con un botón de la barra de tareas asociado.</span><span class="sxs-lookup"><span data-stu-id="85871-139">A new window will open, with an associated taskbar button.</span></span>

2.  <span data-ttu-id="85871-140">Para mostrar las superposiciones, elija **superposición 1** o **superposición 2** en el menú de **Estado de periféricos** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="85871-140">To demonstrate overlays, choose **Overlay 1** or **Overlay 2** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="85871-141">La superposición elegida aparece en el botón de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="85871-141">The chosen overlay appears on the taskbar button.</span></span> <span data-ttu-id="85871-142">Para quitar la superposición, elija **Borrar superposición**.</span><span class="sxs-lookup"><span data-stu-id="85871-142">To remove the overlay, choose **Clear Overlay**.</span></span>
3.  <span data-ttu-id="85871-143">Para mostrar la barra de progreso, elija **simular progreso** en el menú de **Estado de periféricos** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="85871-143">To demonstrate the progress bar, choose **Simulate Progress** from the window's **Peripheral Status** menu.</span></span> <span data-ttu-id="85871-144">El botón de la barra de tareas mostrará un indicador de progreso indeterminado y cambiará a un indicador normal.</span><span class="sxs-lookup"><span data-stu-id="85871-144">The taskbar button will show an indeterminate progress indicator then switch to a normal indicator.</span></span>
4.  <span data-ttu-id="85871-145">Elija **salir** en el menú **archivo** de la ventana para finalizar el programa.</span><span class="sxs-lookup"><span data-stu-id="85871-145">Choose **Exit** from the window's **File** menu to end the program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85871-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85871-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85871-147">Extensiones de la barra de tareas</span><span class="sxs-lookup"><span data-stu-id="85871-147">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> </dl>

 

 



