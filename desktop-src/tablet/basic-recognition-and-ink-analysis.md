---
description: En este tema se presentan las API de análisis de lápiz.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Reconocimiento básico y análisis de entrada de lápiz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4bdfa0d93c25e397caf0f116f0f47b303e9571d342825673572011534404de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111335"
---
# <a name="basic-recognition-and-ink-analysis"></a>Reconocimiento básico y análisis de entrada de lápiz

En este tema se presentan las API de análisis de lápiz.

## <a name="simple-recognition"></a>Reconocimiento simple

La funcionalidad básica expuesta por la API de análisis de entrada de lápiz es el acceso a los resultados de reconocimiento de un fragmento de lápiz determinado. Esto es sencillo y sencillo de hacer, como se muestra en el código de ejemplo siguiente.


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



Los resultados de la operación de reconocimiento son simplemente un valor de cadena que representa el valor reconocido de la entrada manuscrita. La API de análisis de entrada de lápiz expone una funcionalidad de reconocimiento mucho mayor que la cadena reconocida, pero esa es la operación más común.

## <a name="incremental-recognition"></a>Reconocimiento incremental

El proceso de reconocimiento tarda tiempo en completarse y bloquea el acceso a la aplicación bloqueando el subproceso de interfaz de usuario de la aplicación. Por lo tanto, puede ser costoso y frustrante para el usuario final esperar sincrónicamente los resultados. Muchas aplicaciones de Tablet PC requieren el reconocimiento de más de unas pocas líneas de lápiz, y un enfoque incremental para reconocer trazos en un subproceso de fondo es la estrategia óptima. La ventaja de un enfoque incremental en lugar de una operación masiva es que permite que el reconocimiento de los trazos se haga durante un período de tiempo, repartiendo el trabajo en el subproceso en segundo plano en lugar de de forma sincrónica en el subproceso en primer plano. Para admitir el análisis incremental, el [**objeto InkAnalyzer**](inkanalyzer.md) tiene un método [**BackgroundAnalyze,**](iinkanalyzer-backgroundanalyze.md) que controla la creación y administración de un subproceso en segundo plano para la aplicación. **InkAnalyzer** también se encarga automáticamente de administrar lo que se debe reconocer y lo que ya se ha reconocido.

Por lo tanto, hay dos mecanismos para lograr resultados de reconocimiento:

-   El [**método Analyze**](iinkanalyzer-analyze.md) (análisis sincrónico), que funciona mejor para:

    -   Pequeñas cantidades de lápiz.
    -   Cuando se requieren resultados antes de continuar con la siguiente operación en la aplicación, como al mostrar una interfaz de usuario de corrección.

-   El [**método BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) (análisis asincrónico), que funciona mejor para:

    -   Cualquier cantidad de lápiz.
    -   Cuando se usa con un temporizador que pulsa aproximadamente cada 600 milisegundos.

> [!Note]  
> 600 milisegundos es la recomendación actual, pero este tiempo está sujeto a cambios a la espera de pruebas adicionales.

 

Para usar la operación [**BackgroundAnalyze,**](iinkanalyzer-backgroundanalyze.md) el objeto [**InkCollector**](inkcollector-class.md) (u objetos o controles similares, como [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)o [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) en Windows Presentation Foundation) administra la colección y la representación de los trazos de lápiz. Si **InkCollector** está emparejado con las API de análisis de entrada de lápiz, las aplicaciones pueden mantener actualizados los resultados del reconocimiento informando a [**InkAnalyzer**](inkanalyzer.md) sobre cada nuevo trazo agregado a la aplicación. Esto permite que **InkAnalyzer** reconozca los trazos de forma incremental y en un subproceso en segundo plano.

Para realizar un análisis incremental en segundo plano, las aplicaciones deben implementar tres pasos (que se muestran para el código administrado):

1. Agregue el trazo a [**InkAnalyzer cada**](inkanalyzer.md) vez que se genera el evento [**Stroke**](inkoverlay-stroke.md) del objeto [**InkOverlay:**](inkoverlay-class.md)


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



2. [**Invoque las operaciones BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) en un intervalo establecido.


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
> Nota Las aplicaciones no deben invocar simplemente la operación de análisis en segundo plano después de cada nuevo trazo. Se producirá un error (devolver un valor **de false**) si ya se está ejecutando una operación en segundo plano. El motivo de este comportamiento es limitar el número de subprocesos en segundo plano y las operaciones de conciliación necesarias.

 

3. Escuche el evento [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) (código administrado) o el evento [**Results**](-ianalysisevents-results.md) (código de C++) para determinar cuándo ha finalizado el proceso en segundo plano:


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



Ahora que el procesamiento de la entrada de lápiz se realiza en un subproceso en segundo plano, la aplicación tiene la capacidad de aceptar cambios en la entrada de lápiz mientras la operación de fondo funciona. Si usamos un subproceso sincrónico, esto no es posible. El trabajo se ejecuta en el subproceso de la interfaz de usuario, lo que bloquea la capacidad de realizar cambios. Los cambios incluyen la adición de más entrada de lápiz al documento, la eliminación de la entrada de lápiz o la transformación de la ubicación o la apariencia de la entrada de lápiz existente. De hecho, los cambios que se producen durante la operación en segundo plano pueden invalidar los resultados. Por ejemplo, al eliminar un trazo de una palabra se cambia el valor de reconocimiento de esa palabra. La API [**InkAnalyzer**](inkanalyzer.md) tiene un proceso de conciliación integrado que determina automáticamente qué partes de la operación en segundo plano no son válidas como resultado del cambio de entrada de lápiz durante el análisis.

El proceso de conciliación automática se realiza debido a tres factores:

1.  La [**propiedad DirtyRegion.**](iinkanalyzer-getdirtyregion.md)

    -   Cada vez que la aplicación agrega [**(método AddStroke)**](iinkanalyzer-addstroke.md) o quita (método [**RemoveStroke)**](iinkanalyzer-removestroke.md) un trazo hacia o desde [**InkAnalyzer,**](inkanalyzer.md)se captura la ubicación física del trazo y la próxima vez que se invoca una operación de análisis, **InkAnalyzer** garantiza que se analice el trazo o el área ocupada por ese trazo.
    -   Cada vez que la aplicación modifica la entrada de lápiz existente, cambia la ubicación o cambia otros atributos de dibujo de la entrada de lápiz, la ubicación del cambio (los límites de la entrada de lápiz) se puede agregar a la propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) de [**InkAnalyzer**](inkanalyzer.md). Esto garantiza que la próxima vez que la aplicación inicie la operación de análisis, esas áreas se comprueban para obtener los resultados correctos.
    -   Por lo tanto, la propiedad [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) realiza un seguimiento, entre ejecuciones de análisis, de las áreas del documento y, a su vez, de qué trazos deben comprobarse para obtener resultados correctos de reconocimiento y análisis de lápiz.

2.  Análisis limitado.

    -   Cada vez que la aplicación invoca la operación de análisis, la [**propiedad DirtyRegion**](iinkanalyzer-getdirtyregion.md) identifica qué trazos se deben analizar. Esto permite que la operación de análisis limite la operación solo a las regiones desusados e ignore todas las demás regiones, lo que optimiza la cantidad de tiempo invertido en volver a analizar la entrada de lápiz.
    -   [**InkAnalyzer**](inkanalyzer.md) no omite completamente todas las demás regiones de la página, sino que puede examinar las áreas adyacentes para determinar si los cambios realizados en la región desusadas afectan a esas regiones vecinos. Por ejemplo, el analizador clasifica "Is", en el ejemplo de lápiz siguiente, como un tipo **InkWord** único de la [**clase ContextNode:**](icontextnode.md)

![manuscrito "is"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

Al eliminar las "s", se produce una región desaprobada (marcada con un cuadro rojo).

!["i" escrito a mano](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

Después del análisis, el analizador cambia la clasificación de "I" a un tipo **InkDrawing,** aunque esté fuera de la región desusada, porque sin el trazo "s" de soporte, el analizador de entrada de lápiz tiene una probabilidad de 50/50 de que la entrada de lápiz se clasifique como un dibujo o una palabra.

-   Estado almacenado internamente en caché.

    -   Cuando una aplicación invoca una operación de análisis en segundo plano, [**InkAnalyzer**](inkanalyzer.md) almacena en caché una instantánea de los datos podados. Al tomar una instantánea, **InkAnalyzer** puede trabajar en el análisis de los datos independientemente de los datos que usa la aplicación, o bien usar la instantánea como punto de comparación para determinar los cambios realizados por la aplicación durante el análisis en segundo plano.
    -   Almacenar en caché el estado y comparar los cambios es mejor que mantener una lista de todos los cambios que se produjeron por un motivo principal: el proxy de datos. Se trata de un escenario avanzado que se describe más adelante en este documento, pero implica que la aplicación actualice [**InkAnalyzer**](inkanalyzer.md) solo con los datos actuales de entrada de lápiz y que no son de entrada de lápiz antes de la operación de análisis invocada y antes de procesar los resultados de una operación de análisis.

## <a name="simple-ink-analysis"></a>Análisis de entrada de lápiz simple

Los dos escenarios anteriores (reconocimiento simple y reconocimiento incremental) describen cómo acceder a los valores de reconocimiento, pero no mencionan cómo acceder a los resultados de clasificación o análisis de entrada de lápiz. La configuración predeterminada de [**InkAnalyzer ejecuta**](inkanalyzer.md)algoritmos de análisis de entrada de lápiz y algoritmos de reconocimiento. Esta configuración produce los resultados más precisos, ya que las dos tecnologías funcionan juntas para aumentar la precisión. Es decir, los motores de análisis de entrada de lápiz ayudan a separar el dibujo de la escritura y normalizar la escritura en ángulo en un plano horizontal, que es el plano de entrada óptimo para los motores de reconocimiento.

Para acceder a los resultados del análisis de entrada de lápiz, la aplicación usa los métodos [**Analyze**](iinkanalyzer-analyze.md) o [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) exactamente como se describe en los dos escenarios de reconocimiento anteriores. Nada cambia porque los algoritmos de reconocimiento y análisis de entrada de lápiz ya se ejecutan cuando se llama a esos métodos. Sin embargo, el acceso a los resultados es más complicado que leer el valor de una cadena. Por ejemplo, el ejemplo de código siguiente muestra la agrupación y las ubicaciones de todos los segmentos **InkWord** y **InkDrawing** mediante la representación de un rectángulo alrededor del grupo de trazos que forma la clasificación.

En este ejemplo simplemente se usa el evento **de** Paint del formulario para representar rectángulos de color alrededor de las palabras o dibujos. El [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) devuelve una colección de objetos que solo existe si se ha ejecutado la operación de análisis y los resultados contienen clasificaciones con el tipo [**ContextNode**](icontextnode.md) especificado. Si no **existe ningún ContextNode** del tipo deseado en el documento, se omiten los pasos para dibujar los rectángulos.

Cada objeto devuelto por [**el método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) tendrá propiedades relacionadas con ese tipo de clasificación. Por ejemplo, **InkWordNode hace** referencia a todos los trazos que forme una sola palabra en el documento y haga referencia a la cadena reconocida para esa palabra. **InkDrawingNode hace** referencia a todos los trazos que forma el dibujo único del documento y hace referencia al nombre de forma de ese dibujo.

El [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) es muy similar al método [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) que devolvió colecciones de [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) de tipos de escritura o dibujo.


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



Para poner el ejemplo de código anterior en perspectiva, considere el siguiente ejemplo de lápiz:

![ink sample "this is some ink". con un círculo debajo de él](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

Si llama al [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) y pasa el campo estático para **InkWord**, el analizador devuelve una colección de cuatro **objetos InkWordNode:**

![salida del analizador, "this is some ink"](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

Si llama al [**método FindNodesOfType**](iinkanalyzer-findnodesoftype.md) y pasa el campo estático para **InkDrawing**, el analizador devuelve una colección de un **objeto InkDrawingNode:**

![imagen que muestra "oval", el resultado del analizador inkdrawing](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

Una vez **Paint** evento, el código de ejemplo representa rectángulos alrededor de cada uno de los objetos:

![dibujo original con rectángulos representados alrededor del objeto y las palabras](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

Este ejemplo solo se centra en el método [**FindNodesOfType,**](iinkanalyzer-findnodesoftype.md) pero dado que los motores de análisis de entrada de lápiz pueden detectar un conjunto más completo de tipos de entrada de lápiz, el método también se corresponde con todos los tipos de nodos detectables por los motores de análisis de entrada de lápiz (como líneas, párrafos y otras estructuras).

## <a name="using-ink-analysis-with-point-erase"></a>Uso del análisis de entrada de lápiz con borrado de punto

La aplicación debe realizar ajustes en la forma en que actualiza los trazos al realizar el borrado de punto para garantizar un buen rendimiento. En primer lugar, en la capa de aplicación, reemplace el punto del lápiz óptico del trazo existente por el punto del lápiz óptico del nuevo trazo, llame a [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) en ese trazo y actualice la región desusada con los límites del trazo. Esto hará que [**InkAnalyzer**](inkanalyzer.md) obtenga los datos del trazo actualizados cuando se inicie la siguiente ronda de análisis en segundo plano. Esta técnica se muestra en el ejemplo siguiente.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre análisis de entrada de lápiz](ink-analysis-overview.md)
</dt> <dt>

[Uso de Ink Analysis API](ink-analysis-api-usage.md)
</dt> </dl>

 

 
