---
description: La tabla MsiServiceConfig configura un servicio que está instalado o instalado por el paquete actual.
ms.assetid: 0d9fd005-9326-4a18-8496-35b5d1927f47
title: Tabla MsiServiceConfig
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357b6787e56d52a893dd1a118a3e2fcbc13379e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668270"
---
# <a name="msiserviceconfig-table"></a><span data-ttu-id="6811e-103">Tabla MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6811e-103">MsiServiceConfig Table</span></span>

<span data-ttu-id="6811e-104">La tabla MsiServiceConfig configura un servicio que está instalado o instalado por el paquete actual.</span><span class="sxs-lookup"><span data-stu-id="6811e-104">The MsiServiceConfig table configures a service that is installed or being installed by the current package.</span></span>

<span data-ttu-id="6811e-105">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="6811e-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="6811e-106">Esta tabla está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="6811e-106">This table is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="6811e-107">La tabla MsiServiceConfig tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="6811e-107">The MsiServiceConfig table has the following columns.</span></span>



| <span data-ttu-id="6811e-108">Columna</span><span class="sxs-lookup"><span data-stu-id="6811e-108">Column</span></span>           | <span data-ttu-id="6811e-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="6811e-109">Type</span></span>                         | <span data-ttu-id="6811e-110">Clave</span><span class="sxs-lookup"><span data-stu-id="6811e-110">Key</span></span> | <span data-ttu-id="6811e-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="6811e-111">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="6811e-112">MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6811e-112">MsiServiceConfig</span></span> | [<span data-ttu-id="6811e-113">Identificador</span><span class="sxs-lookup"><span data-stu-id="6811e-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="6811e-114">Y</span><span class="sxs-lookup"><span data-stu-id="6811e-114">Y</span></span>   | <span data-ttu-id="6811e-115">N</span><span class="sxs-lookup"><span data-stu-id="6811e-115">N</span></span>        |
| <span data-ttu-id="6811e-116">Nombre</span><span class="sxs-lookup"><span data-stu-id="6811e-116">Name</span></span>             | [<span data-ttu-id="6811e-117">Formatea</span><span class="sxs-lookup"><span data-stu-id="6811e-117">Formatted</span></span>](formatted.md)   | <span data-ttu-id="6811e-118">N</span><span class="sxs-lookup"><span data-stu-id="6811e-118">N</span></span>   | <span data-ttu-id="6811e-119">N</span><span class="sxs-lookup"><span data-stu-id="6811e-119">N</span></span>        |
| <span data-ttu-id="6811e-120">Evento</span><span class="sxs-lookup"><span data-stu-id="6811e-120">Event</span></span>            | [<span data-ttu-id="6811e-121">Entero</span><span class="sxs-lookup"><span data-stu-id="6811e-121">Integer</span></span>](integer.md)       | <span data-ttu-id="6811e-122">N</span><span class="sxs-lookup"><span data-stu-id="6811e-122">N</span></span>   | <span data-ttu-id="6811e-123">N</span><span class="sxs-lookup"><span data-stu-id="6811e-123">N</span></span>        |
| <span data-ttu-id="6811e-124">ConfigType</span><span class="sxs-lookup"><span data-stu-id="6811e-124">ConfigType</span></span>       | [<span data-ttu-id="6811e-125">Entero</span><span class="sxs-lookup"><span data-stu-id="6811e-125">Integer</span></span>](integer.md)       | <span data-ttu-id="6811e-126">N</span><span class="sxs-lookup"><span data-stu-id="6811e-126">N</span></span>   | <span data-ttu-id="6811e-127">N</span><span class="sxs-lookup"><span data-stu-id="6811e-127">N</span></span>        |
| <span data-ttu-id="6811e-128">Argumento</span><span class="sxs-lookup"><span data-stu-id="6811e-128">Argument</span></span>         | [<span data-ttu-id="6811e-129">Formatea</span><span class="sxs-lookup"><span data-stu-id="6811e-129">Formatted</span></span>](formatted.md)   | <span data-ttu-id="6811e-130">N</span><span class="sxs-lookup"><span data-stu-id="6811e-130">N</span></span>   | <span data-ttu-id="6811e-131">Y</span><span class="sxs-lookup"><span data-stu-id="6811e-131">Y</span></span>        |
| <span data-ttu-id="6811e-132">Componente\_</span><span class="sxs-lookup"><span data-stu-id="6811e-132">Component\_</span></span>      | [<span data-ttu-id="6811e-133">Identificador</span><span class="sxs-lookup"><span data-stu-id="6811e-133">Identifier</span></span>](identifier.md) | <span data-ttu-id="6811e-134">N</span><span class="sxs-lookup"><span data-stu-id="6811e-134">N</span></span>   | <span data-ttu-id="6811e-135">N</span><span class="sxs-lookup"><span data-stu-id="6811e-135">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="6811e-136">Columnas</span><span class="sxs-lookup"><span data-stu-id="6811e-136">Columns</span></span>

<dl> <dt>

<span data-ttu-id="6811e-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span><span class="sxs-lookup"><span data-stu-id="6811e-137"><span id="MsiServiceConfig"></span><span id="msiserviceconfig"></span><span id="MSISERVICECONFIG"></span>MsiServiceConfig</span></span>
</dt> <dd>

<span data-ttu-id="6811e-138">Esta es la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="6811e-138">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="6811e-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="6811e-139"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="6811e-140">Esta columna contiene el nombre de un servicio que forma parte de este paquete o que ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="6811e-140">This column contains the name of a service that is a part of this package or that is already is installed.</span></span>

</dd> <dt>

<span data-ttu-id="6811e-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="6811e-141"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="6811e-142">Esta columna especifica cuándo se debe cambiar la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-142">This column specifies when to change the service configuration.</span></span> <span data-ttu-id="6811e-143">Se pueden combinar los valores siguientes para representar varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="6811e-143">The following values can be combined to represent multiple operations.</span></span> <span data-ttu-id="6811e-144">Se omiten los valores que no se incluyan.</span><span class="sxs-lookup"><span data-stu-id="6811e-144">Any values included other than these are ignored.</span></span>



| <span data-ttu-id="6811e-145">Constante</span><span class="sxs-lookup"><span data-stu-id="6811e-145">Constant</span></span>                                         | <span data-ttu-id="6811e-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="6811e-146">Description</span></span>                                              |
|--------------------------------------------------|----------------------------------------------------------|
| <span data-ttu-id="6811e-147">**msidbServiceConfigEventInstall** 1</span><span class="sxs-lookup"><span data-stu-id="6811e-147">**msidbServiceConfigEventInstall** 1</span></span><br/>   | <span data-ttu-id="6811e-148">Realiza la acción durante la instalación del componente.</span><span class="sxs-lookup"><span data-stu-id="6811e-148">Takes the action during installation of the component.</span></span>   |
| <span data-ttu-id="6811e-149">**msidbServiceConfigEventUninstall** 2</span><span class="sxs-lookup"><span data-stu-id="6811e-149">**msidbServiceConfigEventUninstall** 2</span></span><br/> | <span data-ttu-id="6811e-150">Realiza la acción durante la desinstalación del componente.</span><span class="sxs-lookup"><span data-stu-id="6811e-150">Takes the action during uninstallation of the component.</span></span> |
| <span data-ttu-id="6811e-151">**msidbServiceConfigEventReinstall** 4</span><span class="sxs-lookup"><span data-stu-id="6811e-151">**msidbServiceConfigEventReinstall** 4</span></span><br/> | <span data-ttu-id="6811e-152">Realiza la acción durante la reinstalación del componente.</span><span class="sxs-lookup"><span data-stu-id="6811e-152">Takes the action during reinstallation of the component.</span></span> |



 

</dd> <dt>

<span data-ttu-id="6811e-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span><span class="sxs-lookup"><span data-stu-id="6811e-153"><span id="ConfigType"></span><span id="configtype"></span><span id="CONFIGTYPE"></span>ConfigType</span></span>
</dt> <dd>

<span data-ttu-id="6811e-154">El valor de este campo, combinado con el valor del campo arguments, especifica qué cambio se debe hacer en la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-154">The value in this field, combined with the value in the Arguments field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="6811e-155">El cambio especificado tendrá efecto la próxima vez que se inicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="6811e-155">The specified change takes effect the next time the system is started.</span></span>



| <span data-ttu-id="6811e-156">Config</span><span class="sxs-lookup"><span data-stu-id="6811e-156">Config</span></span>                                                      | <span data-ttu-id="6811e-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="6811e-157">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6811e-158">**Servicio \_ de \_ \_ \_ Inicio automático retrasado de configuración** 3</span><span class="sxs-lookup"><span data-stu-id="6811e-158">**SERVICE\_CONFIG\_DELAYED\_AUTO\_START** 3</span></span><br/>       | <span data-ttu-id="6811e-159">Configure el tiempo de espera de un [servicio de inicio automático](../services/automatically-starting-services.md).</span><span class="sxs-lookup"><span data-stu-id="6811e-159">Configure the time delay of an [auto-start service](../services/automatically-starting-services.md).</span></span> <br/> <span data-ttu-id="6811e-160">Escriba 1 en el campo argumento para iniciar el servicio después de otros servicios de inicio automático más un tiempo de retardo.</span><span class="sxs-lookup"><span data-stu-id="6811e-160">Enter 1 in the Argument field to start the service after other auto-start services plus a time delay.</span></span> <br/> <span data-ttu-id="6811e-161">Escriba 0 en el campo argumento para desactivar el retraso del servicio de inicio automático.</span><span class="sxs-lookup"><span data-stu-id="6811e-161">Enter 0 in the Argument field to turn off the auto-start service delay.</span></span><br/> <span data-ttu-id="6811e-162">Solo se aplica a los servicios de inicio automático instalados o a los servicios instalados por este paquete con **\_ \_ Inicio automático de servicio** en el campo StartType de la [tabla ServiceInstall](serviceinstall-table.md).</span><span class="sxs-lookup"><span data-stu-id="6811e-162">Applies only to installed auto-start services or services installed by this package with **SERVICE\_AUTO\_START** in the StartType field of the [ServiceInstall table](serviceinstall-table.md).</span></span><br/>                                                                         |
| <span data-ttu-id="6811e-163">**Servicio \_ de CONFIGURACIÓN \_ de \_ privilegios necesarios \_ información** 6</span><span class="sxs-lookup"><span data-stu-id="6811e-163">**SERVICE\_CONFIG\_REQUIRED\_PRIVILEGES\_INFO** 6</span></span><br/> | <span data-ttu-id="6811e-164">Cambiar la lista de privilegios necesarios para el servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-164">Change the list of privileges required by the service.</span></span><br/> <span data-ttu-id="6811e-165">Escriba una lista de privilegios solicitados en el campo argumento.</span><span class="sxs-lookup"><span data-stu-id="6811e-165">Enter a list of requested privileges in the Argument field.</span></span> <span data-ttu-id="6811e-166">El valor de cadena [con formato](formatted.md) en el campo argumento muestra las [**constantes de privilegio**](../secauthz/privilege-constants.md) para los privilegios solicitados.</span><span class="sxs-lookup"><span data-stu-id="6811e-166">The [Formatted](formatted.md) string value in the Argument field lists the [**Privilege Constants**](../secauthz/privilege-constants.md) for the requested privileges.</span></span> <span data-ttu-id="6811e-167">Puede usar la \[ ~ \] Sintaxis de la cadena [con formato](formatted.md) para insertar un carácter nulo.</span><span class="sxs-lookup"><span data-stu-id="6811e-167">You can use the \[~\] syntax of the [Formatted](formatted.md) string to insert a null character.</span></span> <span data-ttu-id="6811e-168">Separe las constantes de privilegio en la lista mediante \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="6811e-168">Separate the privilege constants in the list by \[~\].</span></span><br/>                                                                                                                              |
| <span data-ttu-id="6811e-169">**Servicio \_ de \_Información del \_ SID \_ del servicio de configuración** 5</span><span class="sxs-lookup"><span data-stu-id="6811e-169">**SERVICE\_CONFIG\_SERVICE\_SID\_INFO** 5</span></span><br/>         | <span data-ttu-id="6811e-170">Agregue un tipo de SID de servicio al token de proceso que contiene este servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-170">Add a service SID type to the process token containing this service.</span></span><br/> <span data-ttu-id="6811e-171">Escriba en el campo de argumento un tipo de SID de servicio válido para la estructura de [**\_ \_ información de SID de servicio**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) : tipo de SID de **servicio \_ \_ \_ ninguno** (0x00), **tipo de SID de servicio \_ \_ \_ restringido** (0x03) o **tipo de SID de servicio no \_ \_ \_ restringido** (0x01).</span><span class="sxs-lookup"><span data-stu-id="6811e-171">Enter in the Argument field a valid service SID type for the [**SERVICE\_SID\_INFO**](/windows/win32/api/winsvc/ns-winsvc-service_sid_info) structure: **SERVICE\_SID\_TYPE\_NONE** (0x00), **SERVICE\_SID\_TYPE\_RESTRICTED** (0x03), or **SERVICE\_SID\_TYPE\_UNRESTRICTED** (0x01).</span></span> <br/>                                                                                                                                                                                                                                              |
| <span data-ttu-id="6811e-172">**Servicio \_ de \_ \_ Información de preapagado de configuración** 7</span><span class="sxs-lookup"><span data-stu-id="6811e-172">**SERVICE\_CONFIG\_PRESHUTDOWN\_INFO** 7</span></span><br/>          | <span data-ttu-id="6811e-173">Configure la duración del tiempo que el [Administrador de control de servicios](../services/service-control-manager.md) (SCM) espera antes de continuar con otras operaciones de apagado.</span><span class="sxs-lookup"><span data-stu-id="6811e-173">Configure the length of the time the [Service Control Manager](../services/service-control-manager.md) (SCM) waits before proceeding with other shutdown operations.</span></span> <span data-ttu-id="6811e-174">El SCM espera este período de tiempo después de enviar la notificación **de \_ \_ cierre del servicio** al servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-174">The SCM waits for this period of time after sending the **SERVICE\_CONTROL\_PRESHUTDOWN** notification to the service.</span></span> <br/> <span data-ttu-id="6811e-175">Escriba la longitud del retraso de tiempo, en milisegundos, en el campo argumento.</span><span class="sxs-lookup"><span data-stu-id="6811e-175">Enter the time delay length, in milliseconds, in the Argument field.</span></span> <span data-ttu-id="6811e-176">Deje el campo de argumento vacío para restablecer el tiempo de retardo en el valor predeterminado de 3 minutos.</span><span class="sxs-lookup"><span data-stu-id="6811e-176">Leave the Argument field empty to reset the time delay to the default of 3 minutes.</span></span> <br/>                                                                                                                               |
| <span data-ttu-id="6811e-177">**Servicio \_ de \_Marca de \_ acciones \_ de error de configuración** 4</span><span class="sxs-lookup"><span data-stu-id="6811e-177">**SERVICE\_CONFIG\_FAILURE\_ACTIONS\_FLAG** 4</span></span><br/>     | <span data-ttu-id="6811e-178">Configure Cuándo se deben ejecutar las acciones de error para este servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-178">Configure when to run the failure actions for this service.</span></span> <span data-ttu-id="6811e-179">Este valor se omite si el servicio no tiene ninguna acción de error configurada.</span><span class="sxs-lookup"><span data-stu-id="6811e-179">This setting is ignored if the service has no configured failure actions.</span></span><br/> <span data-ttu-id="6811e-180">Escriba 0 para ejecutar las acciones solo si el servicio termina sin que se **\_ detenga el servicio** de informes.</span><span class="sxs-lookup"><span data-stu-id="6811e-180">Enter 0 to run the actions only if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> <span data-ttu-id="6811e-181">Escriba 1 para ejecutar las acciones si el servicio finaliza el servicio de informes **\_ detenido** y el miembro **dwWin32ExitCode** de la estructura de [**\_ Estado de servicio**](/windows/win32/api/winsvc/ns-winsvc-service_status) no es **\_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6811e-181">Enter 1 to run the actions if the service terminates reporting **SERVICE\_STOPPED** and the **dwWin32ExitCode** member of [**SERVICE\_STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) structure is not **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="6811e-182">También se ejecutan acciones de error configuradas si el servicio termina sin que se **\_ detenga el servicio** de informes.</span><span class="sxs-lookup"><span data-stu-id="6811e-182">Configured failure actions are also run if the service terminates without reporting **SERVICE\_STOPPED**.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="6811e-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span><span class="sxs-lookup"><span data-stu-id="6811e-183"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="6811e-184">El valor de este campo, combinado con el valor del campo ConfigType, especifica qué cambio se debe hacer en la configuración del servicio.</span><span class="sxs-lookup"><span data-stu-id="6811e-184">The value in this field, combined with the value in the ConfigType field, specify what change to make to the service configuration.</span></span> <span data-ttu-id="6811e-185">El cambio especificado tendrá efecto la próxima vez que se inicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="6811e-185">The specified change takes effect the next time the system is started.</span></span>

</dd> <dt>

<span data-ttu-id="6811e-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="6811e-186"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="6811e-187">Clave externa para la columna componente de la [tabla componente](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="6811e-187">External key to the Component column of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="6811e-188">Validación</span><span class="sxs-lookup"><span data-stu-id="6811e-188">Validation</span></span>

<dl>

[<span data-ttu-id="6811e-189">ICE102</span><span class="sxs-lookup"><span data-stu-id="6811e-189">ICE102</span></span>](ice-102.md)  
[<span data-ttu-id="6811e-190">ICE03</span><span class="sxs-lookup"><span data-stu-id="6811e-190">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="6811e-191">ICE06</span><span class="sxs-lookup"><span data-stu-id="6811e-191">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="6811e-192">ICE32</span><span class="sxs-lookup"><span data-stu-id="6811e-192">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="6811e-193">ICE45</span><span class="sxs-lookup"><span data-stu-id="6811e-193">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="6811e-194">ICE46</span><span class="sxs-lookup"><span data-stu-id="6811e-194">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="6811e-195">ICE69</span><span class="sxs-lookup"><span data-stu-id="6811e-195">ICE69</span></span>](ice69.md)  
</dl>

 

 
