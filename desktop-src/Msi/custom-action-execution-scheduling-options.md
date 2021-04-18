---
description: Dado que una acción personalizada se puede programar en las tablas de la interfaz de usuario y de secuencia de ejecución, y se puede ejecutar en el proceso del servicio o del cliente, una acción personalizada puede ejecutarse varias veces.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Opciones de programación de la ejecución de acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667623"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="1deb4-103">Opciones de programación de la ejecución de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="1deb4-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="1deb4-104">Dado que una acción personalizada se puede programar en las tablas de la interfaz de usuario y de secuencia de ejecución, y se puede ejecutar en el proceso del servicio o del cliente, una acción personalizada puede ejecutarse varias veces.</span><span class="sxs-lookup"><span data-stu-id="1deb4-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="1deb4-105">Tenga en cuenta que el instalador:</span><span class="sxs-lookup"><span data-stu-id="1deb4-105">Note that the installer:</span></span>

-   <span data-ttu-id="1deb4-106">Ejecuta inmediatamente las acciones en una tabla de secuencia de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="1deb4-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="1deb4-107">No ejecuta una acción si el campo de expresión condicional de la tabla de secuencia se evalúa como false.</span><span class="sxs-lookup"><span data-stu-id="1deb4-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="1deb4-108">Procesa la tabla de la secuencia de la interfaz de usuario en el proceso de cliente si el nivel de interfaz del usuario interno está establecido en el modo de interfaz de usuario completa (vea [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) para obtener una descripción de los niveles de IU).</span><span class="sxs-lookup"><span data-stu-id="1deb4-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="1deb4-109">Es un servicio registrado de forma predeterminada cuando se usa Windows 2000 y, en este caso, la tabla de secuencia de ejecución se procesa en el servicio de instalador.</span><span class="sxs-lookup"><span data-stu-id="1deb4-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="1deb4-110">Puede utilizar las siguientes marcas de opciones para controlar la ejecución inmediata de acciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="1deb4-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="1deb4-111">Para establecer una opción, agregue el valor de esta tabla al valor del campo Type de la [tabla CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="1deb4-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="1deb4-112">No se debe usar ninguna de las marcas siguientes con [las acciones personalizadas de ejecución aplazada](deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="1deb4-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="1deb4-113"><span id="_default_"></span><span id="_DEFAULT_"></span>predeterminada</span><span class="sxs-lookup"><span data-stu-id="1deb4-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="1deb4-114">Hexadecimal: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="1deb4-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="1deb4-115">Decimal: 0</span><span class="sxs-lookup"><span data-stu-id="1deb4-115">Decimal: 0</span></span>

<span data-ttu-id="1deb4-116">Ejecutar siempre.</span><span class="sxs-lookup"><span data-stu-id="1deb4-116">Always execute.</span></span> <span data-ttu-id="1deb4-117">La acción se puede ejecutar dos veces si está presente en ambas tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1deb4-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="1deb4-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span><span class="sxs-lookup"><span data-stu-id="1deb4-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="1deb4-119">Hexadecimal: 0x00000100</span><span class="sxs-lookup"><span data-stu-id="1deb4-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="1deb4-120">Decimal: 256</span><span class="sxs-lookup"><span data-stu-id="1deb4-120">Decimal: 256</span></span>

<span data-ttu-id="1deb4-121">No ejecute más de una vez si está presente en ambas tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1deb4-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="1deb4-122">Siempre omite la acción en la secuencia de ejecución si se ha ejecutado la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1deb4-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="1deb4-123">Ningún efecto en la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1deb4-123">No effect in UI sequence.</span></span> <span data-ttu-id="1deb4-124">No es necesario que la acción esté presente o se ejecute en la secuencia de IU que se va a omitir en la secuencia de ejecución.</span><span class="sxs-lookup"><span data-stu-id="1deb4-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="1deb4-125">No se ve afectado por la instalación del registro del servicio.</span><span class="sxs-lookup"><span data-stu-id="1deb4-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="1deb4-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span><span class="sxs-lookup"><span data-stu-id="1deb4-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="1deb4-127">Hexadecimal: 0x00000200</span><span class="sxs-lookup"><span data-stu-id="1deb4-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="1deb4-128">Decimal: 512</span><span class="sxs-lookup"><span data-stu-id="1deb4-128">Decimal: 512</span></span>

<span data-ttu-id="1deb4-129">Se ejecuta una vez por proceso, en ambas tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="1deb4-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="1deb4-130">Omite la acción en la secuencia de ejecución si la secuencia de la interfaz de usuario se ha ejecutado en el mismo proceso, por ejemplo, ambas se ejecutan en el proceso del cliente.</span><span class="sxs-lookup"><span data-stu-id="1deb4-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="1deb4-131">Se utiliza para evitar que las acciones que modifican el estado de sesión, como datos de propiedades y de base de datos, se ejecuten dos veces.</span><span class="sxs-lookup"><span data-stu-id="1deb4-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="1deb4-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span><span class="sxs-lookup"><span data-stu-id="1deb4-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="1deb4-133">Hexadecimal: 0x00000300</span><span class="sxs-lookup"><span data-stu-id="1deb4-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="1deb4-134">Decimal: 768</span><span class="sxs-lookup"><span data-stu-id="1deb4-134">Decimal: 768</span></span>

<span data-ttu-id="1deb4-135">Ejecutar solo si se ejecuta en el cliente después de ejecutar la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1deb4-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="1deb4-136">La acción se ejecuta solo si la secuencia de ejecución se ejecuta en el cliente después de la secuencia de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="1deb4-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="1deb4-137">Se puede usar para proporcionar la lógica/o, o para suprimir el procesamiento relacionado con la interfaz de usuario si ya se ha realizado para la sesión de cliente.</span><span class="sxs-lookup"><span data-stu-id="1deb4-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="1deb4-138">Tenga en cuenta que para ejecutar una acción personalizada durante dos modos de ejecución diferentes, cree dos entradas en la [tabla CustomAction](customaction-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1deb4-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="1deb4-139">Por ejemplo, para tener una acción personalizada que llama a una biblioteca de vínculos dinámicos (DLL) de C/C++ ( [tipo de acción personalizada 1](custom-action-type-1.md)) cuando el modo es MSIRUNMODE \_ programado y MSIRUNMODE \_ ROLLBACK, coloque dos entradas en la tabla CustomAction que llamen a la misma dll pero que tengan tipos numéricos diferentes.</span><span class="sxs-lookup"><span data-stu-id="1deb4-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="1deb4-140">Incluya el código que llama a [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) para determinar cuándo se debe ejecutar la acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="1deb4-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1deb4-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1deb4-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1deb4-142">Referencia de acción personalizada</span><span class="sxs-lookup"><span data-stu-id="1deb4-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="1deb4-143">Acerca de las acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="1deb4-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="1deb4-144">Uso de acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="1deb4-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



