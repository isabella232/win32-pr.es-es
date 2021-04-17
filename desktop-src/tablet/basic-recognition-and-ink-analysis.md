---
description: En este tema se presentan las API de análisis de tinta.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconocimiento básico y análisis de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423508"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="7657e-103">Reconocimiento básico y análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7657e-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="7657e-104">En este tema se presentan las API de análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="7657e-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="7657e-105">Reconocimiento simple</span><span class="sxs-lookup"><span data-stu-id="7657e-105">Simple Recognition</span></span>

<span data-ttu-id="7657e-106">La funcionalidad básica expuesta por la API de análisis de tinta es el acceso a los resultados del reconocimiento de un determinado fragmento de tinta.</span><span class="sxs-lookup"><span data-stu-id="7657e-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="7657e-107">Esto es sencillo y sencillo, tal y como se muestra en el código de ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7657e-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="7657e-108">Los resultados de la operación de reconocimiento son simplemente un valor de cadena que representa el valor reconocido de la tinta manuscrita.</span><span class="sxs-lookup"><span data-stu-id="7657e-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="7657e-109">La API de análisis de tinta expone mucha más funcionalidad de reconocimiento que solo la cadena reconocida, pero es la operación más común.</span><span class="sxs-lookup"><span data-stu-id="7657e-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="7657e-110">Reconocimiento Incremental</span><span class="sxs-lookup"><span data-stu-id="7657e-110">Incremental Recognition</span></span>

<span data-ttu-id="7657e-111">El proceso de reconocimiento tarda en completarse y bloquea el acceso a la aplicación mediante el bloqueo del subproceso de la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7657e-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="7657e-112">Por tanto, puede ser costoso y frustrante para el usuario final esperar sincrónicamente los resultados.</span><span class="sxs-lookup"><span data-stu-id="7657e-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="7657e-113">Muchas aplicaciones de Tablet PC requieren el reconocimiento de varias líneas de tinta y un enfoque incremental para reconocer los trazos en un subproceso en segundo plano es la estrategia óptima.</span><span class="sxs-lookup"><span data-stu-id="7657e-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="7657e-114">La ventaja de un enfoque incremental en lugar de una operación masiva es que permite el reconocimiento de los trazos que tienen lugar durante un período de tiempo, redistribuyendo el trabajo en el subproceso en segundo plano en lugar de hacerlo sincrónicamente en el subproceso en primer plano.</span><span class="sxs-lookup"><span data-stu-id="7657e-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="7657e-115">Para admitir el análisis incremental, el objeto [**InkAnalyzer**](inkanalyzer.md) tiene un método [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , que controla la creación y administración de un subproceso en segundo plano para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7657e-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="7657e-116">El **InkAnalyzer** también se encarga automáticamente de administrar lo que se debe reconocer y lo que ya se ha reconocido.</span><span class="sxs-lookup"><span data-stu-id="7657e-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="7657e-117">Por lo tanto, hay dos mecanismos para lograr los resultados del reconocimiento:</span><span class="sxs-lookup"><span data-stu-id="7657e-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="7657e-118">El método [**Analyze**](iinkanalyzer-analyze.md) (análisis sincrónico), que funciona mejor para:</span><span class="sxs-lookup"><span data-stu-id="7657e-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="7657e-119">Pequeñas cantidades de tinta.</span><span class="sxs-lookup"><span data-stu-id="7657e-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="7657e-120">Cuando se requieren resultados antes de continuar con la siguiente operación de la aplicación, como cuando se muestra una interfaz de usuario de corrección.</span><span class="sxs-lookup"><span data-stu-id="7657e-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="7657e-121">El método [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (análisis asincrónico), que funciona mejor para:</span><span class="sxs-lookup"><span data-stu-id="7657e-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="7657e-122">Cualquier cantidad de tinta.</span><span class="sxs-lookup"><span data-stu-id="7657e-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="7657e-123">Cuando se usan con un temporizador que pulso aproximadamente cada 600 milisegundos.</span><span class="sxs-lookup"><span data-stu-id="7657e-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="7657e-124">600 milisegundos es la recomendación actual, pero este tiempo está sujeto a cambios pendientes de pruebas.</span><span class="sxs-lookup"><span data-stu-id="7657e-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="7657e-125">Para usar la operación [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) , el objeto [**InkCollector**](inkcollector-class.md) (u otros objetos o controles similares, como [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)o [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) en Windows Presentation Foundation) administra la recopilación y representación de los trazos de lápiz.</span><span class="sxs-lookup"><span data-stu-id="7657e-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="7657e-126">Si **InkCollector** se empareja con las API de análisis de tinta, las aplicaciones pueden mantener los resultados de reconocimiento actualizados al informar al [**InkAnalyzer**](inkanalyzer.md) sobre cada nuevo trazo que se agrega a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="7657e-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="7657e-127">Esto permite que los **InkAnalyzer** reconozcan los trazos incrementalmente y en un subproceso en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7657e-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="7657e-128">Para realizar el análisis incremental en segundo plano, las aplicaciones deben implementar tres pasos (que se muestran para código administrado):</span><span class="sxs-lookup"><span data-stu-id="7657e-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="7657e-129">Agregue el trazo al [**InkAnalyzer**](inkanalyzer.md) cada vez que se produzca el evento de [**trazo**](inkoverlay-stroke.md) del objeto [**InkOverlay**](inkoverlay-class.md) :</span><span class="sxs-lookup"><span data-stu-id="7657e-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="7657e-130">Invocar las operaciones [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) en un intervalo establecido.</span><span class="sxs-lookup"><span data-stu-id="7657e-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="7657e-131">Nota: las aplicaciones no deben invocar simplemente la operación de análisis en segundo plano después de cada nuevo trazo.</span><span class="sxs-lookup"><span data-stu-id="7657e-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="7657e-132">Esto producirá un error (devuelve un valor **false**) si ya se está ejecutando una operación en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7657e-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="7657e-133">La razón de este comportamiento es limitar el número de subprocesos en segundo plano y las operaciones de conciliación necesarias.</span><span class="sxs-lookup"><span data-stu-id="7657e-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="7657e-134">Escuche el evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (código administrado) o el evento de [**resultados**](-ianalysisevents-results.md) (código de C++) para determinar cuándo ha finalizado el proceso en segundo plano:</span><span class="sxs-lookup"><span data-stu-id="7657e-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="7657e-135">Ahora que el procesamiento de la tinta se realiza en un subproceso en segundo plano, la aplicación tiene la capacidad de aceptar los cambios en la tinta mientras la operación en segundo plano funciona.</span><span class="sxs-lookup"><span data-stu-id="7657e-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="7657e-136">Si usamos un subproceso sincrónico, esto no es posible.</span><span class="sxs-lookup"><span data-stu-id="7657e-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="7657e-137">El trabajo se ejecuta en el subproceso de la interfaz de usuario, con lo que se bloquea la capacidad de realizar cambios.</span><span class="sxs-lookup"><span data-stu-id="7657e-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="7657e-138">Entre los cambios se incluyen agregar más tinta al documento, eliminar la tinta o transformar la ubicación o el aspecto de la tinta existente.</span><span class="sxs-lookup"><span data-stu-id="7657e-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="7657e-139">Los cambios que se producen durante la operación en segundo plano pueden invalidar los resultados de hecho.</span><span class="sxs-lookup"><span data-stu-id="7657e-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="7657e-140">Por ejemplo, al eliminar un trazo de una palabra, cambia el valor de reconocimiento de esa palabra.</span><span class="sxs-lookup"><span data-stu-id="7657e-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="7657e-141">La API de [**InkAnalyzer**](inkanalyzer.md) tiene un proceso de conciliación integrado que determina automáticamente qué partes de la operación en segundo plano dejan de ser válidas como resultado de cambiar la entrada manuscrita durante el análisis.</span><span class="sxs-lookup"><span data-stu-id="7657e-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="7657e-142">El proceso de conciliación automática se logra debido a tres factores:</span><span class="sxs-lookup"><span data-stu-id="7657e-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="7657e-143">La propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="7657e-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="7657e-144">Cada vez que la aplicación agrega (método [**AddStroke**](iinkanalyzer-addstroke.md) ) o quita (método [**RemoveStroke**](iinkanalyzer-removestroke.md) ) un trazo hacia o desde [**InkAnalyzer**](inkanalyzer.md), se captura la ubicación física del trazo y la próxima vez que se invoca una operación de análisis, el **InkAnalyzer** garantiza que se analice el trazo o el área ocupada por ese trazo.</span><span class="sxs-lookup"><span data-stu-id="7657e-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="7657e-145">Cada vez que la aplicación modifica la tinta existente, cambia la ubicación o cambia otros atributos de dibujo de la tinta, se puede Agregar la ubicación del cambio (los límites de la tinta) a la propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) de [**InkAnalyzer**](inkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="7657e-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="7657e-146">Esto garantiza que la próxima vez que la aplicación inicie la operación de análisis, se comprueban los resultados correctos en esas áreas.</span><span class="sxs-lookup"><span data-stu-id="7657e-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="7657e-147">Por lo tanto, la propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) realiza el seguimiento, entre las ejecuciones de análisis, de las áreas del documento y, a su vez, los trazos que deben comprobarse para el análisis y los resultados del reconocimiento de tinta correctos.</span><span class="sxs-lookup"><span data-stu-id="7657e-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="7657e-148">Análisis limitado.</span><span class="sxs-lookup"><span data-stu-id="7657e-148">Limited analysis.</span></span>

    -   <span data-ttu-id="7657e-149">Cada vez que la aplicación invoca la operación de análisis, la propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica qué trazos deben analizarse.</span><span class="sxs-lookup"><span data-stu-id="7657e-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="7657e-150">Esto permite a la operación de análisis limitar la operación solo a las regiones desfasadas y omitir todas las demás regiones, optimizando la cantidad de tiempo empleado en volver a analizar la entrada manuscrita.</span><span class="sxs-lookup"><span data-stu-id="7657e-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="7657e-151">El [**InkAnalyzer**](inkanalyzer.md) no pasa por alto todas las demás regiones de la página, sino que puede examinar las áreas vecinas para determinar si los cambios realizados en la región desfasada afectan a esas regiones vecinas.</span><span class="sxs-lookup"><span data-stu-id="7657e-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="7657e-152">Por ejemplo, el analizador clasifica "es", en el siguiente ejemplo de entrada de lápiz, como un único tipo **InkWord** de la clase [**ContextNode**](icontextnode.md) :</span><span class="sxs-lookup"><span data-stu-id="7657e-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

![escritura a mano "es"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="7657e-154">La eliminación de la "s" da como resultado una región desfasada (marcada con un cuadro rojo).</span><span class="sxs-lookup"><span data-stu-id="7657e-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

!["i" manuscrita](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="7657e-156">Después del análisis, el analizador cambia la clasificación de "I" a un tipo **InkDrawing** , aunque esté fuera de la región desfasada, ya que sin el trazo "s" auxiliar el analizador de tintas tiene una probabilidad de 50/50 de que la tinta se clasifique como dibujo o como una palabra.</span><span class="sxs-lookup"><span data-stu-id="7657e-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="7657e-157">Estado de almacenamiento en caché interno.</span><span class="sxs-lookup"><span data-stu-id="7657e-157">Internally cached state.</span></span>

    -   <span data-ttu-id="7657e-158">Cuando una aplicación invoca una operación de análisis en segundo plano, [**InkAnalyzer**](inkanalyzer.md) almacena en caché una instantánea de los datos eliminados.</span><span class="sxs-lookup"><span data-stu-id="7657e-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="7657e-159">Al tomar una instantánea, **InkAnalyzer** puede trabajar en el análisis de los datos independientemente de los datos que utiliza la aplicación, o bien usar la instantánea como punto de comparación para determinar qué cambios realizó la aplicación durante el análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7657e-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="7657e-160">El almacenamiento en caché del estado y la comparación de los cambios es mejor que mantener una lista de todos los cambios que se produjeron por una razón principal: el proxy de datos.</span><span class="sxs-lookup"><span data-stu-id="7657e-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="7657e-161">Este es un escenario avanzado que se describe más adelante en este documento, pero implica que la aplicación actualice el [**InkAnalyzer**](inkanalyzer.md) solo con los datos de entrada de lápiz y sin tinta actuales antes de la operación de análisis invocada y antes de procesar los resultados de una operación de análisis.</span><span class="sxs-lookup"><span data-stu-id="7657e-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="7657e-162">Análisis de tinta simple</span><span class="sxs-lookup"><span data-stu-id="7657e-162">Simple Ink Analysis</span></span>

<span data-ttu-id="7657e-163">En los dos escenarios anteriores (reconocimiento simple y reconocimiento incremental) se describe cómo obtener acceso a los valores de reconocimiento, pero no se menciona cómo acceder a los resultados de la clasificación o el análisis de tinta.</span><span class="sxs-lookup"><span data-stu-id="7657e-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="7657e-164">La configuración predeterminada de [**InkAnalyzer**](inkanalyzer.md), ejecuta los algoritmos de análisis de tinta y los algoritmos de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="7657e-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="7657e-165">Esta configuración produce los resultados más precisos, ya que las dos tecnologías funcionan conjuntamente para aumentar la precisión.</span><span class="sxs-lookup"><span data-stu-id="7657e-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="7657e-166">Es decir, los motores de análisis de tinta ayudan a separar el dibujo de la escritura y normalizar la escritura angulada en un plano horizontal, que es el plano de entrada óptimo para los motores de reconocimiento.</span><span class="sxs-lookup"><span data-stu-id="7657e-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="7657e-167">Para tener acceso a los resultados del análisis de tinta, la aplicación usa los métodos [**Analyze**](iinkanalyzer-analyze.md) o [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exactamente como se describe en los dos escenarios de reconocimiento anteriores.</span><span class="sxs-lookup"><span data-stu-id="7657e-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="7657e-168">No hay ningún cambio porque los algoritmos de análisis y reconocimiento de tinta ya se están ejecutando cuando se llama a esos métodos.</span><span class="sxs-lookup"><span data-stu-id="7657e-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="7657e-169">Sin embargo, el acceso a los resultados es más complicado que leer el valor de una cadena.</span><span class="sxs-lookup"><span data-stu-id="7657e-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="7657e-170">Como ejemplo, el ejemplo de código siguiente muestra la agrupación y las ubicaciones de todos los segmentos **InkWord** y los segmentos **InkDrawing** mediante la representación de un rectángulo alrededor del grupo de trazos que componen la clasificación.</span><span class="sxs-lookup"><span data-stu-id="7657e-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="7657e-171">En este ejemplo se usa simplemente el evento **Paint** del formulario para representar rectángulos coloreados alrededor de las palabras o los dibujos.</span><span class="sxs-lookup"><span data-stu-id="7657e-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="7657e-172">El método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) devuelve una colección de objetos que solo existe si se ha ejecutado la operación de análisis y los resultados contienen clasificaciones con el tipo [**ContextNode**](icontextnode.md) especificado.</span><span class="sxs-lookup"><span data-stu-id="7657e-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="7657e-173">Si no existe ningún **ContextNode** del tipo deseado en el documento, se omiten los pasos para dibujar los rectángulos.</span><span class="sxs-lookup"><span data-stu-id="7657e-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="7657e-174">Cada objeto devuelto desde el método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) tendrá propiedades relacionadas con ese tipo de clasificación.</span><span class="sxs-lookup"><span data-stu-id="7657e-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="7657e-175">Por ejemplo, el **InkWordNode** hace referencia a todos los trazos que componen una sola palabra en el documento y hacen referencia a la cadena reconocida para esa palabra.</span><span class="sxs-lookup"><span data-stu-id="7657e-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="7657e-176">El **InkDrawingNode** hace referencia a todos los trazos que componen el dibujo único en el documento y hacen referencia al nombre de la forma para ese dibujo.</span><span class="sxs-lookup"><span data-stu-id="7657e-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="7657e-177">El método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) es muy similar al método [**DivisionResult:: ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) que devuelve colecciones de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de tipos de escritura o de dibujo.</span><span class="sxs-lookup"><span data-stu-id="7657e-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="7657e-178">Para colocar el ejemplo de código anterior en perspectiva, considere el siguiente ejemplo de entrada de lápiz:</span><span class="sxs-lookup"><span data-stu-id="7657e-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![ejemplo de entrada de lápiz "Esto es algo de tinta".](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="7657e-181">Si llama al método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) y pasa el campo estático para **InkWord**, el analizador devuelve una colección de cuatro objetos **InkWordNode** :</span><span class="sxs-lookup"><span data-stu-id="7657e-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![salida del analizador, "esta es una tinta"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="7657e-183">Si llama al método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) y pasa el campo estático para **InkDrawing**, el analizador devuelve una colección de un objeto **InkDrawingNode** :</span><span class="sxs-lookup"><span data-stu-id="7657e-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![imagen que muestra "oval", el resultado del analizador de inkdrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="7657e-185">Una vez que se ha desencadenado el evento **Paint** , el código de ejemplo representa rectángulos alrededor de cada uno de los objetos:</span><span class="sxs-lookup"><span data-stu-id="7657e-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![dibujo original con rectángulos representados alrededor del objeto y palabras](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="7657e-187">Este ejemplo solo se toca en el método [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) , pero dado que los motores de análisis de tinta pueden detectar un conjunto más completo de tipos de entrada de lápiz, el método también se corresponde con todos los tipos de nodos detectados por los motores de análisis de tinta (como líneas, párrafos y otras estructuras).</span><span class="sxs-lookup"><span data-stu-id="7657e-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="7657e-188">Usar el análisis de tinta con borrado de punto</span><span class="sxs-lookup"><span data-stu-id="7657e-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="7657e-189">La aplicación debe realizar ajustes en la forma en que actualiza los trazos al realizar el borrado de puntos para garantizar un buen rendimiento.</span><span class="sxs-lookup"><span data-stu-id="7657e-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="7657e-190">En primer lugar, en el nivel de aplicación, reemplace el punto de lápiz del trazo existente por el punto de lápiz del nuevo trazo y, a continuación, llame a [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) en ese trazo y actualice la región desfasada con los límites del trazo.</span><span class="sxs-lookup"><span data-stu-id="7657e-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="7657e-191">Esto hará que [**InkAnalyzer**](inkanalyzer.md) recupere los datos de trazo actualizados cuando se inicie la siguiente ronda de análisis en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="7657e-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="7657e-192">Esta técnica se muestra en el ejemplo siguiente.</span><span class="sxs-lookup"><span data-stu-id="7657e-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="7657e-193">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7657e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7657e-194">Información general de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7657e-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="7657e-195">Uso de la API de análisis de tinta</span><span class="sxs-lookup"><span data-stu-id="7657e-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
