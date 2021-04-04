---
description: Las aplicaciones pueden administrar un contexto de activación llamando directamente a las funciones de contexto de activación.
ms.assetid: 606147a8-435d-43d4-8fb5-79d2d1a8d870
title: Uso de la API de contexto de activación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62b3aec5b7840e70e8fae93575e65c2f06668936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154092"
---
# <a name="using-the-activation-context-api"></a><span data-ttu-id="a31b7-103">Uso de la API de contexto de activación</span><span class="sxs-lookup"><span data-stu-id="a31b7-103">Using the Activation Context API</span></span>

<span data-ttu-id="a31b7-104">Las aplicaciones pueden administrar un [contexto de activación](activation-contexts.md) llamando directamente a las funciones de contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="a31b7-104">Applications can manage an [activation context](activation-contexts.md) by directly calling the activation context functions.</span></span> <span data-ttu-id="a31b7-105">Los contextos de activación son estructuras de datos en memoria.</span><span class="sxs-lookup"><span data-stu-id="a31b7-105">Activation contexts are data structures in memory.</span></span> <span data-ttu-id="a31b7-106">El sistema puede utilizar la información del contexto de activación para redirigir una aplicación para cargar una versión de DLL determinada, una instancia de objeto COM o una versión de ventana personalizada.</span><span class="sxs-lookup"><span data-stu-id="a31b7-106">The system can use the information in the activation context to redirect an application to load a particular DLL version, COM object instance, or custom window version.</span></span> <span data-ttu-id="a31b7-107">Para obtener más información, vea [referencia de contexto de activación](activation-context-reference.md).</span><span class="sxs-lookup"><span data-stu-id="a31b7-107">For more information, see [Activation Context Reference](activation-context-reference.md).</span></span>

<span data-ttu-id="a31b7-108">La interfaz de programación de aplicaciones (API) se puede usar para administrar el contexto de activación y crear objetos con nombre de versión con [manifiestos](manifests.md).</span><span class="sxs-lookup"><span data-stu-id="a31b7-108">The application programming interface (API) can be used to manage the activation context and create version-named objects with [manifests](manifests.md).</span></span> <span data-ttu-id="a31b7-109">Los dos escenarios siguientes muestran cómo una aplicación puede administrar un contexto de activación llamando directamente a las funciones de contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="a31b7-109">The following two scenarios illustrate how an application can manage an activation context by directly calling the activation context functions.</span></span> <span data-ttu-id="a31b7-110">Sin embargo, en la mayoría de los casos, el sistema administra el contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="a31b7-110">In most cases however, the activation context is managed by the system.</span></span> <span data-ttu-id="a31b7-111">Normalmente, los desarrolladores de aplicaciones y los proveedores de ensamblados no necesitan realizar llamadas a la pila para administrar el contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="a31b7-111">Application developers and assembly providers do not commonly need to make calls to the stack to manage the activation context.</span></span>

-   <span data-ttu-id="a31b7-112">Procesos y aplicaciones que implementan capas de distribución o direccionamiento indirecto.</span><span class="sxs-lookup"><span data-stu-id="a31b7-112">Processes and applications that implement indirection or dispatch layers.</span></span>

    <span data-ttu-id="a31b7-113">Por ejemplo, un usuario que administra contextos de activación en el bucle de eventos.</span><span class="sxs-lookup"><span data-stu-id="a31b7-113">For example, a user managing activation contexts in the event loop.</span></span> <span data-ttu-id="a31b7-114">Cada vez que se tiene acceso a la ventana, por ejemplo moviendo el mouse sobre la ventana, se llama a [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) , que activa el contexto de activación actual para el recurso, tal como se muestra en el siguiente fragmento de código.</span><span class="sxs-lookup"><span data-stu-id="a31b7-114">Each time the window is accessed, such as by moving the mouse over the window, [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx) is called, which activates the current activation context for the resource, as shown in the following code fragment.</span></span>

    <dl> <span data-ttu-id="a31b7-115">CONTROLAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="a31b7-115">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a31b7-116">CreateWindow ();</span><span class="sxs-lookup"><span data-stu-id="a31b7-116">CreateWindow();</span></span>  
    <span data-ttu-id="a31b7-117">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-117">...</span></span>  
    <span data-ttu-id="a31b7-118">GetCurrentActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="a31b7-118">GetCurrentActCtx(&ActCtx);</span></span>  
    <span data-ttu-id="a31b7-119">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-119">...</span></span>  
    <span data-ttu-id="a31b7-120">ReleaseActCtx (&ActCtx);</span><span class="sxs-lookup"><span data-stu-id="a31b7-120">ReleaseActCtx(&ActCtx);</span></span>  
    </dl>

    <span data-ttu-id="a31b7-121">En el fragmento de código siguiente, la función de la API activa los contextos de activación adecuados antes de llamar a [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span><span class="sxs-lookup"><span data-stu-id="a31b7-121">In the following code fragment, the API function activates the appropriate activation contexts before calling [**CallWindowProc**](/windows/win32/api/winuser/nf-winuser-callwindowproca).</span></span> <span data-ttu-id="a31b7-122">Cuando se llama a **CallWindowProc** , usa este contexto para pasar un mensaje a Windows.</span><span class="sxs-lookup"><span data-stu-id="a31b7-122">When **CallWindowProc** is called, it uses this context to pass a message to Windows.</span></span> <span data-ttu-id="a31b7-123">Cuando se hayan completado todas las operaciones de recursos, la función desactivará el contexto.</span><span class="sxs-lookup"><span data-stu-id="a31b7-123">When all resource operations have completed, the function will deactivate the context.</span></span>

    <dl> <span data-ttu-id="a31b7-124">ULONG \_ ptr ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="a31b7-124">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="a31b7-125">CONTROLAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="a31b7-125">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a31b7-126">Si (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="a31b7-126">if(ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="a31b7-127">{</span><span class="sxs-lookup"><span data-stu-id="a31b7-127">{</span></span>  
    <span data-ttu-id="a31b7-128">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-128">...</span></span>  
    <span data-ttu-id="a31b7-129">CallWindowProc(...);</span><span class="sxs-lookup"><span data-stu-id="a31b7-129">CallWindowProc(...);</span></span>  
    <span data-ttu-id="a31b7-130">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-130">...</span></span>  
    <span data-ttu-id="a31b7-131">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="a31b7-131">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="a31b7-132">}</span><span class="sxs-lookup"><span data-stu-id="a31b7-132">}</span></span>  
    </dl>

-   <span data-ttu-id="a31b7-133">Capa de distribución del delegado.</span><span class="sxs-lookup"><span data-stu-id="a31b7-133">Delegator dispatch layer.</span></span>

    <span data-ttu-id="a31b7-134">Este escenario se aplica a los administradores que administran varias entidades con un nivel de API común, como un administrador de controladores.</span><span class="sxs-lookup"><span data-stu-id="a31b7-134">This scenario applies to managers that manage multiple entities with a common API layer, such as a driver manager.</span></span> <span data-ttu-id="a31b7-135">Aunque aún no se ha implementado, un ejemplo de esto sería el controlador ODBC.</span><span class="sxs-lookup"><span data-stu-id="a31b7-135">Although it has not yet been implemented, an example of this would be the ODBC driver.</span></span>

    <span data-ttu-id="a31b7-136">En este escenario, el nivel intermedio es capaz de procesar enlaces de ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a31b7-136">In this scenario, the middle layer becomes capable of processing assembly bindings.</span></span> <span data-ttu-id="a31b7-137">Para obtener el controlador de enlace específico de la versión, los publicadores deben proporcionar un manifiesto y especificar dependencias en componentes específicos de ese manifiesto.</span><span class="sxs-lookup"><span data-stu-id="a31b7-137">To get the version-specific binding driver, publishers must provide a manifest and specify dependencies on specific components in that manifest.</span></span> <span data-ttu-id="a31b7-138">La aplicación base no se enlaza de forma dinámica a los componentes; en tiempo de ejecución, el administrador de controladores administra las llamadas.</span><span class="sxs-lookup"><span data-stu-id="a31b7-138">The base application does not dynamically bind to the components; at run time, the driver manager manages the calls.</span></span> <span data-ttu-id="a31b7-139">Cuando se llama al controlador ODBC en función de la cadena de conexión, se carga el controlador adecuado.</span><span class="sxs-lookup"><span data-stu-id="a31b7-139">When the ODBC driver is called based on the connect string it loads the appropriate driver.</span></span> <span data-ttu-id="a31b7-140">Después crea el contexto de activación con la información del archivo de manifiesto del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="a31b7-140">It then creates the activation context using the information in the assembly manifest file.</span></span>

    <span data-ttu-id="a31b7-141">Sin el manifiesto, la acción predeterminada para el controlador es usar el mismo contexto que el especificado por la aplicación, en este ejemplo, la versión 2 de MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="a31b7-141">Without the manifest, the default action for the driver is to use the same context as that specified by the application—in this example, version 2 of MSVCRT.</span></span> <span data-ttu-id="a31b7-142">Como existe un manifiesto, se establece un contexto de activación independiente.</span><span class="sxs-lookup"><span data-stu-id="a31b7-142">Since a manifest does exist, a separate activation context is established.</span></span> <span data-ttu-id="a31b7-143">Cuando se ejecuta el controlador ODBC, se enlaza a la versión 1 del ensamblado MSVCRT.</span><span class="sxs-lookup"><span data-stu-id="a31b7-143">When the ODBC driver runs, it binds to version 1 of the MSVCRT assembly.</span></span>

    <span data-ttu-id="a31b7-144">Cada vez que el administrador de controladores llama a la capa de envío (por ejemplo, para obtener el siguiente conjunto de datos), usa los ensamblados adecuados basados en el contexto de activación.</span><span class="sxs-lookup"><span data-stu-id="a31b7-144">Each time the driver manager calls the dispatch layer—for example, to get the next set of data—it uses the appropriate assemblies based on the activation context.</span></span> <span data-ttu-id="a31b7-145">En el fragmento de código siguiente se muestra esto.</span><span class="sxs-lookup"><span data-stu-id="a31b7-145">The following code fragment illustrates this.</span></span>

    <dl> <span data-ttu-id="a31b7-146">CONTROLAR hActCtx;</span><span class="sxs-lookup"><span data-stu-id="a31b7-146">HANDLE hActCtx;</span></span>  
    <span data-ttu-id="a31b7-147">ULONG \_ ptr ulpCookie;</span><span class="sxs-lookup"><span data-stu-id="a31b7-147">ULONG\_PTR ulpCookie;</span></span>  
    <span data-ttu-id="a31b7-148">ACTCTX ActCtxToCreate = {...};</span><span class="sxs-lookup"><span data-stu-id="a31b7-148">ACTCTX ActCtxToCreate = {...};</span></span>  
    <span data-ttu-id="a31b7-149">hActCtx = CreateActCtx (&ActCtxToCreate);</span><span class="sxs-lookup"><span data-stu-id="a31b7-149">hActCtx = CreateActCtx(&ActCtxToCreate);</span></span>  
    <span data-ttu-id="a31b7-150">...;</span><span class="sxs-lookup"><span data-stu-id="a31b7-150">...;</span></span>  
    <span data-ttu-id="a31b7-151">Si (ActivateActCtx (hActCtx, &ulpCookie))</span><span class="sxs-lookup"><span data-stu-id="a31b7-151">if (ActivateActCtx(hActCtx, &ulpCookie))</span></span>  
    <span data-ttu-id="a31b7-152">{</span><span class="sxs-lookup"><span data-stu-id="a31b7-152">{</span></span>  
    <span data-ttu-id="a31b7-153">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-153">...</span></span>  
    <span data-ttu-id="a31b7-154">ConnectDb(...);</span><span class="sxs-lookup"><span data-stu-id="a31b7-154">ConnectDb(...);</span></span>  
    <span data-ttu-id="a31b7-155">DeactivateActCtx (0, ulpCookie);</span><span class="sxs-lookup"><span data-stu-id="a31b7-155">DeactivateActCtx(0, ulpCookie);</span></span>  
    <span data-ttu-id="a31b7-156">}</span><span class="sxs-lookup"><span data-stu-id="a31b7-156">}</span></span>  
    <span data-ttu-id="a31b7-157">...</span><span class="sxs-lookup"><span data-stu-id="a31b7-157">...</span></span>  
    <span data-ttu-id="a31b7-158">ReleaseActCtx(hActCtx);</span><span class="sxs-lookup"><span data-stu-id="a31b7-158">ReleaseActCtx(hActCtx);</span></span>  
    </dl>

 

 
