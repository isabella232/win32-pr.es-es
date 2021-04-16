---
title: Pruebas con AccChecker
description: Describe el flujo de trabajo de pruebas típico que incorpora AccChecker.
ms.assetid: 18C2DDEE-D199-4C22-9ADF-1E07B1325A06
keywords:
- pruebas con AccChecker
- AccChecker, flujo de trabajo de prueba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c8bb90ce0d9fdde290bfb0f3ce0ee9f873f2b6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531906"
---
# <a name="testing-with-accchecker"></a><span data-ttu-id="4b791-105">Pruebas con AccChecker</span><span class="sxs-lookup"><span data-stu-id="4b791-105">Testing with AccChecker</span></span>

<span data-ttu-id="4b791-106">En el escenario siguiente se describen los pasos que suele seguir al realizar pruebas con AccChecker.</span><span class="sxs-lookup"><span data-stu-id="4b791-106">The following scenario describes the steps that you typically follow when testing with AccChecker.</span></span>

> [!Note]  
> <span data-ttu-id="4b791-107">Cuando se ejecutan rutinas de comprobación de AccChecker, la interacción del usuario con el equipo host puede interferir con algunas rutinas.</span><span class="sxs-lookup"><span data-stu-id="4b791-107">When AccChecker verification routines are running, user interaction with the host machine can interfere with some routines.</span></span> <span data-ttu-id="4b791-108">Se recomienda que no se produzca ninguna interacción del usuario hasta que AccChecker notifique al usuario que se han completado todas las tareas.</span><span class="sxs-lookup"><span data-stu-id="4b791-108">We recommend that no further user interaction occur until AccChecker notifies the user that all tasks are complete.</span></span>

 

1.  <span data-ttu-id="4b791-109">Ejecute comprobaciones de AccChecker en una aplicación o un control de destino determinados.</span><span class="sxs-lookup"><span data-stu-id="4b791-109">Run AccChecker verifications on a particular target application or control.</span></span> <span data-ttu-id="4b791-110">Para obtener más información, consulte la [pestaña comprobaciones](the-accchecker-graphical-user-interface.md).</span><span class="sxs-lookup"><span data-stu-id="4b791-110">For more information, see [Verifications Tab](the-accchecker-graphical-user-interface.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="4b791-111">AccChecker no explora todas las permutaciones de la interfaz de usuario de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4b791-111">AccChecker doesn't explore all UI permutations in an application.</span></span> <span data-ttu-id="4b791-112">Los elementos ocultos en controles como ventanas, paneles, pestañas y menús deben exponerse manualmente.</span><span class="sxs-lookup"><span data-stu-id="4b791-112">Elements hidden within controls such as windows, panes, tabs, and menus must be exposed manually.</span></span>

     

2.  <span data-ttu-id="4b791-113">Examine el registro de errores de AccChecker y evalúe o clasifique los resultados.</span><span class="sxs-lookup"><span data-stu-id="4b791-113">Examine the AccChecker error log and assess or triage the results.</span></span> <span data-ttu-id="4b791-114">Corrija los problemas triviales y registre los errores graves según corresponda.</span><span class="sxs-lookup"><span data-stu-id="4b791-114">Fix trivial issues and log severe bugs as appropriate.</span></span>
3.  <span data-ttu-id="4b791-115">Generar un archivo de supresión para errores y errores que se pueden omitir hasta las pruebas de regresión.</span><span class="sxs-lookup"><span data-stu-id="4b791-115">Generate a suppression file for bugs and errors that can be ignored until regression testing.</span></span>
4.  <span data-ttu-id="4b791-116">Vuelva a ejecutar las comprobaciones de AccChecker con el archivo de supresión y las correcciones de errores iniciales.</span><span class="sxs-lookup"><span data-stu-id="4b791-116">Re-run AccChecker verifications with the suppression file and initial bug fixes.</span></span> <span data-ttu-id="4b791-117">Esto proporciona una instantánea de los problemas en la implementación actual de Microsoft Active Accessibility y establece una línea base para las pruebas de regresión.</span><span class="sxs-lookup"><span data-stu-id="4b791-117">This provides a snapshot of the issues in the current implementation of Microsoft Active Accessibility and establishes a baseline for regression testing.</span></span>
5.  <span data-ttu-id="4b791-118">Integre las API de AccChecker y el archivo de supresión en un marco de pruebas automatizadas para las pruebas de regresión en los errores registrados en las comprobaciones de AccChecker iniciales.</span><span class="sxs-lookup"><span data-stu-id="4b791-118">Integrate the AccChecker APIs and suppression file into an automated test framework for regression testing on bugs logged from the initial AccChecker verifications.</span></span>
    > [!Note]  
    > <span data-ttu-id="4b791-119">A medida que se corrijan los errores, el archivo de supresión debe modificarse según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="4b791-119">As bugs are fixed, the suppression file should be modified as required.</span></span>

     

6.  <span data-ttu-id="4b791-120">Confirme que no se han introducido regresiones ni nuevos errores de accesibilidad en la aplicación o el control.</span><span class="sxs-lookup"><span data-stu-id="4b791-120">Confirm that no regressions or new accessibility bugs have been introduced into the application or control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b791-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4b791-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b791-122">UI Accessibility Checker</span><span class="sxs-lookup"><span data-stu-id="4b791-122">UI Accessibility Checker</span></span>](ui-accessibility-checker.md)
</dt> </dl>

 

 




