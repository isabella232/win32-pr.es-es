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
# <a name="plug-ins-and-the-realtimestylus-class"></a><span data-ttu-id="f7f93-103">Complementos y la clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f7f93-103">Plug-ins and the RealTimeStylus Class</span></span>

<span data-ttu-id="f7f93-104">El objeto [**RealTimeStylus**](realtimestylus-class.md) está diseñado para proporcionar acceso en tiempo real al flujo de datos desde el lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f7f93-104">The [**RealTimeStylus**](realtimestylus-class.md) object is designed to provide real-time access to the data stream from the tablet pen.</span></span> <span data-ttu-id="f7f93-105">Los complementos, los objetos que implementan la interfaz [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) o [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) , se pueden agregar a un objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f7f93-105">Plug-ins, objects that implement the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) or [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interface, can be added to a **RealTimeStylus** object.</span></span> <span data-ttu-id="f7f93-106">Los complementos sincrónicos se suelen llamar directamente mediante el objeto **RealTimeStylus** en un subproceso de prioridad alta, mientras que los complementos asincrónicos se suelen llamar en el subproceso de la interfaz de usuario (IU) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7f93-106">Synchronous plug-ins are generally called directly by the **RealTimeStylus** object on a high-priority thread, while asynchronous plug-ins are generally called on the application's user interface (UI) thread.</span></span> <span data-ttu-id="f7f93-107">Cree o use complementos sincrónicos para tareas que requieran acceso en tiempo real al flujo de datos y que se despidan computacionalmente, como el filtrado de paquetes.</span><span class="sxs-lookup"><span data-stu-id="f7f93-107">Create or use synchronous plug-ins for tasks that require real-time access to the data stream and are computationally undemanding, such as packet filtering.</span></span> <span data-ttu-id="f7f93-108">Cree o use complementos asincrónicos para tareas que no requieran acceso en tiempo real al flujo de datos, como la colección de entradas de lápiz.</span><span class="sxs-lookup"><span data-stu-id="f7f93-108">Create or use asynchronous plug-ins for tasks that do not require real-time access to the data stream, such as ink collection.</span></span>

<span data-ttu-id="f7f93-109">Es posible que algunas tareas estén exigiendo cálculo, pero que requieran acceso en tiempo real al flujo de datos, como el reconocimiento de gestos de varios trazos.</span><span class="sxs-lookup"><span data-stu-id="f7f93-109">Certain tasks may be computationally demanding yet require real-time access to the data stream, such as multistroke gesture recognition.</span></span> <span data-ttu-id="f7f93-110">Para satisfacer estas necesidades, las API de StylusInput proporcionan un modelo [**RealTimeStylus**](realtimestylus-class.md) en cascada que le permite usar dos objetos **RealTimeStylus** , cada uno de los cuales se ejecuta en su propio subproceso.</span><span class="sxs-lookup"><span data-stu-id="f7f93-110">To address these needs, the StylusInput APIs provide a cascaded [**RealTimeStylus**](realtimestylus-class.md) model that allows you to use two **RealTimeStylus** objects, each running on its own thread.</span></span> <span data-ttu-id="f7f93-111">Para obtener más información sobre el modelo **RealTimeStylus** en cascada, vea [el modelo RealTimeStylus en cascada](the-cascaded-realtimestylus-model.md).</span><span class="sxs-lookup"><span data-stu-id="f7f93-111">For more information about the cascaded **RealTimeStylus** model, see [The Cascaded RealTimeStylus Model](the-cascaded-realtimestylus-model.md).</span></span>

<span data-ttu-id="f7f93-112">Las interfaces [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) y [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) definen los mismos métodos.</span><span class="sxs-lookup"><span data-stu-id="f7f93-112">Both the [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin) and [**IStylusAsyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylusasyncplugin) interfaces define the same methods.</span></span> <span data-ttu-id="f7f93-113">Estos métodos permiten al objeto [**RealTimeStylus**](realtimestylus-class.md) pasar los datos de lápiz a cada complemento, independientemente de si se trata de un complemento asincrónico o sincrónico.</span><span class="sxs-lookup"><span data-stu-id="f7f93-113">These methods allow the [**RealTimeStylus**](realtimestylus-class.md) object to pass the pen data to each plug-in, regardless of whether it is an asynchronous or synchronous plug-in.</span></span> <span data-ttu-id="f7f93-114">Las propiedades [Microsoft. StylusInput. IStylusSyncPlugin. Interest](/previous-versions/ms824752(v=msdn.10)) y [Microsoft. StylusInput. IStylusAsyncPlugin. Interest](/previous-versions/ms824769(v=msdn.10)) permiten que cada complemento se suscriba a datos específicos en el flujo de datos del lápiz de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="f7f93-114">The [Microsoft.StylusInput.IStylusSyncPlugin.DataInterest](/previous-versions/ms824752(v=msdn.10)) and [Microsoft.StylusInput.IStylusAsyncPlugin.DataInterest](/previous-versions/ms824769(v=msdn.10)) properties allow each plug-in to subscribe to specific data in the tablet pen data stream.</span></span> <span data-ttu-id="f7f93-115">Un complemento solo debe suscribirse a los datos necesarios para realizar su tarea, lo que minimiza las demandas de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f7f93-115">A plug-in should only subscribe to the data necessary to perform its task, minimizing performance demands.</span></span> <span data-ttu-id="f7f93-116">Para obtener más información sobre los subprocesos y la clase **RealTimeStylus** , consulte [consideraciones de subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="f7f93-116">For more information about threading and the **RealTimeStylus** class, see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="f7f93-117">El objeto [**RealTimeStylus**](realtimestylus-class.md) usa objetos en el espacio de nombres [Microsoft. StylusInput. PluginData](/previous-versions/ms823992(v=msdn.10)) para pasar los datos de lápiz a sus complementos. **RealTimeStylus** también detecta las excepciones producidas por los complementos. Cuando **RealTimeStylus** detecta excepciones, notifica a los complementos llamando al método [IStylusSyncPlugin. error](/previous-versions/ms824754(v=msdn.10)) o [IStylusAsyncPlugin. error](/previous-versions/ms824771(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="f7f93-117">The [**RealTimeStylus**](realtimestylus-class.md) object uses objects in the [Microsoft.StylusInput.PluginData](/previous-versions/ms823992(v=msdn.10)) namespace to pass the pen data to its plug-ins. The **RealTimeStylus** also catches exceptions thrown by plug-ins. When the **RealTimeStylus** catches exceptions, it notifies the plug-ins by calling the [IStylusSyncPlugin.Error](/previous-versions/ms824754(v=msdn.10)) or [IStylusAsyncPlugin.Error](/previous-versions/ms824771(v=msdn.10)) method.</span></span> <span data-ttu-id="f7f93-118">Para obtener más información sobre el uso de datos de complementos, vea [los datos de complemento y la clase RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="f7f93-118">For more information about using plug-in data, see [Plug-in Data and the RealTimeStylus](plug-in-data-and-the-realtimestylus-class.md) Class.</span></span> <span data-ttu-id="f7f93-119">Para obtener más información sobre el control de errores, vea [consideraciones sobre el control de errores para las API de StylusInput](error-handling-considerations-for-the-stylusinput-apis.md) y la sección de datos de error de los datos de complemento y la clase RealTimeStylus.</span><span class="sxs-lookup"><span data-stu-id="f7f93-119">For more information about error handling, see [Error Handling Considerations for the StylusInput APIs](error-handling-considerations-for-the-stylusinput-apis.md) and the Error Data section of Plug-in Data and the RealTimeStylus Class.</span></span>

> [!Note]  
> <span data-ttu-id="f7f93-120">Se debe adjuntar al menos un complemento al objeto [**RealTimeStylus**](realtimestylus-class.md) antes de que se pueda habilitar el objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f7f93-120">At least one plug-in must be attached to the [**RealTimeStylus**](realtimestylus-class.md) object before the **RealTimeStylus** object can be enabled.</span></span>

 

<span data-ttu-id="f7f93-121">En los temas siguientes se describen algunas categorías comunes de complementos.</span><span class="sxs-lookup"><span data-stu-id="f7f93-121">The following topics describe some common categories of plug-ins.</span></span>

-   [<span data-ttu-id="f7f93-122">Complementos de recopilación de tintas</span><span class="sxs-lookup"><span data-stu-id="f7f93-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
-   [<span data-ttu-id="f7f93-123">Complementos de representador dinámico</span><span class="sxs-lookup"><span data-stu-id="f7f93-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
-   [<span data-ttu-id="f7f93-124">Complementos de reconocedor</span><span class="sxs-lookup"><span data-stu-id="f7f93-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)

## <a name="special-considerations"></a><span data-ttu-id="f7f93-125">Consideraciones especiales</span><span class="sxs-lookup"><span data-stu-id="f7f93-125">Special Considerations</span></span>

<span data-ttu-id="f7f93-126">Debido a la naturaleza compleja del objeto [**RealTimeStylus**](realtimestylus-class.md) , debe tener en cuenta lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f7f93-126">Because of the complex nature of the [**RealTimeStylus**](realtimestylus-class.md) object, you should take note of the following.</span></span>

<span data-ttu-id="f7f93-127">El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento modifica la colección de complementos a la que está adjuntada.</span><span class="sxs-lookup"><span data-stu-id="f7f93-127">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in modifies the plug-in collection to which it is attached.</span></span> <span data-ttu-id="f7f93-128">Esto solo ocurre cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama como miembro de esa colección.</span><span class="sxs-lookup"><span data-stu-id="f7f93-128">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object as a member of that collection.</span></span>

<span data-ttu-id="f7f93-129">El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produzca una excepción.</span><span class="sxs-lookup"><span data-stu-id="f7f93-129">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="f7f93-130">El objeto [**RealTimeStylus**](realtimestylus-class.md) produce una excepción si un complemento llama al método [Dispose](/previous-versions/ms825891(v=msdn.10)) del objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f7f93-130">The [**RealTimeStylus**](realtimestylus-class.md) object throws an exception if a plug-in calls the **RealTimeStylus** object's [Dispose](/previous-versions/ms825891(v=msdn.10)) method.</span></span> <span data-ttu-id="f7f93-131">Esto solo ocurre cuando el complemento lo hace mientras el objeto **RealTimeStylus** lo llama.</span><span class="sxs-lookup"><span data-stu-id="f7f93-131">This happens only when the plug-in does so while it is being called by the **RealTimeStylus** object.</span></span>

<span data-ttu-id="f7f93-132">El siguiente ejemplo de C \# es código que hace que el objeto [**RealTimeStylus**](realtimestylus-class.md) produzca una excepción.</span><span class="sxs-lookup"><span data-stu-id="f7f93-132">The following C\# example is code that causes the [**RealTimeStylus**](realtimestylus-class.md) object to throw an exception.</span></span>


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



<span data-ttu-id="f7f93-133">Las colecciones de complementos se pueden modificar mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado; sin embargo, esto puede dificultar el comportamiento de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7f93-133">Plug-in collections can be modified while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled; however, this can make the behavior of your application harder to predict.</span></span> <span data-ttu-id="f7f93-134">Cuando se agrega un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) del complemento.</span><span class="sxs-lookup"><span data-stu-id="f7f93-134">When a plug-in is added while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824775(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusEnabled](/previous-versions/ms824758(v=msdn.10)) method.</span></span> <span data-ttu-id="f7f93-135">Cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, el objeto **RealTimeStylus** llama al método [IStylusAsyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) o [IStylusSyncPlugin. RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) del complemento.</span><span class="sxs-lookup"><span data-stu-id="f7f93-135">When a plug-in is removed while the **RealTimeStylus** object is enabled, the **RealTimeStylus** object calls the plug-in's [IStylusAsyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824774(v=msdn.10)) or [IStylusSyncPlugin.RealTimeStylusDisabled](/previous-versions/ms824757(v=msdn.10)) method.</span></span> <span data-ttu-id="f7f93-136">Esto permite que el complemento mantenga su estado adecuado sin tener que comprobar la propiedad [Enabled](/previous-versions/ms824832(v=msdn.10)) del objeto **RealTimeStylus** .</span><span class="sxs-lookup"><span data-stu-id="f7f93-136">This allows the plug-in to maintain its proper state without having to check the [Enabled](/previous-versions/ms824832(v=msdn.10)) property of the **RealTimeStylus** object.</span></span>

<span data-ttu-id="f7f93-137">Cuando se agrega un complemento mientras el objeto [**RealTimeStylus**](realtimestylus-class.md) está habilitado, es posible que los datos del complemento que recibe el complemento no contengan suficiente información para establecer adecuadamente el contexto de los datos iniciales.</span><span class="sxs-lookup"><span data-stu-id="f7f93-137">When a plug-in is added while the [**RealTimeStylus**](realtimestylus-class.md) object is enabled, the plug-in data that the plug-in receives may not contain enough information to adequately establish the context of the initial data.</span></span> <span data-ttu-id="f7f93-138">Por ejemplo, el complemento que se acaba de agregar podría empezar a recibir datos de paquetes de un lápiz que es un trazo medio.</span><span class="sxs-lookup"><span data-stu-id="f7f93-138">For example, the newly added plug-in could start receiving packet data from a pen that is mid-stroke.</span></span> <span data-ttu-id="f7f93-139">Del mismo modo, cuando se quita un complemento mientras el objeto **RealTimeStylus** está habilitado, los datos del complemento que ha recibido el complemento pueden ser insuficientes para finalizar el procesamiento de los datos.</span><span class="sxs-lookup"><span data-stu-id="f7f93-139">Similarly, when a plug-in removed while the **RealTimeStylus** object is enabled, the plug-in data that the plug-in has received may be insufficient to finish processing the data.</span></span>

> [!Note]  
> <span data-ttu-id="f7f93-140">Para la estabilidad general, restablezca el estado interno de un complemento cuando se llame a su método [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) o [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) .</span><span class="sxs-lookup"><span data-stu-id="f7f93-140">For overall stability, reset a plug-in's internal state when either its [**RealTimeStylusEnabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusenabled) or [**RealTimeStylusDisabled**](/windows/desktop/api/RTSCom/nf-rtscom-istylusplugin-realtimestylusdisabled) method is called.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f7f93-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7f93-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7f93-142">El modelo RealTimeStylus en cascada</span><span class="sxs-lookup"><span data-stu-id="f7f93-142">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)
</dt> <dt>

[<span data-ttu-id="f7f93-143">Consideraciones sobre el control de errores para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="f7f93-143">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
</dt> <dt>

[<span data-ttu-id="f7f93-144">Datos de complementos y clase RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="f7f93-144">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
</dt> <dt>

[<span data-ttu-id="f7f93-145">Consideraciones sobre los subprocesos para las API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="f7f93-145">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)
</dt> </dl>

 

 
