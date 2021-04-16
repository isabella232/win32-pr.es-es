---
title: Biblioteca de pruebas de automatización de la interfaz de usuario
description: La biblioteca de pruebas de automatización de la interfaz de usuario (biblioteca de pruebas de UIA) es una API a la que llama la aplicación del controlador en un escenario de pruebas automatizadas.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e64200673d45f800e1e18dee2afd5c4acd2b604f
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104557633"
---
# <a name="ui-automation-test-library"></a><span data-ttu-id="af4c5-103">Biblioteca de pruebas de automatización de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="af4c5-103">UI Automation Test Library</span></span>

<span data-ttu-id="af4c5-104">La biblioteca de pruebas de automatización de la interfaz de usuario (biblioteca de pruebas de UIA) es una API a la que llama la aplicación del *controlador* en un escenario de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="af4c5-104">The UI Automation Test Library (UIA Test Library) is an API that is called by the *driver* application in an automated testing scenario.</span></span> <span data-ttu-id="af4c5-105">El controlador es la aplicación que obtiene un elemento de automatización (objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) de un control que requiere comprobación y lo proporciona a la biblioteca de pruebas de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="af4c5-105">The driver is the application that obtains an automation element ([**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from a control that requires verification, and provides it to the UI Automation Test Library.</span></span> <span data-ttu-id="af4c5-106">A continuación, la biblioteca de prueba comprueba y valida la implementación de la automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="af4c5-106">Then, the test library checks and validates the UI Automation implementation.</span></span> <span data-ttu-id="af4c5-107">Para obtener más información sobre la automatización de la interfaz de usuario y los elementos de automatización, vea [fundamentos de UI Automation](entry-uiautocore-overview.md).</span><span class="sxs-lookup"><span data-stu-id="af4c5-107">To learn more about UI Automation and automation elements, see [UI Automation Fundamentals](entry-uiautocore-overview.md).</span></span>

-   [<span data-ttu-id="af4c5-108">Flujo de trabajo de biblioteca de pruebas de UI Automation</span><span class="sxs-lookup"><span data-stu-id="af4c5-108">UI Automation Test Library Workflow</span></span>](#ui-automation-test-library-workflow)
-   [<span data-ttu-id="af4c5-109">Registro con la biblioteca de pruebas de UI Automation</span><span class="sxs-lookup"><span data-stu-id="af4c5-109">Logging with the UI Automation Test Library</span></span>](#logging-with-the-ui-automation-test-library)
    -   [<span data-ttu-id="af4c5-110">Registro XML</span><span class="sxs-lookup"><span data-stu-id="af4c5-110">XML Logging</span></span>](#xml-logging)
    -   [<span data-ttu-id="af4c5-111">Registro de la consola</span><span class="sxs-lookup"><span data-stu-id="af4c5-111">Console Logging</span></span>](#console-logging)
    -   [<span data-ttu-id="af4c5-112">Requisitos de código para el registro</span><span class="sxs-lookup"><span data-stu-id="af4c5-112">Code Requirements for Logging</span></span>](#code-requirements-for-logging)
    -   [<span data-ttu-id="af4c5-113">Ejemplos de registro</span><span class="sxs-lookup"><span data-stu-id="af4c5-113">Logging Examples</span></span>](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a><span data-ttu-id="af4c5-114">Flujo de trabajo de biblioteca de pruebas de UI Automation</span><span class="sxs-lookup"><span data-stu-id="af4c5-114">UI Automation Test Library Workflow</span></span>

<span data-ttu-id="af4c5-115">En el diagrama siguiente se muestra un flujo de trabajo de prueba que incorpora la biblioteca de pruebas de automatización de la interfaz de usuario mediante el uso de una aplicación de consola como controlador.</span><span class="sxs-lookup"><span data-stu-id="af4c5-115">The following diagram shows a test workflow that incorporates the UI Automation Test Library by using a console application as the driver.</span></span> <span data-ttu-id="af4c5-116">En este caso, el controlador inicia una instancia de Notepad.exe y obtiene un elemento de automatización (es decir, un objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) del control de edición.</span><span class="sxs-lookup"><span data-stu-id="af4c5-116">In this case, the driver starts an instance of Notepad.exe and obtains an automation element (that is, a [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) object) from the edit control.</span></span> <span data-ttu-id="af4c5-117">A continuación, el controlador crea un objeto de biblioteca de pruebas de automatización de la interfaz de usuario basado en la plataforma de interfaz de usuario que se prueba y, a continuación, pasa el elemento de automatización como un parámetro.</span><span class="sxs-lookup"><span data-stu-id="af4c5-117">Next, the driver creates a UI Automation Test Library object based on the UI platform being tested, and then passes in the automation element as a parameter.</span></span> <span data-ttu-id="af4c5-118">La biblioteca de pruebas de automatización de la interfaz de usuario determina que el elemento de automatización es un tipo de control de [documento](uiauto-supportdocumentcontroltype.md) y, a continuación, ejecuta las pruebas de control de documento, las pruebas de patrón de control de [texto](uiauto-implementingtextandtextrange.md) y [desplazamiento](uiauto-implementingscroll.md) , y las pruebas de elementos de automatización genéricas.</span><span class="sxs-lookup"><span data-stu-id="af4c5-118">The UI Automation Test Library determines that the automation element is a [Document](uiauto-supportdocumentcontroltype.md) control type, and then executes the Document control tests, the [Text](uiauto-implementingtextandtextrange.md) and [Scroll](uiauto-implementingscroll.md) control pattern tests, and generic automation element tests.</span></span>

![Diagrama que muestra el flujo de la aplicación al controlador a UIATestLibrary con flechas rojas.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a><span data-ttu-id="af4c5-120">Registro con la biblioteca de pruebas de UI Automation</span><span class="sxs-lookup"><span data-stu-id="af4c5-120">Logging with the UI Automation Test Library</span></span>

<span data-ttu-id="af4c5-121">La biblioteca de pruebas de automatización de la interfaz de usuario usa archivos dll externos para registrar los resultados de las series de pruebas.</span><span class="sxs-lookup"><span data-stu-id="af4c5-121">The UI Automation Test Library uses external DLLs to log results from test runs.</span></span> <span data-ttu-id="af4c5-122">Admite el registro como XML y el registro en la consola.</span><span class="sxs-lookup"><span data-stu-id="af4c5-122">It supports logging as XML and logging to the console.</span></span>

### <a name="xml-logging"></a><span data-ttu-id="af4c5-123">Registro XML</span><span class="sxs-lookup"><span data-stu-id="af4c5-123">XML Logging</span></span>

<span data-ttu-id="af4c5-124">El registro XML se usa normalmente en la comprobación de la automatización de la interfaz de usuario de Visual, pero también se puede incorporar a un flujo de trabajo de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="af4c5-124">XML logging is typically used by Visual UI Automation Verify, but it can also be incorporated into a command-line workflow.</span></span>

<span data-ttu-id="af4c5-125">Si se especifica el registro XML, la aplicación de controlador debe serializar la salida mediante la creación de un objeto **XmlWriter** y pasarlo al método **XmlLog. GetTestRunXml** .</span><span class="sxs-lookup"><span data-stu-id="af4c5-125">If XML logging is specified, the driver application must serialize the output by creating an **XmlWriter** object and passing it to the **XmlLog.GetTestRunXml** method.</span></span> <span data-ttu-id="af4c5-126">Después, el controlador puede utilizar el XML serializado internamente o escribirlo en un archivo.</span><span class="sxs-lookup"><span data-stu-id="af4c5-126">The driver can then use the serialized XML internally or write it to a file.</span></span>

<span data-ttu-id="af4c5-127">Los siguientes archivos dll son necesarios para el registro de XML.</span><span class="sxs-lookup"><span data-stu-id="af4c5-127">The following DLLs are required for XML logging.</span></span>

-   <span data-ttu-id="af4c5-128">WUIALogging.dll</span><span class="sxs-lookup"><span data-stu-id="af4c5-128">WUIALogging.dll</span></span>
-   <span data-ttu-id="af4c5-129">WUIALoggerXml.dll</span><span class="sxs-lookup"><span data-stu-id="af4c5-129">WUIALoggerXml.dll</span></span>

### <a name="console-logging"></a><span data-ttu-id="af4c5-130">Registro de la consola</span><span class="sxs-lookup"><span data-stu-id="af4c5-130">Console Logging</span></span>

<span data-ttu-id="af4c5-131">De forma predeterminada, la biblioteca de pruebas de automatización de la interfaz de usuario usa el registro de la consola, donde todos los resultados del registro se canalizan como texto sin formato a la ventana de la consola.</span><span class="sxs-lookup"><span data-stu-id="af4c5-131">By default, the UI Automation Test Library uses console logging, where all logging output is piped as plain text to the console window.</span></span> <span data-ttu-id="af4c5-132">WUIALogging.dll es necesario para el registro de la consola.</span><span class="sxs-lookup"><span data-stu-id="af4c5-132">WUIALogging.dll is required for console logging.</span></span>

### <a name="code-requirements-for-logging"></a><span data-ttu-id="af4c5-133">Requisitos de código para el registro</span><span class="sxs-lookup"><span data-stu-id="af4c5-133">Code Requirements for Logging</span></span>

<span data-ttu-id="af4c5-134">Una aplicación de controlador debe incluir los siguientes fragmentos de código para usar el registro de la biblioteca de pruebas de automatización de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="af4c5-134">A driver application must include the following code snippets to use UI Automation Test Library logging.</span></span>


```CSharp
\\ Include logging functionality.
using Microsoft.Test.UIAutomation.Logging;

...

\\ Select a logger.
UIAVerifyLogger.SetLoggerType(LogTypes.DefaultLogger | 
                              LogTypes.ConsoleLogger | 
                              LogTypes.XmlLogger);

...

\\ Output comment to selected logger.
UIAVerifyLogger.LogComment("...");
```



### <a name="logging-examples"></a><span data-ttu-id="af4c5-135">Ejemplos de registro</span><span class="sxs-lookup"><span data-stu-id="af4c5-135">Logging Examples</span></span>

<span data-ttu-id="af4c5-136">En los siguientes ejemplos se muestra la funcionalidad básica de registro y se muestra cómo usar la API de la biblioteca de pruebas de automatización de la interfaz de usuario en una aplicación básica de controlador de automatización de prueba.</span><span class="sxs-lookup"><span data-stu-id="af4c5-136">The following examples demonstrate basic logging functionality and show how to use the UI Automation Test Library API in a basic test automation driver application.</span></span>


```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample logger.
//
//---------------------------------------------------------------------------
using System;

namespace WUITest
{
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {
        private TestMain() { }

        /// -----------------------------------------------------------------
        /// <summary>
        /// Entry point
        /// </summary>
        /// -----------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Call SetLogger() if you don't want to use the default logger.
            // To set the logger type, call SetLogger(<string>).
            // <string> can be specified from the command line or from the 
            // the UI Automation Test Library enumeration:
            //  
            //     Logger.SetLogger(LogTypes.ConsoleLogger);
            //     Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.SetLogger(LogTypes.DefaultLogger);

            Logger.StartTest("Test 1");
            Logger.LogComment("This is a comment");
            Logger.LogError(new Exception("My error"), false);
            Logger.EndTest();

            Logger.StartTest("Test 2");
            Logger.LogComment("This is a second comment");
            Logger.LogPass();
            Logger.EndTest();

            Logger.ReportResults();

        }
    }
}
```




```CSharp
//---------------------------------------------------------------------------
//
// Description: Sample test automation.
//
//---------------------------------------------------------------------------

using System;
using System.Windows;

namespace WUITest
{
    using System.Diagnostics;
    using System.Threading;
    using System.Windows.Automation;
    using Microsoft.Test.UIAutomation;
    using Microsoft.Test.UIAutomation.Core;
    using Microsoft.Test.UIAutomation.TestManager;
    using Microsoft.Test.UIAutomation.Tests.Controls;
    using Microsoft.Test.UIAutomation.Tests.Patterns;
    using Microsoft.Test.UIAutomation.Tests.Scenarios;
    using Microsoft.Test.UIAutomation.Logging;

    public sealed class TestMain
    {

        // Time in milliseconds to wait for the application to start.
        static int MAXTIME = 5000;
        // Time in milliseconds to wait before trying to find the application.
        static int TIMEWAIT = 100; 

        /// -------------------------------------------------------------------
        /// <summary>
        /// Start Notepad, obtain an AutomationElement object, and run tests.
        /// </summary>
        /// -------------------------------------------------------------------
        [STAThread]
        static void Main(string[] args)
        {
            // Dump the information to the console window.  
            // Use a different LogTypes value if you need to dump to another logger, 
            // or create your own logger that complies with the interface.
            UIAVerifyLogger.SetLoggerType(LogTypes.ConsoleLogger);

            // Get the automation element.
            AutomationElement element = StartApplication("NOTEPAD.EXE", null);

            // Call the UI Automation Test Library tests.
            TestRuns.RunAllTests(element, true, TestPriorities.Pri0, 
                    TestCaseType.Generic, false, true, null);

            // Clean up.
            ((WindowPattern)element.GetCurrentPattern(WindowPattern.Pattern)).Close();

            // Dump the summary of results.
            UIAVerifyLogger.ReportResults();
        }

        /// -------------------------------------------------------------------------
        /// <summary>
        /// Start the application and retrieve its AutomationElement. 
        /// </summary>
        /// -------------------------------------------------------------------------
        static public AutomationElement StartApplication(string appPath, 
                string arguments)
        {
            Process process;

            Library.ValidateArgumentNonNull(appPath, "appPath");

            ProcessStartInfo psi = new ProcessStartInfo();

            process = new Process();
            psi.FileName = appPath;

            if (arguments != null)
            {
                psi.Arguments = arguments;
            }

            UIAVerifyLogger.LogComment("Starting({0})", appPath);
            process.StartInfo = psi;

            process.Start();

            int runningTime = 0;
            while (process.MainWindowHandle.Equals(IntPtr.Zero))
            {
                if (runningTime > MAXTIME)
                    throw new Exception("Could not find " + appPath);

                Thread.Sleep(TIMEWAIT);
                runningTime += TIMEWAIT;

                process.Refresh();
            }

            UIAVerifyLogger.LogComment("{0} started", appPath);

            UIAVerifyLogger.LogComment("Obtained an AutomationElement for {0}", appPath);
            return AutomationElement.FromHandle(process.MainWindowHandle);

        }
    }
}
```



 

 




