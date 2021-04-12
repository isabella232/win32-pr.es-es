---
description: El uso del entorno de desarrollo integrado (IDE) de Microsoft Visual Basic para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso.
ms.assetid: d31efc97-c286-434d-93f5-77b34ec16205
title: Depuración en el IDE de Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74574fdb289e1ad334337f17943c6961b95bf288
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423271"
---
# <a name="debugging-in-the-visual-basic-ide"></a><span data-ttu-id="5aa83-103">Depuración en el IDE de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5aa83-103">Debugging in the Visual Basic IDE</span></span>

<span data-ttu-id="5aa83-104">El uso del entorno de desarrollo integrado (IDE) de Microsoft Visual Basic para la depuración proporciona a los desarrolladores de Visual Basic acceso a herramientas conocidas y facilidad de uso.</span><span class="sxs-lookup"><span data-stu-id="5aa83-104">Using the Microsoft Visual Basic integrated development environment (IDE) for debugging gives Visual Basic developers access to familiar tools and ease-of-use.</span></span> <span data-ttu-id="5aa83-105">Aunque es posible que sea necesario depurar muchos componentes por completo con el entorno de Microsoft Visual C++, una estrategia podría ser primero depurar tanta funcionalidad como sea posible con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5aa83-105">While many components will eventually need to be more fully debugged using the Microsoft Visual C++ environment, one strategy might be to first debug as much functionality as possible with Visual Basic.</span></span> <span data-ttu-id="5aa83-106">Por ejemplo, es posible que desee usar el IDE de Visual Basic para la depuración en COM+ cuando aún no esté depurando multithreading, seguimiento de componentes, llamadas remotas o aislamiento de procesos.</span><span class="sxs-lookup"><span data-stu-id="5aa83-106">For example, you might want to use the Visual Basic IDE for debugging within COM+ when you aren't yet debugging multithreading, component tracking, remote calls, or process isolation.</span></span>

<span data-ttu-id="5aa83-107">En general, cuando se usa el entorno de Visual Basic para la depuración, primero se compila el proyecto y se agrega el archivo DLL a una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="5aa83-107">In general, when using the Visual Basic environment for debugging, you first compile the project and add the DLL to a COM+ application.</span></span> <span data-ttu-id="5aa83-108">A continuación, establezca la compatibilidad binaria para el proyecto, haciendo referencia al archivo DLL que ha creado e inicie el proyecto para comenzar la depuración.</span><span class="sxs-lookup"><span data-stu-id="5aa83-108">Then you set binary compatibility for the project, referencing the DLL you made, and start the project to begin debugging.</span></span>

## <a name="general-guidelines-for-debugging-in-the-visual-basic-environment"></a><span data-ttu-id="5aa83-109">Directrices generales para la depuración en el entorno de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5aa83-109">General Guidelines for Debugging in the Visual Basic Environment</span></span>

-   <span data-ttu-id="5aa83-110">Durante la depuración mediante Visual Basic, COM+ trata los componentes de Visual Basic como si pertenecieran a una aplicación de biblioteca, incluso si los componentes se registran como pertenecientes a una aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="5aa83-110">While you are debugging using Visual Basic, COM+ treats the Visual Basic components as if they belong to a library application, even if the components are registered as belonging to a server application.</span></span> <span data-ttu-id="5aa83-111">Dado que se ejecuta como una aplicación de biblioteca, los iconos de componente de la herramienta administrativa Servicios de componentes no giran cuando se depuran los componentes.</span><span class="sxs-lookup"><span data-stu-id="5aa83-111">Because it runs as a library application, the component icons in the Component Services administrative tool do not spin as the components are debugged.</span></span>
-   <span data-ttu-id="5aa83-112">Si cambia atributos de transacción en un componente durante la depuración o realiza un cambio en el código fuente que requiere Visual Basic para generar un nuevo CLSID o ProgID, asegúrese de eliminar y volver a instalar la aplicación COM+ que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="5aa83-112">If you change transaction attributes on a component during debugging or make a source code change that requires Visual Basic to generate a new CLSID or ProgID, be sure to delete and reinstall the COM+ application containing the component.</span></span> <span data-ttu-id="5aa83-113">Si ha establecido la compatibilidad binaria para el componente, se le advertirá de que se han producido cambios.</span><span class="sxs-lookup"><span data-stu-id="5aa83-113">If you have set binary compatibility for the component, you will be warned that changes have occurred.</span></span>

## <a name="notes-on-debugging-within-a-com-application"></a><span data-ttu-id="5aa83-114">Notas sobre la depuración en una aplicación COM+</span><span class="sxs-lookup"><span data-stu-id="5aa83-114">Notes on Debugging Within a COM+ Application</span></span>

-   <span data-ttu-id="5aa83-115">Si realiza cambios en el IDE de Visual Basic en las interfaces del componente, los nombres de clase, los nombres de proyecto, la compatibilidad transaccional u otra configuración, puede que haya discrepancias entre los datos de configuración en el explorador de servicios de componentes y la configuración real que se ejecuta en el depurador de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5aa83-115">If you make changes in the Visual Basic IDE in your component's interfaces, class names, project names, transactional support or other settings, there may be mismatches between the configuration data in the Component Services explorer and the actual configuration running in the Visual Basic debugger.</span></span>
-   <span data-ttu-id="5aa83-116">No exporte una aplicación COM+ mientras depura un componente en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5aa83-116">Do not export a COM+ application while you are debugging a component in the application.</span></span> <span data-ttu-id="5aa83-117">COM+ tratará el entorno de desarrollo de Visual Basic como componente.</span><span class="sxs-lookup"><span data-stu-id="5aa83-117">COM+ will treat the Visual Basic development environment as the component.</span></span>
-   <span data-ttu-id="5aa83-118">Si está ejecutando un componente fuera del depurador y, a continuación, decide iniciar la depuración, es posible que una instancia del componente siga ejecutándose en COM+ al iniciarlo en el depurador.</span><span class="sxs-lookup"><span data-stu-id="5aa83-118">If you are running a component outside the debugger and then decide to begin debugging, an instance of the component may still be running in COM+ when you start it in the debugger.</span></span> <span data-ttu-id="5aa83-119">COM+ detectará esta condición e intentará apagar de forma silenciosa la instancia que controla.</span><span class="sxs-lookup"><span data-stu-id="5aa83-119">COM+ will detect this condition and attempt to silently shut down the instance it controls.</span></span> <span data-ttu-id="5aa83-120">Para evitar este problema, quite el componente de la herramienta administrativa Servicios de componentes antes de comenzar la depuración.</span><span class="sxs-lookup"><span data-stu-id="5aa83-120">To avoid this problem, remove the component from the Component Services administrative tool before you begin debugging.</span></span>

<span data-ttu-id="5aa83-121">**Para depurar mediante el entorno de Visual Basic**</span><span class="sxs-lookup"><span data-stu-id="5aa83-121">**To debug using the Visual Basic environment**</span></span>

1.  <span data-ttu-id="5aa83-122">Abra el proyecto de componente en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5aa83-122">Open the component project in Visual Basic.</span></span>

2.  <span data-ttu-id="5aa83-123">Compile el componente y, a continuación, establezca la compatibilidad binaria en el proyecto con el componente compilado.</span><span class="sxs-lookup"><span data-stu-id="5aa83-123">Compile your component, and then set binary compatibility in your project to the compiled component.</span></span>

3.  <span data-ttu-id="5aa83-124">Establezca la propiedad MTSTransactionMode en un valor distinto de 0-NotAnMTSObject.</span><span class="sxs-lookup"><span data-stu-id="5aa83-124">Set the MTSTransactionMode property to a value other than 0 - NotAnMTSObject.</span></span> <span data-ttu-id="5aa83-125">Al iniciar el proyecto, esta configuración solicita Visual Basic para activar el componente dentro de COM+.</span><span class="sxs-lookup"><span data-stu-id="5aa83-125">When you start the project, this setting prompts Visual Basic to activate your component within COM+.</span></span>

4.  <span data-ttu-id="5aa83-126">En el menú **proyecto** , haga clic en **propiedades** y, a continuación, escriba el programa de inicio en la pestaña **depuración** . El programa de inicio es el ejecutable de cliente que llama a este componente.</span><span class="sxs-lookup"><span data-stu-id="5aa83-126">From the **Project** menu, click **Properties**, and then enter the start program on the **Debugging** tab. The start program is the client executable that calls this component.</span></span>

    > [!Note]  
    > <span data-ttu-id="5aa83-127">El programa de inicio debe ser local para el componente que está depurando.</span><span class="sxs-lookup"><span data-stu-id="5aa83-127">The start program must be local to the component you are debugging.</span></span>

     

5.  <span data-ttu-id="5aa83-128">Presione la tecla F5 para empezar a depurar el componente.</span><span class="sxs-lookup"><span data-stu-id="5aa83-128">Press the F5 key to begin debugging the component.</span></span>

<span data-ttu-id="5aa83-129">Después de presionar F5, Visual Basic inicia la aplicación cliente y ejecuta el componente en modo de depuración.</span><span class="sxs-lookup"><span data-stu-id="5aa83-129">After you press F5, Visual Basic launches the client application and runs the component in debug mode.</span></span> <span data-ttu-id="5aa83-130">Puede colocar puntos de interrupción en el código del componente y establecer inspecciones en las variables.</span><span class="sxs-lookup"><span data-stu-id="5aa83-130">You can place breakpoints in the component's code and set watches on variables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa83-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5aa83-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa83-132">Compatibilidad con la depuración de Visual Basic COM+ en contraste con MTS</span><span class="sxs-lookup"><span data-stu-id="5aa83-132">COM+ Visual Basic Debugging Support Contrasted with MTS</span></span>](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[<span data-ttu-id="5aa83-133">Depurar componentes Visual Basic compilados</span><span class="sxs-lookup"><span data-stu-id="5aa83-133">Debugging Compiled Visual Basic Components</span></span>](debugging-compiled-visual-basic-components.md)
</dt> </dl>

 

 



