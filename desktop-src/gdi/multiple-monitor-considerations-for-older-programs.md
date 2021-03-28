---
description: Por lo general, las aplicaciones antiguas no necesitan cambios para trabajar en varios sistemas de supervisión.
ms.assetid: 908cf88c-69ed-4855-817d-ba749e14ff85
title: Consideraciones de varios monitores para programas anteriores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feebb356cb2f9c5480c84f1718b51d6e866ef621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984922"
---
# <a name="multiple-monitor-considerations-for-older-programs"></a><span data-ttu-id="d753d-103">Consideraciones de varios monitores para programas anteriores</span><span class="sxs-lookup"><span data-stu-id="d753d-103">Multiple Monitor Considerations for Older Programs</span></span>

<span data-ttu-id="d753d-104">Por lo general, las aplicaciones antiguas no necesitan cambios para trabajar en varios sistemas de supervisión.</span><span class="sxs-lookup"><span data-stu-id="d753d-104">Generally, older applications do not need changes to work on multiple monitor systems.</span></span> <span data-ttu-id="d753d-105">Para la mayoría, el sistema parecerá tener una sola pantalla.</span><span class="sxs-lookup"><span data-stu-id="d753d-105">For most, the system will appear to have only one display.</span></span> <span data-ttu-id="d753d-106">Las métricas del sistema reflejan la pantalla principal y las aplicaciones de pantalla completa que aparecen en el servidor principal.</span><span class="sxs-lookup"><span data-stu-id="d753d-106">System metrics reflect the primary display and fullscreen applications show up on the primary.</span></span> <span data-ttu-id="d753d-107">El sistema controla la minimización, la maximización, los menús y los cuadros de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d753d-107">The system handles minimization, maximization, menus, and dialog boxes.</span></span>

<span data-ttu-id="d753d-108">Sin embargo, algunos programas tendrán problemas.</span><span class="sxs-lookup"><span data-stu-id="d753d-108">However, some programs will have problems.</span></span> <span data-ttu-id="d753d-109">Algunos de los problemas que podrían tener problemas son las aplicaciones de control remoto, las que tienen acceso directo al hardware y las que han revisado el controlador de pantalla o el GDI.</span><span class="sxs-lookup"><span data-stu-id="d753d-109">Some that could have problems are remote control applications, those that have direct hardware access, and those that have patched the GDI or DISPLAY driver.</span></span> <span data-ttu-id="d753d-110">En estos casos, puede ser necesario que el usuario deshabilite cualquier monitor más allá del monitor principal.</span><span class="sxs-lookup"><span data-stu-id="d753d-110">In these cases, the user may be required to disable any monitor beyond the primary monitor.</span></span>

 

 



