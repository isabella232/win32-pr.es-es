---
description: Esta aplicación muestra cómo trabajar con la clase RealTimeStylus.
ms.assetid: 0ba753d1-d81a-4f7a-942c-2967c46febec
title: Ejemplo de complemento RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f593bf9e4fe0fb3d8ab12674047d6c05f28617a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279381"
---
# <a name="realtimestylus-plug-in-sample"></a><span data-ttu-id="73023-103">Ejemplo de complemento RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="73023-103">RealTimeStylus Plug-in Sample</span></span>

<span data-ttu-id="73023-104">Esta aplicación muestra cómo trabajar con la clase [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="73023-104">This application demonstrates working with the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span> <span data-ttu-id="73023-105">Para obtener información general detallada sobre las API de StylusInput, incluida la clase **RealTimeStylus** , consulte [acceso y manipulación de entradas del lápiz óptico](accessing-and-manipulating-stylus-input.md).</span><span class="sxs-lookup"><span data-stu-id="73023-105">For a detailed overview of the StylusInput APIs, including the **RealTimeStylus** class, see [Accessing and Manipulating Stylus Input](accessing-and-manipulating-stylus-input.md).</span></span> <span data-ttu-id="73023-106">Para obtener información sobre los complementos sincrónicos y asincrónicos, vea [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).</span><span class="sxs-lookup"><span data-stu-id="73023-106">For information about synchronous and asynchronous plug-ins, see [Plug-ins and the RealTimeStylus Class](plug-ins-and-the-realtimestylus-class.md).</span></span>

## <a name="overview-of-the-sample"></a><span data-ttu-id="73023-107">Información general sobre el ejemplo</span><span class="sxs-lookup"><span data-stu-id="73023-107">Overview of the Sample</span></span>

<span data-ttu-id="73023-108">Los complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) se pueden agregar a un objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="73023-108">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface can be added to a [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="73023-109">Esta aplicación de ejemplo utiliza varios tipos de complementos:</span><span class="sxs-lookup"><span data-stu-id="73023-109">This sample application uses several types of plug-in:</span></span>

-   <span data-ttu-id="73023-110">Complemento de filtros de paquetes: modifica paquetes.</span><span class="sxs-lookup"><span data-stu-id="73023-110">Packet Filter Plug-in: Modifies packets.</span></span> <span data-ttu-id="73023-111">En el complemento de filtro de paquetes de este ejemplo se modifica la información de los paquetes mediante la restricción de todos los datos de paquetes (x, y) dentro de un área rectangular.</span><span class="sxs-lookup"><span data-stu-id="73023-111">The packet filter plug-in in this sample modifies packet information by constraining all (x,y) packet data within a rectangular area.</span></span>
-   <span data-ttu-id="73023-112">Complemento de representador dinámico personalizado: modifica las cualidades de representación dinámica.</span><span class="sxs-lookup"><span data-stu-id="73023-112">Custom Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="73023-113">El complemento de representación dinámica personalizado en este ejemplo modifica el modo en que se representa la entrada de lápiz dibujando un círculo pequeño alrededor de cada punto (x, y) de un trazo.</span><span class="sxs-lookup"><span data-stu-id="73023-113">The custom dynamic rendering plug-in in this sample modifies the way ink is rendered by drawing a small circle around each (x,y) point on a stroke.</span></span>
-   <span data-ttu-id="73023-114">Complemento de representador dinámico: modifica las cualidades de representación dinámica.</span><span class="sxs-lookup"><span data-stu-id="73023-114">Dynamic Renderer Plug-in: Modifies dynamic rendering qualities.</span></span> <span data-ttu-id="73023-115">En este ejemplo se muestra el uso del objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) como complemento para controlar la representación dinámica de la entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="73023-115">This sample demonstrates use of the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object as a plug-in to handle dynamic rendering of ink.</span></span>
-   <span data-ttu-id="73023-116">Complemento de reconocedor de gestos: reconoce los gestos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73023-116">Gesture Recognizer Plug-in: Recognizes application gestures.</span></span> <span data-ttu-id="73023-117">En este ejemplo se muestra el uso del objeto [**GestureRecognizer**](gesturerecognizer-class.md) como complemento para reconocer los gestos de la aplicación (cuando se ejecuta en un sistema con el reconocedor de gestos de Microsoft presente).</span><span class="sxs-lookup"><span data-stu-id="73023-117">This sample demonstrates use of the [**GestureRecognizer**](gesturerecognizer-class.md) object as a plug-in to recognize application gestures (when running on a system with the Microsoft gesture recognizer present).</span></span>

<span data-ttu-id="73023-118">Además, este ejemplo proporciona una interfaz de usuario que permite al usuario agregar, quitar y cambiar el orden de cada complemento de la colección.</span><span class="sxs-lookup"><span data-stu-id="73023-118">In addition, this sample provides a user interface that enables the user to add, remove, and change the order of each plug-in in the collection.</span></span> <span data-ttu-id="73023-119">La solución de ejemplo contiene dos proyectos, RealTimeStylusPluginApp y RealTimeStylusPlugins.</span><span class="sxs-lookup"><span data-stu-id="73023-119">The sample solution contains two projects, RealTimeStylusPluginApp and RealTimeStylusPlugins.</span></span> <span data-ttu-id="73023-120">RealTimeStylusPluginApp contiene la interfaz de usuario para el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="73023-120">RealTimeStylusPluginApp contains the user interface for the sample.</span></span> <span data-ttu-id="73023-121">RealTimeStylusPlugins contiene las implementaciones de los complementos. El proyecto RealTimeStylusPlugins define el espacio de nombres RealTimeStylusPlugins, que contiene el filtro de paquetes y los complementos personalizados de representadores dinámicos. El proyecto RealTimeStylusPluginApp hace referencia a este espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="73023-121">RealTimeStylusPlugins contains the implementations of the plug-ins. The RealTimeStylusPlugins project defines the RealTimeStylusPlugins namespace, which contains the packet filter and custom dynamic renderer plug-ins. This namespace is referenced by the RealTimeStylusPluginApp project.</span></span> <span data-ttu-id="73023-122">El proyecto RealTimeStylusPlugins usa los espacios de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))y [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="73023-122">The RealTimeStylusPlugins project uses the [Microsoft.Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)), and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces.</span></span>

<span data-ttu-id="73023-123">Para obtener información general sobre los espacios de nombres [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) y [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consulte [arquitectura de las API de StylusInput](architecture-of-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="73023-123">For an overview of the [Microsoft.StylusInput](/previous-versions/ms824750(v=msdn.10)) and [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespaces see [Architecture of the StylusInput APIs](architecture-of-the-stylusinput-apis.md).</span></span>

## <a name="packet-filter-plug-in"></a><span data-ttu-id="73023-124">Complemento de filtro de paquetes</span><span class="sxs-lookup"><span data-stu-id="73023-124">Packet Filter Plug-in</span></span>

<span data-ttu-id="73023-125">El complemento de filtro de paquetes es un complemento sincrónico que muestra la modificación de paquetes.</span><span class="sxs-lookup"><span data-stu-id="73023-125">The packet filter plug-in is a synchronous plug-in that demonstrates packet modification.</span></span> <span data-ttu-id="73023-126">Específicamente, define un rectángulo en el formulario.</span><span class="sxs-lookup"><span data-stu-id="73023-126">Specifically, it defines a rectangle on the form.</span></span> <span data-ttu-id="73023-127">Los paquetes que se dibujen fuera de la región se representan dentro de la región.</span><span class="sxs-lookup"><span data-stu-id="73023-127">Any packets that are drawn outside the region are rendered inside the region.</span></span> <span data-ttu-id="73023-128">La clase de complemento, `PacketFilterPlugin` , se registra para recibir notificaciones `StylusDown` de `StylusUp` eventos de `Packets` entrada de lápiz, y.</span><span class="sxs-lookup"><span data-stu-id="73023-128">The plug-in class, `PacketFilterPlugin`, registers for notification of `StylusDown`, `StylusUp`, and `Packets` pen input events.</span></span> <span data-ttu-id="73023-129">La clase implementa los métodos [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))y los [paquetes](/previous-versions/ms824756(v=msdn.10)) definidos en la clase [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="73023-129">The class implements the [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10)), and [Packets](/previous-versions/ms824756(v=msdn.10)) methods defined on [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class.</span></span>

<span data-ttu-id="73023-130">El constructor público para `PacketFilterPlugin` requiere una estructura de [rectángulo](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="73023-130">The public constructor for `PacketFilterPlugin` requires a [Rectangle](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) structure.</span></span> <span data-ttu-id="73023-131">Este rectángulo define el área rectangular, en coordenadas de espacio de tinta (. 01mm = 1 HIMETRIC unidad), en la que se incluirán los paquetes.</span><span class="sxs-lookup"><span data-stu-id="73023-131">This rectangle defines the rectangular area, in ink space coordinates (.01mm = 1 HIMETRIC unit), in which packets will be contained.</span></span> <span data-ttu-id="73023-132">El rectángulo se mantiene en un campo privado, `rectangle` .</span><span class="sxs-lookup"><span data-stu-id="73023-132">The rectangle is held in a private field, `rectangle`.</span></span>


```C++
public class PacketFilterPlugin:IStylusSyncPlugin  
{
    private System.Drawing.Rectangle rectangle = System.Drawing.Rectangle.Empty;
    public PacketFilterPlugin(Rectangle r)
    {
        rectangle = r;
    }
    // ...
```



<span data-ttu-id="73023-133">La `PacketFilterPlugin` clase se registra para las notificaciones de eventos mediante la implementación del descriptor de acceso get para la propiedad de tipo de [interés](/previous-versions/ms824752(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="73023-133">The `PacketFilterPlugin` class registers for event notifications by implementing the get accessor for the [DataInterest](/previous-versions/ms824752(v=msdn.10)) property.</span></span> <span data-ttu-id="73023-134">En este caso, el complemento ha interesado en responder a las `StylusDown` `Packets` notificaciones,, `StylusUp` y `Error` .</span><span class="sxs-lookup"><span data-stu-id="73023-134">In this case, the plug-in has interested in responding to the `StylusDown`, `Packets`, `StylusUp`, and `Error` notifications.</span></span> <span data-ttu-id="73023-135">El ejemplo devuelve estos valores tal como se define en la enumeración [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="73023-135">The sample returns these values as defined in the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span> <span data-ttu-id="73023-136">Se llama al método [StylusDown](/previous-versions/ms824761(v=msdn.10)) cuando la punta del lápiz se pone en contacto con la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="73023-136">The [StylusDown](/previous-versions/ms824761(v=msdn.10)) method is called when the pen tip contacts the digitizer surface.</span></span> <span data-ttu-id="73023-137">Se llama al método [StylusUp](/previous-versions/ms824764(v=msdn.10)) cuando la punta del lápiz sale de la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="73023-137">The [StylusUp](/previous-versions/ms824764(v=msdn.10)) method is called when the pen tip leaves the digitizer surface.</span></span> <span data-ttu-id="73023-138">Se llama al método de [paquetes](/previous-versions/ms824756(v=msdn.10)) cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) recibe paquetes.</span><span class="sxs-lookup"><span data-stu-id="73023-138">The [Packets](/previous-versions/ms824756(v=msdn.10)) method is called when the [**RealTimeStylus**](realtimestylus-class.md) object receives packets.</span></span> <span data-ttu-id="73023-139">Se llama al método [error](/previous-versions/ms585069(v=vs.100)) cuando el complemento actual o un complemento anterior produce una excepción.</span><span class="sxs-lookup"><span data-stu-id="73023-139">The [Error](/previous-versions/ms585069(v=vs.100)) method is called when the current plug-in or a previous plug-in throws an exception.</span></span>


```C++
public DataInterestMask DataInterest
{
    get
    {
        return DataInterestMask.StylusDown | 
               DataInterestMask.Packets | 
               DataInterestMask.StylusUp | 
               DataInterestMask.Error;
    }
}           
    //...
```



<span data-ttu-id="73023-140">La `PacketFilterPlugin` clase controla la mayoría de estas notificaciones en un método auxiliar, `ModifyPacketData` .</span><span class="sxs-lookup"><span data-stu-id="73023-140">The `PacketFilterPlugin` class handles most of these notifications in a helper method, `ModifyPacketData`.</span></span> <span data-ttu-id="73023-141">El `ModifyPacketData` método obtiene los valores x e y de cada nuevo paquete de la clase [PacketsData](/previous-versions/ms824590(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="73023-141">The `ModifyPacketData` method gets the x and y values for each new packet from the [PacketsData](/previous-versions/ms824590(v=msdn.10)) class.</span></span> <span data-ttu-id="73023-142">Si alguno de los valores está fuera del rectángulo, el método reemplaza el valor por el punto más cercano que todavía está dentro del rectángulo.</span><span class="sxs-lookup"><span data-stu-id="73023-142">If either value is outside the rectangle, the method replaces the value with the nearest point that still falls within the rectangle.</span></span> <span data-ttu-id="73023-143">Este es un ejemplo de cómo un complemento puede reemplazar los datos de paquetes a medida que se reciben desde el flujo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="73023-143">This is an example of how a plug-in can replace packet data as it is received from the pen-input stream.</span></span>


```C++
private void ModifyPacketData(StylusDataBase data)
{
    for (int i = 0; i < data.Count ; i += data.PacketPropertyCount)
    {
        // packet data always has x followed by y followed by the rest
        int x = data[i];
        int y = data[i+1];

        // Constrain points to the input rectangle
        x = Math.Max(x, rectangle.Left);
        x = Math.Min(x, rectangle.Right);
        y = Math.Max(y, rectangle.Top);
        y = Math.Min(y, rectangle.Bottom);

        // If necessary, modify the x,y packet data
        if (x != data[i])
        {
            data[i] = x;
        }
        if (y != data[i+1])
        {
            data[i+1] = y;
        } 
    }
}
```



## <a name="custom-dynamic-renderer-plug-in"></a><span data-ttu-id="73023-144">Complemento de representador dinámico personalizado</span><span class="sxs-lookup"><span data-stu-id="73023-144">Custom Dynamic Renderer Plug-in</span></span>

<span data-ttu-id="73023-145">La `CustomDynamicRenderer` clase también implementa la clase [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) para recibir notificaciones de entrada de lápiz.</span><span class="sxs-lookup"><span data-stu-id="73023-145">The `CustomDynamicRenderer` class also implements the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) class to receive pen-input notifications.</span></span> <span data-ttu-id="73023-146">Después, controla la `Packets` notificación para dibujar un círculo pequeño alrededor de cada nuevo punto de paquete.</span><span class="sxs-lookup"><span data-stu-id="73023-146">It then handles the `Packets` notification to draw a small circle around each new packet point.</span></span>

<span data-ttu-id="73023-147">La clase contiene una variable de [gráficos](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) que contiene una referencia al objeto Graphics pasado al constructor de clase.</span><span class="sxs-lookup"><span data-stu-id="73023-147">The class contains a [Graphics](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) variable that holds a reference to the graphics object passed into the class constructor.</span></span> <span data-ttu-id="73023-148">Es el objeto Graphics que se usa para la representación dinámica.</span><span class="sxs-lookup"><span data-stu-id="73023-148">This is the graphics object used for dynamic rendering.</span></span>


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



<span data-ttu-id="73023-149">Cuando el complemento de representador dinámico personalizado recibe una notificación de paquetes, extrae los datos (x, y) y dibuja un círculo verde pequeño alrededor del punto.</span><span class="sxs-lookup"><span data-stu-id="73023-149">When the custom dynamic renderer plug-in receives a Packets notification, it extracts the (x,y) data and draws a small green circle around the point.</span></span> <span data-ttu-id="73023-150">Este es un ejemplo de representación personalizada basada en el flujo de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="73023-150">This is an example of custom rendering based on the pen-input stream.</span></span>


```C++
public void Packets(RealTimeStylus sender,  PacketsData data)
{           
    for (int i = 0; i < data.Count; i += data.PacketPropertyCount)
    {
        // Packet data always has x followed by y followed by the rest
        Point point = new Point(data[i], data[i+1]);

        // Since the packet data is in Ink Space coordinates, we need to convert to Pixels...
        point.X = (int)Math.Round((float)point.X * (float)myGraphics.DpiX/2540.0F);
        point.Y = (int)Math.Round((float)point.Y * (float)myGraphics.DpiY/2540.0F);

        // Draw a circle corresponding to the packet
        myGraphics.DrawEllipse(Pens.Green, point.X - 2, point.Y - 2, 4, 4);
    }
}
```



## <a name="the-realtimestyluspluginapp-project"></a><span data-ttu-id="73023-151">El proyecto RealTimeStylusPluginApp</span><span class="sxs-lookup"><span data-stu-id="73023-151">The RealTimeStylusPluginApp Project</span></span>

<span data-ttu-id="73023-152">En el proyecto RealTimeStylusPluginApp se muestran los complementos descritos anteriormente, así como los complementos [**GestureRecognizer**](gesturerecognizer-class.md) y [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . La interfaz de usuario del proyecto se compone de:</span><span class="sxs-lookup"><span data-stu-id="73023-152">The RealTimeStylusPluginApp project demonstrates the plug-ins previously described, as well as the [**GestureRecognizer**](gesturerecognizer-class.md) and [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) plug-ins. The project's user interface consists of:</span></span>

-   <span data-ttu-id="73023-153">Un formulario que contiene un control [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) que se usa para definir el área de entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="73023-153">A Form that contains a [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) control used to define the ink entry area.</span></span>
-   <span data-ttu-id="73023-154">Control [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) para enumerar y seleccionar los complementos disponibles.</span><span class="sxs-lookup"><span data-stu-id="73023-154">A [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) control to list and select the available plug-ins.</span></span>
-   <span data-ttu-id="73023-155">Un par de [objetos de botón](/dotnet/api/system.windows.forms.button?view=netcore-3.1) que permiten volver a ordenar los complementos.</span><span class="sxs-lookup"><span data-stu-id="73023-155">A pair of [Button objects](/dotnet/api/system.windows.forms.button?view=netcore-3.1) to enable re-ordering the plug-ins.</span></span>

<span data-ttu-id="73023-156">El proyecto define una estructura, `PlugInListItem` , para facilitar la administración de los complementos que se usan en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="73023-156">The project defines a structure, `PlugInListItem`, to make managing the plug-ins used in the project easier.</span></span> <span data-ttu-id="73023-157">La `PlugInListItem` estructura contiene el complemento y una descripción.</span><span class="sxs-lookup"><span data-stu-id="73023-157">The `PlugInListItem` structure contains the plug-in and a description.</span></span>

<span data-ttu-id="73023-158">La `RealTimeStylusPluginApp` propia clase implementa la clase [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="73023-158">The `RealTimeStylusPluginApp` class itself implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) class.</span></span> <span data-ttu-id="73023-159">Esto es necesario para que se `RealTimeStylusPluginApp` pueda notificar a la clase cuando el complemento [**GestureRecognizer**](gesturerecognizer-class.md) agrega datos de gestos a la cola de salida.</span><span class="sxs-lookup"><span data-stu-id="73023-159">This is necessary so that the `RealTimeStylusPluginApp` class can be notified when the [**GestureRecognizer**](gesturerecognizer-class.md) plug-in adds gesture data to the output queue.</span></span> <span data-ttu-id="73023-160">La aplicación se registra para la notificación de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="73023-160">The application registers for notification of [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)).</span></span> <span data-ttu-id="73023-161">Cuando se reciben datos de gestos, `RealTimeStylusPluginApp` coloca una descripción en la barra de estado en la parte inferior del formulario.</span><span class="sxs-lookup"><span data-stu-id="73023-161">When gesture data is received, `RealTimeStylusPluginApp` places a description of it on the status bar at the bottom of the form.</span></span>


```C++
public void CustomStylusDataAdded(RealTimeStylus sender, CustomStylusData data)
{
    if (data.CustomDataId == GestureRecognizer.GestureRecognitionDataGuid)
    {
        GestureRecognitionData grd = data.Data as GestureRecognitionData;
        if (grd != null)
        {
            if (grd.Count > 0)
            {
                GestureAlternate ga = grd[0];
                sbGesture.Text = "Gesture=" + ga.Id + ", Confidence=" + ga.Confidence;
            }
        }
    }
}
```



> [!Note]  
> En la implementación de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , es interesante que pueda identificar los datos de gestos personalizados en la cola de salida por GUID (mediante el campo [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) o por tipo (mediante el resultado de la instrucción as). En el ejemplo se usan ambas técnicas de identificación para fines de demostración. <span data-ttu-id="73023-164">También es válido cualquier enfoque por sí solo.</span><span class="sxs-lookup"><span data-stu-id="73023-164">Either approach alone is also valid.</span></span>

 

<span data-ttu-id="73023-165">En el controlador de eventos de carga del formulario, la aplicación crea instancias de las `PacketFilter` `CustomDynamicRenderer` clases y y las agrega al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="73023-165">In the Form's Load event handler, the application creates instances of the `PacketFilter` and `CustomDynamicRenderer` classes and adds them to the list box.</span></span> <span data-ttu-id="73023-166">A continuación, la aplicación intenta crear una instancia de la clase [**GestureRecognizer**](gesturerecognizer-class.md) y, si se realiza correctamente, la agrega al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="73023-166">The application then attempts to create an instance of the [**GestureRecognizer**](gesturerecognizer-class.md) class and, if successful, adds it to the list box.</span></span> <span data-ttu-id="73023-167">Se produce un error si el reconocedor de gestos no está presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="73023-167">This fails if the gesture recognizer is not present on the system.</span></span> <span data-ttu-id="73023-168">A continuación, la aplicación crea una instancia de un objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y lo agrega al cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="73023-168">Next, the application instantiates a [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object and adds it to the list box.</span></span> <span data-ttu-id="73023-169">Por último, la aplicación habilita cada uno de los complementos y el propio objeto [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="73023-169">Finally, the application enables each of the plug-ins and the [**RealTimeStylus**](realtimestylus-class.md) object itself.</span></span>

<span data-ttu-id="73023-170">Otro aspecto importante que hay que tener en cuenta sobre el ejemplo es que en los métodos auxiliares, el objeto [**RealTimeStylus**](realtimestylus-class.md) se deshabilita primero antes de que se agreguen o quiten complementos y se vuelvan a habilitar después de completar la adición o la eliminación.</span><span class="sxs-lookup"><span data-stu-id="73023-170">Another important thing to note about the sample is that in the helper methods, the [**RealTimeStylus**](realtimestylus-class.md) object is first disabled before plug-ins are added or removed and then re-enabled after the addition or removal is complete.</span></span>


```C++
private void RemoveFromPluginCollection(int index)
{
    IStylusSyncPlugin plugin = ((PluginListItem)chklbPlugins.Items[index]).Plugin;

    bool rtsEnabled = myRealTimeStylus.Enabled;
    myRealTimeStylus.Enabled = false;
    myRealTimeStylus.SyncPluginCollection.Remove(plugin);
    myRealTimeStylus.Enabled = rtsEnabled;
}
```



## <a name="related-topics"></a><span data-ttu-id="73023-171">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="73023-171">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="73023-172">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="73023-172">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms575176(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="73023-173">[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73023-173">[Microsoft.StylusInput.GestureRecognizer](/previous-versions/ms826046(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="73023-174">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73023-174">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="73023-175">[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="73023-175">[Microsoft.StylusInput.DataInterestMask](/previous-versions/ms575174(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="73023-176">[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73023-176">[Microsoft.StylusInput.IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="73023-177">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="73023-177">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="73023-178">[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="73023-178">[Microsoft.StylusInput.PluginData.PacketsData](/previous-versions/ms575281(v=vs.100))</span></span>
</dt> <dt>

[<span data-ttu-id="73023-179">Acceso y manipulación de la entrada del lápiz óptico</span><span class="sxs-lookup"><span data-stu-id="73023-179">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[<span data-ttu-id="73023-180">Complementos y la clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="73023-180">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="73023-181">Ejemplo de colección de tintas RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="73023-181">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
