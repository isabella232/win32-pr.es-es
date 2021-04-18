---
description: Información general de la biblioteca administrada y notas sobre el uso de la biblioteca administrada de la plataforma de Tablet PC.
ms.assetid: d283ea1c-faf3-4222-a9a7-c67087636b86
title: Uso de la biblioteca administrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1a1050705a6d74e6b183d04ec1c8f82d3954f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105707507"
---
# <a name="using-the-managed-library"></a><span data-ttu-id="22742-103">Uso de la biblioteca administrada</span><span class="sxs-lookup"><span data-stu-id="22742-103">Using the Managed Library</span></span>

<span data-ttu-id="22742-104">La Common Language Runtime es la base de Microsoft .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="22742-104">The common language runtime is the foundation of the Microsoft .NET Framework.</span></span> <span data-ttu-id="22742-105">Puede pensar en el Common Language Runtime como un agente que administra el código en tiempo de ejecución, proporcionando servicios principales como la administración de memoria, la administración de subprocesos y la comunicación remota, al tiempo que aplica una seguridad estricta del código.</span><span class="sxs-lookup"><span data-stu-id="22742-105">You can think of the common language runtime as an agent that manages code at execution time, providing core services such as memory management, thread management, and remoting, while also enforcing strict code safety.</span></span> <span data-ttu-id="22742-106">De hecho, el concepto de administración de código es un principio fundamental del Common Language Runtime.</span><span class="sxs-lookup"><span data-stu-id="22742-106">In fact, the concept of code management is a fundamental principle of the common language runtime.</span></span> <span data-ttu-id="22742-107">El código que tiene como destino el Common Language Runtime se conoce como código administrado.</span><span class="sxs-lookup"><span data-stu-id="22742-107">Code that targets the common language runtime is known as managed code.</span></span> <span data-ttu-id="22742-108">El código que no tiene como destino el Common Language Runtime se denomina código nativo.</span><span class="sxs-lookup"><span data-stu-id="22742-108">Code that does not target the common language runtime is known as native code.</span></span>

<span data-ttu-id="22742-109">La biblioteca de clases de Framework es una completa colección orientada a objetos de clases reutilizables que puede usar para desarrollar aplicaciones que abarcan desde aplicaciones tradicionales de línea de comandos o de interfaz gráfica de usuario (GUI) hasta aplicaciones basadas en las innovaciones más recientes proporcionadas por ASP.NET y servicios Web.</span><span class="sxs-lookup"><span data-stu-id="22742-109">The Framework class library is a comprehensive, object-oriented collection of reusable classes that you can use to develop applications ranging from traditional command-line or graphical user interface (GUI) applications to applications based on the latest innovations provided by ASP.NET and Web Services.</span></span>

<span data-ttu-id="22742-110">La biblioteca administrada de Tablet PC contiene un conjunto de objetos administrados que extiende el marco de trabajo para proporcionar compatibilidad con la entrada y la salida de escritura a mano en Tablet PC, así como el intercambio de datos con otros equipos.</span><span class="sxs-lookup"><span data-stu-id="22742-110">The Tablet PC Managed Library contains a set of managed objects that extends the Framework to provide support for input and output of handwriting on Tablet PC as well as data interchange with other computers.</span></span>

## <a name="exceptions"></a><span data-ttu-id="22742-111">Excepciones</span><span class="sxs-lookup"><span data-stu-id="22742-111">Exceptions</span></span>

<span data-ttu-id="22742-112">Los objetos de biblioteca administrada de la API de Tablet PC encapsulan las implementaciones de la biblioteca COM.</span><span class="sxs-lookup"><span data-stu-id="22742-112">The managed library objects in the Tablet PC API wrap the COM library implementations.</span></span> <span data-ttu-id="22742-113">Cuando el objeto o el control de la biblioteca COM subyacente devuelve un error, la API administrada generará una excepción Marshal. ThrowExceptionForHR que proporciona los detalles sobre la excepción COM interna.</span><span class="sxs-lookup"><span data-stu-id="22742-113">When the underlying COM library object or control returns an error, the managed API's will throw a Marshal.ThrowExceptionForHR exception that provides the details on the inner COM exception.</span></span> <span data-ttu-id="22742-114">Puede hacer referencia a los valores HRESULT en la referencia de la biblioteca COM para obtener más información sobre los posibles errores que se pueden devolver.</span><span class="sxs-lookup"><span data-stu-id="22742-114">You can refer to the HRESULT values in the COM Library Reference for details on the possible errors that may be returned.</span></span>

## <a name="object-comparison"></a><span data-ttu-id="22742-115">Comparación de objetos</span><span class="sxs-lookup"><span data-stu-id="22742-115">Object Comparison</span></span>

<span data-ttu-id="22742-116">En el caso de todos los objetos de la biblioteca administrada de la plataforma de Tablet PC, [**Equals**](/previous-versions/windows/) no se invalida para comparar correctamente dos objetos que son iguales.</span><span class="sxs-lookup"><span data-stu-id="22742-116">For all objects in the Tablet PC Platform Managed library, [**Equals**](/previous-versions/windows/) is not overridden to correctly compare two objects that are the same.</span></span> <span data-ttu-id="22742-117">La interfaz de programación de aplicaciones (API) administrada no admite la comparación de igualdad de objetos, ya sea a través de la función **Equals** o a través del operador Equals (= =).</span><span class="sxs-lookup"><span data-stu-id="22742-117">The managed application programming interface (API) does not support the comparison of objects for equality, either through the **Equals** function or through the equals (==) operator.</span></span>

## <a name="binding-to-the-latest-microsoftinkdll"></a><span data-ttu-id="22742-118">Enlazar a la Microsoft.Ink.dll más reciente</span><span class="sxs-lookup"><span data-stu-id="22742-118">Binding to the Latest Microsoft.Ink.dll</span></span>

<span data-ttu-id="22742-119">El ensamblado de Microsoft.Ink.dll más reciente es un reemplazo compatible de Microsoft.Ink.dll versión 1,0 y Microsoft.Ink.15.dll.</span><span class="sxs-lookup"><span data-stu-id="22742-119">The latest Microsoft.Ink.dll assembly is a compatible replacement for Microsoft.Ink.dll version 1.0 and Microsoft.Ink.15.dll.</span></span> <span data-ttu-id="22742-120">En la mayoría de los casos, no es necesario realizar ningún cambio en las aplicaciones que se distribuyen con los ensamblados anteriores.</span><span class="sxs-lookup"><span data-stu-id="22742-120">In most cases, you do not need to make any changes to your applications that are distributed with the older assemblies.</span></span> <span data-ttu-id="22742-121">Sin embargo, en algunos casos debe indicar al cargador de Common Language Runtime que utilice la biblioteca de vínculos dinámicos (DLL) más reciente donde se hace referencia a los archivos dll más antiguos.</span><span class="sxs-lookup"><span data-stu-id="22742-121">However, in some cases you need to instruct the common language runtime loader to use the newer dynamic-link library (DLL) wherever the older DLLs have been referenced.</span></span>

<span data-ttu-id="22742-122">La única vez que necesita enlazar explícitamente al nuevo ensamblado mediante el uso de la técnica siguiente es si la aplicación usa un componente que hace referencia al ensamblado de la versión 1,0 o 1,5 en combinación con un componente que hace referencia a un ensamblado de versión más reciente, como 1,7, y si esos componentes pueden intercambiar datos.</span><span class="sxs-lookup"><span data-stu-id="22742-122">The only time you need to explicitly bind to the new assembly by using the following technique is if your application uses a component that references the version 1.0 or 1.5 assembly in combination with a component that references a more recent version assembly,such as 1.7, and if those components may exchange data.</span></span>

<span data-ttu-id="22742-123">La mejor manera de indicar al cargador de Common Language Runtime que use el archivo DLL más reciente es redirigir las versiones de ensamblado en el nivel de aplicación.</span><span class="sxs-lookup"><span data-stu-id="22742-123">The best way to instruct the common language runtime loader to use the newer DLL is to redirect assembly versions at the application level.</span></span> <span data-ttu-id="22742-124">Puede especificar que la aplicación use la versión más reciente del ensamblado colocando la información de enlace del ensamblado en el archivo de configuración de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="22742-124">You can specify that your application use the newer version of the assembly by putting assembly binding information in your application's configuration file.</span></span> <span data-ttu-id="22742-125">Para obtener más información acerca de la redirección de versiones de ensamblado en el nivel de aplicación, consulte [redirección de versiones de ensamblado](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), concretamente la sección "especificar el enlace de ensamblados en archivos de configuración".</span><span class="sxs-lookup"><span data-stu-id="22742-125">For more information about redirecting assembly versions at the application level, see [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue), specifically the section "Specifying Assembly Binding in Configuration Files."</span></span>

<span data-ttu-id="22742-126">Tendrá que crear un archivo de configuración en el mismo directorio que el archivo ejecutable.</span><span class="sxs-lookup"><span data-stu-id="22742-126">You will need to create a configuration file in the same directory as your executable file.</span></span> <span data-ttu-id="22742-127">El archivo de configuración debe tener el mismo nombre que el ejecutable, seguido de la extensión del archivo. config.</span><span class="sxs-lookup"><span data-stu-id="22742-127">The configuration file must have the same name as your executable, followed by the .config file extension.</span></span> <span data-ttu-id="22742-128">Por ejemplo, para una aplicación, MyApp.exe, el archivo de configuración debe ser el archivo de MyApp.exe.config.</span><span class="sxs-lookup"><span data-stu-id="22742-128">For example, for an application, MyApp.exe, the configuration file must be the MyApp.exe.config file.</span></span> <span data-ttu-id="22742-129">El archivo de configuración usa un elemento [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) para forzar que todas las versiones anteriores se asignen a la versión más reciente, como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="22742-129">The configuration file uses a [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) element to force all prior versions to be mapped to the latest version, as shown in the following example:</span></span>

`<bindingRedirect oldVersion="0.0.0.0-1.7.2600.xxxx" newVersion="1.7.2600.xxxx" />`

<span data-ttu-id="22742-130">Para obtener más información sobre los archivos de configuración, incluidos ejemplos de cómo construir el lenguaje de marcado extensible (XML) para el archivo de configuración, vea [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) y [redirección de versiones de ensamblado](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span><span class="sxs-lookup"><span data-stu-id="22742-130">For more information about configuration files, including examples of how to construct the Extensible Markup Language (XML) for the configuration file, see both [bindingRedirect](/previous-versions/dotnet/netframework-1.1/eftw1fys(v=vs.71)) and [Redirecting Assembly Versions](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconassemblyversionredirection.asp%3fframe%3dtrue).</span></span>

<span data-ttu-id="22742-131">Las aplicaciones creadas con el kit de desarrollo de Microsoft Windows XP Tablet PC Edition 1,7 y versiones posteriores se enlazan automáticamente a la nueva versión del ensamblado Microsoft. Ink.</span><span class="sxs-lookup"><span data-stu-id="22742-131">Applications created with Microsoft Windows XP Tablet PC Edition Development Kit 1.7 and later versions are automatically bound to the new version of the Microsoft.Ink assembly.</span></span> <span data-ttu-id="22742-132">Para obtener más información sobre el enlace de ensamblados, vea [cómo el motor en tiempo de ejecución ubica ensamblados](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span><span class="sxs-lookup"><span data-stu-id="22742-132">For more information about assembly binding see [How the Runtime Locates Assemblies](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconHowRuntimeLocatesAssemblies.asp).</span></span>

> [!Note]  
> <span data-ttu-id="22742-133">El uso de la Directiva de aplicación para enlazar con el ensamblado actualizado no funciona para las aplicaciones que usan la clase [divisor](/previous-versions/ms583616(v=vs.100)) o la clase [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="22742-133">Using application policy to bind to the updated assembly does not work for applications that use the [Divider](/previous-versions/ms583616(v=vs.100)) class or the [PenInputPanel](/previous-versions/aa514041(v=msdn.10)) class.</span></span> <span data-ttu-id="22742-134">Las aplicaciones que usan cualquiera de esas clases deben seguir usando Microsoft.Ink.15.dll o volver a compilarse después de hacer referencia al ensamblado actualizado.</span><span class="sxs-lookup"><span data-stu-id="22742-134">Applications that use either of those classes must either continue to use Microsoft.Ink.15.dll or be recompiled after referencing the updated assembly.</span></span>

 

## <a name="working-with-events"></a><span data-ttu-id="22742-135">Trabajar con eventos</span><span class="sxs-lookup"><span data-stu-id="22742-135">Working with Events</span></span>

<span data-ttu-id="22742-136">Si el código de un controlador de eventos para cualquiera de los objetos administrados produce una excepción, la excepción no se entrega al usuario.</span><span class="sxs-lookup"><span data-stu-id="22742-136">If the code within an event handler for any of the managed objects throws an exception, the exception is not delivered to the user.</span></span> <span data-ttu-id="22742-137">Para asegurarse de que se entreguen las excepciones, use bloques try-catch en los controladores de eventos para los eventos administrados.</span><span class="sxs-lookup"><span data-stu-id="22742-137">To ensure that exceptions are delivered, use try-catch blocks in your event handlers for managed events.</span></span>

## <a name="managing-forms"></a><span data-ttu-id="22742-138">Administrar formularios</span><span class="sxs-lookup"><span data-stu-id="22742-138">Managing Forms</span></span>

<span data-ttu-id="22742-139">La clase de [formulario](/dotnet/api/system.windows.forms.form?view=netcore-3.1) y sus clases base no definen un finalizador.</span><span class="sxs-lookup"><span data-stu-id="22742-139">The [Form](/dotnet/api/system.windows.forms.form?view=netcore-3.1) class and its base classes do not define a finalizer.</span></span> <span data-ttu-id="22742-140">Para limpiar los recursos en un formulario, escriba una subclase que proporcione un finalizador (por ejemplo, el destructor de C \# mediante el ~) que llama a [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span><span class="sxs-lookup"><span data-stu-id="22742-140">To clean up your resources on a form, write a subclass that provides a finalizer (for example, the C\# destructor using the ~) that calls [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1).</span></span> <span data-ttu-id="22742-141">Para realizar la limpieza, el finalizador invalida Dispose y llama a la clase base Dispose.</span><span class="sxs-lookup"><span data-stu-id="22742-141">To do the cleanup the finalizer overrides Dispose and then calls the base class Dispose.</span></span> <span data-ttu-id="22742-142">No haga referencia a otros objetos que requieran el método [Finalize](/previous-versions/windows/) en el método Dispose cuando el parámetro booleano sea **false**, ya que es posible que esos objetos ya se hayan finalizado.</span><span class="sxs-lookup"><span data-stu-id="22742-142">Do not refer to other objects that require the [Finalize](/previous-versions/windows/) method in the Dispose method when the Boolean parameter is **FALSE**, because those objects may already have been finalized.</span></span> <span data-ttu-id="22742-143">Para obtener más información sobre la liberación de recursos [, vea métodos de finalización y destructores](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span><span class="sxs-lookup"><span data-stu-id="22742-143">For more information about releasing resources see [Finalize Methods and Destructors](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconfinalizemethodscdestructors.asp).</span></span>

## <a name="forms-and-the-recognizercontext"></a><span data-ttu-id="22742-144">Formularios y RecognizerContext</span><span class="sxs-lookup"><span data-stu-id="22742-144">Forms and the RecognizerContext</span></span>

<span data-ttu-id="22742-145">Los eventos [RecognizerContext](/previous-versions/ms552546(v=vs.100)) se ejecutan en un subproceso diferente del subproceso en el que se encuentra el formulario.</span><span class="sxs-lookup"><span data-stu-id="22742-145">[RecognizerContext](/previous-versions/ms552546(v=vs.100)) events run in a different thread than the thread that the form is on.</span></span> <span data-ttu-id="22742-146">Los controles de Windows Forms se enlazan a un subproceso concreto y no son seguros para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="22742-146">Controls in Windows Forms are bound to a specific thread and are not thread safe.</span></span> <span data-ttu-id="22742-147">Por lo tanto, debe usar uno de los métodos de invocación del control para calcular las referencias de la llamada al subproceso adecuado.</span><span class="sxs-lookup"><span data-stu-id="22742-147">Therefore, you must use one of the control's invoke methods to marshal the call to the proper thread.</span></span> <span data-ttu-id="22742-148">Cuatro métodos en un control son seguros para subprocesos: los métodos [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1)y [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="22742-148">Four methods on a control are thread safe: the [Invoke](/dotnet/api/system.windows.forms.control.invoke?view=netcore-3.1), [BeginInvoke](/dotnet/api/system.windows.forms.control.begininvoke?view=netcore-3.1), [EndInvoke](/dotnet/api/system.windows.forms.control.endinvoke?view=netcore-3.1), and [CreateGraphics](/dotnet/api/system.windows.forms.control.creategraphics?view=netcore-3.1) methods.</span></span> <span data-ttu-id="22742-149">Para todas las demás llamadas a métodos, use uno de estos métodos de invocación cuando llame a desde un subproceso diferente.</span><span class="sxs-lookup"><span data-stu-id="22742-149">For all other method calls, use one of these invoke methods when calling from a different thread.</span></span> <span data-ttu-id="22742-150">Para obtener más información sobre el uso de estos métodos, vea [manipular controles desde subprocesos](/previous-versions/757y83z4(v=vs.140)).</span><span class="sxs-lookup"><span data-stu-id="22742-150">For more information on using these methods, see [Manipulating Controls from Threads](/previous-versions/757y83z4(v=vs.140)).</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="22742-151">Esperando eventos</span><span class="sxs-lookup"><span data-stu-id="22742-151">Waiting for Events</span></span>

<span data-ttu-id="22742-152">El entorno de Tablet PC es multiproceso.</span><span class="sxs-lookup"><span data-stu-id="22742-152">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="22742-153">Utilice la función [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) en lugar de otros métodos wait para permitir que las llamadas del modelo de objetos componentes (com) reentrantes escriban el apartamento multiproceso (MTA) mientras la aplicación está esperando en un evento.</span><span class="sxs-lookup"><span data-stu-id="22742-153">Use the [**CoWaitForMultipleHandles**](/windows/win32/api/combaseapi/nf-combaseapi-cowaitformultiplehandles) function instead of other wait methods to allow re-entrant Component Object Model (COM) calls to enter your multithreaded apartment (MTA) while your application is waiting on an event.</span></span>

## <a name="using-ink-strokes-collections"></a><span data-ttu-id="22742-154">Usar colecciones de trazos de lápiz</span><span class="sxs-lookup"><span data-stu-id="22742-154">Using Ink Strokes Collections</span></span>

<span data-ttu-id="22742-155">Las instancias de las colecciones de [trazos](/previous-versions/ms552701(v=vs.100)) que se obtienen a partir de un objeto de [entrada manuscrita](/previous-versions/aa515768(v=msdn.10)) no se recolectan como elementos no utilizados.</span><span class="sxs-lookup"><span data-stu-id="22742-155">Instances of [Strokes](/previous-versions/ms552701(v=vs.100)) collections which are obtained from an [Ink](/previous-versions/aa515768(v=msdn.10)) object are not garbage collected.</span></span> <span data-ttu-id="22742-156">Para evitar una pérdida de memoria, siempre que trabaje con una de estas colecciones, use la instrucción "Using" tal y como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="22742-156">In order to avoid a memory leak, any time that you are working with one of these collections, make use of the "using" statement as shown below.</span></span>


```C++
using (Strokes strokes = myInk.Strokes)
{
    int i = strokes.Count;
}
```



## <a name="disposing-managed-objects-and-controls"></a><span data-ttu-id="22742-157">Desechar controles y objetos administrados</span><span class="sxs-lookup"><span data-stu-id="22742-157">Disposing Managed Objects and Controls</span></span>

<span data-ttu-id="22742-158">Para evitar una pérdida de memoria, debe llamar explícitamente al método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) en cualquier objeto o control de Tablet PC al que se haya adjuntado un controlador de eventos antes de que el objeto o el control salga del ámbito.</span><span class="sxs-lookup"><span data-stu-id="22742-158">To avoid a memory leak you must explicitly call the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method on any Tablet PC object or control to which an event handler has been attached before the object or control goes out of scope.</span></span>

<span data-ttu-id="22742-159">Para mejorar el rendimiento de la aplicación, elimine manualmente los siguientes objetos, controles y colecciones cuando ya no se necesiten.</span><span class="sxs-lookup"><span data-stu-id="22742-159">To improve the performance of your application, manually dispose of the following objects, controls, and collection when they are no longer needed.</span></span>

-   <span data-ttu-id="22742-160">[Divisor](/previous-versions/ms583616(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-160">[Divider](/previous-versions/ms583616(v=vs.100))</span></span>
-   <span data-ttu-id="22742-161">[Entrada de lápiz](/previous-versions/aa515768(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="22742-161">[Ink](/previous-versions/aa515768(v=msdn.10))</span></span>
-   <span data-ttu-id="22742-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-162">[InkCollector](/previous-versions/ms583683(v=vs.100))</span></span>
-   <span data-ttu-id="22742-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-163">[InkEdit](/previous-versions/ms552265(v=vs.100))</span></span>
-   <span data-ttu-id="22742-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-164">[InkOverlay](/previous-versions/ms552322(v=vs.100))</span></span>
-   <span data-ttu-id="22742-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="22742-165">[InkPicture](/previous-versions/aa514604(v=msdn.10))</span></span>
-   <span data-ttu-id="22742-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="22742-166">[PenInputPanel](/previous-versions/aa514041(v=msdn.10))</span></span>
-   <span data-ttu-id="22742-167">[Estableció](/previous-versions/ms552546(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-167">[RecognizerContext](/previous-versions/ms552546(v=vs.100))</span></span>
-   <span data-ttu-id="22742-168">[Trazos](/previous-versions/ms552701(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="22742-168">[Strokes](/previous-versions/ms552701(v=vs.100))</span></span>

<span data-ttu-id="22742-169">En el siguiente \# ejemplo de C se muestran algunos escenarios en los que se usa el método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="22742-169">The following C\# example demonstrates some scenarios in which the [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method is used.</span></span>


```C++
// A field for a Divider object
private Microsoft.Ink.Divider theDivider;

// A method that creates a Divider object
public void CreateDivider()
{
    // Make sure any previous Divider object was disposed of.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
    // Create the Divider object.
    theDivider = new Microsoft.Ink.Divider();

    // The remainder of the method
}

// A method that disposes of the Divider object
public void DisposeDivider()
{
    // The remainder of the method

    // Dispose of the Divider object.
    if (null != theDivider)
    {
        theDivider.Dispose();
        theDivider = null;
    }
}

// A method that uses a local PenInputPanel object.
public void UsePenInputPanel()
{
    // Create the PenInputPanel object.
    Microsoft.Ink.PenInputPanel thePenInputPanel =
        new Microsoft.Ink.PenInputPanel();

    // The remainder of the method

    // Dispose of the PenInputPanel object before exiting.
    thePenInputPanel.Dispose();
    thePenInputPanel = null;
}
```



 

 