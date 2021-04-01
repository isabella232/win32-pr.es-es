---
description: En las secciones siguientes se describe el uso de acciones personalizadas.
ms.assetid: dd2a0681-f50d-4232-bdcc-8aee6bb121a1
title: Uso de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1937adbf64b94667fc3e7c44d82843b561dfb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275754"
---
# <a name="using-custom-actions"></a><span data-ttu-id="517a1-103">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-103">Using Custom Actions</span></span>

<span data-ttu-id="517a1-104">En las secciones siguientes se describe el uso de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="517a1-104">The following sections describe using custom actions.</span></span>

-   [<span data-ttu-id="517a1-105">Invocar acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-105">Invoking Custom Actions</span></span>](invoking-custom-actions.md)
-   [<span data-ttu-id="517a1-106">Secuenciar acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-106">Sequencing Custom Actions</span></span>](sequencing-custom-actions.md)
-   [<span data-ttu-id="517a1-107">Obtener información de contexto para las acciones personalizadas de ejecución aplazada</span><span class="sxs-lookup"><span data-stu-id="517a1-107">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
-   [<span data-ttu-id="517a1-108">Agregar acciones personalizadas a ProgressBar</span><span class="sxs-lookup"><span data-stu-id="517a1-108">Adding Custom Actions to the ProgressBar</span></span>](adding-custom-actions-to-the-progressbar.md)
-   [<span data-ttu-id="517a1-109">Depuración de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-109">Debugging Custom Actions</span></span>](debugging-custom-actions.md)
-   [<span data-ttu-id="517a1-110">Determinar el nivel de interfaz de usuario a partir de una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="517a1-110">Determining UI Level from a Custom Action</span></span>](determining-ui-level-from-a-custom-action.md)
-   [<span data-ttu-id="517a1-111">Desinstalación de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-111">Uninstalling Custom Actions</span></span>](uninstalling-custom-actions.md)
-   [<span data-ttu-id="517a1-112">Devolver mensajes de error de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-112">Returning Error Messages from Custom Actions</span></span>](returning-error-messages-from-custom-actions.md)
-   [<span data-ttu-id="517a1-113">Establecer un punto de restauración desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="517a1-113">Setting a restore point from a Custom Action</span></span>](setting-a-restore-point-from-a-custom-action.md)
-   [<span data-ttu-id="517a1-114">Funciones que no se usan en acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="517a1-114">Functions Not for Use in Custom Actions</span></span>](functions-not-for-use-in-custom-actions.md)
-   [<span data-ttu-id="517a1-115">Cambiar el estado del sistema mediante una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="517a1-115">Changing the System State Using a Custom Action</span></span>](changing-the-system-state-using-a-custom-action.md)
-   [<span data-ttu-id="517a1-116">Obtener acceso a la sesión del instalador actual desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="517a1-116">Accessing the Current Installer Session from Inside a Custom Action</span></span>](accessing-the-current-installer-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="517a1-117">Obtener acceso a una base de datos o una sesión desde una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="517a1-117">Accessing a Database or Session from Inside a Custom Action</span></span>](accessing-a-database-or-session-from-inside-a-custom-action.md)
-   [<span data-ttu-id="517a1-118">Usar una acción personalizada para iniciar un archivo instalado al final de la instalación</span><span class="sxs-lookup"><span data-stu-id="517a1-118">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>](using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation.md)
-   [<span data-ttu-id="517a1-119">Usar una acción personalizada para crear cuentas de usuario en un equipo local</span><span class="sxs-lookup"><span data-stu-id="517a1-119">Using a Custom Action to Create User Accounts on a Local Computer</span></span>](using-a-custom-action-to-create-user-accounts-on-a-local-computer.md)
-   [<span data-ttu-id="517a1-120">Uso de acciones personalizadas de 64 bits</span><span class="sxs-lookup"><span data-stu-id="517a1-120">Using 64-bit Custom Actions</span></span>](using-64-bit-custom-actions.md)

<span data-ttu-id="517a1-121">Para obtener información general sobre las acciones personalizadas, consulte [acerca de las acciones personalizadas](about-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="517a1-121">For an overview of custom actions, see [About Custom Actions](about-custom-actions.md).</span></span>

<span data-ttu-id="517a1-122">Para obtener más información sobre la codificación de acciones personalizadas en la [tabla CustomAction](customaction-table.md), vea [Custom Action Reference](custom-action-reference.md).</span><span class="sxs-lookup"><span data-stu-id="517a1-122">For more information about encoding custom actions into the [CustomAction table](customaction-table.md), see [Custom Action Reference](custom-action-reference.md).</span></span>

<span data-ttu-id="517a1-123">Para obtener un resumen de las acciones personalizadas y cómo se codifican en la tabla CustomAction, vea [lista de Resumen de todos los tipos de acción personalizados](summary-list-of-all-custom-action-types.md).</span><span class="sxs-lookup"><span data-stu-id="517a1-123">For a summary of custom actions and how they are encoded into the CustomAction table, see [Summary List of All Custom Action Types](summary-list-of-all-custom-action-types.md).</span></span>

 

 



