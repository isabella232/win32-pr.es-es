---
title: Automatización de la interfaz de usuario de pruebas
description: La Automatización de la interfaz de usuario test library (biblioteca de pruebas de UIA) es una API a la que llama la aplicación de controlador en un escenario de pruebas automatizadas.
ms.assetid: A11341E5-71FC-442C-8F78-C40E717BF798
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac2c02433eaaa9f5d5658ca9f469803042b0a637bb20e6cdce72299bf7c4643f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133538"
---
# <a name="ui-automation-test-library"></a>Automatización de la interfaz de usuario de pruebas

La Automatización de la interfaz de usuario test library (biblioteca de pruebas de UIA)  es una API a la que llama la aplicación del controlador en un escenario de pruebas automatizadas. El controlador es la aplicación que obtiene un elemento de automatización (objeto [**IUIAutomationElement)**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) de un control que requiere comprobación y lo proporciona a la biblioteca Automatización de la interfaz de usuario test. A continuación, la biblioteca de pruebas comprueba y valida la Automatización de la interfaz de usuario implementación. Para obtener más información sobre los Automatización de la interfaz de usuario y los elementos de automatización, [vea Automatización de la interfaz de usuario Fundamentals](entry-uiautocore-overview.md).

-   [Automatización de la interfaz de usuario flujo de trabajo de la biblioteca de pruebas](#ui-automation-test-library-workflow)
-   [Registro con la biblioteca Automatización de la interfaz de usuario pruebas](#logging-with-the-ui-automation-test-library)
    -   [Registro XML](#xml-logging)
    -   [Registro de la consola](#console-logging)
    -   [Requisitos de código para el registro](#code-requirements-for-logging)
    -   [Ejemplos de registro](#logging-examples)

## <a name="ui-automation-test-library-workflow"></a>Automatización de la interfaz de usuario flujo de trabajo de la biblioteca de pruebas

En el diagrama siguiente se muestra un flujo de trabajo de prueba que incorpora la biblioteca Automatización de la interfaz de usuario pruebas mediante una aplicación de consola como controlador. En este caso, el controlador inicia una instancia de Notepad.exe y obtiene un elemento de automatización (es decir, un objeto [**IUIAutomationElement)**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) del control de edición. A continuación, el controlador crea un Automatización de la interfaz de usuario biblioteca de pruebas basado en la plataforma de interfaz de usuario que se está probando y, a continuación, pasa el elemento de automatización como un parámetro. La Automatización de la interfaz de usuario test library determina que el elemento de automatización es un tipo de control [Document](uiauto-supportdocumentcontroltype.md) y, a continuación, ejecuta las pruebas de control Document, las pruebas de patrón de control [Text](uiauto-implementingtextandtextrange.md) y [Scroll](uiauto-implementingscroll.md) y las pruebas de elementos de automatización genéricos.

![Diagrama que muestra el flujo de controlador a aplicación a controlador a UIATestLibrary mediante flechas de color rojo.](images/uia-test-library-workflow.png)

## <a name="logging-with-the-ui-automation-test-library"></a>Registro con la biblioteca Automatización de la interfaz de usuario pruebas

La biblioteca Automatización de la interfaz de usuario pruebas usa archivos DLL externos para registrar los resultados de las ejecuciones de pruebas. Admite el registro como XML y el registro en la consola.

### <a name="xml-logging"></a>Registro XML

El registro XML lo suele usar Visual Automatización de la interfaz de usuario Verify, pero también se puede incorporar en un flujo de trabajo de línea de comandos.

Si se especifica el registro XML, la aplicación de controlador debe serializar la salida mediante la creación de un objeto **XmlWriter** y su paso al **método XmlLog.GetTestRunXml.** A continuación, el controlador puede usar el XML serializado internamente o escribirlo en un archivo.

Los siguientes archivos DLL son necesarios para el registro XML.

-   WUIALogging.dll
-   WUIALoggerXml.dll

### <a name="console-logging"></a>Registro de la consola

De forma predeterminada, la Automatización de la interfaz de usuario de pruebas usa el registro de consola, donde toda la salida del registro se canalizará como texto sin formato a la ventana de la consola. WUIALogging.dll es necesario para el registro de la consola.

### <a name="code-requirements-for-logging"></a>Requisitos de código para el registro

Una aplicación de controlador debe incluir los siguientes fragmentos de código para usar Automatización de la interfaz de usuario de la biblioteca de pruebas.


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

En los ejemplos siguientes se muestra la funcionalidad de registro básica y se muestra cómo usar la API Automatización de la interfaz de usuario Test Library en una aplicación de controlador de automatización de pruebas básica.


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



 

 




