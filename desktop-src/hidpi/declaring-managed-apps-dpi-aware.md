---
title: Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor
description: Tenga en cuenta que en esta página se trata el desarrollo heredado de WPF para Windows 8.1. Si va a desarrollar aplicaciones de WPF para Windows 10, consulte la documentación más reciente en GitHub..
ms.assetid: 04a36dc7-684f-4846-aeba-970117070b4c
keywords:
- Interfaz de usuario de Windows, aplicaciones compatibles con PPP
- Interfaz de usuario de Windows, alta PPP
- Aplicaciones con reconocimiento de PPP
- PPP alto
- escribir aplicaciones Win32 con reconocimiento de PPP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a32bfaf76271e61d0dc3791d5aaae9609be6d8c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149273"
---
# <a name="developing-a-per-monitor-dpi-aware-wpf-application"></a><span data-ttu-id="ebdc8-110">Desarrollo de una aplicación WPF con reconocimiento de PPP por monitor</span><span class="sxs-lookup"><span data-stu-id="ebdc8-110">Developing a Per-Monitor DPI-Aware WPF Application</span></span>

<span data-ttu-id="ebdc8-111">**API importantes**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-111">**Important APIs**</span></span>

-   [<span data-ttu-id="ebdc8-112">**SetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-112">**SetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness)
-   [<span data-ttu-id="ebdc8-113">**GetProcessDpiAwareness**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-113">**GetProcessDpiAwareness**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness)
-   [<span data-ttu-id="ebdc8-114">**GetDpiForMonitor**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-114">**GetDpiForMonitor**</span></span>](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor)

> [!Note]  
> <span data-ttu-id="ebdc8-115">**En esta página se trata el desarrollo heredado de WPF para Windows 8.1.**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-115">**This page covers legacy WPF development for Windows 8.1.**</span></span> <span data-ttu-id="ebdc8-116">Si va a desarrollar aplicaciones de WPF para Windows 10, consulte la <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">documentación más reciente en github.</a></span><span class="sxs-lookup"><span data-stu-id="ebdc8-116">If you are developing WPF applications for Windows 10, please see the <a href="https://github.com/microsoft/WPF-Samples/blob/master/PerMonitorDPI/readme.md">latest documentation on GitHub.</a></span></span>

 

<span data-ttu-id="ebdc8-117">Windows 8.1 ofrece a los desarrolladores nuevas funciones para crear aplicaciones de escritorio que tengan en cuenta el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-117">Windows 8.1 gives developers new functionality to create desktop applications that are per-monitor DPI-aware.</span></span> <span data-ttu-id="ebdc8-118">Con el fin de aprovechar esta funcionalidad, una aplicación por monitor con reconocimiento de PPP debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-118">In order to take advantage of this functionality, a per monitor DPI-aware application must do the following:</span></span>

-   <span data-ttu-id="ebdc8-119">Cambiar las dimensiones de la ventana para mantener un tamaño físico que parezca coherente en cualquier pantalla</span><span class="sxs-lookup"><span data-stu-id="ebdc8-119">Change window dimensions to maintain a physical size that appears consistent on any display</span></span>
-   <span data-ttu-id="ebdc8-120">Volver a diseñar y volver a representar gráficos para el nuevo tamaño de la ventana</span><span class="sxs-lookup"><span data-stu-id="ebdc8-120">Re-layout and re-render graphics for the new window size</span></span>
-   <span data-ttu-id="ebdc8-121">Seleccione las fuentes que se van a escalar correctamente para el nivel de PPP</span><span class="sxs-lookup"><span data-stu-id="ebdc8-121">Select fonts that are scaled appropriately for the DPI level</span></span>
-   <span data-ttu-id="ebdc8-122">Seleccionar y cargar recursos de mapa de bits adaptados para el nivel de PPP</span><span class="sxs-lookup"><span data-stu-id="ebdc8-122">Select and load bitmap assets that are tailored for the DPI level</span></span>

<span data-ttu-id="ebdc8-123">Para facilitar la creación de una aplicación con reconocimiento de PPP por monitor, Windows 8.1 proporciona el siguiente Win32APIs de Microsoft:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-123">To facilitate making a per-monitor DPI-aware application, Windows 8.1 provides the following Microsoft Win32APIs:</span></span>

-   <span data-ttu-id="ebdc8-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (o entrada de manifiesto de PPP) establece el proceso en un nivel de reconocimiento de PPP especificado que, a continuación, determina el modo en que Windows escala la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-124">[**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) (or DPI manifest entry) sets the process to a specified DPI awareness level, which then determines how Windows scales the UI.</span></span> <span data-ttu-id="ebdc8-125">Esto sustituye a [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-125">This supersedes [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware).</span></span>
-   <span data-ttu-id="ebdc8-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) devuelve el nivel de reconocimiento de PPP.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-126">[**GetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getprocessdpiawareness) returns the DPI awareness level.</span></span> <span data-ttu-id="ebdc8-127">Esto sustituye a [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-127">This supersedes [**IsProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-isprocessdpiaware).</span></span>
-   <span data-ttu-id="ebdc8-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) devuelve el PPP de un monitor.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-128">[**GetDpiForMonitor**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-getdpiformonitor) returns the DPI for a monitor.</span></span>
-   <span data-ttu-id="ebdc8-129">La notificación de la ventana de [**\_ DPICHANGED de WM**](wm-dpichanged.md) se envía a las aplicaciones compatibles con PPP por monitor cuando la posición de una ventana cambia de modo que la mayor parte de su área intersecte con un monitor con un DPI diferente del PPP antes de que cambie la posición o cuando el usuario mueva el control deslizante de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-129">The [**WM\_DPICHANGED**](wm-dpichanged.md) window notification is sent to per-monitor DPI-aware applications when a window’s position changes such that most of its area intersects a monitor with a DPI that is different from the DPI before the position change or when the user moves the display slider.</span></span> <span data-ttu-id="ebdc8-130">Para crear una aplicación que cambie de tamaño y se represente cuando un usuario la mueva a una pantalla diferente, utilice esta notificación.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-130">To create an application that resizes and re-renders itself when a user moves it to a different display, use this notification.</span></span>

<span data-ttu-id="ebdc8-131">Para obtener más información sobre los distintos niveles de reconocimiento de PPP admitidos para las aplicaciones de escritorio en Windows 8.1 vea el tema [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-131">For more details on various DPI awareness levels supported for desktop applications in Windows 8.1 see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span>

## <a name="dpi-scaling-and-wpf"></a><span data-ttu-id="ebdc8-132">Escala de PPP y WPF</span><span class="sxs-lookup"><span data-stu-id="ebdc8-132">DPI Scaling and WPF</span></span>

<span data-ttu-id="ebdc8-133">De forma predeterminada, las aplicaciones de Windows Presentation Foundation (WPF) son compatibles con los valores de PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-133">Windows Presentation Foundation (WPF) applications are by default system DPI-aware.</span></span> <span data-ttu-id="ebdc8-134">Para obtener definiciones de los distintos niveles de reconocimiento de PPP, vea el tema [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-134">For definitions of the different DPI awareness levels see the topic [Writing DPI-Aware Desktop and Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/mt843498(v=vs.85).aspx(d=robot)).</span></span> <span data-ttu-id="ebdc8-135">El sistema de gráficos de WPF usa unidades independientes del dispositivo para habilitar la resolución y la independencia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-135">The WPF graphics system uses device-independent units to enable resolution and device independence.</span></span> <span data-ttu-id="ebdc8-136">WPF escala cada píxel independiente del dispositivo automáticamente en función de los PPP actuales del sistema.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-136">WPF scales each device independent pixel automatically based on current system DPI.</span></span> <span data-ttu-id="ebdc8-137">Esto permite que las aplicaciones de WPF se escalen automáticamente cuando el PPP del monitor en el que se encuentra la ventana es el mismo DPI del sistema.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-137">This allows WPF applications to scale automatically when the DPI of the monitor the window is on is same system DPI.</span></span> <span data-ttu-id="ebdc8-138">Sin embargo, dado que las aplicaciones de WPF son compatibles con los PPP del sistema, la aplicación se escalará mediante el sistema operativo cuando la aplicación se mueva a un monitor con un PPP diferente o cuando se use el control deslizante del panel de control para cambiar el PPP.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-138">However, since WPF applications are system dpi-aware, the application will be scaled by the OS when the application is moved to a monitor with a different DPI or when the slider in the control panel is used to change the DPI.</span></span> <span data-ttu-id="ebdc8-139">El escalado en el sistema operativo puede dar lugar a que las aplicaciones WPF parezcan borrosas, especialmente cuando el escalado es no integral.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-139">Scaling in the OS may result in WPF applications to appear blurry especially when the scaling is non-integral.</span></span> <span data-ttu-id="ebdc8-140">Para evitar el escalado de aplicaciones de WPF, es necesario actualizarla para que sea compatible con el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-140">In order to avoid scaling WPF applications, they need to be updated to be per-monitor DPI-aware.</span></span>

## <a name="per-monitor-aware-wpf-sample-walkthrough"></a><span data-ttu-id="ebdc8-141">Tutorial de ejemplo de WPF con reconocimiento de supervisión</span><span class="sxs-lookup"><span data-stu-id="ebdc8-141">Per Monitor Aware WPF Sample Walkthrough</span></span>

<span data-ttu-id="ebdc8-142">El [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) es una aplicación WPF de ejemplo que se ha actualizado para que sea compatible con los PPP de cada monitor.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-142">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) is a sample WPF application updated to be per-monitor DPI-aware.</span></span> <span data-ttu-id="ebdc8-143">El ejemplo consta de dos proyectos:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-143">The sample consists of two projects:</span></span>

-   <span data-ttu-id="ebdc8-144">NativeHelpers. vcxproj: se trata de un proyecto auxiliar nativo que implementa la funcionalidad básica para crear una aplicación WPF como reconocimiento de PPP por monitor mediante el Win32APIs anterior.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-144">NativeHelpers.vcxproj: This is a native helper project that implements the core functionality to make a WPF application as per-monitor DPI-aware utilizing the Win32APIs above.</span></span> <span data-ttu-id="ebdc8-145">El proyecto contiene dos clases:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-145">The project contains two classes:</span></span>
    -   <span data-ttu-id="ebdc8-146">PerMonDPIHelpers: una clase que proporciona funciones auxiliares para las operaciones relacionadas con PPP, como la recuperación del valor de PPP actual del monitor activo, el establecimiento de un proceso para el reconocimiento de PPP por monitor, etc.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-146">PerMonDPIHelpers: A class that provides helper functions for DPI related operations like retrieving the current DPI of the active monitor, setting a process to be per-monitor DPI-aware, etc.</span></span>
    -   <span data-ttu-id="ebdc8-147">PerMonitorDPIWindow: una clase base derivada de **System. Windows. Window** que implementa la funcionalidad para hacer que una ventana de la aplicación WPF tenga en cuenta el reconocimiento de PPP por monitor.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-147">PerMonitorDPIWindow: A base class derived from **System.Windows.Window** that implements functionality to make a WPF application window to be per-monitor dpi-aware.</span></span> <span data-ttu-id="ebdc8-148">Ajusta el tamaño de la ventana, el tamaño de la representación de gráficos y el tamaño de fuente en función de los PPP del monitor en lugar de los PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-148">Adjusts window size, graphics rendering size and font size based on the DPI of the monitor rather than the system DPI.</span></span>
-   <span data-ttu-id="ebdc8-149">WPFApplication. csproj: aplicación WPF de ejemplo que usa PerMonitorDPIWindow (PerMonitorDPIWindow) y muestra cómo se cambia el tamaño de la representación y la ventana de la aplicación cuando la ventana se mueve a un monitor con un PPP diferente o cuando se usa el control deslizante del panel de control para cambiar el PPP.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-149">WPFApplication.csproj: Sample WPF application that consumes the PerMonitorDPIWindow (PerMonitorDPIWindow), and showcases how the application window and rendering resizes when the window is moved to a monitor with a different DPI or when the slider in the Display control panel is used to change the DPI.</span></span>

<span data-ttu-id="ebdc8-150">Para ejecutar el ejemplo, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-150">To run the sample follow the steps below:</span></span>

1.  <span data-ttu-id="ebdc8-151">Descargar y descomprimir el [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span><span class="sxs-lookup"><span data-stu-id="ebdc8-151">Download and unzip the [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware)</span></span>
2.  <span data-ttu-id="ebdc8-152">Iniciar Microsoft Visual Studio y seleccionar **archivo > abrir > proyecto o solución**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-152">Start Microsoft Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="ebdc8-153">Busque el directorio que contiene el ejemplo descomprimido.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-153">Browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="ebdc8-154">Vaya al directorio denominado para el ejemplo y haga doble clic en el archivo de solución de Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-154">Go to the directory named for the sample, and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="ebdc8-155">Presione F7 o use compilar > compilar **solución** para compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebdc8-155">Press F7 or use **Build > Build Solution** to build the sample</span></span>
5.  <span data-ttu-id="ebdc8-156">Presione Ctrl + F5 o use **Debug > iniciar sin depurar** para ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebdc8-156">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="ebdc8-157">Para ver el impacto del cambio de PPP en una aplicación WPF que se actualiza para que sea compatible con PPP por monitor mediante la clase base en el ejemplo, mueva la ventana de la aplicación a y desde las pantallas que tienen diferentes ppp.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-157">To see the impact of changing DPI on a WPF application that is updated to be per-monitor DPI-aware using the base class in the sample, move the application window to and from displays that have different DPIs.</span></span> <span data-ttu-id="ebdc8-158">A medida que la ventana se mueve entre monitores, el tamaño de la ventana y la escala de la interfaz de usuario se actualizan en función del DPI de la pantalla mediante el sistema de gráficos escalable de WPF, en lugar de escalarse mediante el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-158">As the window is moved between monitors, the window size and the UI scale is updated based on the DPI of the display by using WPF’s scalable graphics system, rather than being scaled by the OS.</span></span> <span data-ttu-id="ebdc8-159">La interfaz de usuario de la aplicación se representa de forma nativa y no aparece borrosa.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-159">The application’s UI is rendered natively and does not appear blurry.</span></span> <span data-ttu-id="ebdc8-160">Si no tiene dos pantallas con distintos PPP, cámbielos cambiando el control deslizante en el panel de control de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-160">If you don’t have two displays with different DPI, change the DPI by changing the slider in the Display control panel.</span></span> <span data-ttu-id="ebdc8-161">Cambiar el control deslizante y hacer clic en **aplicar** cambiará el tamaño de la ventana de la aplicación y actualizará automáticamente la escala de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-161">Changing the slider and clicking **Apply** will resize the application’s window and update the UI scale automatically.</span></span>

## <a name="updating-an-existing-wpf-application-to-be-per-monitor-dpi-aware-using-helper-project-in-the-wpf-sample"></a><span data-ttu-id="ebdc8-162">Actualizar una aplicación de WPF existente para que sea compatible con PPP por monitor mediante el proyecto auxiliar en el ejemplo de WPF</span><span class="sxs-lookup"><span data-stu-id="ebdc8-162">Updating an existing WPF Application to be per-monitor dpi-aware using helper project in the WPF Sample</span></span>

<span data-ttu-id="ebdc8-163">Si tiene una aplicación de WPF existente y desea aprovechar el proyecto auxiliar de PPP del ejemplo para que sea compatible con los PPP, siga estos pasos.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-163">If you have an existing WPF application and wish to leverage the DPI helper project from the sample to make it DPI aware, follow these steps.</span></span>

1.  <span data-ttu-id="ebdc8-164">Descargar y descomprimir el ejemplo de WPF con reconocimiento de monitor</span><span class="sxs-lookup"><span data-stu-id="ebdc8-164">Download and unzip the Per Monitor Aware WPF sample</span></span>
2.  <span data-ttu-id="ebdc8-165">Inicie Visual Studio y seleccione **archivo > abrir > proyecto o solución**</span><span class="sxs-lookup"><span data-stu-id="ebdc8-165">Start Visual Studio and select **File > Open > Project/Solution**</span></span>
3.  <span data-ttu-id="ebdc8-166">Busque el directorio que contiene una aplicación de WPF existente y haga doble clic en el archivo de solución de Visual Studio (. sln).</span><span class="sxs-lookup"><span data-stu-id="ebdc8-166">Browse to the directory which contains an existing WPF application and double-click the Visual Studio Solution (.sln) file</span></span>
4.  <span data-ttu-id="ebdc8-167">Haga clic con el botón derecho en la **solución > agregar > proyecto existente** ![ una captura de pantalla que muestra la selección del menú Agregar: proyecto existente.](images/scrvs-image1.png)</span><span class="sxs-lookup"><span data-stu-id="ebdc8-167">Right click on **Solution > Add > Existing Project**![a screenshot that illustrates the add: existing project menu selection](images/scrvs-image1.png)</span></span>
5.  <span data-ttu-id="ebdc8-168">En el cuadro de diálogo de selección de archivo, busque el directorio que contiene el ejemplo descomprimido.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-168">In the file selection dialogue browse to the directory that contains the unzipped sample.</span></span> <span data-ttu-id="ebdc8-169">Abra el directorio denominado para el ejemplo, vaya a la carpeta "NativeHelpers", seleccione el archivo de proyecto de Visual C++ "NativeHelpers. vcxproj" y haga clic en **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-169">Open to the directory named for the sample, browse to the folder "NativeHelpers", select the Visual C++ project file "NativeHelpers.vcxproj” and click **OK**</span></span>
6.  <span data-ttu-id="ebdc8-170">Haga clic con el botón derecho en el proyecto NativeHelpers y seleccione **compilar**.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-170">Right click on the project NativeHelpers and select **Build**.</span></span> <span data-ttu-id="ebdc8-171">Se generará NativeHelpers.dll que se agregará como referencia a la aplicación WPF en el paso siguiente ![ una captura de pantalla que ilustra la selección del menú compilar.](images/scrvs-image2.png)</span><span class="sxs-lookup"><span data-stu-id="ebdc8-171">This will generate NativeHelpers.dll that will be added as a reference to the WPF Application in the next step![a screen shot illustrating the build menu selection](images/scrvs-image2.png)</span></span>
7.  <span data-ttu-id="ebdc8-172">Agregue una referencia a NativeHelpers.dll desde la aplicación WPF.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-172">Add a reference to NativeHelpers.dll from your WPF Application.</span></span> <span data-ttu-id="ebdc8-173">Expanda el proyecto de aplicación WPF, haga clic con el botón derecho en **referencias** y haga clic en **Agregar referencia..** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-173">Expand your WPF application project, right click on **References** and click on **Add Reference...**</span></span>
8.  <span data-ttu-id="ebdc8-174">En el cuadro de diálogo resultante, expanda la sección **solución** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-174">In the resulting dialogue, expand the **Solution** section.</span></span> <span data-ttu-id="ebdc8-175">En **proyectos**, seleccione NativeHelpers y haga clic en **Aceptar** ![ una captura de pantalla que ilustra el cuadro de diálogo Administrador de recursos.](images/scrvs-image3.png)</span><span class="sxs-lookup"><span data-stu-id="ebdc8-175">Under **Projects**, select NativeHelpers, and click **OK**![a screen shot illustrating the resource manager dialog](images/scrvs-image3.png)</span></span>
9.  <span data-ttu-id="ebdc8-176">Expanda el proyecto de aplicación de WPF, expanda **propiedades** y Abra **AssemblyInfo. CS**.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-176">Expand your WPF application project, expand **Properties**, and open **AssemblyInfo.cs**.</span></span> <span data-ttu-id="ebdc8-177">Realice las siguientes adiciones a AssemblyInfo. cs.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-177">Make the following additions to AssemblyInfo.cs</span></span>
    -   <span data-ttu-id="ebdc8-178">Agregar referencia a System. Windows. media en la sección de referencia (mediante System. Windows. Media;)</span><span class="sxs-lookup"><span data-stu-id="ebdc8-178">Add reference to System.Windows.Media in the reference section (using System.Windows.Media;)</span></span>
    -   <span data-ttu-id="ebdc8-179">Agregue el atributo DisableDpiAwareness ( `[assembly: DisableDpiAwareness]` )</span><span class="sxs-lookup"><span data-stu-id="ebdc8-179">Add the DisableDpiAwareness attribute (`[assembly: DisableDpiAwareness]`)</span></span>

    ![una captura de pantalla que ilustra las propiedades adicionales](images/scrvs-image4.png)
10. <span data-ttu-id="ebdc8-181">Heredar la clase de ventana principal de WPF de la clase base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="ebdc8-181">Inherit the main WPF window class from PerMonitorDPIWindow base class</span></span>
    -   <span data-ttu-id="ebdc8-182">Actualice el archivo. CS de la ventana principal de WPF para que herede de la clase base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="ebdc8-182">Update the .cs file of the main WPF window to inherit from the PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="ebdc8-183">Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `using NativeHelpers;`</span><span class="sxs-lookup"><span data-stu-id="ebdc8-183">Add a reference to NativeHelpers in the reference section by adding the line `using NativeHelpers;`</span></span>
        -   <span data-ttu-id="ebdc8-184">Heredar la clase de ventana principal de la clase PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="ebdc8-184">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![una captura de pantalla que ilustra la referencia de c++](images/scrvs-image5.png)
    -   <span data-ttu-id="ebdc8-186">Actualice el archivo. XAML de la ventana principal de WPF para que herede de la clase base PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="ebdc8-186">Update the .xaml file of the main WPF window to inherit from PerMonitorDPIWindow base class</span></span>
        -   <span data-ttu-id="ebdc8-187">Agregue una referencia a NativeHelpers en la sección de referencia agregando la línea `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span><span class="sxs-lookup"><span data-stu-id="ebdc8-187">Add a reference to NativeHelpers in the reference section by adding the line `xmlns:src="clr-namespace:NativeHelpers;assembly=NativeHelpers"`</span></span>
        -   <span data-ttu-id="ebdc8-188">Heredar la clase de ventana principal de la clase PerMonitorDPIWindow</span><span class="sxs-lookup"><span data-stu-id="ebdc8-188">Inherit the main window class from PerMonitorDPIWindow class</span></span>

        ![una captura de pantalla que ilustra cómo agregar la referencia de. Xaml](images/scrvs-image6.png)
11. <span data-ttu-id="ebdc8-190">Presione F7 o use compilar > compilar **solución** para compilar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebdc8-190">Press F7 or use **Build > Build Solution** to build the sample</span></span>
12. <span data-ttu-id="ebdc8-191">Presione Ctrl + F5 o use **Debug > iniciar sin depurar** para ejecutar el ejemplo</span><span class="sxs-lookup"><span data-stu-id="ebdc8-191">Press Ctrl+F5 or use **Debug > Start Without Debugging** to run the sample</span></span>

<span data-ttu-id="ebdc8-192">La aplicación de [ejemplo de WPF con reconocimiento de monitor](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) muestra cómo se puede actualizar una aplicación de WPF para que sea compatible con el reconocimiento de PPP por monitor respondiendo a la notificación de ventana de [**\_ DPICHANGED de WM**](wm-dpichanged.md) .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-192">The [Per Monitor Aware WPF sample](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/PerMonitorDPIAware) application illustrates how a WPF application can be updated to be per-monitor DPI-aware by responding to the [**WM\_DPICHANGED**](wm-dpichanged.md) window notification.</span></span> <span data-ttu-id="ebdc8-193">En respuesta a la notificación de ventana, el ejemplo actualiza la transformación de escala que usa WPF en función del DPI actual del monitor en el que se encuentra la ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-193">In response to the window notification, the sample updates the scale transform used by WPF based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="ebdc8-194">El *wParam* de la notificación de ventana contiene el nuevo PPP en el *wParam*.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-194">The *wParam* of the window notification contains the new DPI in the *wParam*.</span></span> <span data-ttu-id="ebdc8-195">*LParam* contiene un rectángulo con el tamaño y la posición de la nueva ventana sugerida, escalada para el nuevo dpi.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-195">The *lParam* contains a rectangle that has the size and position of the new suggested window, scaled for the new DPI.</span></span>

<span data-ttu-id="ebdc8-196">Nota:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-196">Note:</span></span>

> [!Note]  
> <span data-ttu-id="ebdc8-197">Dado que este ejemplo sobrescribe el tamaño de la ventana y la transformación de escala del nodo raíz de la ventana de WPF, el desarrollador de aplicaciones puede necesitar más trabajo si:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-197">Since this sample overwrites the window size and the scale transform of the root node of the WPF window, further work may be required by application developer if:</span></span>
>
> -   <span data-ttu-id="ebdc8-198">El tamaño de la ventana afecta a otras partes de la aplicación como esta ventana de WPF que se hospeda dentro de otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-198">The size of the window impacts other portions of the application like this WPF Window being hosted inside another application.</span></span>
> -   <span data-ttu-id="ebdc8-199">La aplicación WPF que está ampliando esta clase está estableciendo otra transformación en el visual raíz. es posible que el ejemplo sobrescriba otra transformación que esté siendo aplicada por la propia aplicación WPF.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-199">The WPF application that is extending this class is setting some other transform on the root visual; the sample may overwrite some other transform that is being applied by the WPF application itself.</span></span>

 

## <a name="overview-of-the-helper-project-in-the-wpf-sample"></a><span data-ttu-id="ebdc8-200">Información general sobre el proyecto auxiliar en el ejemplo de WPF</span><span class="sxs-lookup"><span data-stu-id="ebdc8-200">Overview of the helper project in the WPF sample</span></span>

<span data-ttu-id="ebdc8-201">Para hacer que una aplicación WPF existente por monitor sea compatible con PPP, la biblioteca NativeHelpers proporciona la funcionalidad siguiente:</span><span class="sxs-lookup"><span data-stu-id="ebdc8-201">In order to make an existing WPF application per-monitor DPI-aware the NativeHelpers library provides following functionality:</span></span>

-   <span data-ttu-id="ebdc8-202">**Marca la aplicación WPF según el reconocimiento de PPP por ponitor:** La aplicación WPF se marca como con reconocimiento de PPP por monitor mediante una llamada a [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) para el proceso actual.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-202">**Marks the WPF application as per-ponitor DPI-aware:** The WPF application is marked as per-monitor DPI-aware by calling [**SetProcessDpiAwareness**](/windows/desktop/api/ShellScalingAPI/nf-shellscalingapi-setprocessdpiawareness) for the current process.</span></span> <span data-ttu-id="ebdc8-203">Al marcar la aplicación como compatible con PPP por monitor, se asegurará de que</span><span class="sxs-lookup"><span data-stu-id="ebdc8-203">Marking the application as per-monitor DPI-aware will ensure that</span></span>

    -   <span data-ttu-id="ebdc8-204">El sistema operativo no escala la aplicación cuando el PPP del sistema no coincide con el PPP actual del monitor en el que está la ventana de la aplicación</span><span class="sxs-lookup"><span data-stu-id="ebdc8-204">The OS does not scale the application when the system DPI does not match the current DPI of the monitor the application window is on</span></span>
    -   <span data-ttu-id="ebdc8-205">El mensaje de [**\_ DPICHANGED de WM**](wm-dpichanged.md) se envía cada vez que cambia el PPP de la ventana</span><span class="sxs-lookup"><span data-stu-id="ebdc8-205">The [**WM\_DPICHANGED**](wm-dpichanged.md) message is sent whenever the DPI of the window changes</span></span>

-   <span data-ttu-id="ebdc8-206">**Ajusta la dimensión de la ventana, vuelve a crear el diseño y vuelve a representar el contenido de los gráficos y selecciona fuentes basadas en los PPP iniciales del monitor en el que se encuentra la ventana:** Una vez que la aplicación se marca como con reconocimiento de PPP por monitor, WPF seguirá escalando el tamaño de la ventana, los gráficos y el tamaño de fuente en función de los PPP del sistema.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-206">**Adjusts the window dimension, re-layout and re-render graphics content and select fonts based on initial DPI of the monitor the window is on:** Once the application is marked as per-monitor DPI-aware, WPF will still scale the window size, graphics and font size based on the system DPI.</span></span> <span data-ttu-id="ebdc8-207">Dado que, al iniciarse la aplicación, no se garantiza que el valor de PPP del sistema sea el mismo que el valor de PPP del monitor en el que se inicia la ventana, la biblioteca ajusta estos valores una vez que se carga la ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-207">Since, at app launch, the system DPI is not guaranteed to be the same as the DPI of the monitor the window is launched on, the library adjust these values once the window is loaded.</span></span> <span data-ttu-id="ebdc8-208">La clase base **PerMonitorDPIWindow** los actualiza en el controlador **alloaded ()** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-208">The base class **PerMonitorDPIWindow** updates these in the **OnLoaded()** handler.</span></span>

    <span data-ttu-id="ebdc8-209">El tamaño de la ventana se actualiza cambiando las propiedades de **ancho** y **alto** de la ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-209">The Window size is updated by changing the **Width** and **Height** properties of the Window.</span></span> <span data-ttu-id="ebdc8-210">El diseño y el tamaño se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana de WPF.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-210">The layout and size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span>

    ```C++
    void PerMonitorDPIWindow::OnLoaded(Object^ , RoutedEventArgs^ ) 
    {   
    if (m_perMonitorEnabled)
        {
        m_source = (HwndSource^) PresentationSource::FromVisual((Visual^) this);
        HwndSourceHook^ hook = gcnew HwndSourceHook(this, &PerMonitorDPIWindow::HandleMessages);
        m_source->AddHook(hook); 
                
        //Calculate the DPI used by WPF.                    
        m_wpfDPI = 96.0 *  m_source->CompositionTarget->TransformToDevice.M11; 

        //Get the Current DPI of the monitor of the window. 
        m_currentDPI = NativeHelpers::PerMonitorDPIHelper::GetDpiForWindow(m_source->Handle);

        //Calculate the scale factor used to modify window size, graphics and text
        m_scaleFactor = m_currentDPI / m_wpfDPI; 
            
        //Update Width and Height based on the on the current DPI of the monitor
        Width = Width * m_scaleFactor;
        Height = Height * m_scaleFactor;

        //Update graphics and text based on the current DPI of the monitor
    UpdateLayoutTransform(m_scaleFactor);
        }
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

-   <span data-ttu-id="ebdc8-211">**Responde a WM \_ Notificación de ventana de DPICHANGED:** actualice el tamaño de la ventana, los gráficos y el tamaño de fuente en función de los PPP pasados en la notificación de ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-211">**Responds to WM\_DPICHANGED window notification:** Update the window size, graphics and font size based on the DPI passed in the window notification.</span></span> <span data-ttu-id="ebdc8-212">La clase base **PerMonitorDPIWindow** controla la notificación de ventana en el método **HandleMessages ()** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-212">The base class **PerMonitorDPIWindow** handles the window notification in the **HandleMessages()** method.</span></span>

    <span data-ttu-id="ebdc8-213">El tamaño de la ventana se actualiza mediante una llamada a **SetWindowPos** mediante la información que se pasa en el *lParam* del mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-213">The Window size is updated by calling **SetWindowPos** using the information passed in the *lparam* of the window message.</span></span> <span data-ttu-id="ebdc8-214">El diseño y el tamaño de los gráficos se actualizan aplicando una transformación de escala adecuada al nodo raíz de la ventana de WPF.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-214">The layout and graphics size are updated by applying an appropriate scale transform to the root node of the WPF window.</span></span> <span data-ttu-id="ebdc8-215">El factor de escala se calcula utilizando los PPP pasados en el *wParam* del mensaje de ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-215">The scale factor is calculated by using the DPI passed in the *wparam* of the window message.</span></span>

    ```C++
    IntPtr PerMonitorDPIWindow::HandleMessages(IntPtr hwnd, int msg, IntPtr wParam, IntPtr lParam, bool% )
    {
    double oldDpi;
    switch (msg)
        {
        case WM_DPICHANGED:
        LPRECT lprNewRect = (LPRECT)lParam.ToPointer();
        SetWindowPos(static_cast<HWND>(hwnd.ToPointer()), 0, lprNewRect->left, lprNewRect-
            >top, lprNewRect->right - lprNewRect->left, lprNewRect->bottom - lprNewRect->top, 
           SWP_NOZORDER | SWP_NOOWNERZORDER | SWP_NOACTIVATE);
        oldDpi = m_currentDPI;
        m_currentDPI = static_cast<int>(LOWORD(wParam.ToPointer()));
        if (oldDpi != m_currentDPI) 
            {
            OnDPIChanged();
            }
        break;
        }
    return IntPtr::Zero;
    }

    void PerMonitorDPIWindow::OnDPIChanged() 
    {
    m_scaleFactor = m_currentDPI / m_wpfDPI;
    UpdateLayoutTransform(m_scaleFactor);
    DPIChanged(this, EventArgs::Empty);
    }

    void PerMonitorDPIWindow::UpdateLayoutTransform(double scaleFactor)
    {
    // Adjust the rendering graphics and text size by applying the scale transform to the top         
    level visual node of the Window     

    if (m_perMonitorEnabled) 
        {       
            auto child = GetVisualChild(0);
            if (m_scaleFactor != 1.0) 
           {
            ScaleTransform^ dpiScale = gcnew ScaleTransform(scaleFactor, scaleFactor);
            child->SetValue(Window::LayoutTransformProperty, dpiScale);
            }
            else 
            {
            child->SetValue(Window::LayoutTransformProperty, nullptr);
            }           
        }
    }
    ```

    

## <a name="handling-dpi-change-for-assets-like-images"></a><span data-ttu-id="ebdc8-216">Controlar el cambio de PPP para activos como imágenes</span><span class="sxs-lookup"><span data-stu-id="ebdc8-216">Handling DPI change for assets like images</span></span>

<span data-ttu-id="ebdc8-217">Para actualizar el contenido de los gráficos, la aplicación WPF de ejemplo aplica una transformación de escala al nodo raíz de la aplicación WPF.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-217">In order to update graphics content, the sample WPF application applies a scale transform to the root node of the WPF application.</span></span> <span data-ttu-id="ebdc8-218">Aunque esto funciona bien para el contenido representado de forma nativa por WPF (rectángulo, texto, etc.), esto implica que WPF escala los recursos de mapa de bits como imágenes.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-218">While this works well for content that is rendered natively by WPF (rectangle, text etc.), this implies that bitmap assets like images are scaled by WPF.</span></span>

<span data-ttu-id="ebdc8-219">Con el fin de evitar los mapas de bits desenfocados causados por el escalado, el desarrollador de aplicaciones WPF puede escribir un control de imagen PPP personalizado que seleccione un recurso diferente en función del valor de PPP actual del monitor en el que se encuentra la ventana.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-219">In order to avoid blurred bitmaps caused by scaling, the WPF application developer can write a custom DPI image control that selects a different asset based on the current DPI of the monitor the window is on.</span></span> <span data-ttu-id="ebdc8-220">El control de imagen puede basarse en el evento **DPIChanged ()** que se desencadena para la ventana de WPF que usa desde **PerMonitorDPIWindow**, cuando cambia el PPP.</span><span class="sxs-lookup"><span data-stu-id="ebdc8-220">The image control can rely on the **DPIChanged()** event fired for the WPF window that consumes from the **PerMonitorDPIWindow**, when the DPI changes.</span></span>

> [!Note]  
> <span data-ttu-id="ebdc8-221">El control imagen también debe seleccionar el control derecho durante el inicio de la aplicación en el controlador de eventos de la ventana de WPF **cargado ()** .</span><span class="sxs-lookup"><span data-stu-id="ebdc8-221">The image control should also select the right control during app launch in the **Loaded()** WPF window event handler.</span></span>

 

 

 