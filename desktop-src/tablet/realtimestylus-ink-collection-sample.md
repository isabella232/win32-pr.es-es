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
# <a name="realtimestylus-ink-collection-sample"></a>Ejemplo de colección de tintas RealTimeStylus

Esta aplicación muestra la representación y recopilación de entradas manuscritas cuando se usa la clase [**RealTimeStylus**](realtimestylus-class.md) .

## <a name="the-inkcollection-project"></a>El proyecto InkCollection

Este ejemplo consta de una única solución que contiene un proyecto, InkCollection. La aplicación define el `InkCollection` espacio de nombres que contiene una sola clase, también denominada `InkCollection` . La clase hereda de la clase [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa la interfaz [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) .


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



La clase InkCollection define un conjunto de constantes privadas que se usan para especificar varios grosores de la tinta. La clase también declara instancias privadas de la clase [**RealTimeStylus**](realtimestylus-class.md) , `myRealTimeStylus` , la clase [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) , `myDynamicRenderer` y la clase de [representador](/previous-versions/ms828481(v=msdn.10)) `myRenderer` . **DynamicRenderer** representa el [trazo](/previous-versions/ms552692(v=vs.100)) que se está recopilando actualmente. El objeto representador, `myRenderer` , representa los objetos Stroke que ya se han recopilado.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



La clase también declara un objeto [Hashtable](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , `myPackets` , que se utiliza para almacenar los datos de paquetes que se están recopilando mediante uno o varios objetos [cursor](/previous-versions/ms552104(v=vs.100)) . Los valores de [identificador](/previous-versions/ms824826(v=msdn.10)) del objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) se usan como la clave de tabla hash para identificar de forma exclusiva los datos de paquete recopilados para un objeto de cursor determinado.

Una instancia privada del objeto de [entrada de lápiz](/previous-versions/aa515768(v=msdn.10)) , `myInk` , almacena los objetos de [trazo](/previous-versions/ms552692(v=vs.100)) recopilados por `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>El evento de carga de formulario

En el controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, `myDynamicRenderer` se crea una instancia de con el [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) que toma un control como argumento y `myRenderer` se construye con un constructor sin argumentos.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Preste atención al comentario que sigue a la creación de instancias de los representadores, ya que `myDynamicRenderer` usa los valores predeterminados de [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) al representar la tinta. Este es el comportamiento estándar. Sin embargo, si desea proporcionar a la entrada de lápiz `myDynamicRenderer` una apariencia diferente a la de la entrada de lápiz representada por `myRenderer` , puede cambiar la propiedad [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) en `myDynamicRenderer` . Para ello, quite la marca de comentario de las líneas siguientes antes de compilar y ejecutar la aplicación.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



A continuación, la aplicación crea el objeto [**RealTimeStylus**](realtimestylus-class.md) que se usa para recibir notificaciones del lápiz y agrega el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a la cola de notificaciones de complementos sincrónicos. Concretamente `myRealTimeStylus` , `myDynamicRenderer` se agrega a la propiedad [SyncPluginCollection](/previous-versions/ms824833(v=msdn.10)) .


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



A continuación, se agrega el formulario a la cola de notificaciones de complementos asincrónica. En concreto, `InkCollection` se agrega a la propiedad [AsyncPluginCollection](/previous-versions/ms824831(v=msdn.10)) . Por último, `myRealTimeStylus` y `myDynamicRenderer` están habilitados, y se crean instancias de los paquetes y myInk.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Además de enlazar los controladores de menú para cambiar el color y el tamaño de la tinta, se requiere un bloque más breve de código antes de implementar la interfaz. El ejemplo debe controlar el evento [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) del formulario. En el controlador de eventos, la aplicación debe actualizarse `myDynamicRenderer` porque es posible que se esté recopilando un objeto [Stroke](/previous-versions/ms552692(v=vs.100)) en el momento en que se produce el evento Paint. En ese caso, es necesario volver a dibujar la parte del objeto de trazo que ya se ha recopilado. El [representador](/previous-versions/ms828481(v=msdn.10)) estático se usa para volver a dibujar los objetos de trazo que ya se han recopilado. Estos trazos están en el objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) porque se colocan allí cuando se dibujan, tal como se muestra en la sección siguiente.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implementar la interfaz IStylusAsyncPlugin

La aplicación de ejemplo define los tipos de notificaciones que tiene interés en recibir en la implementación de la propiedad de [interés](/previous-versions/ms824769(v=msdn.10)) . Por lo tanto, la propiedad de tipo de interés define las notificaciones que el objeto [**RealTimeStylus**](realtimestylus-class.md) reenvía al formulario. En este ejemplo, la propiedad Interest define el interés en **StylusDown**, **packets**, **StylusUp** y las notificaciones de **error** a través de la enumeración [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) .


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



La notificación [StylusDown](/previous-versions/ms824779(v=msdn.10)) se produce cuando el lápiz toca la superficie del digitalizador. Cuando esto sucede, el ejemplo asigna una matriz que se usa para almacenar los datos de paquete para el objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) . El [StylusDownData](/previous-versions/ms824107(v=msdn.10)) del método StylusDown se agrega a la matriz y la matriz se inserta en la tabla hash utilizando la propiedad [ID](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como una clave.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



La notificación de [paquetes](/previous-versions/ms824773(v=msdn.10)) se produce cuando el lápiz se mueve en la superficie del digitalizador. Cuando esto ocurre, la aplicación agrega New [StylusDownData](/previous-versions/ms824107(v=msdn.10)) en la matriz de paquetes para el objeto [Stylus](/previous-versions/ms824824(v=msdn.10)) . Para ello, se usa la propiedad [ID](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como clave para recuperar la matriz de paquetes del lápiz óptico de la tabla hash. A continuación, se insertan los datos del nuevo paquete en la matriz recuperada.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



La notificación [StylusUp](/previous-versions/ms824782(v=msdn.10)) se produce cuando el lápiz sale de la superficie del digitalizador. Cuando se produce esta notificación, el ejemplo recupera la matriz de paquetes para este objeto de [lápiz](/previous-versions/ms824824(v=msdn.10)) de la tabla hash y lo quita de la tabla hash, ya que ya no es necesario, agrega los nuevos datos del paquete y usa la matriz de datos de paquetes para crear un nuevo objeto [Stroke](/previous-versions/ms552692(v=vs.100)) , `stroke` .


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



Para ver un ejemplo en el que se muestra un uso más sólido de la clase [**RealTimeStylus**](realtimestylus-class.md) , incluido el uso de la creación de complementos personalizados, vea [ejemplo de complemento RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. Ink. Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Acceso y manipulación de la entrada del lápiz óptico](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
