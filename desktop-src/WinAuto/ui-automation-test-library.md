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
# <a name="ui-automation-test-library"></a>Biblioteca de pruebas de automatización de la interfaz de usuario

La biblioteca de pruebas de automatización de la interfaz de usuario (biblioteca de pruebas de UIA) es una API a la que llama la aplicación del *controlador* en un escenario de pruebas automatizadas. El controlador es la aplicación que obtiene un elemento de automatización (objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) de un control que requiere comprobación y lo proporciona a la biblioteca de pruebas de automatización de la interfaz de usuario. A continuación, la biblioteca de prueba comprueba y valida la implementación de la automatización de la interfaz de usuario. Para obtener más información sobre la automatización de la interfaz de usuario y los elementos de automatización, vea [fundamentos de UI Automation](entry-uiautocore-overview.md).

-   [Flujo de trabajo de biblioteca de pruebas de UI Automation](#ui-automation-test-library-workflow)
-   [Registro con la biblioteca de pruebas de UI Automation](#logging-with-the-ui-automation-test-library)
    -   [Registro XML](#xml-logging)
    -   [Registro de la consola](#console-logging)
    -   [Requisitos de código para el registro](#code-requirements-for-logging)
    -   [Ejemplos de registro](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Flujo de trabajo de biblioteca de pruebas de UI Automation

En el diagrama siguiente se muestra un flujo de trabajo de prueba que incorpora la biblioteca de pruebas de automatización de la interfaz de usuario mediante el uso de una aplicación de consola como controlador. En este caso, el controlador inicia una instancia de Notepad.exe y obtiene un elemento de automatización (es decir, un objeto [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ) del control de edición. A continuación, el controlador crea un objeto de biblioteca de pruebas de automatización de la interfaz de usuario basado en la plataforma de interfaz de usuario que se prueba y, a continuación, pasa el elemento de automatización como un parámetro. La biblioteca de pruebas de automatización de la interfaz de usuario determina que el elemento de automatización es un tipo de control de [documento](uiauto-supportdocumentcontroltype.md) y, a continuación, ejecuta las pruebas de control de documento, las pruebas de patrón de control de [texto](uiauto-implementingtextandtextrange.md) y [desplazamiento](uiauto-implementingscroll.md) , y las pruebas de elementos de automatización genéricas.

![Diagrama que muestra el flujo de la aplicación al controlador a UIATestLibrary con flechas rojas.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Registro con la biblioteca de pruebas de UI Automation

La biblioteca de pruebas de automatización de la interfaz de usuario usa archivos dll externos para registrar los resultados de las series de pruebas. Admite el registro como XML y el registro en la consola.

### <a name="xml-logging"></a>Registro XML

El registro XML se usa normalmente en la comprobación de la automatización de la interfaz de usuario de Visual, pero también se puede incorporar a un flujo de trabajo de línea de comandos.

Si se especifica el registro XML, la aplicación de controlador debe serializar la salida mediante la creación de un objeto **XmlWriter** y pasarlo al método **XmlLog. GetTestRunXml** . Después, el controlador puede utilizar el XML serializado internamente o escribirlo en un archivo.

Los siguientes archivos dll son necesarios para el registro de XML.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Registro de la consola

De forma predeterminada, la biblioteca de pruebas de automatización de la interfaz de usuario usa el registro de la consola, donde todos los resultados del registro se canalizan como texto sin formato a la ventana de la consola. WUIALogging.dll es necesario para el registro de la consola.

### <a name="code-requirements-for-logging"></a>Requisitos de código para el registro

Una aplicación de controlador debe incluir los siguientes fragmentos de código para usar el registro de la biblioteca de pruebas de automatización de la interfaz de usuario.


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



### <a name="logging-examples"></a>Ejemplos de registro

En los siguientes ejemplos se muestra la funcionalidad básica de registro y se muestra cómo usar la API de la biblioteca de pruebas de automatización de la interfaz de usuario en una aplicación básica de controlador de automatización de prueba.


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



 

 




