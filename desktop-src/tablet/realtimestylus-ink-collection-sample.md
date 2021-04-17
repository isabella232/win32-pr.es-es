---
description: Esta aplicación muestra la representación y recopilación de entradas manuscritas cuando se usa la clase RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Ejemplo de colección de tintas RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24fe67ed59ea1a69f5d0d9a2656169f2df88a450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706776"
---
# <a name="realtimestylus-ink-collection-sample"></a><span data-ttu-id="7d512-103">Ejemplo de colección de tintas RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="7d512-103">RealTimeStylus Ink Collection Sample</span></span>

<span data-ttu-id="7d512-104">Esta aplicación muestra la representación y recopilación de entradas manuscritas cuando se usa la clase [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="7d512-104">This application demonstrates ink collection and rendering when using the [**RealTimeStylus**](realtimestylus-class.md) class.</span></span>

## <a name="the-inkcollection-project"></a><span data-ttu-id="7d512-105">El proyecto InkCollection</span><span class="sxs-lookup"><span data-stu-id="7d512-105">The InkCollection Project</span></span>

<span data-ttu-id="7d512-106">Este ejemplo consta de una única solución que contiene un proyecto, InkCollection.</span><span class="sxs-lookup"><span data-stu-id="7d512-106">This sample consists of a single solution that contains one project, InkCollection.</span></span> <span data-ttu-id="7d512-107">La aplicación define el `InkCollection` espacio de nombres que contiene una sola clase, también denominada `InkCollection` .</span><span class="sxs-lookup"><span data-stu-id="7d512-107">The application defines the `InkCollection` namespace that contains a single class, also called `InkCollection`.</span></span> <span data-ttu-id="7d512-108">La clase hereda de la clase [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .</span><span class="sxs-lookup"><span data-stu-id="7d512-108">The class inherits from the [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and implements the [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface.</span></span>


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



<span data-ttu-id="7d512-109">La clase InkCollection define un conjunto de constantes privadas que se usan para especificar varios grosores de la tinta.</span><span class="sxs-lookup"><span data-stu-id="7d512-109">The InkCollection Class defines a set of private constants used to specify various ink thickness.</span></span> <span data-ttu-id="7d512-110">La clase también declara instancias privadas de la clase [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la clase [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` y la clase de [representador](/previous-versions/ms828481(v=msdn.10)) `myRenderer` .</span><span class="sxs-lookup"><span data-stu-id="7d512-110">The class also declares private instances of the [**RealTimeStylus**](realtimestylus-class.md) class, `myRealTimeStylus`, the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) class, `myDynamicRenderer`, and the [Renderer](/previous-versions/ms828481(v=msdn.10)) class `myRenderer`.</span></span> <span data-ttu-id="7d512-111">**DynamicRenderer** representa el [trazo](/previous-versions/ms552692(v=vs.100)) que se está recopilando actualmente.</span><span class="sxs-lookup"><span data-stu-id="7d512-111">The **DynamicRenderer** renders the [Stroke](/previous-versions/ms552692(v=vs.100)) that is currently being collected.</span></span> <span data-ttu-id="7d512-112">El objeto representador, `myRenderer` , representa los objetos Stroke que ya se han recopilado.</span><span class="sxs-lookup"><span data-stu-id="7d512-112">The Renderer object, `myRenderer`, renders Stroke objects that have already been collected.</span></span>


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



<span data-ttu-id="7d512-113">La clase también declara un objeto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , que se utiliza para almacenar los datos de paquetes que se están recopilando mediante uno o varios objetos [cursor](/previous-versions/ms552104(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-113">The class also declares a [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) object, `myPackets`, which is used to store packet data that is being collected by one or more [Cursor](/previous-versions/ms552104(v=vs.100)) objects.</span></span> <span data-ttu-id="7d512-114">Los valores de [identificador](/previous-versions/ms824826(v=msdn.10)) del objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) se usan como la clave de tabla hash para identificar de forma exclusiva los datos de paquete recopilados para un objeto de cursor determinado.</span><span class="sxs-lookup"><span data-stu-id="7d512-114">The [Stylus](/previous-versions/ms824824(v=msdn.10)) object's [Id](/previous-versions/ms824826(v=msdn.10)) values are used as the hashtable key to uniquely identify the packet data collected for a given Cursor object.</span></span>

<span data-ttu-id="7d512-115">Una instancia privada del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) , `myInk` , almacena los objetos de [trazo](/previous-versions/ms552692(v=vs.100)) recopilados por `myRealTimeStylus` .</span><span class="sxs-lookup"><span data-stu-id="7d512-115">A private instance of the [Ink](/previous-versions/aa515768(v=msdn.10)) object, `myInk`, stores [Stroke](/previous-versions/ms552692(v=vs.100)) objects collected by `myRealTimeStylus`.</span></span>


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a><span data-ttu-id="7d512-116">El evento de carga de formulario</span><span class="sxs-lookup"><span data-stu-id="7d512-116">The Form Load Event</span></span>

<span data-ttu-id="7d512-117">En el controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, `myDynamicRenderer` se crea una instancia de con el [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) que toma un control como argumento y `myRenderer` se construye con un constructor sin argumentos.</span><span class="sxs-lookup"><span data-stu-id="7d512-117">In the [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler for the form, `myDynamicRenderer` is instantiated by using the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) that takes a control as an argument, and `myRenderer` is constructed with a no-argument constructor.</span></span>


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



<span data-ttu-id="7d512-118">Preste atención al comentario que sigue a la creación de instancias de los representadores, ya que `myDynamicRenderer` usa los valores predeterminados de [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) al representar la tinta.</span><span class="sxs-lookup"><span data-stu-id="7d512-118">Pay attention to the comment that follows the instantiation of the renderers, because `myDynamicRenderer` uses the default values for [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) when rendering the ink.</span></span> <span data-ttu-id="7d512-119">Este es el comportamiento estándar.</span><span class="sxs-lookup"><span data-stu-id="7d512-119">This is standard behavior.</span></span> <span data-ttu-id="7d512-120">Sin embargo, si desea proporcionar a la entrada de lápiz `myDynamicRenderer` una apariencia diferente a la de la entrada de lápiz representada por `myRenderer` , puede cambiar la propiedad [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) en `myDynamicRenderer` .</span><span class="sxs-lookup"><span data-stu-id="7d512-120">However, if you wish to give the ink rendered by `myDynamicRenderer` a different look from ink rendered by `myRenderer`, you can change the [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) property on `myDynamicRenderer`.</span></span> <span data-ttu-id="7d512-121">Para ello, quite la marca de comentario de las líneas siguientes antes de compilar y ejecutar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7d512-121">To do so, uncomment the following lines before you build and run the application.</span></span>


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



<span data-ttu-id="7d512-122">A continuación, la aplicación crea el objeto [**RealTimeStylus**](realtimestylus-class.md) que se usa para recibir notificaciones del lápiz y agrega el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a la cola de notificaciones de complementos sincrónicos.</span><span class="sxs-lookup"><span data-stu-id="7d512-122">Next, the application creates the [**RealTimeStylus**](realtimestylus-class.md) object that is used to receive stylus notifications and adds the [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) object to the synchronous plug-in notification queue.</span></span> <span data-ttu-id="7d512-123">Concretamente `myRealTimeStylus` , `myDynamicRenderer` se agrega a la propiedad [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-123">Specifically, `myRealTimeStylus` adds `myDynamicRenderer` to the [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) property.</span></span>


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



<span data-ttu-id="7d512-124">A continuación, se agrega el formulario a la cola de notificaciones de complementos asincrónica.</span><span class="sxs-lookup"><span data-stu-id="7d512-124">The form is then added to the asynchronous plug-in notification queue.</span></span> <span data-ttu-id="7d512-125">En concreto, `InkCollection` se agrega a la propiedad [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-125">Specifically, `InkCollection` is added to the [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) property.</span></span> <span data-ttu-id="7d512-126">Por último, `myRealTimeStylus` y `myDynamicRenderer` están habilitados, y se crean instancias de los paquetes y myInk.</span><span class="sxs-lookup"><span data-stu-id="7d512-126">Finally, `myRealTimeStylus` and `myDynamicRenderer` are enabled, and myPackets and myInk are instantiated.</span></span>


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



<span data-ttu-id="7d512-127">Además de enlazar los controladores de menú para cambiar el color y el tamaño de la tinta, se requiere un bloque más breve de código antes de implementar la interfaz.</span><span class="sxs-lookup"><span data-stu-id="7d512-127">Aside from hooking up the menu handlers for changing ink color and size, one more brief block of code is required before implementing the interface.</span></span> <span data-ttu-id="7d512-128">El ejemplo debe controlar el evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del formulario.</span><span class="sxs-lookup"><span data-stu-id="7d512-128">The sample must handle the form's [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event.</span></span> <span data-ttu-id="7d512-129">En el controlador de eventos, la aplicación debe actualizarse `myDynamicRenderer` porque es posible que se esté recopilando un objeto [Stroke](/previous-versions/ms552692(v=vs.100)) en el momento en que se produce el evento Paint.</span><span class="sxs-lookup"><span data-stu-id="7d512-129">In the event handler, the application must refresh `myDynamicRenderer` because it is possible that a [Stroke](/previous-versions/ms552692(v=vs.100)) object is being collected at the time the Paint event occurs.</span></span> <span data-ttu-id="7d512-130">En ese caso, es necesario volver a dibujar la parte del objeto de trazo que ya se ha recopilado.</span><span class="sxs-lookup"><span data-stu-id="7d512-130">In that case, the portion of the Stroke object that has already been collected needs to be redrawn.</span></span> <span data-ttu-id="7d512-131">El [representador](/previous-versions/ms828481(v=msdn.10)) estático se usa para volver a dibujar los objetos de trazo que ya se han recopilado.</span><span class="sxs-lookup"><span data-stu-id="7d512-131">The static [Renderer](/previous-versions/ms828481(v=msdn.10)) is used to re-draw Stroke objects that have already been collected.</span></span> <span data-ttu-id="7d512-132">Estos trazos están en el objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) porque se colocan allí cuando se dibujan, tal como se muestra en la sección siguiente.</span><span class="sxs-lookup"><span data-stu-id="7d512-132">These strokes are in the [Ink](/previous-versions/aa515768(v=msdn.10)) object because they are placed there when drawn, as shown in the next section.</span></span>


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a><span data-ttu-id="7d512-133">Implementar la interfaz IStylusAsyncPlugin</span><span class="sxs-lookup"><span data-stu-id="7d512-133">Implementing the IStylusAsyncPlugin Interface</span></span>

<span data-ttu-id="7d512-134">La aplicación de ejemplo define los tipos de notificaciones que tiene interés en recibir en la implementación de la propiedad de [interés](/previous-versions/ms824769(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-134">The sample application defines the types of notifications it has interest in receiving in the implementation of the [DataInterest](/previous-versions/ms824769(v=msdn.10)) property.</span></span> <span data-ttu-id="7d512-135">Por lo tanto, la propiedad de tipo de interés define las notificaciones que el objeto [**RealTimeStylus**](realtimestylus-class.md) reenvía al formulario.</span><span class="sxs-lookup"><span data-stu-id="7d512-135">The DataInterest property therefore defines which notifications that the [**RealTimeStylus**](realtimestylus-class.md) object forwards to the form.</span></span> <span data-ttu-id="7d512-136">En este ejemplo, la propiedad Interest define el interés en **StylusDown**, **packets**, **StylusUp** y las notificaciones de **error** a través de la enumeración [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-136">For this sample, the DataInterest property defines interest in the **StylusDown**, **Packets**, **StylusUp**, and **Error** notifications through the [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) enumeration.</span></span>


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
```



<span data-ttu-id="7d512-137">La notificación [StylusDown](/previous-versions/ms824779(v=msdn.10)) se produce cuando el lápiz toca la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="7d512-137">The [StylusDown](/previous-versions/ms824779(v=msdn.10)) notification occurs when the pen touches the digitizer surface.</span></span> <span data-ttu-id="7d512-138">Cuando esto sucede, el ejemplo asigna una matriz que se usa para almacenar los datos de paquete para el objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-138">When this happens, the sample allocates an array that is used to store the packet data for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="7d512-139">El [StylusDownData](/previous-versions/ms824107(v=msdn.10)) del método StylusDown se agrega a la matriz y la matriz se inserta en la tabla hash utilizando la propiedad [ID](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como una clave.</span><span class="sxs-lookup"><span data-stu-id="7d512-139">The [StylusDownData](/previous-versions/ms824107(v=msdn.10)) from the StylusDown method is added to the array, and the array is inserted into the hashtable by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as a key.</span></span>


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



<span data-ttu-id="7d512-140">La notificación de [paquetes](/previous-versions/ms824773(v=msdn.10)) se produce cuando el lápiz se mueve en la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="7d512-140">The [Packets](/previous-versions/ms824773(v=msdn.10)) notification occurs when the pen moves on the digitizer surface.</span></span> <span data-ttu-id="7d512-141">Cuando esto ocurre, la aplicación agrega New [StylusDownData](/previous-versions/ms824107(v=msdn.10)) en la matriz de paquetes para el objeto [Stylus](/previous-versions/ms824824(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="7d512-141">When this occurs, the application adds new [StylusDownData](/previous-versions/ms824107(v=msdn.10)) into the packet array for the [Stylus](/previous-versions/ms824824(v=msdn.10)) object.</span></span> <span data-ttu-id="7d512-142">Para ello, se usa la propiedad [ID](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como clave para recuperar la matriz de paquetes del lápiz óptico de la tabla hash.</span><span class="sxs-lookup"><span data-stu-id="7d512-142">It does this by using the Stylus object's [Id](/previous-versions/ms824826(v=msdn.10)) property as the key to retrieve the packet array for the stylus from the hashtable.</span></span> <span data-ttu-id="7d512-143">A continuación, se insertan los datos del nuevo paquete en la matriz recuperada.</span><span class="sxs-lookup"><span data-stu-id="7d512-143">The new packet data is then inserted into the retrieved array.</span></span>


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



<span data-ttu-id="7d512-144">La notificación [StylusUp](/previous-versions/ms824782(v=msdn.10)) se produce cuando el lápiz sale de la superficie del digitalizador.</span><span class="sxs-lookup"><span data-stu-id="7d512-144">The [StylusUp](/previous-versions/ms824782(v=msdn.10)) notification occurs when the pen leaves the digitizer surface.</span></span> <span data-ttu-id="7d512-145">Cuando se produce esta notificación, el ejemplo recupera la matriz de paquetes para este objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) de la tabla hash y lo quita de la tabla hash, ya que ya no es necesario, agrega los nuevos datos del paquete y usa la matriz de datos de paquetes para crear un nuevo objeto [Stroke](/previous-versions/ms552692(v=vs.100)) , `stroke` .</span><span class="sxs-lookup"><span data-stu-id="7d512-145">When this notification occurs, the sample retrieves the packet array for this [Stylus](/previous-versions/ms824824(v=msdn.10)) object from the hashtable-removing it from the hashtable as it is no longer needed, adds in the new packet data, and uses the array of packet data to create a new [Stroke](/previous-versions/ms552692(v=vs.100)) object, `stroke`.</span></span>


```C++
public void StylusUp(RealTimeStylus sender, StylusUpData data)
{
    ArrayList collectedPackets = (ArrayList)myPackets[data.Stylus.Id];
    myPackets.Remove(data.Stylus.Id);

    collectedPackets.AddRange(data.GetData());

    int[] packets = (int[])(collectedPackets.ToArray(typeof(int)));
    TabletPropertyDescriptionCollection tabletProperties =
        myRealTimeStylus.GetTabletPropertyDescriptionCollection(data.Stylus.TabletContextId);

    Stroke stroke = myInk.CreateStroke(packets, tabletProperties);
    if (stroke != null) 
    {
         stroke.DrawingAttributes.Color = myDynamicRenderer.DrawingAttributes.Color;
         stroke.DrawingAttributes.Width = myDynamicRenderer.DrawingAttributes.Width;
    } 
}
```



<span data-ttu-id="7d512-146">Para ver un ejemplo en el que se muestra un uso más sólido de la clase [**RealTimeStylus**](realtimestylus-class.md) , incluido el uso de la creación de complementos personalizados, vea [ejemplo de complemento RealTimeStylus](realtimestylus-plug-in-sample.md).</span><span class="sxs-lookup"><span data-stu-id="7d512-146">For an example that shows more robust use of the [**RealTimeStylus**](realtimestylus-class.md) class, including the use of custom plug-in creation, see [RealTimeStylus Plug-in Sample](realtimestylus-plug-in-sample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d512-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d512-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7d512-148">[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="7d512-148">[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))</span></span>
</dt> <dt>

<span data-ttu-id="7d512-149">[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7d512-149">[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="7d512-150">[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7d512-150">[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))</span></span>
</dt> <dt>

<span data-ttu-id="7d512-151">[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="7d512-151">[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))</span></span>
</dt> <dt>

[<span data-ttu-id="7d512-152">Acceso y manipulación de la entrada del lápiz óptico</span><span class="sxs-lookup"><span data-stu-id="7d512-152">Accessing and Manipulating Stylus Input</span></span>](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
