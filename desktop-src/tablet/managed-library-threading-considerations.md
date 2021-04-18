---
description: Las siguientes consideraciones sobre el subproceso de Tablet PC son específicas de la biblioteca administrada.
ms.assetid: bcc398d3-22ea-466c-9206-92b0ac208def
title: Consideraciones sobre los subprocesos de biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b8677375b8bbdb5f171329927d01e6178b5cb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706687"
---
# <a name="managed-library-threading-considerations"></a><span data-ttu-id="09cae-103">Consideraciones sobre los subprocesos de biblioteca administrada</span><span class="sxs-lookup"><span data-stu-id="09cae-103">Managed Library Threading Considerations</span></span>

<span data-ttu-id="09cae-104">Las siguientes consideraciones sobre el subproceso de Tablet PC son específicas de la biblioteca administrada.</span><span class="sxs-lookup"><span data-stu-id="09cae-104">The following Tablet PC threading considerations are specific to the Managed Library.</span></span>

-   [<span data-ttu-id="09cae-105">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="09cae-105">Thread-Safety</span></span>](#thread-safety)
-   [<span data-ttu-id="09cae-106">Aplicaciones STA y MTA</span><span class="sxs-lookup"><span data-stu-id="09cae-106">STA and MTA Applications</span></span>](#sta-and-mta-applications)
-   [<span data-ttu-id="09cae-107">Consideraciones sobre el subprocesamiento de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09cae-107">Windows Forms Threading Considerations</span></span>](#windows-forms-threading-considerations)
-   [<span data-ttu-id="09cae-108">Consideraciones sobre el portapapeles</span><span class="sxs-lookup"><span data-stu-id="09cae-108">Clipboard Considerations</span></span>](#clipboard-considerations)
-   [<span data-ttu-id="09cae-109">Excepciones dentro de los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="09cae-109">Exceptions within Event Handlers</span></span>](#exceptions-within-event-handlers)
-   [<span data-ttu-id="09cae-110">Desechar objetos y controles</span><span class="sxs-lookup"><span data-stu-id="09cae-110">Disposing Objects and Controls</span></span>](#disposing-objects-and-controls)
-   [<span data-ttu-id="09cae-111">API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="09cae-111">StylusInput APIs</span></span>](#stylusinput-apis)

## <a name="thread-safety"></a><span data-ttu-id="09cae-112">Thread-Safety</span><span class="sxs-lookup"><span data-stu-id="09cae-112">Thread-Safety</span></span>

<span data-ttu-id="09cae-113">Las clases de biblioteca administrada de la plataforma de Tablet PC no suelen ser seguras para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="09cae-113">The Tablet PC Platform's Managed Library classes are not generally thread-safe.</span></span> <span data-ttu-id="09cae-114">Las colecciones siguientes son seguras para subprocesos en el nivel de miembro; sin embargo, estas colecciones no garantizan que un enumerador esté protegido si otro subproceso funciona en la colección simultáneamente:</span><span class="sxs-lookup"><span data-stu-id="09cae-114">The following collections are thread-safe at the member level; however, these collections do not guarantee that an enumerator is protected if another thread operates on the collection simultaneously:</span></span>

-   <span data-ttu-id="09cae-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-115">[CursorButtons](/previous-versions/ms839506(v=msdn.10))</span></span>
-   <span data-ttu-id="09cae-116">[Cursores](/previous-versions/ms839493(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-116">[Cursors](/previous-versions/ms839493(v=msdn.10))</span></span>
-   <span data-ttu-id="09cae-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-117">[DivisionUnits](/previous-versions/ms837954(v=msdn.10))</span></span>
-   <span data-ttu-id="09cae-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-118">[RecognitionAlternates](/previous-versions/ms830115(v=msdn.10))</span></span>
-   <span data-ttu-id="09cae-119">[Reconocedores](/previous-versions/ms828520(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-119">[Recognizers](/previous-versions/ms828520(v=msdn.10))</span></span>
-   <span data-ttu-id="09cae-120">[Digitaliza](/previous-versions/ms827599(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="09cae-120">[Tablets](/previous-versions/ms827599(v=msdn.10))</span></span>

## <a name="sta-and-mta-applications"></a><span data-ttu-id="09cae-121">Aplicaciones STA y MTA</span><span class="sxs-lookup"><span data-stu-id="09cae-121">STA and MTA Applications</span></span>

<span data-ttu-id="09cae-122">De forma predeterminada, las aplicaciones administradas creadas con los asistentes contenidos en Microsoft Visual Studio .NET son un contenedor uniproceso (STA).</span><span class="sxs-lookup"><span data-stu-id="09cae-122">Managed applications created by using the wizards contained in Microsoft Visual Studio .NET are single-threaded apartment (STA) by default.</span></span> <span data-ttu-id="09cae-123">Puede cambiar el apartamento de la aplicación estableciendo el subproceso STA o el atributo de subproceso de Apartamento multiproceso (MTA) en el punto de entrada de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09cae-123">You can change the apartment for your application by setting the STA thread or multithreaded apartment (MTA) thread attribute on the entry point of your application.</span></span>

<span data-ttu-id="09cae-124">Si la aplicación se ejecuta en un MTA, debe escribir código seguro para subprocesos; sin embargo, si lo hace, puede mejorar determinados problemas de rendimiento de control de eventos.</span><span class="sxs-lookup"><span data-stu-id="09cae-124">If your application runs in an MTA, you must write thread-safe code; however, by doing so you can improve certain event handling performance issues.</span></span>

<span data-ttu-id="09cae-125">Para obtener más información sobre los atributos de subprocesos y subprocesos de MTA, consulte clase [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) y clase [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="09cae-125">For more information about the STA thread and MTA thread attributes, see [STAThreadAttribute](/dotnet/api/system.stathreadattribute?view=netcore-3.1) class and [MTAThreadAttribute](/dotnet/api/system.mtathreadattribute?view=netcore-3.1) Class.</span></span>

## <a name="windows-forms-threading-considerations"></a><span data-ttu-id="09cae-126">Consideraciones sobre el subprocesamiento de Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09cae-126">Windows Forms Threading Considerations</span></span>

<span data-ttu-id="09cae-127">Los controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit](/previous-versions/ms552265(v=vs.100)) extienden Windows Forms controles.</span><span class="sxs-lookup"><span data-stu-id="09cae-127">The [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls extend Windows Forms controls.</span></span> <span data-ttu-id="09cae-128">Los controles de Windows Forms utilizan el modelo de contenedor uniproceso (STA) porque Windows Forms se basan en ventanas nativas de Win32 que son de un solo subproceso.</span><span class="sxs-lookup"><span data-stu-id="09cae-128">Windows Forms controls use the single-threaded apartment (STA) model because Windows Forms are based on native Win32 windows that are inherently single threaded.</span></span> <span data-ttu-id="09cae-129">En código administrado, los controles de entrada de lápiz deben crearse en el mismo subproceso que el subproceso principal del formulario.</span><span class="sxs-lookup"><span data-stu-id="09cae-129">In managed code, ink controls should be created in the same thread as the main thread for the form.</span></span>

<span data-ttu-id="09cae-130">En una aplicación STA, ciertos eventos se producen en un subproceso distinto del subproceso de la interfaz de usuario (IU) de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09cae-130">In an STA application, certain events happen on a thread other than the application's user interface (UI) thread.</span></span> <span data-ttu-id="09cae-131">Al llamar a cualquier Windows Forms objeto o control, incluidos los controles [InkPicture](/previous-versions/aa514604(v=msdn.10)) y [InkEdit](/previous-versions/ms552265(v=vs.100)) , desde dentro de un controlador de eventos de Tablet PC, use el método heredado [control. Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) del objeto o el control.</span><span class="sxs-lookup"><span data-stu-id="09cae-131">When calling any Windows Forms object or control, including the [InkPicture](/previous-versions/aa514604(v=msdn.10)) and [InkEdit](/previous-versions/ms552265(v=vs.100)) controls, from within a Tablet PC event handler, use the object or control's inherited [Control.Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1) method.</span></span> <span data-ttu-id="09cae-132">La propiedad [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) , heredada de la clase control, se puede utilizar para determinar si es necesario.</span><span class="sxs-lookup"><span data-stu-id="09cae-132">The [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property, inherited from the Control class, can be used to determine if this is necessary.</span></span>

<span data-ttu-id="09cae-133">Por ejemplo, en el siguiente controlador de eventos para el evento de [reconocimiento](/previous-versions/ms829424(v=msdn.10)) , se prueba la propiedad [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) y, si es **true**, el controlador de eventos se vuelve a invocar desde el subproceso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="09cae-133">For example, in the following event handler for the [Recognition](/previous-versions/ms829424(v=msdn.10)) event, the [InvokeRequired](/dotnet/api/system.windows.forms.control.invokerequired?view=netcore-3.1) property is tested and if **TRUE**, the event handler is re-invoked from the user interface thread.</span></span>


```C++
void recoContext_Recognition(object sender, 
        RecognizerContextRecognitionEventArgs e)
{
    if (InvokeRequired)
    {
        Invoke( new RecognizerContextRecognitionEventHandler(  
                     recoContext_Recognition ),
                    new object[] { sender, e } );
        return;
    }
     // Use the recognition result here.
}
```



<span data-ttu-id="09cae-134">Si coloca [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) en awebpagein en un explorador (consulte [controles Web](web-controls.md)), se ejecuta como una aplicación Sta.</span><span class="sxs-lookup"><span data-stu-id="09cae-134">If you put a [UserControl](/dotnet/api/system.web.ui.usercontrol?view=netframework-4.8) onto awebpagein a browser (see [Web Controls](web-controls.md)), then it runs as an STA application.</span></span> <span data-ttu-id="09cae-135">En el caso de las aplicaciones Smart Client (no se ve [ninguna implementación táctil](no-touch-deployment.md)), el desarrollador tiene control total sobre el [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="09cae-135">For smart client applications (see [No Touch Deployment](no-touch-deployment.md)), the developer has full control over the [ApartmentState](/dotnet/api/system.threading.apartmentstate?view=netcore-3.1).</span></span> <span data-ttu-id="09cae-136">(El valor predeterminado es generalmente STA, pero puede ser MTA, dependiendo de la versión de CLR). En el caso de problemas de subprocesamiento que impliquen a [**RealTimeStylus**](realtimestylus-class.md), consulte [consideraciones sobre subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="09cae-136">(The default is generally STA, but may be MTA, depending on your version of CLR.) For threading issues involving the [**RealTimeStylus**](realtimestylus-class.md), see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

<span data-ttu-id="09cae-137">Para obtener más información sobre cómo llamar a Windows Forms desde una aplicación MTA, vea [ejemplo de control multiproceso Windows Forms](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="09cae-137">For more information about calling Windows Forms from an MTA application, see [Multithreaded Windows Forms Control Sample](/previous-versions/dotnet/netframework-1.1/3s8xdz5c(v=vs.71)).</span></span>

## <a name="clipboard-considerations"></a><span data-ttu-id="09cae-138">Consideraciones sobre el portapapeles</span><span class="sxs-lookup"><span data-stu-id="09cae-138">Clipboard Considerations</span></span>

<span data-ttu-id="09cae-139">El objeto [Clipboard](../dataxchg/clipboard.md) solo funciona desde un subproceso STA.</span><span class="sxs-lookup"><span data-stu-id="09cae-139">The [Clipboard](../dataxchg/clipboard.md) object works only from an STA thread.</span></span> <span data-ttu-id="09cae-140">Al intentar copiar o pegar desde el Portapapeles desde un subproceso que no es STA, obtiene un [ThreadStateException](/previous-versions/windows/).</span><span class="sxs-lookup"><span data-stu-id="09cae-140">When trying to copy to or paste from the Clipboard from a thread that is not STA, you get a [ThreadStateException](/previous-versions/windows/).</span></span> <span data-ttu-id="09cae-141">Si la aplicación es MTA, cree un subproceso STA para controlar las llamadas al método del portapapeles y algunos de los demás aspectos de la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09cae-141">If your application is MTA, create an STA thread to handle the Clipboard's method calls and some of the other UI aspects of your application.</span></span>

## <a name="exceptions-within-event-handlers"></a><span data-ttu-id="09cae-142">Excepciones dentro de los controladores de eventos</span><span class="sxs-lookup"><span data-stu-id="09cae-142">Exceptions within Event Handlers</span></span>

<span data-ttu-id="09cae-143">No se pueden iniciar excepciones desde los controladores de eventos de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="09cae-143">Exceptions cannot be thrown from within Tablet PC event handlers.</span></span> <span data-ttu-id="09cae-144">Por ejemplo, si un delegado de controlador de eventos para un objeto o colección de Tablet PC tiene tres controladores registrados y el primero de ellos inicia una excepción, se produce la siguiente secuencia:</span><span class="sxs-lookup"><span data-stu-id="09cae-144">For example, if an event handler delegate for a Tablet PC object or collection has three registered handlers and the first one throws an exception, then the following sequence occurs:</span></span>

1.  <span data-ttu-id="09cae-145">El primer controlador se cierra.</span><span class="sxs-lookup"><span data-stu-id="09cae-145">The first handler exits.</span></span>
2.  <span data-ttu-id="09cae-146">La excepción se pierde.</span><span class="sxs-lookup"><span data-stu-id="09cae-146">The exception is lost.</span></span>
3.  <span data-ttu-id="09cae-147">No se invocan los controladores restantes.</span><span class="sxs-lookup"><span data-stu-id="09cae-147">The remaining handlers are not invoked.</span></span>

## <a name="disposing-objects-and-controls"></a><span data-ttu-id="09cae-148">Desechar objetos y controles</span><span class="sxs-lookup"><span data-stu-id="09cae-148">Disposing Objects and Controls</span></span>

<span data-ttu-id="09cae-149">Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el objeto o el control salga del ámbito.</span><span class="sxs-lookup"><span data-stu-id="09cae-149">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="09cae-150">Para mejorar el rendimiento de la aplicación, elimine manualmente cualquier objeto o control de Tablet PC que implemente el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) cuando el objeto o el control ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="09cae-150">To improve performance in your application, manually dispose of any Tablet PC object or control that implements the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method when the object or control is no longer needed.</span></span>

## <a name="stylusinput-apis"></a><span data-ttu-id="09cae-151">API de StylusInput</span><span class="sxs-lookup"><span data-stu-id="09cae-151">StylusInput APIs</span></span>

<span data-ttu-id="09cae-152">Para obtener información sobre las consideraciones de subprocesos para el objeto [**RealTimeStylus**](realtimestylus-class.md) y las interfaces de programación de aplicaciones (API) StylusInput, consulte [consideraciones sobre los subprocesos para las API de StylusInput](threading-considerations-for-the-stylusinput-apis.md).</span><span class="sxs-lookup"><span data-stu-id="09cae-152">For information about threading considerations for the [**RealTimeStylus**](realtimestylus-class.md) object and the StylusInput application programming interfaces (APIs) see [Threading Considerations for the StylusInput APIs](threading-considerations-for-the-stylusinput-apis.md).</span></span>

 

 
