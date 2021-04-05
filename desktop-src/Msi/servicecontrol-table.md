---
description: 'La tabla ServiceControl se utiliza para controlar los servicios instalados o desinstalados. Nota: los servicios que dependen de la presencia de un ensamblado en la caché de ensamblados global (GAC) no se pueden instalar o iniciar con las tablas ServiceInstall y ServiceControl.'
ms.assetid: c51cd9bd-3c55-4eec-ab67-172765adc51c
title: Tabla ServiceControl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2abd123e937673694dffd53773a16fcbd704c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815190"
---
# <a name="servicecontrol-table"></a><span data-ttu-id="7a1e8-103">Tabla ServiceControl</span><span class="sxs-lookup"><span data-stu-id="7a1e8-103">ServiceControl Table</span></span>

<span data-ttu-id="7a1e8-104">La tabla ServiceControl se utiliza para controlar los servicios instalados o desinstalados.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-104">The ServiceControl table is used to control installed or uninstalled services.</span></span>

> [!Note]  
> <span data-ttu-id="7a1e8-105">Los servicios que dependen de la presencia de un [ensamblado](assemblies.md) en la caché de ensamblados global (GAC) no se pueden instalar o iniciar con las tablas [ServiceInstall](serviceinstall-table.md) y ServiceControl.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-105">Services that rely on the presence of an [assembly](assemblies.md) in the Global Assembly Cache (GAC) cannot be installed or started using the [ServiceInstall](serviceinstall-table.md) and ServiceControl tables.</span></span> <span data-ttu-id="7a1e8-106">Si necesita iniciar un servicio que depende de un ensamblado en la GAC, debe usar una acción personalizada secuenciada después de la [acción InstallFinalize](installfinalize-action.md) o una [acción personalizada commit](commit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-106">If you need to start a service that depends on an assembly in the GAC, you must use a custom action sequenced after the [InstallFinalize action](installfinalize-action.md) or a [commit custom action](commit-custom-actions.md).</span></span> <span data-ttu-id="7a1e8-107">Para obtener información sobre cómo instalar ensamblados en la GAC, vea [instalación de ensamblados en la caché global de ensamblados](installation-of-assemblies-to-the-global-assembly-cache.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-107">For information about installing assemblies to the GAC see [Installation of Assemblies to the Global Assembly Cache](installation-of-assemblies-to-the-global-assembly-cache.md).</span></span>

 

<span data-ttu-id="7a1e8-108">La tabla ServiceControl tiene las columnas siguientes.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-108">The ServiceControl table has the following columns.</span></span>



| <span data-ttu-id="7a1e8-109">Columna</span><span class="sxs-lookup"><span data-stu-id="7a1e8-109">Column</span></span>         | <span data-ttu-id="7a1e8-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="7a1e8-110">Type</span></span>                         | <span data-ttu-id="7a1e8-111">Clave</span><span class="sxs-lookup"><span data-stu-id="7a1e8-111">Key</span></span> | <span data-ttu-id="7a1e8-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="7a1e8-112">Nullable</span></span> |
|----------------|------------------------------|-----|----------|
| <span data-ttu-id="7a1e8-113">ServiceControl</span><span class="sxs-lookup"><span data-stu-id="7a1e8-113">ServiceControl</span></span> | [<span data-ttu-id="7a1e8-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a1e8-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a1e8-115">Y</span><span class="sxs-lookup"><span data-stu-id="7a1e8-115">Y</span></span>   | <span data-ttu-id="7a1e8-116">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-116">N</span></span>        |
| <span data-ttu-id="7a1e8-117">Nombre</span><span class="sxs-lookup"><span data-stu-id="7a1e8-117">Name</span></span>           | [<span data-ttu-id="7a1e8-118">Formatea</span><span class="sxs-lookup"><span data-stu-id="7a1e8-118">Formatted</span></span>](formatted.md)   | <span data-ttu-id="7a1e8-119">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-119">N</span></span>   | <span data-ttu-id="7a1e8-120">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-120">N</span></span>        |
| <span data-ttu-id="7a1e8-121">Evento</span><span class="sxs-lookup"><span data-stu-id="7a1e8-121">Event</span></span>          | [<span data-ttu-id="7a1e8-122">Entero</span><span class="sxs-lookup"><span data-stu-id="7a1e8-122">Integer</span></span>](integer.md)       | <span data-ttu-id="7a1e8-123">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-123">N</span></span>   | <span data-ttu-id="7a1e8-124">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-124">N</span></span>        |
| <span data-ttu-id="7a1e8-125">Argumentos</span><span class="sxs-lookup"><span data-stu-id="7a1e8-125">Arguments</span></span>      | [<span data-ttu-id="7a1e8-126">Formatea</span><span class="sxs-lookup"><span data-stu-id="7a1e8-126">Formatted</span></span>](formatted.md)   | <span data-ttu-id="7a1e8-127">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-127">N</span></span>   | <span data-ttu-id="7a1e8-128">Y</span><span class="sxs-lookup"><span data-stu-id="7a1e8-128">Y</span></span>        |
| <span data-ttu-id="7a1e8-129">Esperar</span><span class="sxs-lookup"><span data-stu-id="7a1e8-129">Wait</span></span>           | [<span data-ttu-id="7a1e8-130">Entero</span><span class="sxs-lookup"><span data-stu-id="7a1e8-130">Integer</span></span>](integer.md)       | <span data-ttu-id="7a1e8-131">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-131">N</span></span>   | <span data-ttu-id="7a1e8-132">Y</span><span class="sxs-lookup"><span data-stu-id="7a1e8-132">Y</span></span>        |
| <span data-ttu-id="7a1e8-133">Componente\_</span><span class="sxs-lookup"><span data-stu-id="7a1e8-133">Component\_</span></span>    | [<span data-ttu-id="7a1e8-134">Identificador</span><span class="sxs-lookup"><span data-stu-id="7a1e8-134">Identifier</span></span>](identifier.md) | <span data-ttu-id="7a1e8-135">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-135">N</span></span>   | <span data-ttu-id="7a1e8-136">N</span><span class="sxs-lookup"><span data-stu-id="7a1e8-136">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="7a1e8-137">Columnas</span><span class="sxs-lookup"><span data-stu-id="7a1e8-137">Columns</span></span>

<dl> <dt>

<span data-ttu-id="7a1e8-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span><span class="sxs-lookup"><span data-stu-id="7a1e8-138"><span id="ServiceControl"></span><span id="servicecontrol"></span><span id="SERVICECONTROL"></span>ServiceControl</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-139">Esta es la clave principal de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-139">This is the primary key of this table.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e8-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span><span class="sxs-lookup"><span data-stu-id="7a1e8-140"><span id="Name"></span><span id="name"></span><span id="NAME"></span>Name</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-141">Esta columna es la cadena que nombra el servicio.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-141">This column is the string naming the service.</span></span> <span data-ttu-id="7a1e8-142">Esta columna se puede usar para controlar un servicio que no está instalado.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-142">This column can be used to control a service that is not installed.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e8-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Ceso</span><span class="sxs-lookup"><span data-stu-id="7a1e8-143"><span id="Event"></span><span id="event"></span><span id="EVENT"></span>Event</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-144">Esta columna contiene las operaciones que se van a realizar en el servicio con nombre.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-144">This column contains the operations to be performed on the named service.</span></span> <span data-ttu-id="7a1e8-145">Tenga en cuenta que al detener un servicio, también se detienen todos los servicios que dependen de ese servicio.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-145">Note that when stopping a service, all services that depend on that service are also stopped.</span></span> <span data-ttu-id="7a1e8-146">Al eliminar un servicio que se está ejecutando, el instalador detiene el servicio.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-146">When deleting a service that is running, the installer stops the service.</span></span>

<span data-ttu-id="7a1e8-147">Los valores de este campo son campos de bits que se pueden combinar en un valor único que representa varias operaciones.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-147">The values in this field are bit fields that can be combined into a single value that represents several operations.</span></span>

<span data-ttu-id="7a1e8-148">Los valores siguientes solo se usan durante la instalación de.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-148">The following values are only used during an installation.</span></span>



| <span data-ttu-id="7a1e8-149">Constante</span><span class="sxs-lookup"><span data-stu-id="7a1e8-149">Constant</span></span>                           | <span data-ttu-id="7a1e8-150">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7a1e8-150">Hexadecimal</span></span> | <span data-ttu-id="7a1e8-151">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a1e8-151">Decimal</span></span> | <span data-ttu-id="7a1e8-152">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a1e8-152">Description</span></span>                                                                        |
|------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1e8-153">**msidbServiceControlEventStart**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-153">**msidbServiceControlEventStart**</span></span>  | <span data-ttu-id="7a1e8-154">0x001</span><span class="sxs-lookup"><span data-stu-id="7a1e8-154">0x001</span></span>       | <span data-ttu-id="7a1e8-155">1</span><span class="sxs-lookup"><span data-stu-id="7a1e8-155">1</span></span>       | <span data-ttu-id="7a1e8-156">Inicia el servicio durante la [acción StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-156">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="7a1e8-157">**msidbServiceControlEventStop**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-157">**msidbServiceControlEventStop**</span></span>   | <span data-ttu-id="7a1e8-158">0x002</span><span class="sxs-lookup"><span data-stu-id="7a1e8-158">0x002</span></span>       | <span data-ttu-id="7a1e8-159">2</span><span class="sxs-lookup"><span data-stu-id="7a1e8-159">2</span></span>       | <span data-ttu-id="7a1e8-160">Detiene el servicio durante la [acción StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-160">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="7a1e8-161">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="7a1e8-161">(none)</span></span>                             | <span data-ttu-id="7a1e8-162">0x004</span><span class="sxs-lookup"><span data-stu-id="7a1e8-162">0x004</span></span>       | <span data-ttu-id="7a1e8-163">4</span><span class="sxs-lookup"><span data-stu-id="7a1e8-163">4</span></span>       | <reserved>                                                                   |
| <span data-ttu-id="7a1e8-164">**msidbServiceControlEventDelete**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-164">**msidbServiceControlEventDelete**</span></span> | <span data-ttu-id="7a1e8-165">0x008</span><span class="sxs-lookup"><span data-stu-id="7a1e8-165">0x008</span></span>       | <span data-ttu-id="7a1e8-166">8</span><span class="sxs-lookup"><span data-stu-id="7a1e8-166">8</span></span>       | <span data-ttu-id="7a1e8-167">Elimina el servicio durante la [acción DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-167">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

<span data-ttu-id="7a1e8-168">Los valores siguientes solo se usan durante la desinstalación.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-168">The following values are only used during an uninstall.</span></span>



| <span data-ttu-id="7a1e8-169">Constante</span><span class="sxs-lookup"><span data-stu-id="7a1e8-169">Constant</span></span>                                    | <span data-ttu-id="7a1e8-170">Hexadecimal</span><span class="sxs-lookup"><span data-stu-id="7a1e8-170">Hexadecimal</span></span> | <span data-ttu-id="7a1e8-171">Decimal</span><span class="sxs-lookup"><span data-stu-id="7a1e8-171">Decimal</span></span> | <span data-ttu-id="7a1e8-172">Descripción</span><span class="sxs-lookup"><span data-stu-id="7a1e8-172">Description</span></span>                                                                        |
|---------------------------------------------|-------------|---------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1e8-173">**msidbServiceControlEventUninstallStart**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-173">**msidbServiceControlEventUninstallStart**</span></span>  | <span data-ttu-id="7a1e8-174">0x010</span><span class="sxs-lookup"><span data-stu-id="7a1e8-174">0x010</span></span>       | <span data-ttu-id="7a1e8-175">16</span><span class="sxs-lookup"><span data-stu-id="7a1e8-175">16</span></span>      | <span data-ttu-id="7a1e8-176">Inicia el servicio durante la [acción StartServices](startservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-176">Starts the service during the [StartServices action](startservices-action.md).</span></span>    |
| <span data-ttu-id="7a1e8-177">**msidbServiceControlEventUninstallStop**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-177">**msidbServiceControlEventUninstallStop**</span></span>   | <span data-ttu-id="7a1e8-178">0x020</span><span class="sxs-lookup"><span data-stu-id="7a1e8-178">0x020</span></span>       | <span data-ttu-id="7a1e8-179">32</span><span class="sxs-lookup"><span data-stu-id="7a1e8-179">32</span></span>      | <span data-ttu-id="7a1e8-180">Detiene el servicio durante la [acción StopServices](stopservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-180">Stops the service during the [StopServices action](stopservices-action.md).</span></span>       |
| <span data-ttu-id="7a1e8-181">(ninguno)</span><span class="sxs-lookup"><span data-stu-id="7a1e8-181">(none)</span></span>                                      | <span data-ttu-id="7a1e8-182">0x040</span><span class="sxs-lookup"><span data-stu-id="7a1e8-182">0x040</span></span>       | <span data-ttu-id="7a1e8-183">64</span><span class="sxs-lookup"><span data-stu-id="7a1e8-183">64</span></span>      | <reserved>                                                                   |
| <span data-ttu-id="7a1e8-184">**msidbServiceControlEventUninstallDelete**</span><span class="sxs-lookup"><span data-stu-id="7a1e8-184">**msidbServiceControlEventUninstallDelete**</span></span> | <span data-ttu-id="7a1e8-185">0x080</span><span class="sxs-lookup"><span data-stu-id="7a1e8-185">0x080</span></span>       | <span data-ttu-id="7a1e8-186">128</span><span class="sxs-lookup"><span data-stu-id="7a1e8-186">128</span></span>     | <span data-ttu-id="7a1e8-187">Elimina el servicio durante la [acción DeleteServices](deleteservices-action.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-187">Deletes the service during the [DeleteServices action](deleteservices-action.md).</span></span> |



 

</dd> <dt>

<span data-ttu-id="7a1e8-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argumentos</span><span class="sxs-lookup"><span data-stu-id="7a1e8-188"><span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Arguments</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-189">Una lista de argumentos para iniciar los servicios.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-189">A list of arguments for starting services.</span></span> <span data-ttu-id="7a1e8-190">Los argumentos se separan con caracteres nulos \[ ~ \] .</span><span class="sxs-lookup"><span data-stu-id="7a1e8-190">The arguments are separated by null characters \[~\].</span></span> <span data-ttu-id="7a1e8-191">Por ejemplo, la lista de argumentos uno, dos y tres se muestran como: uno \[ ~ \] dos \[ ~ \] tres.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-191">For example, the list of arguments One, Two, and Three are listed as: One\[~\]Two\[~\]Three.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e8-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Currir</span><span class="sxs-lookup"><span data-stu-id="7a1e8-192"><span id="Wait"></span><span id="wait"></span><span id="WAIT"></span>Wait</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-193">Si se sale de este campo null o se especifica un valor de 1, el instalador espera un máximo de 30 segundos para que el servicio se complete antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-193">Leaving this field null or entering a value of 1 causes the installer to wait a maximum of 30 seconds for the service to complete before proceeding.</span></span> <span data-ttu-id="7a1e8-194">La espera se puede usar para permitir un tiempo adicional para que un evento crítico devuelva un error.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-194">The wait can be used to allow additional time for a critical event to return a failure error.</span></span> <span data-ttu-id="7a1e8-195">Un valor de 0 en este campo significa que solo debe esperar hasta que el administrador de control de servicios (SCM) notifique que este servicio está en estado pendiente antes de continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-195">A value of 0 in this field means to wait only until the service control manager (SCM) reports that this service is in a pending state before continuing with the installation.</span></span>

</dd> <dt>

<span data-ttu-id="7a1e8-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Pone\_</span><span class="sxs-lookup"><span data-stu-id="7a1e8-196"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="7a1e8-197">Clave externa para la columna uno de la [tabla de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-197">External key to column one of the [Component Table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7a1e8-198">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a1e8-198">Remarks</span></span>

<span data-ttu-id="7a1e8-199">Las acciones [StartServices](startservices-action.md), [StopServices](stopservices-action.md)y [DeleteServices](deleteservices-action.md) en [*las tablas de secuencia*](s-gly.md) procesan la información de esta tabla.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-199">The [StartServices](startservices-action.md), [StopServices](stopservices-action.md), and [DeleteServices](deleteservices-action.md) actions in [*sequence tables*](s-gly.md) process the information in this table.</span></span> <span data-ttu-id="7a1e8-200">Para obtener información sobre el uso de *tablas de secuencia*, vea [usar una tabla de secuencia](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e8-200">For information about using *sequence tables*, see [Using a Sequence Table](using-a-sequence-table.md).</span></span>

<span data-ttu-id="7a1e8-201">Use la columna nombre para iniciar, detener o eliminar servicios que se van a reemplazar por la instalación o que dependen de un nuevo servicio que se está instalando.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-201">Use the Name column to start, stop, or delete services that are being replaced by the installation or that are dependent upon a new service that is being installed.</span></span> <span data-ttu-id="7a1e8-202">Por ejemplo, si escribe el servicio en la columna ServiceControl, puede vincular este servicio a mi componente en la \_ columna componente.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-202">For example, entering MyService into the ServiceControl column can tie this service to MyComponent in the Component\_ column.</span></span> <span data-ttu-id="7a1e8-203">Si el campo de bits de la columna de eventos se establece para iniciar mientras se instala, el instalador inicia el servicio al instalar el componente.</span><span class="sxs-lookup"><span data-stu-id="7a1e8-203">If the bit field in the Event column is set for start while installing, then the installer starts MyService when installing MyComponent.</span></span>

## <a name="validation"></a><span data-ttu-id="7a1e8-204">Validación</span><span class="sxs-lookup"><span data-stu-id="7a1e8-204">Validation</span></span>

<dl>

[<span data-ttu-id="7a1e8-205">ICE03</span><span class="sxs-lookup"><span data-stu-id="7a1e8-205">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="7a1e8-206">ICE06</span><span class="sxs-lookup"><span data-stu-id="7a1e8-206">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="7a1e8-207">ICE32</span><span class="sxs-lookup"><span data-stu-id="7a1e8-207">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="7a1e8-208">ICE45</span><span class="sxs-lookup"><span data-stu-id="7a1e8-208">ICE45</span></span>](ice45.md)  
[<span data-ttu-id="7a1e8-209">ICE46</span><span class="sxs-lookup"><span data-stu-id="7a1e8-209">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="7a1e8-210">ICE69</span><span class="sxs-lookup"><span data-stu-id="7a1e8-210">ICE69</span></span>](ice69.md)  
</dl>

 

 



