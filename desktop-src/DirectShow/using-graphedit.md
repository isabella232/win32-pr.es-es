---
description: Usar GraphEdit
ms.assetid: 91a8f111-fce4-4284-afa2-e3ea0ec35bff
title: Usar GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e78118253d86a88231456b72dc8c42ed2a674f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546054"
---
# <a name="using-graphedit"></a><span data-ttu-id="42cf3-103">Usar GraphEdit</span><span class="sxs-lookup"><span data-stu-id="42cf3-103">Using GraphEdit</span></span>

<span data-ttu-id="42cf3-104">GraphEdit está disponible en el kit de desarrollo de software (SDK) de Microsoft Windows ( <https://go.microsoft.com/fwlink/p/?linkid=62332> ).</span><span class="sxs-lookup"><span data-stu-id="42cf3-104">GraphEdit is available in the Microsoft Windows Software Development Kit (SDK) (<https://go.microsoft.com/fwlink/p/?linkid=62332>).</span></span>

<span data-ttu-id="42cf3-105">El nombre de la aplicación GraphEdit es "graphedt.exe".</span><span class="sxs-lookup"><span data-stu-id="42cf3-105">The name of the GraphEdit application is "graphedt.exe".</span></span> <span data-ttu-id="42cf3-106">Después de instalar el SDK, "graphedt.exe" se encuentra en el siguiente directorio: \[ archivos de programa \] \\ Microsoft SDK \\ Windows \\ \[ version \] \\ bin \\ .</span><span class="sxs-lookup"><span data-stu-id="42cf3-106">After you install the SDK, "graphedt.exe" is located in the following directory: \[Program Files\]\\Microsoft SDKs\\Windows\\\[version\]\\Bin\\.</span></span>

<span data-ttu-id="42cf3-107">Antes de ejecutar GraphEdit, use la utilidad regsvr32 para registrar los siguientes archivos dll, que se encuentran en el mismo directorio:</span><span class="sxs-lookup"><span data-stu-id="42cf3-107">Before running GraphEdit, use the regsvr32 utility to register the following DLLs, which are located in the same directory:</span></span>

-   <span data-ttu-id="42cf3-108">proppage.dll</span><span class="sxs-lookup"><span data-stu-id="42cf3-108">proppage.dll</span></span>
-   <span data-ttu-id="42cf3-109">evrprop.dll</span><span class="sxs-lookup"><span data-stu-id="42cf3-109">evrprop.dll</span></span>

<span data-ttu-id="42cf3-110">Estos archivos dll permiten a GraphEdit mostrar páginas de propiedades para algunos de los filtros de DirectShow integrados.</span><span class="sxs-lookup"><span data-stu-id="42cf3-110">These DLLs enable GraphEdit to display property pages for some of the built-in DirectShow filters.</span></span>

## <a name="build-a-file-playback-graph"></a><span data-ttu-id="42cf3-111">Crear un gráfico de reproducción de archivos</span><span class="sxs-lookup"><span data-stu-id="42cf3-111">Build a File Playback Graph</span></span>

<span data-ttu-id="42cf3-112">GraphEdit puede crear un gráfico de filtro para la reproducción de archivos.</span><span class="sxs-lookup"><span data-stu-id="42cf3-112">GraphEdit can build a filter graph for file playback.</span></span> <span data-ttu-id="42cf3-113">Esta característica es equivalente a llamar al método [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="42cf3-113">This feature is equivalent to calling the [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) method in an application.</span></span> <span data-ttu-id="42cf3-114">En el menú **archivo** , haga clic en **representar archivo multimedia**.</span><span class="sxs-lookup"><span data-stu-id="42cf3-114">From the **File** menu, click **Render Media File**.</span></span> <span data-ttu-id="42cf3-115">GraphEdit muestra un cuadro de diálogo **Abrir archivo** .</span><span class="sxs-lookup"><span data-stu-id="42cf3-115">GraphEdit displays an **Open File** dialog box.</span></span> <span data-ttu-id="42cf3-116">Seleccione un archivo multimedia y haga clic en **abrir**.</span><span class="sxs-lookup"><span data-stu-id="42cf3-116">Select a multimedia file and click **Open**.</span></span> <span data-ttu-id="42cf3-117">GraphEdit crea un gráfico de filtro para reproducir el archivo que ha seleccionado.</span><span class="sxs-lookup"><span data-stu-id="42cf3-117">GraphEdit builds a filter graph to play the file you've selected.</span></span>

<span data-ttu-id="42cf3-118">También puede representar un archivo multimedia ubicado en una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="42cf3-118">You can also render a media file located at a URL.</span></span> <span data-ttu-id="42cf3-119">En el menú **archivo** , haga clic en **representar dirección URL**.</span><span class="sxs-lookup"><span data-stu-id="42cf3-119">From the **File** menu, click **Render URL**.</span></span> <span data-ttu-id="42cf3-120">GraphEdit muestra un cuadro de diálogo en el que se va a escribir la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="42cf3-120">GraphEdit displays a dialog box in which to type the URL.</span></span>

## <a name="build-a-filter-graph"></a><span data-ttu-id="42cf3-121">Crear un gráfico de filtro</span><span class="sxs-lookup"><span data-stu-id="42cf3-121">Build a Filter Graph</span></span>

<span data-ttu-id="42cf3-122">GraphEdit puede crear un gráfico de filtro personalizado mediante cualquiera de los filtros registrados en el sistema.</span><span class="sxs-lookup"><span data-stu-id="42cf3-122">GraphEdit can build a custom filter graph, using any of the filters registered on your system.</span></span> <span data-ttu-id="42cf3-123">En el menú **gráfico** , haga clic en **Insertar filtros**.</span><span class="sxs-lookup"><span data-stu-id="42cf3-123">From the **Graph** menu, click **Insert Filters**.</span></span> <span data-ttu-id="42cf3-124">Aparece un cuadro de diálogo con una lista de los filtros del sistema organizados por categoría de filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-124">A dialog box appears with a list of the filters on your system, organized by filter category.</span></span> <span data-ttu-id="42cf3-125">GraphEdit crea esta lista a partir de la información del registro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-125">GraphEdit builds this list from information in the registry.</span></span> <span data-ttu-id="42cf3-126">En la ilustración siguiente se muestra el cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="42cf3-126">The following illustration shows the dialog box.</span></span>

![¿Qué Filtros desea insertar?](images/gedit12.png)

<span data-ttu-id="42cf3-128">Para agregar un filtro al gráfico, seleccione el nombre del filtro y haga clic en el botón **Insertar filtros** o haga doble clic en el nombre del filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-128">To add a filter to the graph, select the name of the filter and click the **Insert Filters** button, or double-click the filter name.</span></span> <span data-ttu-id="42cf3-129">Una vez agregados los filtros, puede conectar dos filtros arrastrando el mouse desde el anclaje de salida de un filtro hasta el anclaje de entrada de otro filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-129">After you have added the filters, you can connect two filters by dragging the mouse from one filter's output pin to another filter's input pin.</span></span> <span data-ttu-id="42cf3-130">Si los pin aceptan la conexión, GraphEdit dibuja una flecha que los conecta.</span><span class="sxs-lookup"><span data-stu-id="42cf3-130">If the pins accept the connection, GraphEdit draws an arrow connecting them.</span></span>

![conexión de dos filtros](images/gedit-connect.png)

## <a name="run-the-graph"></a><span data-ttu-id="42cf3-132">Ejecutar el gráfico</span><span class="sxs-lookup"><span data-stu-id="42cf3-132">Run the Graph</span></span>

<span data-ttu-id="42cf3-133">Una vez que haya creado un gráfico de filtro en la edición del gráfico, puede ejecutar el gráfico para ver si funciona como se espera.</span><span class="sxs-lookup"><span data-stu-id="42cf3-133">Once you have built a filter graph in Graph Edit, you can run the graph to see whether it works as you expect.</span></span> <span data-ttu-id="42cf3-134">El menú **gráfico** contiene los comandos de menú **reproducir**, **pausar** y **detener**.</span><span class="sxs-lookup"><span data-stu-id="42cf3-134">The **Graph** menu contains the menu commands **Play**, **Pause**, and **Stop**.</span></span> <span data-ttu-id="42cf3-135">Estos comandos invocan a los métodos [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) [**Ejecutar**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**pausar**](/windows/desktop/api/Control/nf-control-imediacontrol-pause)y [**detener**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="42cf3-135">These commands invoke to the [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) methods [**Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), [**Pause**](/windows/desktop/api/Control/nf-control-imediacontrol-pause), and [**Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop), respectively.</span></span> <span data-ttu-id="42cf3-136">La barra de herramientas GraphEdit tiene botones para estos comandos, también:</span><span class="sxs-lookup"><span data-stu-id="42cf3-136">The GraphEdit toolbar has buttons for these commands, as well:</span></span>

![botones pausar, reproducir y detener](images/gedit-toolbar.png)

> [!Note]  
> <span data-ttu-id="42cf3-138">El comando GraphEdit **Stop** primero pausa el gráfico y busca el tiempo cero (suponiendo que se pueda buscar en el gráfico).</span><span class="sxs-lookup"><span data-stu-id="42cf3-138">The GraphEdit **Stop** command first pauses the graph and seeks to time zero (assuming the graph is seekable).</span></span> <span data-ttu-id="42cf3-139">Para la reproducción de archivos, esta acción restablece la ventana de vídeo en el primer fotograma.</span><span class="sxs-lookup"><span data-stu-id="42cf3-139">For file playback, this action resets the video window to the first frame.</span></span> <span data-ttu-id="42cf3-140">A continuación, GraphEdit llama a [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span><span class="sxs-lookup"><span data-stu-id="42cf3-140">Then GraphEdit calls [**IMediaControl::Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop).</span></span>

 

<span data-ttu-id="42cf3-141">Si el gráfico es buscable, puede buscarlo arrastrando la barra deslizante que aparece debajo de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="42cf3-141">If the graph is seekable, you can seek it by dragging the slider bar that appears below the toolbar.</span></span> <span data-ttu-id="42cf3-142">Al arrastrar la barra deslizante se invoca el método [**IMediaSeeking:: SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="42cf3-142">Dragging the slider bar invokes the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span>

## <a name="view-property-pages"></a><span data-ttu-id="42cf3-143">Ver páginas de propiedades</span><span class="sxs-lookup"><span data-stu-id="42cf3-143">View Property Pages</span></span>

<span data-ttu-id="42cf3-144">Algunos filtros admiten páginas de propiedades personalizadas, que proporcionan una interfaz de usuario para establecer las propiedades del filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-144">Some filters support custom property pages, which provide a user interface for setting properties on the filter.</span></span> <span data-ttu-id="42cf3-145">Para ver la página de propiedades de un filtro en GraphEdit, haga clic con el botón secundario en el filtro y seleccione **propiedades** en la ventana emergente.</span><span class="sxs-lookup"><span data-stu-id="42cf3-145">To view a filter's property page in GraphEdit, right-click the filter and select **Properties** from the pop-up window.</span></span> <span data-ttu-id="42cf3-146">GraphEdit muestra una página de propiedades que contiene las hojas de propiedades definidas por el filtro (si existe).</span><span class="sxs-lookup"><span data-stu-id="42cf3-146">GraphEdit displays a property page that contains the property sheets defined by the filter (if any).</span></span> <span data-ttu-id="42cf3-147">Además, GraphEdit incluye una hoja de propiedades para cada pin del filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-147">In addition, GraphEdit includes a property sheet for each pin on the filter.</span></span> <span data-ttu-id="42cf3-148">Las hojas de propiedades de anclaje están definidas por GraphEdit, no por el filtro.</span><span class="sxs-lookup"><span data-stu-id="42cf3-148">The pin property sheets are defined by GraphEdit, not by the filter.</span></span> <span data-ttu-id="42cf3-149">Si el PIN está conectado, la hoja de propiedades del PIN muestra el tipo de medio para la conexión.</span><span class="sxs-lookup"><span data-stu-id="42cf3-149">If the pin is connected, the pin property sheet displays the media type for the connection.</span></span> <span data-ttu-id="42cf3-150">De lo contrario, muestra los tipos de medios preferidos del PIN.</span><span class="sxs-lookup"><span data-stu-id="42cf3-150">Otherwise, it lists the pin's preferred media types.</span></span>

> [!Note]  
> <span data-ttu-id="42cf3-151">Para usar las páginas de propiedades integradas de GraphEdit, debe registrar proppage.dll.</span><span class="sxs-lookup"><span data-stu-id="42cf3-151">To use GraphEdit's built-in property pages, you must register proppage.dll.</span></span> <span data-ttu-id="42cf3-152">Este archivo DLL está disponible en el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="42cf3-152">This DLL is available in the Windows SDK.</span></span> <span data-ttu-id="42cf3-153">El archivo DLL también contiene páginas de propiedades adicionales para algunos filtros de DirectShow.</span><span class="sxs-lookup"><span data-stu-id="42cf3-153">The DLL also contains additional property pages for some DirectShow filters.</span></span> <span data-ttu-id="42cf3-154">Estas páginas de propiedades se proporcionan solo con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="42cf3-154">These property pages are provided for debugging purposes only.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="42cf3-155">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42cf3-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42cf3-156">Simular la compilación de gráficos con GraphEdit</span><span class="sxs-lookup"><span data-stu-id="42cf3-156">Simulating Graph Building with GraphEdit</span></span>](simulating-graph-building-with-graphedit.md)
</dt> </dl>

 

 



