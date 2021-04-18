---
description: Una aplicación COM+ es esencialmente una construcción declarativa que le permite configurar cualquier número de componentes en común. Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Configurar aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705274"
---
# <a name="configuring-com-applications"></a><span data-ttu-id="ffc04-104">Configurar aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="ffc04-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="ffc04-105">Una aplicación COM+ es esencialmente una construcción declarativa que le permite configurar cualquier número de componentes en común.</span><span class="sxs-lookup"><span data-stu-id="ffc04-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="ffc04-106">Por ejemplo, puede configurar los componentes de una aplicación con una directiva de seguridad común.</span><span class="sxs-lookup"><span data-stu-id="ffc04-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="ffc04-107">La configuración es una parte esencial del proceso de desarrollo de aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="ffc04-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="ffc04-108">La forma de configurar una aplicación determinará el modo en que COM+ proporcionará los servicios y cómo se comporta cuando se ejecuta.</span><span class="sxs-lookup"><span data-stu-id="ffc04-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="ffc04-109">Puede configurar aplicaciones COM+ mediante la herramienta de administración de servicios de componentes o los objetos e interfaces de administración que admiten scripts que proporcionan la funcionalidad subyacente de la herramienta de administración.</span><span class="sxs-lookup"><span data-stu-id="ffc04-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="ffc04-110">Para obtener más información sobre cómo realizar la administración con scripts, vea [automatizar la administración de com+](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="ffc04-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="ffc04-111">Puede configurar los elementos de los siguientes niveles en las aplicaciones COM+:</span><span class="sxs-lookup"><span data-stu-id="ffc04-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="ffc04-112">Configuración de nivel de aplicación</span><span class="sxs-lookup"><span data-stu-id="ffc04-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="ffc04-113">Configuración de nivel de componente (nivel de clase)</span><span class="sxs-lookup"><span data-stu-id="ffc04-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="ffc04-114">Configuración de nivel de interfaz</span><span class="sxs-lookup"><span data-stu-id="ffc04-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="ffc04-115">Configuración de nivel de método</span><span class="sxs-lookup"><span data-stu-id="ffc04-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="ffc04-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffc04-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="ffc04-117">La forma de instalar los componentes en una aplicación puede afectar al modo en que se pueden configurar.</span><span class="sxs-lookup"><span data-stu-id="ffc04-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="ffc04-118">Siempre debe instalar los componentes en las aplicaciones COM+ (en lugar de importarlos).</span><span class="sxs-lookup"><span data-stu-id="ffc04-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="ffc04-119">Al instalar los componentes, se registrarán por completo, junto con las interfaces y las bibliotecas de tipos, en la base de datos de registro de clases COM+ (RegDB) para que pueda configurarlos.</span><span class="sxs-lookup"><span data-stu-id="ffc04-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="ffc04-120">Configuración de Application-Level</span><span class="sxs-lookup"><span data-stu-id="ffc04-120">Application-Level Settings</span></span>



| <span data-ttu-id="ffc04-121">Atributo</span><span class="sxs-lookup"><span data-stu-id="ffc04-121">Attribute</span></span>                                                                                        | <span data-ttu-id="ffc04-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc04-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffc04-123">Activación</span><span class="sxs-lookup"><span data-stu-id="ffc04-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="ffc04-124">Especifica el tipo de aplicación: aplicación de servidor o aplicación de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ffc04-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="ffc04-125">Habilitar comprobaciones de acceso</span><span class="sxs-lookup"><span data-stu-id="ffc04-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="ffc04-126">Activa y desactiva la comprobación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ffc04-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="ffc04-127">Nivel de seguridad</span><span class="sxs-lookup"><span data-stu-id="ffc04-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="ffc04-128">Especifica que las comprobaciones de acceso se realizarán en el nivel de proceso (niveles de comprobación de acceso generados a partir de los roles) o en los niveles de componente (seguridad basada en roles).</span><span class="sxs-lookup"><span data-stu-id="ffc04-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="ffc04-129">Nivel de autenticación</span><span class="sxs-lookup"><span data-stu-id="ffc04-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="ffc04-130">Establece el nivel de autenticación utilizado en las llamadas a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ffc04-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ffc04-131">Nivel de suplantación</span><span class="sxs-lookup"><span data-stu-id="ffc04-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="ffc04-132">Establece el nivel de suplantación utilizado en las llamadas a otras aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="ffc04-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="ffc04-133">MSMQ</span><span class="sxs-lookup"><span data-stu-id="ffc04-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="ffc04-134">Especifica que los componentes de la aplicación usarán los servicios de cola.</span><span class="sxs-lookup"><span data-stu-id="ffc04-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="ffc04-135">Habilitar CRM</span><span class="sxs-lookup"><span data-stu-id="ffc04-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="ffc04-136">Habilita el uso de administradores de compensación de recursos.</span><span class="sxs-lookup"><span data-stu-id="ffc04-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="ffc04-137">Ejecutar la aplicación como servicio</span><span class="sxs-lookup"><span data-stu-id="ffc04-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="ffc04-138">Configura e implementa una aplicación de servidor COM+ como un servicio NT.</span><span class="sxs-lookup"><span data-stu-id="ffc04-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="ffc04-139">Servicio SOAP de COM+</span><span class="sxs-lookup"><span data-stu-id="ffc04-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="ffc04-140">Expone una aplicación COM+ como un servicio Web XML.</span><span class="sxs-lookup"><span data-stu-id="ffc04-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="ffc04-141">Agrupación de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ffc04-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="ffc04-142">Agrega escalabilidad para los procesos de un solo subproceso y se integra con el servicio de reciclaje de aplicaciones COM+.</span><span class="sxs-lookup"><span data-stu-id="ffc04-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="ffc04-143">Reciclaje de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="ffc04-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="ffc04-144">Aumenta la estabilidad de la aplicación al cerrar correctamente un proceso asociado a una aplicación y reiniciarlo.</span><span class="sxs-lookup"><span data-stu-id="ffc04-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="ffc04-145">Proceso de volcado</span><span class="sxs-lookup"><span data-stu-id="ffc04-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="ffc04-146">Vuelca todo el estado de un proceso sin terminarlo, con fines de depuración.</span><span class="sxs-lookup"><span data-stu-id="ffc04-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="ffc04-147">Cierre de proceso de servidor</span><span class="sxs-lookup"><span data-stu-id="ffc04-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="ffc04-148">Cierra un proceso después de un período de inactividad especificado.</span><span class="sxs-lookup"><span data-stu-id="ffc04-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="ffc04-149">Permisos</span><span class="sxs-lookup"><span data-stu-id="ffc04-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="ffc04-150">Deshabilita los cambios en los valores de configuración, incluida la eliminación.</span><span class="sxs-lookup"><span data-stu-id="ffc04-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="ffc04-151">Identidad de seguridad</span><span class="sxs-lookup"><span data-stu-id="ffc04-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="ffc04-152">Especifica la identidad en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ffc04-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="ffc04-153">Iniciar en el depurador</span><span class="sxs-lookup"><span data-stu-id="ffc04-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="ffc04-154">Especifica que la aplicación se iniciará en un depurador con la configuración de línea de comandos especificada por el usuario.</span><span class="sxs-lookup"><span data-stu-id="ffc04-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="ffc04-155">Habilitar compatibilidad con 3GB</span><span class="sxs-lookup"><span data-stu-id="ffc04-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="ffc04-156">Habilita el uso del espacio de direcciones de memoria de proceso extendido.</span><span class="sxs-lookup"><span data-stu-id="ffc04-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="ffc04-157">Configuración de Component-Level (nivel de clase)</span><span class="sxs-lookup"><span data-stu-id="ffc04-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ffc04-158">Atributo</span><span class="sxs-lookup"><span data-stu-id="ffc04-158">Attribute</span></span></th>
<th><span data-ttu-id="ffc04-159">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc04-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ffc04-160"><a href="configuring-transactions.md">Transactions</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-161">Establece los requisitos de transacción automática deshabilitado, no admitido, admitido, requerido o requiere nuevo.</span><span class="sxs-lookup"><span data-stu-id="ffc04-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc04-162"><a href="setting-the-synchronization-attribute.md">Sincronización</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-163">Establece los requisitos de sincronización deshabilitados, no admitidos, admitidos, obligatorios o requiere nuevos.</span><span class="sxs-lookup"><span data-stu-id="ffc04-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc04-164"><a href="enabling-jit-activation-for-a-component.md">Activación JIT</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-165">Habilita la activación Just-in-Time.</span><span class="sxs-lookup"><span data-stu-id="ffc04-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc04-166"><a href="configuring-a-component-to-be-pooled.md">Agrupación de objetos</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-167">Habilita la agrupación de objetos.</span><span class="sxs-lookup"><span data-stu-id="ffc04-167">Enables object pooling.</span></span> <span data-ttu-id="ffc04-168">Se pueden configurar los valores de tiempo de espera mínimo y máximo del grupo y el tiempo de espera del objeto.</span><span class="sxs-lookup"><span data-stu-id="ffc04-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc04-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Construcción de objetos</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-170">Habilita la construcción de objetos con parámetros con una cadena de constructor especificada administrativamente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="ffc04-171">La cadena del constructor no se debe utilizar para almacenar información confidencial de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ffc04-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc04-172"><a href="enabling-access-checks-at-the-component-level.md">Comprobaciones de acceso de nivel de componente</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-173">Activa o desactiva la comprobación de seguridad basada en roles de nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc04-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Asignación de roles declarativos</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-175">Habilita la asignación explícita de roles al componente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc04-176"><a href="persistent-client-side-failures.md">Queue (clase de excepción)</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-177">Indica una clase de excepción para controlar los errores del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc04-178"><a href="com--instrumentation-concepts.md">Estadísticas y eventos de instrumentación</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-179">Habilita los informes detallados de eventos del sistema y estadísticas de objetos.</span><span class="sxs-lookup"><span data-stu-id="ffc04-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ffc04-180"><a href="context-activation.md">Contexto de activación</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-181">Habilita la activación forzada de un objeto en el contexto del autor de la llamada o en el contexto predeterminado.</span><span class="sxs-lookup"><span data-stu-id="ffc04-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ffc04-182"><a href="what-s-new-in-com--1-5.md">Crear componentes privados</a></span><span class="sxs-lookup"><span data-stu-id="ffc04-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="ffc04-183">Marca el componente como privado para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="ffc04-183">Marks component as private to the application.</span></span> <span data-ttu-id="ffc04-184">Un componente privado solo se puede visualizar y activar en otros componentes de la misma aplicación.</span><span class="sxs-lookup"><span data-stu-id="ffc04-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="ffc04-185">Interface-Level configuración</span><span class="sxs-lookup"><span data-stu-id="ffc04-185">Interface-Level Setting</span></span>



| <span data-ttu-id="ffc04-186">Atributo</span><span class="sxs-lookup"><span data-stu-id="ffc04-186">Attribute</span></span>                                                                                           | <span data-ttu-id="ffc04-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc04-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffc04-188">En cola</span><span class="sxs-lookup"><span data-stu-id="ffc04-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="ffc04-189">Indica una interfaz queuable, definida en IDL.</span><span class="sxs-lookup"><span data-stu-id="ffc04-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="ffc04-190">Asignación de roles declarativos</span><span class="sxs-lookup"><span data-stu-id="ffc04-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="ffc04-191">Habilita la asignación explícita de roles a la interfaz, así como a los roles heredados implícitamente desde el nivel de componente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="ffc04-192">Method-Level configuración</span><span class="sxs-lookup"><span data-stu-id="ffc04-192">Method-Level Setting</span></span>



| <span data-ttu-id="ffc04-193">Atributo</span><span class="sxs-lookup"><span data-stu-id="ffc04-193">Attribute</span></span>                                                                                           | <span data-ttu-id="ffc04-194">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffc04-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ffc04-195">Auto-Done</span><span class="sxs-lookup"><span data-stu-id="ffc04-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="ffc04-196">Desactiva automáticamente el objeto en el método y el resultado de la transacción.</span><span class="sxs-lookup"><span data-stu-id="ffc04-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="ffc04-197">Asignación de roles declarativos</span><span class="sxs-lookup"><span data-stu-id="ffc04-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="ffc04-198">Habilita la asignación explícita de roles al método, así como a los roles heredados implícitamente de los niveles de interfaz y de componente.</span><span class="sxs-lookup"><span data-stu-id="ffc04-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="ffc04-199">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffc04-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffc04-200">Automatizar la administración de COM+</span><span class="sxs-lookup"><span data-stu-id="ffc04-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="ffc04-201">Crear aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="ffc04-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="ffc04-202">Implementación de aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="ffc04-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




