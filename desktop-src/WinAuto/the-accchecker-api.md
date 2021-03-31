---
title: La API de AccChecker
description: La API de AccChecker admite las pruebas automatizadas. Después de filtrar una aplicación mediante las pruebas manuales con la GUI de AccChecker, puede escribir pruebas automatizadas que incorporen el mensaje y los registros de supresión creados con la herramienta de la GUI.
ms.assetid: 9AD9A259-130B-4968-B7FD-DAFA89320391
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c098d25e282a8df8ff4125dfd2ce1f94d795b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903181"
---
# <a name="the-accchecker-api"></a><span data-ttu-id="1c4cb-104">La API de AccChecker</span><span class="sxs-lookup"><span data-stu-id="1c4cb-104">The AccChecker API</span></span>

<span data-ttu-id="1c4cb-105">La API de AccChecker admite las pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="1c4cb-105">The AccChecker API supports automated testing.</span></span> <span data-ttu-id="1c4cb-106">Después de filtrar una aplicación mediante las pruebas manuales con la GUI de AccChecker, puede escribir pruebas automatizadas que incorporen el mensaje y los registros de supresión creados con la herramienta de la GUI.</span><span class="sxs-lookup"><span data-stu-id="1c4cb-106">After screening an application by using manual testing with the AccChecker GUI, you can write automated tests that incorporate the message and suppression logs created with the GUI tool.</span></span>

<span data-ttu-id="1c4cb-107">En el ejemplo de código siguiente se muestra cómo usar la API AccChecker para probar la funcionalidad de tabulación en la aplicación del panel de control de Firewall de Windows.</span><span class="sxs-lookup"><span data-stu-id="1c4cb-107">The following code example demonstrates how to use the AccChecker API to test tabbing functionality in the Windows Firewall control panel application.</span></span>


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
        //  get our user interface ready for AccChecker
        Setup();
 
        //  AccChecker's class representing verifications that you can run
        AccCheck.Verification.VerificationManager vm = new AccCheck.Verification.VerificationManager();
 
        //  create a console logger to get output in the console
        ConsoleLogger consoleLogger = new ConsoleLogger();
 
        //  add AccChecker's Console Logger
        vm.AddLogger(consoleLogger);
 
        //  disable all verifications
        vm.DisableVerifications(AccCheck.Verification.VerificationFilter.All);
 
        // enable the ones we want to run
        vm.EnableRoutine("CheckTabbing");
 
        //  run it against the firewall
        vm.ExecuteEnabled(_fireWallHwnd);
 
        //  check if the verification failed by looking at the logger
        if (consoleLogger.ErrorCount > 0)
        {
            Console.WriteLine("Test failed!");
 
            Console.WriteLine("Error count = " + consoleLogger.ErrorCount);
        }
 
        // cleanup our user interface
        Cleanup();
    }
```



## <a name="related-topics"></a><span data-ttu-id="1c4cb-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1c4cb-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c4cb-109">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="1c4cb-109">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




