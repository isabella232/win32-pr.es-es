---
title: Actualizar desde la versión anterior
description: Actualizar desde la versión anterior
ms.assetid: a3f0c0bb-8c12-4907-8e49-49b098449c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e2cf49fbe21c2522226ec61ab57c93d9df27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695246"
---
# <a name="updating-from-previous-version"></a><span data-ttu-id="1364d-103">Actualizar desde la versión anterior</span><span class="sxs-lookup"><span data-stu-id="1364d-103">Updating from Previous Version</span></span>

<span data-ttu-id="1364d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="1364d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="1364d-105">Las aplicaciones compiladas y compiladas con la versión anterior 1,5 de Microsoft Agent deben ejecutarse sin modificaciones en la nueva versión 2,0.</span><span class="sxs-lookup"><span data-stu-id="1364d-105">Applications built and compiled with the previous 1.5 version of Microsoft Agent should run without modification under the new 2.0 version.</span></span> <span data-ttu-id="1364d-106">La propiedad [**Connected**](connected-property.md) ya no se puede establecer en **false**; algunas propiedades del objeto SpeechInput que se han reemplazado siguen existiendo, pero ya no convierten los valores y el servidor ya no desencadena los eventos de [**reinicio**](https://www.bing.com/search?q=**Restart**) y [**apagado**](https://www.bing.com/search?q=**Shutdown**) .</span><span class="sxs-lookup"><span data-stu-id="1364d-106">The [**Connected**](connected-property.md) property can no longer be set to **False**; certain properties of the SpeechInput object that have been replaced still exist, but no longer turn any values, and the server no longer fires the [**Restart**](https://www.bing.com/search?q=**Restart**) and [**Shutdown**](https://www.bing.com/search?q=**Shutdown**) events.</span></span>

<span data-ttu-id="1364d-107">Sin embargo, si actualiza las aplicaciones para que usen el Control Agent 2,0, puede que tenga que modificar el código.</span><span class="sxs-lookup"><span data-stu-id="1364d-107">However, if you update your applications to use the Agent 2.0 control, you may have to modify your code.</span></span> <span data-ttu-id="1364d-108">Si ha instalado la versión 2,0 del agente de Microsoft y carga un proyecto de Visual Basic usa la versión anterior del control del agente, Visual Basic incluye una opción que muestra automáticamente un mensaje que indica que detectó una nueva versión del control.</span><span class="sxs-lookup"><span data-stu-id="1364d-108">If you have installed the 2.0 version of Microsoft Agent and load a Visual Basic project use the earlier version of the Agent control, Visual Basic includes an option that will automatically display a message indicating that it detected a new version of the control.</span></span> <span data-ttu-id="1364d-109">Para garantizar el correcto funcionamiento de la aplicación, elija usar siempre la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="1364d-109">To ensure proper operation of your application, always choose to use the later version.</span></span>

<span data-ttu-id="1364d-110">En el caso de otros lenguajes de programación (como Microsoft Office VBA 97), para actualizar el control, puede que tenga que quitar primero el control del agente 1,5 y guardar el código.</span><span class="sxs-lookup"><span data-stu-id="1364d-110">For other programming languages (such as Microsoft Office 97 VBA), to update the control, you may have to first remove the 1.5 Agent control and save your code.</span></span> <span data-ttu-id="1364d-111">A continuación, salga del entorno de programación, reinicie el entorno de programación, vuelva a cargar el código e inserte el nuevo control.</span><span class="sxs-lookup"><span data-stu-id="1364d-111">Then, quit the programming environment, restart the programming environment, reload your code and insert the new control.</span></span> <span data-ttu-id="1364d-112">Evite la edición de una aplicación habilitada para el agente 2,0 en la misma instancia del entorno de programación en el que está editando una aplicación habilitada para el agente 1,5.</span><span class="sxs-lookup"><span data-stu-id="1364d-112">Avoid editing an Agent 2.0-enabled application in the same instance of the programming environment that you are editing an Agent 1.5-enabled application in.</span></span> <span data-ttu-id="1364d-113">Es posible que algunos entornos de programación no controlen las diferencias entre las dos versiones de los controles.</span><span class="sxs-lookup"><span data-stu-id="1364d-113">Some programming environments may not handle the differences between the two versions of controls.</span></span>

<span data-ttu-id="1364d-114">Debe poder desinstalar la versión del agente 1,5 en el sistema después de instalar la versión 2,0 del agente.</span><span class="sxs-lookup"><span data-stu-id="1364d-114">You should be able to uninstall the Agent 1.5 release on your system after installing the Agent 2.0 release.</span></span> <span data-ttu-id="1364d-115">Sin embargo, si el agente 1,5 está instalado en la versión 2,0, es posible que tenga que volver a instalar 2,0.</span><span class="sxs-lookup"><span data-stu-id="1364d-115">However, if Agent 1.5 is installed over the 2.0 release, you may have to reinstall 2.0.</span></span>

 

 




