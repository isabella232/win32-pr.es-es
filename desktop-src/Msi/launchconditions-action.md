---
description: La acción LaunchConditions consulta la tabla LaunchCondition y evalúa cada instrucción condicional registrada en ella. Si se produce un error en cualquiera de estas instrucciones condicionales, se muestra un mensaje de error al usuario y se finaliza la instalación.
ms.assetid: b356987d-3efe-4a57-a745-91a1b34222e9
title: Acción LaunchConditions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f6bb3eaf2a98c630bb9cacd18ff449083eb9c1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686802"
---
# <a name="launchconditions-action"></a><span data-ttu-id="0394e-104">Acción LaunchConditions</span><span class="sxs-lookup"><span data-stu-id="0394e-104">LaunchConditions Action</span></span>

<span data-ttu-id="0394e-105">La acción LaunchConditions consulta la [tabla LaunchCondition](launchcondition-table.md) y evalúa cada instrucción condicional registrada en ella.</span><span class="sxs-lookup"><span data-stu-id="0394e-105">The LaunchConditions action queries the [LaunchCondition table](launchcondition-table.md) and evaluates each conditional statement recorded there.</span></span> <span data-ttu-id="0394e-106">Si se produce un error en cualquiera de estas instrucciones condicionales, se muestra un mensaje de error al usuario y se finaliza la instalación.</span><span class="sxs-lookup"><span data-stu-id="0394e-106">If any of these conditional statements fail, an error message is displayed to the user and the installation is terminated.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="0394e-107">Restricciones de secuencia</span><span class="sxs-lookup"><span data-stu-id="0394e-107">Sequence Restrictions</span></span>

<span data-ttu-id="0394e-108">La acción LaunchConditions es opcional.</span><span class="sxs-lookup"><span data-stu-id="0394e-108">The LaunchConditions action is optional.</span></span> <span data-ttu-id="0394e-109">Esta acción suele ser la primera de la secuencia, pero la [acción AppSearch](appsearch-action.md) se puede secuenciar antes de la acción LaunchConditions.</span><span class="sxs-lookup"><span data-stu-id="0394e-109">This action is normally the first in the sequence, but the [AppSearch Action](appsearch-action.md) may be sequenced before the LaunchConditions action.</span></span> <span data-ttu-id="0394e-110">Si hay condiciones de inicio que no se aplican a todos los modos de instalación, se debe usar la propiedad de modo de instalación adecuada en una expresión condicional en la tabla de secuencia adecuada.</span><span class="sxs-lookup"><span data-stu-id="0394e-110">If there are launch conditions that do not apply to all installation modes, the appropriate installation mode property should be used in a conditional expression in the appropriate sequence table.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="0394e-111">Mensajes ActionData</span><span class="sxs-lookup"><span data-stu-id="0394e-111">ActionData Messages</span></span>

<span data-ttu-id="0394e-112">No hay mensajes ActionData.</span><span class="sxs-lookup"><span data-stu-id="0394e-112">There are no ActionData messages.</span></span>

 

 



