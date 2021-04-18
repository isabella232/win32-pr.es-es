---
description: Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada.
ms.assetid: 48707ae1-9488-4bbb-8447-b24e383affb7
title: Cambiar el estado del sistema mediante una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace5dc323bcf809c76eeb55cfa859a8621312df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667003"
---
# <a name="changing-the-system-state-using-a-custom-action"></a><span data-ttu-id="fc0d0-103">Cambiar el estado del sistema mediante una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="fc0d0-103">Changing the System State Using a Custom Action</span></span>

<span data-ttu-id="fc0d0-104">Las acciones personalizadas diseñadas para cambiar el estado del sistema deben ser acciones personalizadas de ejecución aplazada.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-104">Custom actions intended to change the system state must be deferred execution custom actions.</span></span> <span data-ttu-id="fc0d0-105">Las acciones personalizadas que establecen las propiedades, los Estados de las características, los Estados de los componentes o los directorios de destino, o la programación de las operaciones del sistema mediante la inserción de filas en tablas de secuencia pueden usar la ejecución inmediata de forma segura.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-105">Custom actions that set properties, feature states, component states, or target directories, or schedule system operations by inserting rows into sequence tables can use immediate execution safely.</span></span> <span data-ttu-id="fc0d0-106">Sin embargo, las acciones personalizadas que cambian el sistema directamente o llaman a otro servicio de sistema deben aplazarse hasta el momento en que se ejecuta el script de instalación.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-106">However, custom actions that change the system directly or call another system service must be deferred to the time when the installation script is executed.</span></span> <span data-ttu-id="fc0d0-107">Para obtener más información, vea [acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="fc0d0-107">For more information, see [Deferred Execution Custom Actions](deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="fc0d0-108">No debe intentar usar una acción personalizada de ejecución inmediata para cambiar el estado del sistema, porque todas las acciones personalizadas que cambian el estado deben tener una acción personalizada rollback correspondiente para deshacer el cambio de estado del sistema en una reversión de la instalación.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-108">You should not attempt to use an immediate execution custom action to change the system state, because every custom action that changes the state needs to have a corresponding rollback custom action to undo the system state change on an installation rollback.</span></span> <span data-ttu-id="fc0d0-109">Todas las acciones personalizadas de reversión también se difieren en acciones personalizadas y deben preceder a la acción que deshacer.</span><span class="sxs-lookup"><span data-stu-id="fc0d0-109">All rollback custom actions are also deferred custom actions and must precede the action they undo.</span></span> <span data-ttu-id="fc0d0-110">Para obtener más información, consulte [reversión de acciones personalizadas](rollback-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="fc0d0-110">For more information, see [Rollback Custom Actions](rollback-custom-actions.md).</span></span>

 

 



