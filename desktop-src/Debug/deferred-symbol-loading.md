---
description: Para ahorrar tiempo y memoria cuando se trabaja con muchos archivos de símbolos, utilice la función SymSetOptions para establecer la opción de carga de símbolos diferida ( \_ cargas diferidas de SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Carga de símbolos diferidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998060"
---
# <a name="deferred-symbol-loading"></a><span data-ttu-id="13cd7-103">Carga de símbolos diferidos</span><span class="sxs-lookup"><span data-stu-id="13cd7-103">Deferred Symbol Loading</span></span>

<span data-ttu-id="13cd7-104">Para conservar el tiempo y la memoria cuando se trabaja con muchos archivos de símbolos, utilice la función [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) para establecer la opción de carga de símbolos diferida ( \_ cargas diferidas \_ de SYMOPT) y, a continuación, use la función [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) para cargar símbolos aplazados para todos los módulos.</span><span class="sxs-lookup"><span data-stu-id="13cd7-104">To conserve time and memory when working with many symbol files, use the [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) function to set the deferred symbol loading (SYMOPT\_DEFERRED\_LOADS) option, then use the [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) or [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) function to load symbols deferred for all modules.</span></span> <span data-ttu-id="13cd7-105">El controlador de símbolos mostrará los símbolos que están disponibles para los módulos, pero no asignará la información de depuración en memoria hasta que se solicite.</span><span class="sxs-lookup"><span data-stu-id="13cd7-105">The symbol handler will list symbols that are available for the modules, but will not map the debug information into memory until it is requested.</span></span> <span data-ttu-id="13cd7-106">Este es el método preferido para usar los símbolos de depuración de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="13cd7-106">This is the preferred method to efficiently use debugging symbols.</span></span> <span data-ttu-id="13cd7-107">Todas las funciones que utilizan símbolos se ven afectadas por la carga de símbolos diferidos.</span><span class="sxs-lookup"><span data-stu-id="13cd7-107">All functions that use symbols are affected by deferred symbol loading.</span></span>

 

 



