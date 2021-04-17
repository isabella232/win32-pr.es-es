---
description: El objeto RealTimeStylus está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de Tablet PC.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Complementos y la clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08177c5f4110897fa1887857788766f67ae38167
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697754"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Complementos y la clase RealTimeStylus

El objeto [**RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de Tablet PC. Los complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , se pueden agregar a un objeto **RealTimeStylus** . Los complementos sincrónicos se suelen llamar directamente mediante el objeto **RealTimeStylus** en un subproceso de prioridad alta, mientras que los complementos asincrónicos se suelen llamar en el subproceso de la interfaz de usuario (IU) de la aplicación. Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que se despidan computacionalmente, como el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieran acceso en tiempo real al flujo de datos, como la colección de entradas de lápiz.

Es posible que algunas tareas estén exigiendo cálculo, pero que requieran acceso en tiempo real al flujo de datos, como el reconocimiento de gestos de varios trazos. Para satisfacer estas necesidades, las API de StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que le permite usar dos objetos **RealTimeStylus** , cada uno de los cuales se ejecuta en su propio subproceso. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).

Las interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) y [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definen los mismos métodos. Estos métodos permiten al objeto [**RealTimeStylus**](realtimestylus-class.md) pasar los datos de lápiz a cada complemento, independientemente de si se trata de un complemento asincrónico o sincrónico. Las propiedades [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms824752(v=msdn.10)) y [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms824769(v=msdn.10)) permiten que cada complemento se suscriba a datos específicos en el flujo de datos del lápiz de Tablet PC. Un complemento solo debe suscribirse a los datos necesarios para realizar su tarea, lo que minimiza las demandas de rendimiento. Para obtener más información sobre los subprocesos y la clase **RealTimeStylus** , consulte [consideraciones de subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).

El objeto [**RealTimeStylus**](realtimestylus-class.md) usa objetos en el espacio de nombres [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para pasar los datos de lápiz a sus complementos. **RealTimeStylus** también detecta las excepciones producidas por los complementos. Cuando **RealTimeStylus** detecta excepciones, notifica a los complementos llamando al método [IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) . Para obtener más información sobre el uso de datos de complementos, vea [los datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) . Para obtener más información sobre el control de errores, vea [consideraciones sobre el control de errores para las API de StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) y la sección de datos de error de los datos de complemento y la clase RealTimeStylus.

> [!Note]  
> Se debe adjuntar al menos un complemento al objeto [**RealTimeStylus**](realtimestylus-class.md) antes de que se pueda habilitar el objeto **RealTimeStylus** .

 

En los temas siguientes se describen algunas categorías comunes de complementos.

-   [Complementos de recopilación de tintas](ink-collection-plug-ins.md)
-   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
-   [Complementos de reconocedor](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Consideraciones especiales

Debido a la naturaleza compleja del objeto [**RealTimeStylus**](realtimestylus-class.md) , debe tener en cuenta lo siguiente.

El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento modifica la colección de complementos a la que está adjuntada. Esto solo ocurre cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama como miembro de esa colección.

El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produzca una excepción.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.Dispose();
    }
    
    // ...
}
```



El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento llama al método [Dispose](/previous-versions/ms825891(v=msdn.10)) del objeto **RealTimeStylus** . Esto solo ocurre cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama.

El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produzca una excepción.


```csharp
using Microsoft.Ink;
using Microsoft.StylusInput;
using Microsoft.StylusInput.PluginData;

// ...
public class thePlugin : Microsoft.StylusInput.IStylusAsyncPlugin
{
    Microsoft.StylusInput.GestureRecognizer theGestureRecognizer;

    // ...

    // Called when a system gesture occurs.
    public void SystemGesture(RealTimeStylus sender, SystemGestureData data)
    {
        // The following line will cause the realtime stylus that calls this method
        // to throw an exception.
        sender.AsyncPluginCollection.Add(this.theGestureRecognizer);
    }
    
    // ...
}
```



Las colecciones de complementos se pueden modificar mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; sin embargo, esto puede dificultar el comportamiento de la aplicación. Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del complemento. Cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del complemento. Esto permite que el complemento mantenga su estado adecuado sin tener que comprobar la propiedad [Enabled](/previous-versions/ms824832(v=msdn.10)) del objeto **RealTimeStylus** .

Cuando se agrega un complemento mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, es posible que los datos del complemento que recibe el complemento no contengan suficiente información para establecer adecuadamente el contexto de los datos iniciales. Por ejemplo, el complemento que se acaba de agregar podría empezar a recibir datos de paquetes de un lápiz que es un trazo medio. Del mismo modo, cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, los datos del complemento que ha recibido el complemento pueden ser insuficientes para finalizar el procesamiento de los datos.

> [!Note]  
> Para la estabilidad general, restablezca el estado interno de un complemento cuando se llame a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Consideraciones sobre el control de errores para las API de StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Consideraciones sobre los subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
