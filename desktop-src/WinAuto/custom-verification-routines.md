---
title: Rutinas de comprobación personalizadas
description: En esta sección se describe cómo crear una rutina de comprobación personalizada para la herramienta del comprobador de accesibilidad de la interfaz de usuario (AccChecker).
ms.assetid: 56F3EA1F-39C3-4DD9-8F2B-0C3608DD8737
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d66ad2fe0e27d16b55dd2d50d367250aadd15c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994010"
---
# <a name="custom-verification-routines"></a><span data-ttu-id="5b44f-103">Rutinas de comprobación personalizadas</span><span class="sxs-lookup"><span data-stu-id="5b44f-103">Custom Verification Routines</span></span>

<span data-ttu-id="5b44f-104">En esta sección se describe cómo crear una rutina de comprobación personalizada para la herramienta del comprobador de accesibilidad de la interfaz de usuario (AccChecker).</span><span class="sxs-lookup"><span data-stu-id="5b44f-104">This section describes how to create a custom verification routine for the UI Accessibility Checker (AccChecker) tool.</span></span>

-   [<span data-ttu-id="5b44f-105">Creación de una comprobación personalizada</span><span class="sxs-lookup"><span data-stu-id="5b44f-105">Creating a Custom Verification</span></span>](#creating-a-custom-verification)
    -   [<span data-ttu-id="5b44f-106">Comprobación personalizada de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b44f-106">Sample Custom Verification</span></span>](#sample-custom-verification)
-   [<span data-ttu-id="5b44f-107">Uso de una comprobación personalizada</span><span class="sxs-lookup"><span data-stu-id="5b44f-107">Using a Custom Verification</span></span>](#using-a-custom-verification)
    -   [<span data-ttu-id="5b44f-108">La interfaz gráfica de usuario (GUI) de AccChecker</span><span class="sxs-lookup"><span data-stu-id="5b44f-108">The AccChecker Graphical User Interface (GUI)</span></span>](#the-accchecker-graphical-user-interface-gui)
    -   [<span data-ttu-id="5b44f-109">Automatización de AccChecker</span><span class="sxs-lookup"><span data-stu-id="5b44f-109">AccChecker Automation</span></span>](#accchecker-automation)
-   [<span data-ttu-id="5b44f-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b44f-110">Related topics</span></span>](#related-topics)

<span data-ttu-id="5b44f-111">El comprobador de accesibilidad de la interfaz de usuario (AccChecker) es una herramienta de prueba de accesibilidad diseñada para comprobar la implementación de Microsoft Active Accessibility (MSAA) en una interfaz de usuario de una aplicación o un control.</span><span class="sxs-lookup"><span data-stu-id="5b44f-111">UI Accessibility Checker (AccChecker) is an accessibility test tool designed to verify the implementation of Microsoft Active Accessibility (MSAA) in a control or application UI.</span></span> <span data-ttu-id="5b44f-112">Los problemas de accesibilidad de gran impacto que podrían estar expuestos por la implementación de MSAA se prueban con un conjunto de rutinas de comprobación automatizadas integradas.</span><span class="sxs-lookup"><span data-stu-id="5b44f-112">High impact accessibility issues that might be exposed by the MSAA implementation are tested with a set of built-in automated verification routines.</span></span> <span data-ttu-id="5b44f-113">Estas rutinas de verificación nativas se pueden aumentar con rutinas personalizadas mediante la plataforma extensible AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-113">These native verification routines can be augmented with customized routines using the extensible AccChecker platform.</span></span>

## <a name="creating-a-custom-verification"></a><span data-ttu-id="5b44f-114">Creación de una comprobación personalizada</span><span class="sxs-lookup"><span data-stu-id="5b44f-114">Creating a Custom Verification</span></span>

<span data-ttu-id="5b44f-115">Una comprobación personalizada se genera como una biblioteca de clases (DLL) que implementa una interfaz única ( `IVerificationRoutine` ) que contiene un miembro ( `Execute` ):</span><span class="sxs-lookup"><span data-stu-id="5b44f-115">A custom verification is built as a class library (DLL) that implements a single interface (`IVerificationRoutine`) containing one member (`Execute`):</span></span>


```CSharp
void Execute(
    System.IntPtr hwnd, 
    AccCheck.Logging.ILogger logger, 
    bool AllowUI, 
    AccCheck.GraphicsHelper graphics
);
```



<span data-ttu-id="5b44f-116">**Parámetros**</span><span class="sxs-lookup"><span data-stu-id="5b44f-116">**Parameters**</span></span>

<span data-ttu-id="5b44f-117">*identificador*</span><span class="sxs-lookup"><span data-stu-id="5b44f-117">*hwnd*</span></span>

<span data-ttu-id="5b44f-118">Tipo: **System. IntPtr**</span><span class="sxs-lookup"><span data-stu-id="5b44f-118">Type: **System.IntPtr**</span></span>

<span data-ttu-id="5b44f-119">HWND del elemento que se está comprobando.</span><span class="sxs-lookup"><span data-stu-id="5b44f-119">The HWND of the element being verified.</span></span>

<span data-ttu-id="5b44f-120">*registrador*</span><span class="sxs-lookup"><span data-stu-id="5b44f-120">*logger*</span></span>

<span data-ttu-id="5b44f-121">Tipo: **AccCheck. Logging. ILogger**</span><span class="sxs-lookup"><span data-stu-id="5b44f-121">Type: **AccCheck.Logging.ILogger**</span></span>

<span data-ttu-id="5b44f-122">Método de registro seleccionado.</span><span class="sxs-lookup"><span data-stu-id="5b44f-122">The selected logging method.</span></span> <span data-ttu-id="5b44f-123">Entre los posibles tipos se incluyen **AccumulatingLogger** (usado por AccChecker para almacenar en caché todas las entradas del registro hasta que se completen las comprobaciones), **ConsoleLogger**, **TextFileLogger** y **XMLSerializingLogger**.</span><span class="sxs-lookup"><span data-stu-id="5b44f-123">Possible types include **AccumulatingLogger** (used by AccChecker to cache all log entries until verifications are complete), **ConsoleLogger**, **TextFileLogger**, and **XMLSerializingLogger**.</span></span>

<span data-ttu-id="5b44f-124">*AllowUI*</span><span class="sxs-lookup"><span data-stu-id="5b44f-124">*AllowUI*</span></span>

<span data-ttu-id="5b44f-125">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="5b44f-125">Type: **bool**</span></span>

<span data-ttu-id="5b44f-126">Indica si la rutina de comprobación muestra la interfaz de usuario que está probando.</span><span class="sxs-lookup"><span data-stu-id="5b44f-126">Indicates whether the verification routine displays the UI it is testing.</span></span> <span data-ttu-id="5b44f-127">Normalmente, se establece en false en escenarios de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="5b44f-127">Generally set to false in automated testing scenarios.</span></span>

<span data-ttu-id="5b44f-128">*tarjetas*</span><span class="sxs-lookup"><span data-stu-id="5b44f-128">*graphics*</span></span>

<span data-ttu-id="5b44f-129">Tipo: **AccCheck. GraphicsHelper**</span><span class="sxs-lookup"><span data-stu-id="5b44f-129">Type: **AccCheck.GraphicsHelper**</span></span>

<span data-ttu-id="5b44f-130">Se usa para capturas de pantallas y otras visualizaciones dentro de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-130">Used for screenshots and other visualizations within AccChecker.</span></span>

### <a name="sample-custom-verification"></a><span data-ttu-id="5b44f-131">Comprobación personalizada de ejemplo</span><span class="sxs-lookup"><span data-stu-id="5b44f-131">Sample Custom Verification</span></span>

<span data-ttu-id="5b44f-132">El ejemplo siguiente es una comprobación personalizada de C# que realiza una comprobación de profundidad del árbol de elementos simple.</span><span class="sxs-lookup"><span data-stu-id="5b44f-132">The following example is a C# custom verification that performs a simple element tree depth check.</span></span> <span data-ttu-id="5b44f-133">Se registra un error si el árbol de elementos tiene más de 50 niveles de profundidad, se registra una advertencia si el árbol de elementos tiene entre 20 y 50 niveles de profundidad y se registra un mensaje informativo en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5b44f-133">An error is logged if the element tree is greater than 50 levels deep, a warning is logged if the element tree is 20 to 50 levels deep, and an informational message is logged otherwise.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Text;
using AccCheck;
using AccCheck.Logging;
using AccCheck.Verification;

namespace VerificationRoutines
{
    \\ Verification routine attributes.
    \\ If these values are not specified, the verification will not be displayed in the 
    \\ AccChecker UI. However, it is still loaded and will be included in all subsequent 
    \\ verification runs since it cannot be unchecked and excluded.
    [Verification(
        // Title - the title of the verification routine.
        "Sample Check Tree Depth",
        // Description - this attribute is not currently displayed.
        "Checks that the accessibility tree isn't excessively deep.",
        // Group Title - the verification group to add the routine. This can be a new or 
        //  existing group.
        Group = "TreeDepthCheck"
        )]

    public class CheckTreeDepth : IVerificationRoutine
    {
        private const int S_OK = 0;
        private const int ERROR_TREE_DEPTH = 50;
        private const int WARNING_TREE_DEPTH = 20;
        private int _depth = 0;

        private void TraverseTree(Accessible parent, int level)
        {
            if (level > _depth)
            {
                _depth = level;
            }

            // never go deeper than ERROR_TREE_DEPTH, that's a sign of a loop
            if (_depth > ERROR_TREE_DEPTH)
            {
                return;
            }

            Accessible[] children;
            if (parent.Children(out children) == S_OK)
            {
                foreach (Accessible child in children)
                {
                    TraverseTree(child, level + 1);
                }
            }
        }

        public void Execute(IntPtr hwnd, ILogger logger, bool AllowUI, 
                GraphicsHelper graphics)
        {
            Accessible root;
            if (Accessible.FromWindow(hwnd, out root) == S_OK)
            {
                TraverseTree(root, 0);
            }
            else
            {
                return;
            }

            if (_depth >= ERROR_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Error, "DepthCheck", String.Format(
                    "The tree is too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else if (_depth >= WARNING_TREE_DEPTH)
            {
                logger.Log(new LogEvent(EventLevel.Warning, "DepthCheck", String.Format(
                    "The tree might be too deep; the tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
            else
            {
                logger.Log(new LogEvent(EventLevel.Information, "DepthCheck", String.Format(
                    "The tree is {0} levels deep", _depth), "", 
                    System.Drawing.Rectangle.Empty, this.GetType()));
            }
        }
    }
}
```



> [!Note]  
> <span data-ttu-id="5b44f-134">La documentación de ayuda incluye una solución Microsoft Visual Studio que contiene el código de ejemplo de comprobación.</span><span class="sxs-lookup"><span data-stu-id="5b44f-134">A Microsoft Visual Studio solution that contains verification sample code is included with the help documentation.</span></span> <span data-ttu-id="5b44f-135">Los archivos se encuentran en la ruta de instalación de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-135">The files are located in the AccChecker installation path.</span></span>

 

## <a name="using-a-custom-verification"></a><span data-ttu-id="5b44f-136">Uso de una comprobación personalizada</span><span class="sxs-lookup"><span data-stu-id="5b44f-136">Using a Custom Verification</span></span>

<span data-ttu-id="5b44f-137">En esta sección se describe cómo incorporar una comprobación personalizada en escenarios de prueba de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-137">This section describes how to incorporate a custom verification into AccChecker test scenarios.</span></span>

### <a name="the-accchecker-graphical-user-interface-gui"></a><span data-ttu-id="5b44f-138">La interfaz gráfica de usuario (GUI) de AccChecker</span><span class="sxs-lookup"><span data-stu-id="5b44f-138">The AccChecker Graphical User Interface (GUI)</span></span>

<span data-ttu-id="5b44f-139">Para incluir una rutina de comprobación personalizada en la aplicación AccChecker, simplemente haga clic en abrir DLL en el menú Archivo y busque el archivo DLL de la rutina.</span><span class="sxs-lookup"><span data-stu-id="5b44f-139">To include a custom verification routine in the AccChecker application, simply click Open DLL from the File menu and locate the DLL for the routine.</span></span> <span data-ttu-id="5b44f-140">La rutina personalizada se agregará a la parte inferior de la lista de comprobaciones en el panel Seleccionar rutinas de comprobación.</span><span class="sxs-lookup"><span data-stu-id="5b44f-140">The custom routine will be added to the bottom of the list of verifications in the Select verification routines pane.</span></span>

<span data-ttu-id="5b44f-141">En la captura de pantalla siguiente se muestra la comprobación personalizada de profundidad de árbol de comprobación de ejemplo agregada a AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-141">The following screen shot shows the Sample Check Tree Depth custom verification added to AccChecker.</span></span>

![ejemplo de rutina de comprobación personalizada de profundidad de árbol de comprobación agregada a la interfaz de usuario de accchecker](images/accchecker-sample-custom-verification.png)

> [!Note]  
> <span data-ttu-id="5b44f-143">Si los valores de atributo de comprobación no se especifican en la rutina de comprobación personalizada, la comprobación se seguirá cargando en AccChecker aunque no aparezca en la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="5b44f-143">If the verification attribute values are not specified in the custom verification routine, the verification is still loaded into AccChecker even though it does not appear in the UI.</span></span> <span data-ttu-id="5b44f-144">Puesto que no se muestra en la interfaz de usuario, no se puede desactivar y excluir de las ejecuciones de comprobación posteriores.</span><span class="sxs-lookup"><span data-stu-id="5b44f-144">Since it is not displayed in the UI, it cannot be unchecked and excluded from subsequent verification runs.</span></span>

 

### <a name="accchecker-automation"></a><span data-ttu-id="5b44f-145">Automatización de AccChecker</span><span class="sxs-lookup"><span data-stu-id="5b44f-145">AccChecker Automation</span></span>

<span data-ttu-id="5b44f-146">Incorporar una rutina de comprobación personalizada en un marco de AccChecker automatizado es tan sencillo como agregar el archivo DLL de comprobación y habilitar las rutinas de comprobación deseadas.</span><span class="sxs-lookup"><span data-stu-id="5b44f-146">Incorporating a custom verification routine into an automated AccChecker framework is as simple as adding the verification DLL and enabling the desired verification routines.</span></span>

<span data-ttu-id="5b44f-147">En el fragmento de código siguiente se muestra cómo usar la API AccChecker para probar la funcionalidad de tabulación en la aplicación del panel de control de Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="5b44f-147">The following code snippet demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


```CSharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using AccCheck.Logging;

public class TestCases : TestBase
{
    public void AccessibilityTestCase()
    {
        //  Get our user interface ready for AccChecker.
        Setup();

        //  AccChecker's class representing verifications that you can run.
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();

        //  Create a console logger to get output in the console.
        ConsoleLogger consoleLogger = new ConsoleLogger();

        //  Add the AccChecker Console Logger.
        vm.AddLogger(consoleLogger);

        //  Disable all verifications; all verifications are enabled by default.
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);

        // Add a custom verification DLL.
        vm.AddVerificationDll("CheckTreeDepthVerification.dll");
        
        // Enable the routine we want to run.
        vm.EnableRoutine("Sample Check Tree Depth");

        //  Run the verification routine against the firewall.
        vm.ExecuteEnabled(_fireWallHwnd);

        //  Check the logger to see if the verification failed.
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }

        // Clean up the user interface.
        Cleanup();
    }
}
```



> [!Note]  
> La documentación de ayuda incluye una solución Microsoft Visual Studio 2008 que contiene el código de ejemplo de comprobación. <span data-ttu-id="5b44f-149">Los archivos se encuentran en la ruta de instalación de AccChecker.</span><span class="sxs-lookup"><span data-stu-id="5b44f-149">The files are located in the AccChecker installation path.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b44f-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b44f-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b44f-151">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="5b44f-151">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




