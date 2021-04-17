---
description: Funciones de salida de depuración
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Funciones de salida de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105659299"
---
# <a name="debug-output-functions"></a><span data-ttu-id="650b6-103">Funciones de salida de depuración</span><span class="sxs-lookup"><span data-stu-id="650b6-103">Debug Output Functions</span></span>

<span data-ttu-id="650b6-104">Las [clases base de DirectShow](directshow-base-classes.md) proporcionan varias macros para mostrar información de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="650b6-105">Función</span><span class="sxs-lookup"><span data-stu-id="650b6-105">Function</span></span>                                               | <span data-ttu-id="650b6-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="650b6-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="650b6-107">**DbgCheckModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="650b6-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="650b6-108">Comprueba si el registro está habilitado para los tipos de mensaje y el nivel especificados.</span><span class="sxs-lookup"><span data-stu-id="650b6-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="650b6-109">**DbgDumpObjectRegister**</span><span class="sxs-lookup"><span data-stu-id="650b6-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="650b6-110">Muestra información acerca de los objetos activos.</span><span class="sxs-lookup"><span data-stu-id="650b6-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="650b6-111">**DbgInitialise**</span><span class="sxs-lookup"><span data-stu-id="650b6-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="650b6-112">Inicializa la biblioteca de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="650b6-113">**DbgLog**</span><span class="sxs-lookup"><span data-stu-id="650b6-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="650b6-114">Envía una cadena a la ubicación de salida de depuración, si el registro está habilitado para el tipo y el nivel especificados.</span><span class="sxs-lookup"><span data-stu-id="650b6-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="650b6-115">**DbgOutString**</span><span class="sxs-lookup"><span data-stu-id="650b6-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="650b6-116">Envía una cadena a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="650b6-117">**DbgSetModuleLevel**</span><span class="sxs-lookup"><span data-stu-id="650b6-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="650b6-118">Establece el nivel de registro para uno o más tipos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="650b6-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="650b6-119">**DbgTerminate**</span><span class="sxs-lookup"><span data-stu-id="650b6-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="650b6-120">Limpia la biblioteca de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="650b6-121">**TipoDePresentación**</span><span class="sxs-lookup"><span data-stu-id="650b6-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="650b6-122">Envía información sobre un tipo de medio a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="650b6-123">**DumpGraph**</span><span class="sxs-lookup"><span data-stu-id="650b6-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="650b6-124">Envía información sobre un gráfico de filtro a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="650b6-125">**GuidNames**</span><span class="sxs-lookup"><span data-stu-id="650b6-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="650b6-126">Matriz global que contiene cadenas que representan los GUID definidos en UUID. h.</span><span class="sxs-lookup"><span data-stu-id="650b6-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="650b6-127">**NAME**</span><span class="sxs-lookup"><span data-stu-id="650b6-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="650b6-128">Genera una cadena de solo depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="650b6-129">**Tenga en cuenta**</span><span class="sxs-lookup"><span data-stu-id="650b6-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="650b6-130">Envía una cadena a la ubicación de salida de depuración.</span><span class="sxs-lookup"><span data-stu-id="650b6-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="650b6-131">**TE**</span><span class="sxs-lookup"><span data-stu-id="650b6-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="650b6-132">Genera un recordatorio en tiempo de compilación.</span><span class="sxs-lookup"><span data-stu-id="650b6-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="650b6-133">**Claves del registro**</span><span class="sxs-lookup"><span data-stu-id="650b6-133">**Registry Keys**</span></span>

<span data-ttu-id="650b6-134">La función de salida de depuración de DirectShow usa un conjunto de claves del registro.</span><span class="sxs-lookup"><span data-stu-id="650b6-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="650b6-135">La ubicación de estas claves del registro depende de la versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="650b6-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="650b6-136">*Antes de Windows Vista*, las claves de depuración se encuentran en la siguiente ruta de acceso:</span><span class="sxs-lookup"><span data-stu-id="650b6-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="650b6-137">**HKEY \_ \_** Depuración de \\ **software** \\  de máquina local</span><span class="sxs-lookup"><span data-stu-id="650b6-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="650b6-138">En Windows Vista o posterior, se encuentran en la siguiente ruta de acceso:</span><span class="sxs-lookup"><span data-stu-id="650b6-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="650b6-139">**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**</span><span class="sxs-lookup"><span data-stu-id="650b6-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="650b6-140">En el caso de los filtros de terceros, la ubicación depende de la versión de las [clases base de DirectShow](directshow-base-classes.md) que se usó para generar el filtro.</span><span class="sxs-lookup"><span data-stu-id="650b6-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="650b6-141">La versión incluida en el Windows SDK para Windows Vista utiliza la ruta de acceso más reciente.</span><span class="sxs-lookup"><span data-stu-id="650b6-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="650b6-142">Las versiones anteriores usaban la ruta de acceso anterior.</span><span class="sxs-lookup"><span data-stu-id="650b6-142">Previous versions used the older path.</span></span>

<span data-ttu-id="650b6-143">En las notas siguientes, la etiqueta *<DebugRoot>* se usa para indicar estas dos rutas de acceso.</span><span class="sxs-lookup"><span data-stu-id="650b6-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="650b6-144">Reemplace la ruta de acceso correcta, dependiendo de la versión de Windows o de la versión de las clases base.</span><span class="sxs-lookup"><span data-stu-id="650b6-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="650b6-145">**Depurar registro**</span><span class="sxs-lookup"><span data-stu-id="650b6-145">**Debug Logging**</span></span>

<span data-ttu-id="650b6-146">DirectShow define varios tipos de mensajes, que se muestran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="650b6-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="650b6-147">Value</span><span class="sxs-lookup"><span data-stu-id="650b6-147">Value</span></span>                   | <span data-ttu-id="650b6-148">Descripción</span><span class="sxs-lookup"><span data-stu-id="650b6-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="650b6-149">ERROR de registro \_</span><span class="sxs-lookup"><span data-stu-id="650b6-149">LOG\_ERROR</span></span>              | <span data-ttu-id="650b6-150">Notificación de error.</span><span class="sxs-lookup"><span data-stu-id="650b6-150">Error notification.</span></span>                                     |
| <span data-ttu-id="650b6-151">bloqueo de registro \_</span><span class="sxs-lookup"><span data-stu-id="650b6-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="650b6-152">Bloqueo y desbloqueo de secciones críticas.</span><span class="sxs-lookup"><span data-stu-id="650b6-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="650b6-153">memoria de registro \_</span><span class="sxs-lookup"><span data-stu-id="650b6-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="650b6-154">Asignación de memoria y creación y destrucción de objetos.</span><span class="sxs-lookup"><span data-stu-id="650b6-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="650b6-155">tiempo de registro \_</span><span class="sxs-lookup"><span data-stu-id="650b6-155">LOG\_TIMING</span></span>             | <span data-ttu-id="650b6-156">Medidas de tiempo y rendimiento.</span><span class="sxs-lookup"><span data-stu-id="650b6-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="650b6-157">seguimiento de registro \_</span><span class="sxs-lookup"><span data-stu-id="650b6-157">LOG\_TRACE</span></span>              | <span data-ttu-id="650b6-158">Seguimiento de llamadas general.</span><span class="sxs-lookup"><span data-stu-id="650b6-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="650b6-159">CUSTOM1 a través de CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="650b6-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="650b6-160">Disponible para mensajes de depuración personalizados</span><span class="sxs-lookup"><span data-stu-id="650b6-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="650b6-161">Cada una de las funciones de registro de depuración de DirectShow especifica un tipo de mensaje y un nivel de registro.</span><span class="sxs-lookup"><span data-stu-id="650b6-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="650b6-162">El mensaje de depuración solo se muestra cuando el nivel de depuración actual para ese tipo de mensaje es igual o mayor que el nivel especificado en la función de registro.</span><span class="sxs-lookup"><span data-stu-id="650b6-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="650b6-163">De lo contrario, se omite el mensaje.</span><span class="sxs-lookup"><span data-stu-id="650b6-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="650b6-164">Por ejemplo, el código siguiente genera la cadena "This is a Debug Message" si el nivel de seguimiento del registro \_ es 3 o superior:</span><span class="sxs-lookup"><span data-stu-id="650b6-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="650b6-165">Cada módulo puede establecer su propio nivel de depuración para cada tipo de mensaje.</span><span class="sxs-lookup"><span data-stu-id="650b6-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="650b6-166">(Un *módulo* es un archivo dll o ejecutable que se puede cargar mediante la función **LoadLibrary** ). Los niveles de depuración de un módulo aparecen en el registro con la siguiente clave:</span><span class="sxs-lookup"><span data-stu-id="650b6-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="650b6-167">**HKEY \_ local \_ Machine**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="650b6-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="650b6-168">donde *<Message Type>* es el tipo de mensaje menos el "Registro \_ " inicial; por ejemplo, el **bloqueo** de mensajes de bloqueo de registro \_ .</span><span class="sxs-lookup"><span data-stu-id="650b6-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="650b6-169">Cuando se carga un módulo, la biblioteca de depuración encuentra los niveles de registro del módulo en el registro.</span><span class="sxs-lookup"><span data-stu-id="650b6-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="650b6-170">Si las claves del registro no existen, la biblioteca de depuración las crea.</span><span class="sxs-lookup"><span data-stu-id="650b6-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="650b6-171">Un módulo también puede establecer sus propios niveles en tiempo de ejecución mediante la función [**DbgSetModuleLevel**](dbgsetmodulelevel.md) .</span><span class="sxs-lookup"><span data-stu-id="650b6-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="650b6-172">Para enviar un mensaje a la salida de depuración, llame a la macro [**DbgLog**](dbglog.md) .</span><span class="sxs-lookup"><span data-stu-id="650b6-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="650b6-173">En el ejemplo siguiente se crea un mensaje de nivel 3 de tipo \_ Trace log:</span><span class="sxs-lookup"><span data-stu-id="650b6-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="650b6-174">También puede especificar niveles de registro globales, con la siguiente clave del registro:</span><span class="sxs-lookup"><span data-stu-id="650b6-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="650b6-175">La biblioteca de depuración utiliza cualquier nivel mayor, el nivel global o el nivel de módulo.</span><span class="sxs-lookup"><span data-stu-id="650b6-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="650b6-176">**Ubicación de salida de depuración**</span><span class="sxs-lookup"><span data-stu-id="650b6-176">**Debug Output Location**</span></span>

<span data-ttu-id="650b6-177">La ubicación de salida de depuración viene determinada por otra clave del registro:</span><span class="sxs-lookup"><span data-stu-id="650b6-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="650b6-178">**HKEY \_ \_Máquina local** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **LogToFile**</span><span class="sxs-lookup"><span data-stu-id="650b6-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="650b6-179">Si el valor de esta clave es `Console` , el resultado se dirige a la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="650b6-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="650b6-180">Si el valor es `Deb` , `Debug` , `Debugger` o una cadena vacía, la salida va a la ventana del depurador.</span><span class="sxs-lookup"><span data-stu-id="650b6-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="650b6-181">De lo contrario, la salida se escribe en un archivo especificado por la clave del registro.</span><span class="sxs-lookup"><span data-stu-id="650b6-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="650b6-182">Antes de que un ejecutable use la biblioteca de depuración de DirectShow, debe llamar a la función [**DbgInitialise**](dbginitialise.md) .</span><span class="sxs-lookup"><span data-stu-id="650b6-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="650b6-183">Después, debe llamar a la función [**DbgTerminate**](dbgterminate.md) .</span><span class="sxs-lookup"><span data-stu-id="650b6-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="650b6-184">No es necesario que las DLL llamen a estas funciones, ya que el punto de entrada de DLL (definido en la biblioteca de clases base) las llama automáticamente.</span><span class="sxs-lookup"><span data-stu-id="650b6-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="650b6-185">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="650b6-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="650b6-186">Herramientas de depuración</span><span class="sxs-lookup"><span data-stu-id="650b6-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



