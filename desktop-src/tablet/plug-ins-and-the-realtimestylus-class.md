---
description: El objeto RealTimeStylus está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de tableta.
ms.assetid: 7217e2d5-ca62-4d65-bf22-9511b367c798
title: Complementos y la clase RealTimeStylus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc522eb6f73b384d0c2c1846edb2b20cdcb89d34ef42633b08ca865950c8ce16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119843385"
---
# <a name="plug-ins-and-the-realtimestylus-class"></a>Complementos y la clase RealTimeStylus

El [**objeto RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de tableta. Los complementos, objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) se pueden agregar a un objeto **RealTimeStylus.** Normalmente, el objeto **RealTimeStylus** llama directamente a los complementos sincrónicos en un subproceso de alta prioridad, mientras que los complementos asincrónicos suelen llamarse en el subproceso de la interfaz de usuario (UI) de la aplicación. Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que no sean exigentes desde el punto de conexión, como el filtrado de paquetes. Cree o use complementos asincrónicos para tareas que no requieren acceso en tiempo real al flujo de datos, como la colección de entrada de lápiz.

Algunas tareas pueden ser exigentes desde el punto de vista computacional, pero requieren acceso en tiempo real al flujo de datos, como el reconocimiento de gestos multistroke. Para satisfacer estas necesidades, las API StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que permite usar dos objetos **RealTimeStylus,** cada uno de los que se ejecuta en su propio subproceso. Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).

Las interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) e [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definen los mismos métodos. Estos métodos permiten que el objeto [**RealTimeStylus**](realtimestylus-class.md) pase los datos del lápiz a cada complemento, independientemente de si se trata de un complemento asincrónico o sincrónico. Las [propiedades Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) y [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) permiten a cada complemento suscribirse a datos específicos en el flujo de datos del lápiz de tableta. Un complemento solo debe suscribirse a los datos necesarios para realizar su tarea, lo que minimiza las demandas de rendimiento. Para obtener más información sobre los subprocesos y la **clase RealTimeStylus,** vea Consideraciones sobre subprocesos para [las API StylusInput](threading-considerations-for-the-stylusinput-apis.md).

El [**objeto RealTimeStylus**](realtimestylus-class.md) usa objetos en el espacio de nombres [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) para pasar los datos del lápiz a sus complementos. **RealTimeStylus** también detecta excepciones producidas por complementos. Cuando **RealTimeStylus** detecta excepciones, notifica a los complementos mediante una llamada al método [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin.Error.](/previous-versions/ms824771(v=msdn.10)) Para obtener más información sobre el uso de datos de complemento, vea [Datos de complemento y la clase RealTimeStylus.](plug-in-data-and-the-realtimestylus-class.md) Para obtener más información sobre el control de errores, vea Consideraciones sobre el control de errores para las [API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) y la sección Datos de error de Los datos de complemento y la clase RealTimeStylus.

> [!Note]  
> Se debe adjuntar al menos un complemento al objeto [**RealTimeStylus**](realtimestylus-class.md) para poder habilitar el objeto **RealTimeStylus.**

 

En los temas siguientes se describen algunas categorías comunes de complementos.

-   [Complementos de ink-collection](ink-collection-plug-ins.md)
-   [Complementos de representador dinámico](dynamic-renderer-plug-ins.md)
-   [Complementos de Recognizer](recognizer-plug-ins.md)

## <a name="special-considerations"></a>Consideraciones especiales

Debido a la naturaleza compleja del [**objeto RealTimeStylus,**](realtimestylus-class.md) debe tener en cuenta lo siguiente.

El [**objeto RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento modifica la colección de complementos a la que está asociado. Esto sucede solo cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama como miembro de esa colección.

El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción.


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



El [**objeto RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento llama al método [Dispose](/previous-versions/ms825891(v=msdn.10)) del objeto **RealTimeStylus.** Esto solo ocurre cuando el complemento lo hace mientras lo llama el **objeto RealTimeStylus.**

El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción.


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



Las colecciones de complementos se pueden modificar mientras el [**objeto RealTimeStylus**](realtimestylus-class.md) está habilitado; sin embargo, esto puede dificultar la predicción del comportamiento de la aplicación. Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del complemento. Cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del complemento. Esto permite que el complemento mantenga su estado adecuado sin tener que comprobar la propiedad [Enabled](/previous-versions/ms824832(v=msdn.10)) del **objeto RealTimeStylus.**

Cuando se agrega un complemento mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, es posible que los datos de complemento que recibe el complemento no contengan suficiente información para establecer adecuadamente el contexto de los datos iniciales. Por ejemplo, el complemento recién agregado podría empezar a recibir datos de paquetes de un lápiz que es de trazo medio. De forma similar, cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, los datos del complemento que ha recibido el complemento pueden ser insuficientes para terminar de procesar los datos.

> [!Note]  
> Para una estabilidad general, restablezca el estado interno de un complemento cuando se llame a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled.**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[El modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[Consideraciones sobre el control de errores para las API StylusInput](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[Datos de complementos y clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[Consideraciones sobre subprocesos para las API StylusInput](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
