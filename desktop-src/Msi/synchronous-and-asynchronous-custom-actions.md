---
description: El Windows Installer procesa las acciones personalizadas como un subproceso independiente de la instalación principal.
ms.assetid: 6451029c-87f4-44ee-aa2b-cc9a1c25bcc0
title: Acciones personalizadas sincrónicas y asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 067c5b40840269f3a0393faee8fe670f5e522c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677528"
---
# <a name="synchronous-and-asynchronous-custom-actions"></a><span data-ttu-id="1aa1a-103">Acciones personalizadas sincrónicas y asincrónicas</span><span class="sxs-lookup"><span data-stu-id="1aa1a-103">Synchronous and Asynchronous Custom Actions</span></span>

<span data-ttu-id="1aa1a-104">El Windows Installer procesa las acciones personalizadas como un subproceso independiente de la instalación principal.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-104">The Windows Installer processes custom actions as a separate thread from the main installation.</span></span> <span data-ttu-id="1aa1a-105">Durante la ejecución sincrónica de una acción personalizada, el instalador espera a que el subproceso de la acción personalizada se complete antes de continuar con la instalación principal.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-105">During synchronous execution of a custom action, the installer waits for the thread of the custom action to complete before continuing the main installation.</span></span> <span data-ttu-id="1aa1a-106">Durante la ejecución asincrónica, el instalador ejecuta la acción personalizada simultáneamente a medida que continúa la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-106">During asynchronous execution, the installer runs the custom action simultaneously as the current installation continues.</span></span> <span data-ttu-id="1aa1a-107">Por lo tanto, los autores de acciones personalizadas deben tener en cuenta todos los subprocesos asincrónicos que puedan estar realizando cambios en la base de datos de instalación entre las llamadas de función.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-107">Authors of custom actions must therefore be aware of any asynchronous threads that may be making changes to the installation database between function calls.</span></span>

<span data-ttu-id="1aa1a-108">En concreto, las llamadas a [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) y [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) deben evitarse en acciones personalizadas asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-108">In particular, calls to [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) and [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha) should be avoided in asynchronous custom actions.</span></span> <span data-ttu-id="1aa1a-109">En su lugar, use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) para obtener una ruta de acceso de destino.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-109">Instead use [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya) to obtain a target path.</span></span> <span data-ttu-id="1aa1a-110">Las operaciones de base de datos masivas como las operaciones de importación, exportación y transformación deben evitarse en cualquier tipo de acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-110">Bulk database operations such as import, export, and transform operations should be avoided in any type of custom action.</span></span>

<span data-ttu-id="1aa1a-111">Las marcas de opciones se pueden establecer en el campo Type de la [tabla CustomAction](customaction-table.md) para especificar que los subprocesos de acción principal y personalizada se ejecuten de forma sincrónica o asincrónica.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-111">Option flags can be set in the Type field of the [CustomAction table](customaction-table.md) to specify that the main and custom action threads run synchronously or asynchronously.</span></span> <span data-ttu-id="1aa1a-112">Vea [Opciones de procesamiento de devolución de acción personalizada](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="1aa1a-112">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

<span data-ttu-id="1aa1a-113">El instalador solo puede ejecutar acciones [personalizadas de reversión](rollback-custom-actions.md) y acciones de [instalación simultáneas](concurrent-installations.md) como acciones personalizadas sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="1aa1a-113">The installer can only execute [Rollback Custom Actions](rollback-custom-actions.md) and [Concurrent Installation](concurrent-installations.md) actions as synchronous custom actions.</span></span>

 

 



