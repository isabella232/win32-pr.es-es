---
title: Estrategias de control de versiones y de reserva
description: Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva no se ha alcanzado todavía, la aplicación debe tratar la situación correctamente.
ms.assetid: 6a34a783-98fd-406e-a96d-8e2a09a51c2d
ms.tgt_platform: multiple
keywords:
- Control de versiones y estrategias de reserva AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f6383ad06e73457e18dddfac53295a0c16389c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903091"
---
# <a name="versioning-and-fallback-strategies"></a><span data-ttu-id="e4698-104">Estrategias de control de versiones y de reserva</span><span class="sxs-lookup"><span data-stu-id="e4698-104">Versioning and Fallback Strategies</span></span>

<span data-ttu-id="e4698-105">Cuando una aplicación detecta una actualización parcial mediante una de las técnicas anteriores o lee un conjunto de objetos cuya fecha efectiva no se ha alcanzado todavía, la aplicación debe tratar la situación correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4698-105">When an application detects a partial update using one of the preceding techniques or reads a set of objects whose effective date has not yet been reached, the application must deal with the situation gracefully.</span></span> <span data-ttu-id="e4698-106">En algunas aplicaciones, la respuesta correcta es "revertir" a una versión anterior de los objetos en cuestión.</span><span class="sxs-lookup"><span data-stu-id="e4698-106">For some applications, the graceful response is to "fall back" to a previous version of the objects in question.</span></span> <span data-ttu-id="e4698-107">Active Directory Domain Services no proporcionan una utilidad de control de versiones, las aplicaciones que quieran esta funcionalidad deben proporcionarlas.</span><span class="sxs-lookup"><span data-stu-id="e4698-107">Active Directory Domain Services do not provide a versioning facility—applications that want this capability must provide it themselves.</span></span> <span data-ttu-id="e4698-108">Los enfoques para el control de versiones incluyen mantener los valores de "última buena conocida" almacenados en caché localmente y almacenar varios conjuntos de objetos en el directorio, por ejemplo, en los contenedores "antiguos", "actual" y "nuevo".</span><span class="sxs-lookup"><span data-stu-id="e4698-108">Approaches to versioning include keeping the "last known good" values cached locally and storing multiple sets of objects in the directory, for example, in "old," "current," and "new" containers.</span></span> <span data-ttu-id="e4698-109">Muchos otros esquemas son posibles.</span><span class="sxs-lookup"><span data-stu-id="e4698-109">Many other schemes are possible.</span></span>

<span data-ttu-id="e4698-110">Las implementaciones deben tener cuidado para evitar consecuencias imprevistas.</span><span class="sxs-lookup"><span data-stu-id="e4698-110">Implementations must take care to avoid unintended consequences.</span></span> <span data-ttu-id="e4698-111">Solo se debe usar una versión anterior de los objetos cuando se detecta una actualización parcial o cuando los nuevos objetos todavía no son "efectivos".</span><span class="sxs-lookup"><span data-stu-id="e4698-111">An earlier version of objects should be used only when a partial update is detected or the new objects are not yet "effective."</span></span> <span data-ttu-id="e4698-112">Al revertirse porque algo de la aplicación "no funciona" podría eludir la intención de un administrador.</span><span class="sxs-lookup"><span data-stu-id="e4698-112">Falling back because something in the application "does not work" might circumvent an administrator's intent.</span></span> <span data-ttu-id="e4698-113">Por ejemplo, dos equipos que anteriormente podían comunicarse podrían no ser capaces de hacerlo debido a un cambio en la Directiva del Protocolo de seguridad de Internet (IPsec).</span><span class="sxs-lookup"><span data-stu-id="e4698-113">For example, two computers that formerly could communicate might find themselves unable to do so because of a change in Internet Protocol security (IPsec) policy.</span></span> <span data-ttu-id="e4698-114">Si esto es intencionado en parte del administrador, los sistemas afectados no deben revertir a la Directiva que les permitió comunicarse, ya que esto sería una brecha de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4698-114">If this is intentional on the part of the administrator, the affected systems should not fall back to the policy that allowed them to communicate, as this would be a security breach.</span></span>

 

 




