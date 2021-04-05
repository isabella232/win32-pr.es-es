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
# <a name="realtimestylus-plug-in-sample"></a>Ejemplo de complemento RealTimeStylus

Esta aplicación muestra cómo trabajar con la clase [**RealTimeStylus**](realtimestylus-class.md) . Para obtener información general detallada sobre las API de StylusInput, incluida la clase **RealTimeStylus** , consulte [acceso y manipulación de entradas del lápiz óptico](accessing-and-manipulating-stylus-input.md). Para obtener información sobre los complementos sincrónicos y asincrónicos, vea [Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md).

## <a name="overview-of-the-sample"></a>Información general sobre el ejemplo

Los complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) se pueden agregar a un objeto [**RealTimeStylus**](realtimestylus-class.md) . Esta aplicación de ejemplo utiliza varios tipos de complementos:

-   Complemento de filtros de paquetes: modifica paquetes. En el complemento de filtro de paquetes de este ejemplo se modifica la información de los paquetes mediante la restricción de todos los datos de paquetes (x, y) dentro de un área rectangular.
-   Complemento de representador dinámico personalizado: modifica las cualidades de representación dinámica. El complemento de representación dinámica personalizado en este ejemplo modifica el modo en que se representa la entrada de lápiz dibujando un círculo pequeño alrededor de cada punto (x, y) de un trazo.
-   Complemento de representador dinámico: modifica las cualidades de representación dinámica. En este ejemplo se muestra el uso del objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) como complemento para controlar la representación dinámica de la entrada de lápiz.
-   Complemento de reconocedor de gestos: reconoce los gestos de la aplicación. En este ejemplo se muestra el uso del objeto [**GestureRecognizer**](gesturerecognizer-class.md) como complemento para reconocer los gestos de la aplicación (cuando se ejecuta en un sistema con el reconocedor de gestos de Microsoft presente).

Además, este ejemplo proporciona una interfaz de usuario que permite al usuario agregar, quitar y cambiar el orden de cada complemento de la colección. La solución de ejemplo contiene dos proyectos, RealTimeStylusPluginApp y RealTimeStylusPlugins. RealTimeStylusPluginApp contiene la interfaz de usuario para el ejemplo. RealTimeStylusPlugins contiene las implementaciones de los complementos. El proyecto RealTimeStylusPlugins define el espacio de nombres RealTimeStylusPlugins, que contiene el filtro de paquetes y los complementos personalizados de representadores dinámicos. El proyecto RealTimeStylusPluginApp hace referencia a este espacio de nombres. El proyecto RealTimeStylusPlugins usa los espacios de nombres [Microsoft. Ink](/previous-versions/ms826516(v=msdn.10)), [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10))y [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) .

Para obtener información general sobre los espacios de nombres [Microsoft. StylusInput](/previous-versions/ms824750(v=msdn.10)) y [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) , consulte [arquitectura de las API de StylusInput](architecture-of-the-stylusinput-apis.md).

## <a name="packet-filter-plug-in"></a>Complemento de filtro de paquetes

El complemento de filtro de paquetes es un complemento sincrónico que muestra la modificación de paquetes. Específicamente, define un rectángulo en el formulario. Los paquetes que se dibujen fuera de la región se representan dentro de la región. La clase de complemento, `PacketFilterPlugin` , se registra para recibir notificaciones `StylusDown` de `StylusUp` eventos de `Packets` entrada de lápiz, y. La clase implementa los métodos [StylusDown](/previous-versions/ms824761(v=msdn.10)), [StylusUp](/previous-versions/ms824764(v=msdn.10))y los [paquetes](/previous-versions/ms824756(v=msdn.10)) definidos en la clase [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) .

El constructor público para `PacketFilterPlugin` requiere una estructura de [rectángulo](/dotnet/api/system.drawing.rectangle?view=netcore-3.1) . Este rectángulo define el área rectangular, en coordenadas de espacio de tinta (. 01mm = 1 HIMETRIC unidad), en la que se incluirán los paquetes. El rectángulo se mantiene en un campo privado, `rectangle` .


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



La `PacketFilterPlugin` clase se registra para las notificaciones de eventos mediante la implementación del descriptor de acceso get para la propiedad de tipo de [interés](/previous-versions/ms824752(v=msdn.10)) . En este caso, el complemento ha interesado en responder a las `StylusDown` `Packets` notificaciones,, `StylusUp` y `Error` . El ejemplo devuelve estos valores tal como se define en la enumeración [DataInterestMask](/previous-versions/ms824787(v=msdn.10)) . Se llama al método [StylusDown](/previous-versions/ms824761(v=msdn.10)) cuando la punta del lápiz se pone en contacto con la superficie del digitalizador. Se llama al método [StylusUp](/previous-versions/ms824764(v=msdn.10)) cuando la punta del lápiz sale de la superficie del digitalizador. Se llama al método de [paquetes](/previous-versions/ms824756(v=msdn.10)) cuando el objeto [**RealTimeStylus**](realtimestylus-class.md) recibe paquetes. Se llama al método [error](/previous-versions/ms585069(v=vs.100)) cuando el complemento actual o un complemento anterior produce una excepción.


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



La `PacketFilterPlugin` clase controla la mayoría de estas notificaciones en un método auxiliar, `ModifyPacketData` . El `ModifyPacketData` método obtiene los valores x e y de cada nuevo paquete de la clase [PacketsData](/previous-versions/ms824590(v=msdn.10)) . Si alguno de los valores está fuera del rectángulo, el método reemplaza el valor por el punto más cercano que todavía está dentro del rectángulo. Este es un ejemplo de cómo un complemento puede reemplazar los datos de paquetes a medida que se reciben desde el flujo de entrada manuscrita.


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



## <a name="custom-dynamic-renderer-plug-in"></a>Complemento de representador dinámico personalizado

La `CustomDynamicRenderer` clase también implementa la clase [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) para recibir notificaciones de entrada de lápiz. Después, controla la `Packets` notificación para dibujar un círculo pequeño alrededor de cada nuevo punto de paquete.

La clase contiene una variable de [gráficos](/dotnet/api/system.drawing.graphics?view=dotnet-plat-ext-3.1&preserve-view=true) que contiene una referencia al objeto Graphics pasado al constructor de clase. Es el objeto Graphics que se usa para la representación dinámica.


```C++
private Graphics myGraphics;

public CustomDynamicRendererPlugin(Graphics g)
{
    myGraphics = g;
}
        //...
            
```



Cuando el complemento de representador dinámico personalizado recibe una notificación de paquetes, extrae los datos (x, y) y dibuja un círculo verde pequeño alrededor del punto. Este es un ejemplo de representación personalizada basada en el flujo de entrada manuscrita.


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



## <a name="the-realtimestyluspluginapp-project"></a>El proyecto RealTimeStylusPluginApp

En el proyecto RealTimeStylusPluginApp se muestran los complementos descritos anteriormente, así como los complementos [**GestureRecognizer**](gesturerecognizer-class.md) y [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) . La interfaz de usuario del proyecto se compone de:

-   Un formulario que contiene un control [GroupBox](/dotnet/api/system.windows.forms.groupbox?view=netcore-3.1) que se usa para definir el área de entrada manuscrita.
-   Control [CheckedListBox](/dotnet/api/system.windows.forms.checkedlistbox?view=netcore-3.1) para enumerar y seleccionar los complementos disponibles.
-   Un par de [objetos de botón](/dotnet/api/system.windows.forms.button?view=netcore-3.1) que permiten volver a ordenar los complementos.

El proyecto define una estructura, `PlugInListItem` , para facilitar la administración de los complementos que se usan en el proyecto. La `PlugInListItem` estructura contiene el complemento y una descripción.

La `RealTimeStylusPluginApp` propia clase implementa la clase [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) . Esto es necesario para que se `RealTimeStylusPluginApp` pueda notificar a la clase cuando el complemento [**GestureRecognizer**](gesturerecognizer-class.md) agrega datos de gestos a la cola de salida. La aplicación se registra para la notificación de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)). Cuando se reciben datos de gestos, `RealTimeStylusPluginApp` coloca una descripción en la barra de estado en la parte inferior del formulario.


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
> En la implementación de [CustomStylusDataAdded](/previous-versions/ms824753(v=msdn.10)) , es interesante que pueda identificar los datos de gestos personalizados en la cola de salida por GUID (mediante el campo [GestureRecognitionDataGuid](/previous-versions/ms826344(v=msdn.10)) ) o por tipo (mediante el resultado de la instrucción as). En el ejemplo se usan ambas técnicas de identificación para fines de demostración. También es válido cualquier enfoque por sí solo.

 

En el controlador de eventos de carga del formulario, la aplicación crea instancias de las `PacketFilter` `CustomDynamicRenderer` clases y y las agrega al cuadro de lista. A continuación, la aplicación intenta crear una instancia de la clase [**GestureRecognizer**](gesturerecognizer-class.md) y, si se realiza correctamente, la agrega al cuadro de lista. Se produce un error si el reconocedor de gestos no está presente en el sistema. A continuación, la aplicación crea una instancia de un objeto [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85)) y lo agrega al cuadro de lista. Por último, la aplicación habilita cada uno de los complementos y el propio objeto [**RealTimeStylus**](realtimestylus-class.md) .

Otro aspecto importante que hay que tener en cuenta sobre el ejemplo es que en los métodos auxiliares, el objeto [**RealTimeStylus**](realtimestylus-class.md) se deshabilita primero antes de que se agreguen o quiten complementos y se vuelvan a habilitar después de completar la adición o la eliminación.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Microsoft. StylusInput. DynamicRenderer](/previous-versions/ms575176(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. GestureRecognizer](/previous-versions/ms826046(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. RealTimeStylus](/previous-versions/ms824830(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. DataInterestMask](/previous-versions/ms575174(v=vs.100))
</dt> <dt>

[Microsoft. StylusInput. IStylusSyncPlugin](/previous-versions/ms824751(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. IStylusAsyncPlugin](/previous-versions/ms824768(v=msdn.10))
</dt> <dt>

[Microsoft. StylusInput. PluginData. PacketsData](/previous-versions/ms575281(v=vs.100))
</dt> <dt>

[Acceso y manipulación de la entrada del lápiz óptico](accessing-and-manipulating-stylus-input.md)
</dt> <dt>

[Complementos y la clase RealTimeStylus](plug-ins-and-the-realtimestylus-class.md)
</dt> <dt>

[Ejemplo de colección de tintas RealTimeStylus](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 
