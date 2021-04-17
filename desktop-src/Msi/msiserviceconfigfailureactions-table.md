---
description: En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produzca un error en un servicio. Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.
ms.assetid: 7c450b74-1f91-4a1c-beee-646a407eb8a8
title: Tabla MsiServiceConfigFailureActions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae55d095e227611271de35d673289fc9eb5b174e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668269"
---
# <a name="msiserviceconfigfailureactions-table"></a><span data-ttu-id="1e798-104">Tabla MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="1e798-104">MsiServiceConfigFailureActions Table</span></span>

<span data-ttu-id="1e798-105">En la tabla MsiServiceConfigFailureActions se enumeran las operaciones que se ejecutarán después de que se produzca un error en un servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-105">The MsiServiceConfigFailureActions table lists operations to be run after a service fails.</span></span> <span data-ttu-id="1e798-106">Las operaciones especificadas en esta tabla se ejecutan la próxima vez que se inicia el sistema.</span><span class="sxs-lookup"><span data-stu-id="1e798-106">The operations specified in this table run the next time the system is started.</span></span>

<span data-ttu-id="1e798-107">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="1e798-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="1e798-108">Esta tabla está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="1e798-108">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="1e798-109">La tabla MsiServiceConfigFailureActions tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="1e798-109">The MsiServiceConfigFailureActions table has the following columns.</span></span>



| <span data-ttu-id="1e798-110">Columna</span><span class="sxs-lookup"><span data-stu-id="1e798-110">Column</span></span>                         | <span data-ttu-id="1e798-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="1e798-111">Type</span></span>                         | <span data-ttu-id="1e798-112">Clave</span><span class="sxs-lookup"><span data-stu-id="1e798-112">Key</span></span> | <span data-ttu-id="1e798-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="1e798-113">Nullable</span></span> |
|--------------------------------|------------------------------|-----|----------|
| <span data-ttu-id="1e798-114">MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="1e798-114">MsiServiceConfigFailureActions</span></span> | [<span data-ttu-id="1e798-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="1e798-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="1e798-116">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-116">Y</span></span>   | <span data-ttu-id="1e798-117">N</span><span class="sxs-lookup"><span data-stu-id="1e798-117">N</span></span>        |
| <span data-ttu-id="1e798-118">Nombre</span><span class="sxs-lookup"><span data-stu-id="1e798-118">Name</span></span>                           | [<span data-ttu-id="1e798-119">Formatea</span><span class="sxs-lookup"><span data-stu-id="1e798-119">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1e798-120">N</span><span class="sxs-lookup"><span data-stu-id="1e798-120">N</span></span>   | <span data-ttu-id="1e798-121">N</span><span class="sxs-lookup"><span data-stu-id="1e798-121">N</span></span>        |
| <span data-ttu-id="1e798-122">Evento</span><span class="sxs-lookup"><span data-stu-id="1e798-122">Event</span></span>                          | [<span data-ttu-id="1e798-123">Entero</span><span class="sxs-lookup"><span data-stu-id="1e798-123">Integer</span></span>](integer.md)       | <span data-ttu-id="1e798-124">N</span><span class="sxs-lookup"><span data-stu-id="1e798-124">N</span></span>   | <span data-ttu-id="1e798-125">N</span><span class="sxs-lookup"><span data-stu-id="1e798-125">N</span></span>        |
| <span data-ttu-id="1e798-126">ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="1e798-126">ResetPeriod</span></span>                    | [<span data-ttu-id="1e798-127">Entero</span><span class="sxs-lookup"><span data-stu-id="1e798-127">Integer</span></span>](integer.md)       | <span data-ttu-id="1e798-128">N</span><span class="sxs-lookup"><span data-stu-id="1e798-128">N</span></span>   | <span data-ttu-id="1e798-129">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-129">Y</span></span>        |
| <span data-ttu-id="1e798-130">RebootMessage</span><span class="sxs-lookup"><span data-stu-id="1e798-130">RebootMessage</span></span>                  | [<span data-ttu-id="1e798-131">Formatea</span><span class="sxs-lookup"><span data-stu-id="1e798-131">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1e798-132">N</span><span class="sxs-lookup"><span data-stu-id="1e798-132">N</span></span>   | <span data-ttu-id="1e798-133">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-133">Y</span></span>        |
| <span data-ttu-id="1e798-134">Get-Help</span><span class="sxs-lookup"><span data-stu-id="1e798-134">Command</span></span>                        | [<span data-ttu-id="1e798-135">Formatea</span><span class="sxs-lookup"><span data-stu-id="1e798-135">Formatted</span></span>](formatted.md)   | <span data-ttu-id="1e798-136">N</span><span class="sxs-lookup"><span data-stu-id="1e798-136">N</span></span>   | <span data-ttu-id="1e798-137">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-137">Y</span></span>        |
| <span data-ttu-id="1e798-138">Acciones</span><span class="sxs-lookup"><span data-stu-id="1e798-138">Actions</span></span>                        | [<span data-ttu-id="1e798-139">Texto</span><span class="sxs-lookup"><span data-stu-id="1e798-139">Text</span></span>](text.md)             | <span data-ttu-id="1e798-140">N</span><span class="sxs-lookup"><span data-stu-id="1e798-140">N</span></span>   | <span data-ttu-id="1e798-141">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-141">Y</span></span>        |
| <span data-ttu-id="1e798-142">DelayActions</span><span class="sxs-lookup"><span data-stu-id="1e798-142">DelayActions</span></span>                   | [<span data-ttu-id="1e798-143">Texto</span><span class="sxs-lookup"><span data-stu-id="1e798-143">Text</span></span>](text.md)             | <span data-ttu-id="1e798-144">N</span><span class="sxs-lookup"><span data-stu-id="1e798-144">N</span></span>   | <span data-ttu-id="1e798-145">Y</span><span class="sxs-lookup"><span data-stu-id="1e798-145">Y</span></span>        |
| <span data-ttu-id="1e798-146">Componente\_</span><span class="sxs-lookup"><span data-stu-id="1e798-146">Component\_</span></span>                    | [<span data-ttu-id="1e798-147">Identificador</span><span class="sxs-lookup"><span data-stu-id="1e798-147">Identifier</span></span>](identifier.md) | <span data-ttu-id="1e798-148">N</span><span class="sxs-lookup"><span data-stu-id="1e798-148">N</span></span>   | <span data-ttu-id="1e798-149">N</span><span class="sxs-lookup"><span data-stu-id="1e798-149">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1e798-150">Columnas</span><span class="sxs-lookup"><span data-stu-id="1e798-150">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1e798-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span><span class="sxs-lookup"><span data-stu-id="1e798-151"><span id="MsiServiceConfigFailureActions"></span><span id="msiserviceconfigfailureactions"></span><span id="MSISERVICECONFIGFAILUREACTIONS"></span>MsiServiceConfigFailureActions</span></span>
</dt> <dd>

<span data-ttu-id="1e798-152">Esta es la clave principal de esta tabla que identifica una acción de error.</span><span class="sxs-lookup"><span data-stu-id="1e798-152">This is the primary key of this table that identifies a failure action.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="1e798-153"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="1e798-154">Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="1e798-154">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="1e798-155"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="1e798-156">Esta columna especifica cuándo se debe cambiar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-156">This column specifies when to change the service's configuration.</span></span> <span data-ttu-id="1e798-157">Los valores siguientes son campos de bits que se pueden combinar para representar varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="1e798-157">The following values are bit fields that can be combined to represent multiple operations.</span></span> <span data-ttu-id="1e798-158">Se omiten los demás valores de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="1e798-158">Any other bit field values are ignored.</span></span>



| <span data-ttu-id="1e798-159">Constante</span><span class="sxs-lookup"><span data-stu-id="1e798-159">Constant</span></span>                                         | <span data-ttu-id="1e798-160">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e798-160">Description</span></span>                                     |
|--------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="1e798-161">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="1e798-161">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="1e798-162">Cambiar durante la instalación del componente.</span><span class="sxs-lookup"><span data-stu-id="1e798-162">Change during installation of the component.</span></span>    |
| <span data-ttu-id="1e798-163">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="1e798-163">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="1e798-164">Cambiar durante la desinstalación del componente.</span><span class="sxs-lookup"><span data-stu-id="1e798-164">Change during uninstallation of the component.</span></span>  |
| <span data-ttu-id="1e798-165">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="1e798-165">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="1e798-166">Cambiar durante la reinstalación del componente.</span><span class="sxs-lookup"><span data-stu-id="1e798-166">Change during re-installation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1e798-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span><span class="sxs-lookup"><span data-stu-id="1e798-167"><span id="ResetPeriod"></span><span id="resetperiod"></span><span id="RESETPERIOD"></span>ResetPeriod</span></span>
</dt> <dd>

<span data-ttu-id="1e798-168">El período de restablecimiento en segundos del número de errores del servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-168">The reset period in seconds of service's failure count.</span></span> <span data-ttu-id="1e798-169">El [Administrador de control de servicios](../services/service-control-manager.md) (SCM) cuenta el número de veces que se ha producido un error en cada servicio desde que el sistema se reinició por última vez.</span><span class="sxs-lookup"><span data-stu-id="1e798-169">The [Service Control Manager](../services/service-control-manager.md) (SCM) counts the number of times each service has failed since the system was last restarted.</span></span> <span data-ttu-id="1e798-170">El recuento se restablece en cero si no se produce un error en el servicio durante el período de restablecimiento.</span><span class="sxs-lookup"><span data-stu-id="1e798-170">The count is reset to zero if the service does not fail for the reset period.</span></span> <span data-ttu-id="1e798-171">Cuando se produce un error en el servicio durante el enésima tiempo, el sistema realiza la acción especificada en el elemento \[ N-1 \] de la matriz especificada en el campo acciones.</span><span class="sxs-lookup"><span data-stu-id="1e798-171">When the service fails for the Nth time, the system performs the action specified in the element \[N-1\] of the array specified in the Actions field.</span></span>

<span data-ttu-id="1e798-172">Deje vacío el campo ResetPeriod para indicar que el recuento de errores nunca debe restablecerse.</span><span class="sxs-lookup"><span data-stu-id="1e798-172">Leave ResetPeriod field empty to indicate that failure count should never be reset.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span><span class="sxs-lookup"><span data-stu-id="1e798-173"><span id="RebootMessage"></span><span id="rebootmessage"></span><span id="REBOOTMESSAGE"></span>RebootMessage</span></span>
</dt> <dd>

<span data-ttu-id="1e798-174">Mensaje que se envía a los usuarios antes de reiniciar el equipo en respuesta a una acción de **\_ \_ reinicio de acción de SC** especificada en la columna actions.</span><span class="sxs-lookup"><span data-stu-id="1e798-174">The message sent to users before restarting the computer in response to a **SC\_ACTION\_REBOOT** action specified in the Actions column.</span></span> <span data-ttu-id="1e798-175">Puede usar una cadena vacía, "", para enviar el mensaje actual sin cambios.</span><span class="sxs-lookup"><span data-stu-id="1e798-175">You can use an empty string, "", to send the current message unchanged.</span></span> <span data-ttu-id="1e798-176">Puede utilizar \[ ~ \] la sintaxis del tipo de datos [con formato](formatted.md) para eliminar el mensaje actual y no enviar ningún mensaje.</span><span class="sxs-lookup"><span data-stu-id="1e798-176">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current message and send no message.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span><span class="sxs-lookup"><span data-stu-id="1e798-177"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>Command</span></span>
</dt> <dd>

<span data-ttu-id="1e798-178">La línea de comandos ejecutada por el proceso creado por la función [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) en respuesta a una acción de comando de ejecución de la **\_ acción \_ \_ SC** especificada en la columna actions.</span><span class="sxs-lookup"><span data-stu-id="1e798-178">The command line run by the process created by the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function in response to a **SC\_ACTION\_RUN\_COMMAND** action specified in the Actions column.</span></span> <span data-ttu-id="1e798-179">El nuevo proceso se ejecuta en la misma cuenta que el servicio y solo si el campo acción **es \_ \_ \_ comando SC Action Run**.</span><span class="sxs-lookup"><span data-stu-id="1e798-179">The new process runs under the same account as the service and only if the Action field is **SC\_ACTION\_RUN\_COMMAND**.</span></span> <span data-ttu-id="1e798-180">Puede usar una cadena vacía, "", para usar la línea de comandos actual sin modificar.</span><span class="sxs-lookup"><span data-stu-id="1e798-180">You can use an empty string, "", to use the current command line unchanged.</span></span> <span data-ttu-id="1e798-181">Puede utilizar \[ ~ \] la sintaxis del tipo de datos [con formato](formatted.md) para eliminar la línea de comandos actual y no ejecutar ninguna operación cuando se produce un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-181">You can use \[~\] syntax of the [Formatted](formatted.md) data type to delete the current command line and run no operation when the service fails.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Operaciones</span><span class="sxs-lookup"><span data-stu-id="1e798-182"><span id="Actions"></span><span id="actions"></span><span id="ACTIONS"></span>Actions</span></span>
</dt> <dd>

<span data-ttu-id="1e798-183">Este campo contiene una matriz de valores enteros que especifican las acciones realizadas por el SCM si se produce un error en el servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-183">This field contains an array of integer values that specify the actions taken by the SCM if the service fails.</span></span> <span data-ttu-id="1e798-184">Separe los valores de la matriz por \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="1e798-184">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="1e798-185">El valor entero del elemento n de la matriz especifica la acción que se realiza cuando se produce un error en el servicio durante el número de horas.</span><span class="sxs-lookup"><span data-stu-id="1e798-185">The integer value in the Nth element of the array specifies the action performed when the service fails for the Nth time.</span></span> <span data-ttu-id="1e798-186">Cada miembro de la matriz es uno de los siguientes valores enteros.</span><span class="sxs-lookup"><span data-stu-id="1e798-186">Each member of the array is one of following integer values.</span></span>



| <span data-ttu-id="1e798-187">Constante</span><span class="sxs-lookup"><span data-stu-id="1e798-187">Constant</span></span>                                 | <span data-ttu-id="1e798-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="1e798-188">Description</span></span>           |
|------------------------------------------|-----------------------|
| <span data-ttu-id="1e798-189">**SC \_ ACCIÓN \_ ninguno** 0</span><span class="sxs-lookup"><span data-stu-id="1e798-189">**SC\_ACTION\_NONE** 0</span></span><br/>         | <span data-ttu-id="1e798-190">No se requiere ninguna acción.</span><span class="sxs-lookup"><span data-stu-id="1e798-190">No action.</span></span>            |
| <span data-ttu-id="1e798-191">**SC \_ ACCIÓN de \_ reinicio** 2</span><span class="sxs-lookup"><span data-stu-id="1e798-191">**SC\_ACTION\_REBOOT** 2</span></span><br/>       | <span data-ttu-id="1e798-192">Reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="1e798-192">Restart the computer.</span></span> |
| <span data-ttu-id="1e798-193">**SC \_ ACCIÓN de \_ reinicio** 1</span><span class="sxs-lookup"><span data-stu-id="1e798-193">**SC\_ACTION\_RESTART** 1</span></span><br/>      | <span data-ttu-id="1e798-194">Reinicie el servicio.</span><span class="sxs-lookup"><span data-stu-id="1e798-194">Restart the service.</span></span>  |
| <span data-ttu-id="1e798-195">**SC \_ \_ \_ Comando de ejecución de acción** 3</span><span class="sxs-lookup"><span data-stu-id="1e798-195">**SC\_ACTION\_RUN\_COMMAND** 3</span></span><br/> | <span data-ttu-id="1e798-196">Ejecutar un comando.</span><span class="sxs-lookup"><span data-stu-id="1e798-196">Run a command.</span></span>        |



 

</dd> <dt>

<span data-ttu-id="1e798-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span><span class="sxs-lookup"><span data-stu-id="1e798-197"><span id="DelayActions"></span><span id="delayactions"></span><span id="DELAYACTIONS"></span>DelayActions</span></span>
</dt> <dd>

<span data-ttu-id="1e798-198">Este campo contiene una matriz de valores enteros que especifican el tiempo en milisegundos que se debe esperar antes de realizar la acción especificada en la columna de acción.</span><span class="sxs-lookup"><span data-stu-id="1e798-198">This field contains an array of integer values that specify the time in milliseconds to wait before performing the action specified in the Action column.</span></span> <span data-ttu-id="1e798-199">Separe los valores de la matriz por \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="1e798-199">Separate the values in the array by \[~\].</span></span> <span data-ttu-id="1e798-200">El número de elementos de la matriz DelayActions debe ser igual al número de elementos de la matriz actions.</span><span class="sxs-lookup"><span data-stu-id="1e798-200">The number of elements in the DelayActions array must be equal to the number of elements in the Actions array.</span></span> <span data-ttu-id="1e798-201">El elemento n de la matriz DelayActions especifica el retardo de tiempo para el elemento n de la matriz actions.</span><span class="sxs-lookup"><span data-stu-id="1e798-201">The Nth element of the DelayActions array specifies the time delay for the nth element of the Actions array.</span></span>

</dd> <dt>

<span data-ttu-id="1e798-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="1e798-202"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="1e798-203">Clave externa para la columna uno de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="1e798-203">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1e798-204">Validación</span><span class="sxs-lookup"><span data-stu-id="1e798-204">Validation</span></span>

<dl>

[<span data-ttu-id="1e798-205">ICE102</span><span class="sxs-lookup"><span data-stu-id="1e798-205">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="1e798-206">ICE03</span><span class="sxs-lookup"><span data-stu-id="1e798-206">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="1e798-207">ICE06</span><span class="sxs-lookup"><span data-stu-id="1e798-207">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="1e798-208">ICE32</span><span class="sxs-lookup"><span data-stu-id="1e798-208">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="1e798-209">ICE45</span><span class="sxs-lookup"><span data-stu-id="1e798-209">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="1e798-210">ICE46</span><span class="sxs-lookup"><span data-stu-id="1e798-210">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="1e798-211">ICE69</span><span class="sxs-lookup"><span data-stu-id="1e798-211">ICE69</span></span>](ice69.md)  
</dl>

 

 
