---
description: Esta aplicación muestra la colección de entrada de lápiz y la representación cuando se usa la clase RealTimeStylus.
ms.assetid: f8bce153-cc5d-4087-896f-3f60afc80bc8
title: Ejemplo de colección de lápiz De RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11065a40118c83be2451f9b2ac2431e5d7edb6cf31808030861d9f059774bf78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119708398"
---
# <a name="realtimestylus-ink-collection-sample"></a>Ejemplo de colección de lápiz De RealTimeStylus

Esta aplicación muestra la colección de entrada de lápiz y la representación cuando se usa la [**clase RealTimeStylus.**](realtimestylus-class.md)

## <a name="the-inkcollection-project"></a>El archivo InkCollection Project

Este ejemplo consta de una única solución que contiene un proyecto, InkCollection. La aplicación define el espacio `InkCollection` de nombres que contiene una sola clase, también denominada `InkCollection` . La clase hereda de la [clase Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) e implementa la [**interfaz IStylusAsyncPlugin.**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin)


```C++
namespace InkCollection
{
    public class InkCollection : Form, IStylusAsyncPlugin
    {
        //...
      
```



La clase InkCollection define un conjunto de constantes privadas que se usan para especificar varios grosores de lápiz. La clase también declara instancias privadas de la clase [**RealTimeStylus,**](realtimestylus-class.md) , la `myRealTimeStylus` [**clase DynamicRenderer,**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) `myDynamicRenderer` y la clase [Renderer](/previous-versions/ms828481(v=msdn.10)) `myRenderer` . DynamicRenderer **representa** el trazo [que](/previous-versions/ms552692(v=vs.100)) se está recopilando actualmente. El objeto Representador, `myRenderer` , representa objetos Stroke que ya se han recopilado.


```C++
private const float ThinInkWidth = 10;
private const float MediumInkWidth = 100;
private const float ThickInkWidth = 200;

private RealTimeStylus myRealTimeStylus;

private DynamicRenderer myDynamicRenderer;
private Renderer myRenderer;
```



La clase también declara un [objeto Hashtable,](/previous-versions/windows/embedded/hh435144(v=msdn.10)) , que se usa para almacenar datos de paquetes recopilados por `myPackets` uno o varios objetos [Cursor.](/previous-versions/ms552104(v=vs.100)) Los [valores id](/previous-versions/ms824824(v=msdn.10)) del objeto [Stylus](/previous-versions/ms824826(v=msdn.10)) se usan como clave de tabla hash para identificar de forma única los datos de paquete recopilados para un objeto Cursor determinado.

Una instancia privada del objeto [Ink,](/previous-versions/aa515768(v=msdn.10)) `myInk` , almacena los objetos [Stroke](/previous-versions/ms552692(v=vs.100)) recopilados por `myRealTimeStylus` .


```C++
private Hashtable myPackets;
        
private Ink myInk;
```



## <a name="the-form-load-event"></a>Evento de carga de formulario

En el controlador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) del formulario, se crea una instancia de mediante dynamicrenderer que toma un control como argumento y se construye con un `myDynamicRenderer` constructor sin [](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) `myRenderer` argumento.


```C++
private void InkCollection_Load(object sender, System.EventArgs e)
{
    myDynamicRenderer = new DynamicRenderer(this);
    myRenderer = new Renderer();
    // ...
```



Preste atención al comentario que sigue a la creación de instancias de los representadores, ya que usa los valores predeterminados para `myDynamicRenderer` [DrawingAttributes](/previous-versions/ms837931(v=msdn.10)) al representar la entrada de lápiz. Este es el comportamiento estándar. Sin embargo, si desea proporcionar la entrada de lápiz que representa un aspecto diferente de la entrada de lápiz que representa , puede cambiar la propiedad `myDynamicRenderer` `myRenderer` [DrawingAttributes](/previous-versions/ms826347(v=msdn.10)) en `myDynamicRenderer` . Para ello, descomprima las siguientes líneas antes de compilar y ejecutar la aplicación.


```C++
    // myDynamicRenderer.DrawingAttributes.PenTip = PenTip.Rectangle;
    // myDynamicRenderer.DrawingAttributes.Height = (.5F)*MediumInkWidth;
    // myDynamicRenderer.DrawingAttributes.Transparency = 128;
```



A continuación, la aplicación crea el objeto [**RealTimeStylus**](realtimestylus-class.md) que se usa para recibir notificaciones de lápiz óptico y agrega el objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) a la cola de notificaciones del complemento sincrónico. En concreto, `myRealTimeStylus` agrega a la propiedad `myDynamicRenderer` [SyncPluginCollection.](/previous-versions/ms824833(v=msdn.10))


```C++
    myRealTimeStylus = new RealTimeStylus(this, true);

    myRealTimeStylus.SyncPluginCollection.Add(myDynamicRenderer);
```



A continuación, el formulario se agrega a la cola de notificaciones asincrónicas del complemento. En concreto, `InkCollection` se agrega a la propiedad [AsyncPluginCollection.](/previous-versions/ms824831(v=msdn.10)) Por último, `myRealTimeStylus` y `myDynamicRenderer` están habilitados, y se crea una instancia de myPackets y myInk.


```C++
    myRealTimeStylus.AsyncPluginCollection.Add(this);

    myRealTimeStylus.Enabled = true;
    myDynamicRenderer.Enabled = true;  
      
    myPackets = new Hashtable();
    myInk = new Ink();
}
```



Además de enlazar los controladores de menú para cambiar el color y el tamaño de la entrada de lápiz, se necesita un bloque de código más breve antes de implementar la interfaz . El ejemplo debe controlar el evento de [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) formulario. En el controlador de eventos, la aplicación debe actualizarse porque es posible que se repile un objeto Stroke en el momento en `myDynamicRenderer` que se Paint evento. [](/previous-versions/ms552692(v=vs.100)) En ese caso, es necesario volver a dibujar la parte del objeto Stroke que ya se ha recopilado. El [representador estático se](/previous-versions/ms828481(v=msdn.10)) usa para volver a dibujar objetos Stroke que ya se han recopilado. Estos trazos están en el [objeto Ink](/previous-versions/aa515768(v=msdn.10)) porque se colocan allí cuando se dibujan, como se muestra en la sección siguiente.


```C++
private void InkCollection_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
{
    myDynamicRenderer.Refresh();

    myRenderer.Draw(e.Graphics, myInk.Strokes);
} 
```



## <a name="implementing-the-istylusasyncplugin-interface"></a>Implementación de la interfaz IStylusAsyncPlugin

La aplicación de ejemplo define los tipos de notificaciones que tiene interés en recibir en la implementación de la [propiedad DataInterest.](/previous-versions/ms824769(v=msdn.10)) Por lo tanto, la propiedad DataInterest define qué notificaciones reenvía el objeto [**RealTimeStylus**](realtimestylus-class.md) al formulario. Para este ejemplo, la propiedad DataInterest define el interés en las notificaciones **StylusDown**, **Packets**, **StylusUp** y **Error** a través de la [enumeración DataInterestMask.](/previous-versions/ms824787(v=msdn.10))


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



La [notificación StylusDown](/previous-versions/ms824779(v=msdn.10)) se produce cuando el lápiz toca la superficie del digitalizador. Cuando esto sucede, el ejemplo asigna una matriz que se usa para almacenar los datos de paquetes para el [objeto Stylus.](/previous-versions/ms824824(v=msdn.10)) [StylusDownData](/previous-versions/ms824107(v=msdn.10)) del método StylusDown se agrega a la matriz y la matriz se inserta en la tabla hash mediante la propiedad [Id](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como clave.


```C++
public void StylusDown(RealTimeStylus sender, StylusDownData data)
{
    ArrayList collectedPackets = new ArrayList();

    collectedPackets.AddRange(data.GetData());

    myPackets.Add(data.Stylus.Id, collectedPackets);
}
```



La [notificación Paquetes](/previous-versions/ms824773(v=msdn.10)) se produce cuando el lápiz se mueve en la superficie del digitalizador. Cuando esto sucede, la aplicación agrega [el nuevo StylusDownData](/previous-versions/ms824107(v=msdn.10)) a la matriz de paquetes para el [objeto Stylus.](/previous-versions/ms824824(v=msdn.10)) Para ello, usa la propiedad [Id](/previous-versions/ms824826(v=msdn.10)) del objeto Stylus como clave para recuperar la matriz de paquetes para el lápiz óptico de la tabla hash. A continuación, los nuevos datos de paquete se insertan en la matriz recuperada.


```C++
public void Packets(RealTimeStylus sender, PacketsData data)
{
    ((ArrayList)(myPackets[data.Stylus.Id])).AddRange(data.GetData());
}
```



La [notificación StylusUp](/previous-versions/ms824782(v=msdn.10)) se produce cuando el lápiz sale de la superficie del digitalizador. Cuando se produce esta notificación, el ejemplo recupera la matriz de paquetes para este objeto [Stylus](/previous-versions/ms824824(v=msdn.10)) de la tabla hash que lo quita de la tabla hash, ya que ya no es necesario, agrega los nuevos datos de paquetes y usa la matriz de datos de paquetes para crear un nuevo objeto [Stroke,](/previous-versions/ms552692(v=vs.100)) `stroke` .


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



Para obtener un ejemplo que muestra un uso más sólido de la clase [**RealTimeStylus,**](realtimestylus-class.md) incluido el uso de la creación de complementos personalizados, vea Ejemplo de complemento [RealTimeStylus](realtimestylus-plug-in-sample.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft.Ink.Renderer](/previous-versions/ms552630(v=vs.100))
</dt> <dt>

[Microsoft.StylusInput.DynamicRenderer](/previous-versions/ms826345(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft.StylusInput.IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Acceso y manipulación de la entrada de lápiz óptico](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
