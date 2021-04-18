---
description: Depurar componentes escritos en Visual Basic
ms.assetid: 2b00ed29-8b48-4a54-83e8-d5e69e5f883e
title: Depurar componentes escritos en Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 085dd1d6f45cc7f6665851b232402ecee01c069f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705375"
---
# <a name="debugging-components-written-in-visual-basic"></a><span data-ttu-id="5b8e6-103">Depurar componentes escritos en Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b8e6-103">Debugging Components Written in Visual Basic</span></span>

<span data-ttu-id="5b8e6-104">Puede usar el entorno de desarrollo de Microsoft Visual Basic 6,0 para la depuración en ciertos escenarios.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-104">You can use the Microsoft Visual Basic 6.0 development environment for debugging within certain scenarios.</span></span> <span data-ttu-id="5b8e6-105">El uso de Visual Basic para la depuración permite el acceso a herramientas conocidas para los programadores de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-105">Using Visual Basic for debugging allows access to tools familiar to Visual Basic programmers.</span></span> <span data-ttu-id="5b8e6-106">Por otro lado, dado que durante la depuración Visual Basic componentes se ejecutan dentro del proceso del entorno de Visual Basic, puede que sea necesario depurar el componente una vez compilado con el entorno de desarrollo de Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-106">On the other hand, because during debugging Visual Basic components run within the Visual Basic environment's process, it may be necessary to debug your component after it has been compiled by using the Microsoft Visual C++ development environment.</span></span>

<span data-ttu-id="5b8e6-107">Para obtener más información sobre la depuración en el entorno de desarrollo integrado (IDE) de Visual Basic, consulte [depuración en el IDE de Visual Basic](debugging-in-the-visual-basic-ide.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e6-107">For more information about debugging within the Visual Basic integrated development environment (IDE), see [Debugging in the Visual Basic IDE](debugging-in-the-visual-basic-ide.md).</span></span> <span data-ttu-id="5b8e6-108">Para obtener más información sobre la depuración de componentes Visual Basic una vez compilados con el entorno de desarrollo de Visual C++, vea [depurar componentes Compilados Visual Basic](debugging-compiled-visual-basic-components.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e6-108">For more on debugging Visual Basic components after they're compiled using the Visual C++ development environment, see [Debugging Compiled Visual Basic Components](debugging-compiled-visual-basic-components.md).</span></span>

<span data-ttu-id="5b8e6-109">Además, se han resuelto varias limitaciones asociadas al uso del entorno de Visual Basic para depurar componentes con MTS para COM+.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-109">Also, several limitations associated with using the Visual Basic environment to debug components with MTS have been resolved for COM+.</span></span> <span data-ttu-id="5b8e6-110">Para obtener más información, consulte [compatibilidad con la depuración de COM+ Visual Basic en contraste con MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span><span class="sxs-lookup"><span data-stu-id="5b8e6-110">For more information, see [COM+ Visual Basic Debugging Support Contrasted with MTS](com--visual-basic-debugging-support-contrasted-with-mts.md).</span></span>

> [!Note]  
> <span data-ttu-id="5b8e6-111">Si ya ha usado Visual Basic en el mismo equipo que COM+, es posible que haya observado que el complemento Servicios de componentes está disponible en el entorno de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-111">If you have already used Visual Basic on the same computer as COM+, you may have noticed the Component Services add-in available in the Visual Basic environment.</span></span> <span data-ttu-id="5b8e6-112">Originalmente en MTS, esta característica se diseñó para actualizar el registro cada vez que se volvió a compilar un componente en una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-112">Originally in MTS, this feature was designed to update the registry each time you recompiled a component in a COM+ application.</span></span> <span data-ttu-id="5b8e6-113">Sin embargo, dada la naturaleza de la interacción del registro de Microsoft Windows y la base de datos de registro de COM+, es posible que algunas configuraciones no se actualicen por completo.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-113">However, given the nature of the interaction of the Microsoft Windows Registry and the COM+ registration database, some settings may not be completely updated.</span></span> <span data-ttu-id="5b8e6-114">Por lo tanto, en lugar de usar los comandos disponibles con este complemento, debe quitar y volver a instalar los componentes para actualizar la configuración después de volver a compilar.</span><span class="sxs-lookup"><span data-stu-id="5b8e6-114">Therefore, instead of using the commands available with this add-in, you should remove and reinstall your components to update settings after recompiling.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5b8e6-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5b8e6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b8e6-116">Depurar componentes escritos en Visual C++</span><span class="sxs-lookup"><span data-stu-id="5b8e6-116">Debugging Components Written in Visual C++</span></span>](debugging-components-written-in-visual-c--.md)
</dt> </dl>

 

 



