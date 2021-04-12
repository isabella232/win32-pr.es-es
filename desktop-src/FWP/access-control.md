---
title: Access Control (plataforma de filtrado de Windows)
description: En la plataforma de filtrado de Windows (WFP), el servicio motor de filtrado de base (BFE) implementa el modelo de control de acceso de Windows estándar basado en los tokens de acceso y los descriptores de seguridad.
ms.assetid: 936ad5f0-d5cd-47ed-b9e5-a7d82a4da603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0df63b6fe92b18614a7ccf205ccf826927664ee
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "104361796"
---
# <a name="access-control-windows-filtering-platform"></a><span data-ttu-id="ef4f1-103">Access Control (plataforma de filtrado de Windows)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-103">Access Control (Windows Filtering Platform)</span></span>

<span data-ttu-id="ef4f1-104">En la plataforma de filtrado de Windows (WFP), el servicio motor de filtrado de base (BFE) implementa el [modelo de control de acceso de Windows](/windows/desktop/SecAuthZ/access-control-model) estándar basado en los tokens de acceso y los descriptores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-104">In Windows Filtering Platform (WFP), the Base Filtering Engine (BFE) service implements the standard [Windows access control model](/windows/desktop/SecAuthZ/access-control-model) based on access tokens and security descriptors.</span></span>

## <a name="access-control-model"></a><span data-ttu-id="ef4f1-105">Modelo de Access Control</span><span class="sxs-lookup"><span data-stu-id="ef4f1-105">Access Control Model</span></span>

<span data-ttu-id="ef4f1-106">Los descriptores de seguridad se pueden especificar al agregar nuevos objetos de WFP, como filtros y subcapas.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-106">Security descriptors can be specified when adding new WFP objects, such as filters and sub-layers.</span></span> <span data-ttu-id="ef4f1-107">Los descriptores de seguridad se administran mediante las funciones de administración de WFP **Fwpm \* GetSecurityInfo0** y **Fwpm \* SetSecurityInfo0**, donde \* *\** _ representa el nombre del objeto WFP.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-107">Security descriptors are managed using the WFP management functions **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0**, where \**\** _ stands for the WFP object's name.</span></span> <span data-ttu-id="ef4f1-108">Estas funciones son semánticamente idénticas a las funciones de Windows [_ *GetSecurityInfo* \*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-108">These functions are semantically identical to the Windows [_ *GetSecurityInfo*\*](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) and [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) functions.</span></span>

> [!Note]  
> <span data-ttu-id="ef4f1-109">No se puede llamar a las funciones **Fwpm \* SetSecurityInfo0** desde una transacción explícita.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-109">The **Fwpm\*SetSecurityInfo0** functions cannot be called from within an explicit transaction.</span></span>

 

> [!Note]  
> <span data-ttu-id="ef4f1-110">Solo se puede llamar a las funciones **Fwpm \* SetSecurityInfo0** desde una sesión dinámica si se usan para administrar un objeto dinámico creado dentro de la misma sesión.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-110">The **Fwpm\*SetSecurityInfo0** functions can only be called from within a dynamic session if they are being used to manage a dynamic object created within the same session.</span></span>

 

<span data-ttu-id="ef4f1-111">El descriptor de seguridad predeterminado para el motor de filtro (el objeto de motor raíz en el diagrama siguiente) es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-111">The default security descriptor for the filter engine (the root Engine object in the diagram below) is as follows.</span></span>

-   <span data-ttu-id="ef4f1-112">Conceda derechos de acceso **genéricos \_** (GA) al grupo de administradores integrado.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-112">Grant **GENERIC\_ALL** (GA) access rights to the built-in Administrators group.</span></span>
-   <span data-ttu-id="ef4f1-113">Conceda derechos de acceso genéricos de **\_ escritura** genérica de **\_ lectura** (de **GW) ( \_** GX) a los operadores de configuración de red.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-113">Grant **GENERIC\_READ** (GR) **GENERIC\_WRITE** (GW) **GENERIC\_EXECUTE** (GX) access rights to network configuration operators.</span></span>
-   <span data-ttu-id="ef4f1-114">Conceda derechos de acceso de **GRGWGX** a los siguientes identificadores de seguridad de servicio (SSID): MpsSvc (Firewall de Windows), NapAgent (agente de protección de acceso a redes), policyagent (agente de directivas IPSec), RPCSS (llamada a procedimiento remoto) y WdiServiceHost (host de servicio de diagnóstico).</span><span class="sxs-lookup"><span data-stu-id="ef4f1-114">Grant **GRGWGX** access rights to the following service security identifiers (SSIDs): MpsSvc (Windows Firewall), NapAgent (Network Access Protection Agent), PolicyAgent (IPsec Policy Agent), RpcSs (Remote Procedure Call), and WdiServiceHost (Diagnostic Service Host).</span></span>
-   <span data-ttu-id="ef4f1-115">Conceda **FWPM \_ ACTRL \_ Open** y **FWPM \_ ACTRL \_ clasificación** a todos los usuarios.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-115">Grant **FWPM\_ACTRL\_OPEN** and **FWPM\_ACTRL\_CLASSIFY** to everyone.</span></span> <span data-ttu-id="ef4f1-116">(Estos son derechos de acceso específicos de WFP, que se describen en la tabla siguiente).</span><span class="sxs-lookup"><span data-stu-id="ef4f1-116">(These are WFP-specific access rights, described in table below.)</span></span>

<span data-ttu-id="ef4f1-117">Los descriptores de seguridad predeterminados restantes se derivan a través de la herencia.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-117">The remaining default security descriptors are derived through inheritance.</span></span>

<span data-ttu-id="ef4f1-118">Hay algunas comprobaciones de acceso, como las llamadas de función **Fwpm \* Add0**, **Fwpm \* CreateEnumHandle0**, **Fwpm \* SubscribeChanges0** , que no se pueden realizar en el nivel de objeto individual.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-118">There are some access checks, such as for **Fwpm\*Add0**, **Fwpm\*CreateEnumHandle0**, **Fwpm\*SubscribeChanges0** function calls, that cannot be done at the individual object level.</span></span> <span data-ttu-id="ef4f1-119">Para estas funciones, hay objetos de contenedor para cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-119">For these functions, there are container objects for each object type.</span></span> <span data-ttu-id="ef4f1-120">En el caso de los tipos de objeto estándar (por ejemplo, proveedores, llamadas, filtros), las funciones **Fwpm \* GetSecurityInfo0** y **Fwpm \* SetSecurityInfo0** existentes están sobrecargadas, de modo que un parámetro **GUID** null identifica el contenedor asociado.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-120">For the standard object types (for example, providers, callouts, filters), the existing **Fwpm\*GetSecurityInfo0** and **Fwpm\*SetSecurityInfo0** functions are overloaded, such that a null **GUID** parameter identifies the associated container.</span></span> <span data-ttu-id="ef4f1-121">Para los demás tipos de objeto (por ejemplo, eventos de red y asociaciones de seguridad de IPsec), existen funciones explícitas para administrar la información de seguridad del contenedor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-121">For the other object types (for example, network events and IPsec security associations), there are explicit functions for managing the container's security information.</span></span>

<span data-ttu-id="ef4f1-122">BFE admite la herencia automática de entradas de control de acceso (ACE) de lista de Access Control discrecional (DACL).</span><span class="sxs-lookup"><span data-stu-id="ef4f1-122">BFE supports automatic inheritance of Discretionary Access Control List (DACL) access control entries (ACEs).</span></span> <span data-ttu-id="ef4f1-123">BFE no es compatible con las ACE de la lista de Access Control del sistema (SACL).</span><span class="sxs-lookup"><span data-stu-id="ef4f1-123">BFE does not support System Access Control List (SACL) ACEs.</span></span> <span data-ttu-id="ef4f1-124">Los objetos heredan las ACE de su contenedor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-124">Objects inherit ACEs from their container.</span></span> <span data-ttu-id="ef4f1-125">Los contenedores heredan las ACE del motor de filtro.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-125">Containers inherit ACEs from the filter engine.</span></span> <span data-ttu-id="ef4f1-126">Las rutas de propagación se muestran en el diagrama siguiente.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-126">The propagation paths are shown in the diagram below.</span></span>

![Diagrama que muestra las rutas de propagación de ACE, comenzando por ' Engine '.](images/access-control.jpg)

<span data-ttu-id="ef4f1-128">En el caso de los tipos de objeto estándar, BFE aplica todos los derechos de acceso genéricos y estándar.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-128">For the standard object types, BFE enforces all the generic and standard access rights.</span></span> <span data-ttu-id="ef4f1-129">Además, WFP define los siguientes derechos de acceso específicos.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-129">In addition, WFP defines the following specific access rights.</span></span>



| <span data-ttu-id="ef4f1-130">Derecho de acceso de WFP</span><span class="sxs-lookup"><span data-stu-id="ef4f1-130">WFP Access Right</span></span>                                                                                                                        | <span data-ttu-id="ef4f1-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="ef4f1-131">Description</span></span>                                                                                                                                                              |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef4f1-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-132"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span><br/>                                       | <span data-ttu-id="ef4f1-133">Necesario para agregar un objeto a un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-133">Required to add an object to a container.</span></span><br/>                                                                                                                     |
| <span data-ttu-id="ef4f1-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-134"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>                       | <span data-ttu-id="ef4f1-135">Necesario para crear una asociación con un objeto.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-135">Required to create an association to an object.</span></span> <span data-ttu-id="ef4f1-136">Por ejemplo, para agregar un filtro que haga referencia a una llamada, el llamador debe tener \_ acceso de vínculo de adición a la llamada.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-136">For example, to add a filter that references a callout, the caller must have ADD\_LINK access to the callout.</span></span><br/> |
| <span data-ttu-id="ef4f1-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-137"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span><br/>    | <span data-ttu-id="ef4f1-138">Requerido para iniciar una transacción de lectura explícita.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-138">Required to begin an explicit read transaction.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ef4f1-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-139"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span><br/> | <span data-ttu-id="ef4f1-140">Requerido para iniciar una transacción de escritura explícita.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-140">Required to begin an explicit write transaction.</span></span><br/>                                                                                                              |
| <span data-ttu-id="ef4f1-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_clasificación de ACTRL de FWPM \_**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-141"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span><br/>                        | <span data-ttu-id="ef4f1-142">Necesario para clasificar en una capa de modo de usuario.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-142">Required to classify against a user-mode layer.</span></span><br/>                                                                                                               |
| <span data-ttu-id="ef4f1-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL ( \_ enumeración)**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-143"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span><br/>                                    | <span data-ttu-id="ef4f1-144">Necesario para enumerar los objetos de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-144">Required to enumerate the objects in a container.</span></span> <span data-ttu-id="ef4f1-145">Sin embargo, el enumerador solo devuelve los objetos a los que el autor de la llamada tiene acceso de lectura de FWPM \_ ACTRL \_ .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-145">However, the enumerator only returns objects to which the caller has FWPM\_ACTRL\_READ access.</span></span><br/>              |
| <span data-ttu-id="ef4f1-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-146"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span><br/>                                    | <span data-ttu-id="ef4f1-147">Necesario para abrir una sesión con BFE.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-147">Required to open a session with BFE.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="ef4f1-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-148"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span><br/>                                    | <span data-ttu-id="ef4f1-149">Necesario para leer las propiedades de un objeto.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-149">Required to read an object's properties.</span></span><br/>                                                                                                                      |
| <span data-ttu-id="ef4f1-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM \_ ACTRL \_ leer \_ estadísticas**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-150"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span><br/>                 | <span data-ttu-id="ef4f1-151">Necesario para leer las estadísticas.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-151">Required to read statistics.</span></span><br/>                                                                                                                                  |
| <span data-ttu-id="ef4f1-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**suscripción a FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-152"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span><br/>                     | <span data-ttu-id="ef4f1-153">Necesario para suscribirse a las notificaciones.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-153">Required to subscribe for notifications.</span></span> <span data-ttu-id="ef4f1-154">Los suscriptores solo recibirán notificaciones de los objetos a los que tengan acceso de lectura de FWPM \_ ACTRL \_ .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-154">Subscribers will only receive notifications for objects to which they have FWPM\_ACTRL\_READ access.</span></span><br/>                 |
| <span data-ttu-id="ef4f1-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-155"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span><br/>                                 | <span data-ttu-id="ef4f1-156">Necesario para establecer las opciones del motor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-156">Required to set engine options.</span></span><br/>                                                                                                                               |



 

<span data-ttu-id="ef4f1-157">BFE omite todas las comprobaciones de acceso para los llamadores en modo kernel.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-157">BFE skips all access checks for kernel-mode callers.</span></span>

<span data-ttu-id="ef4f1-158">Para evitar que los administradores se bloqueen a través de BFE, los miembros del grupo de administradores integrados siempre reciben **FWPM \_ ACTRL \_ abierto** en el objeto Engine.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-158">In order to prevent administrators from locking themselves out of BFE, members of the built-in administrators group are always granted **FWPM\_ACTRL\_OPEN** to the engine object.</span></span> <span data-ttu-id="ef4f1-159">Por lo tanto, un administrador puede recuperar el acceso a través de los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-159">Thus, an administrator can regain access through the following steps.</span></span>

-   <span data-ttu-id="ef4f1-160">Habilite el **privilegio \_ usar \_ \_ nombre de propiedad** .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-160">Enable the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="ef4f1-161">Llame a [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="ef4f1-161">Call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span> <span data-ttu-id="ef4f1-162">La llamada se realiza correctamente porque el autor de la llamada es miembro de los administradores integrados.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-162">The call succeeds because the caller is a member of Built-in Administrators.</span></span>
-   <span data-ttu-id="ef4f1-163">Tomar posesión del objeto de motor.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-163">Take ownership of the engine object.</span></span> <span data-ttu-id="ef4f1-164">Esto se realiza correctamente porque el autor de la llamada tiene el privilegio de **\_ tomar \_ posesión del \_ nombre** .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-164">This succeeds because the caller has the **SE\_TAKE\_OWNERSHIP\_NAME** privilege.</span></span>
-   <span data-ttu-id="ef4f1-165">Actualice la DACL.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-165">Update the DACL.</span></span> <span data-ttu-id="ef4f1-166">Esto se realiza correctamente porque el propietario siempre tiene acceso de **escritura de \_ DAC**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-166">This succeeds because the owner always has **WRITE\_DAC** access</span></span>

<span data-ttu-id="ef4f1-167">Dado que BFE admite su propia auditoría personalizada, no genera auditorías de acceso a objetos genéricos.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-167">Since BFE supports its own custom auditing, it does not generate generic object access audits.</span></span> <span data-ttu-id="ef4f1-168">Por lo tanto, se omite la SACL.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-168">Thus, the SACL is ignored.</span></span>

## <a name="wfp-required-access-rights"></a><span data-ttu-id="ef4f1-169">Derechos de acceso de WFP requeridos</span><span class="sxs-lookup"><span data-stu-id="ef4f1-169">WFP Required Access Rights</span></span>

<span data-ttu-id="ef4f1-170">En la tabla siguiente se muestran los derechos de acceso requeridos por las funciones de WFP para tener acceso a varios objetos de plataforma de filtrado.</span><span class="sxs-lookup"><span data-stu-id="ef4f1-170">The table below shows the access rights required by the WFP functions in order to access various filtering platform objects.</span></span> <span data-ttu-id="ef4f1-171">Las **\* *funciones FwpmFilter _ se muestran como ejemplo de acceso a los objetos estándar. Todas las demás funciones que tienen acceso a objetos estándar siguen el modelo de acceso de* las funciones _ FwpmFilter \*** .</span><span class="sxs-lookup"><span data-stu-id="ef4f1-171">The **FwpmFilter\**_ functions are listed as an example for accessing the standard objects. All the other functions that access standard objects follow the _\* FwpmFilter\**\* functions access model.</span></span>



<span data-ttu-id="ef4f1-172">Función</span><span class="sxs-lookup"><span data-stu-id="ef4f1-172">Function</span></span>

<span data-ttu-id="ef4f1-173">Objeto comprobado</span><span class="sxs-lookup"><span data-stu-id="ef4f1-173">Object Checked</span></span>

<span data-ttu-id="ef4f1-174">Acceso requerido</span><span class="sxs-lookup"><span data-stu-id="ef4f1-174">Access Required</span></span>

[<span data-ttu-id="ef4f1-175">**FwpmEngineOpen0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-175">**FwpmEngineOpen0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0)

<span data-ttu-id="ef4f1-176">Motor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-176">Engine</span></span>

<span data-ttu-id="ef4f1-177">**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-177">**FWPM\_ACTRL\_OPEN**</span></span>

[<span data-ttu-id="ef4f1-178">**FwpmEngineGetOption0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-178">**FwpmEngineGetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginegetoption0)

<span data-ttu-id="ef4f1-179">Motor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-179">Engine</span></span>

<span data-ttu-id="ef4f1-180">**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-180">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-181">**FwpmEngineSetOption0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-181">**FwpmEngineSetOption0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)

<span data-ttu-id="ef4f1-182">Motor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-182">Engine</span></span>

<span data-ttu-id="ef4f1-183">**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-183">**FWPM\_ACTRL\_WRITE**</span></span>

[<span data-ttu-id="ef4f1-184">**FwpmSessionCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-184">**FwpmSessionCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmsessioncreateenumhandle0)

<span data-ttu-id="ef4f1-185">Motor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-185">Engine</span></span>

<span data-ttu-id="ef4f1-186">**FWPM \_ ACTRL ( \_ enumeración)**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-186">**FWPM\_ACTRL\_ENUM**</span></span>

[<span data-ttu-id="ef4f1-187">**FwpmTransactionBegin0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-187">**FwpmTransactionBegin0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0)

<span data-ttu-id="ef4f1-188">Motor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-188">Engine</span></span>

<span data-ttu-id="ef4f1-189">**FWPM \_ ACTRL \_ Begin \_ lectura \_ TXN**  &  **FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-189">**FWPM\_ACTRL\_BEGIN\_READ\_TXN** & **FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>

[<span data-ttu-id="ef4f1-190">**FwpmFilterAdd0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-190">**FwpmFilterAdd0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)

<span data-ttu-id="ef4f1-191">Proveedor de contenedores</span><span class="sxs-lookup"><span data-stu-id="ef4f1-191">Container Provider</span></span><br/> <span data-ttu-id="ef4f1-192">Nivel</span><span class="sxs-lookup"><span data-stu-id="ef4f1-192">Layer</span></span><br/> <span data-ttu-id="ef4f1-193">Sub-Layer</span><span class="sxs-lookup"><span data-stu-id="ef4f1-193">Sub-Layer</span></span><br/> <span data-ttu-id="ef4f1-194">Llamada</span><span class="sxs-lookup"><span data-stu-id="ef4f1-194">Callout</span></span><br/> <span data-ttu-id="ef4f1-195">Contexto de proveedor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-195">Provider Context</span></span><br/>

<span data-ttu-id="ef4f1-196">**FWPM \_ ACTRL \_ ADDFWPM \_ ACTRL \_ Add \_ Link**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-196">**FWPM\_ACTRL\_ADDFWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ef4f1-197">**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-197">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ef4f1-198">**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-198">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ef4f1-199">**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-199">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/> <span data-ttu-id="ef4f1-200">**FWPM \_ ACTRL \_ agregar \_ vínculo**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-200">**FWPM\_ACTRL\_ADD\_LINK**</span></span><br/>

<span data-ttu-id="ef4f1-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-201">[**FwpmFilterDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebyid0)[**FwpmFilterDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilterdeletebykey0)</span></span><br/>

<span data-ttu-id="ef4f1-202">Filter</span><span class="sxs-lookup"><span data-stu-id="ef4f1-202">Filter</span></span>

<span data-ttu-id="ef4f1-203">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-203">**DELETE**</span></span>

<span data-ttu-id="ef4f1-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-204">[**FwpmFilterGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbyid0)[**FwpmFilterGetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltergetbykey0)</span></span><br/>

<span data-ttu-id="ef4f1-205">Filter</span><span class="sxs-lookup"><span data-stu-id="ef4f1-205">Filter</span></span>

<span data-ttu-id="ef4f1-206">**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-206">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-207">**FwpmFilterCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-207">**FwpmFilterCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltercreateenumhandle0)

<span data-ttu-id="ef4f1-208">Filtro de contenedor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-208">Container Filter</span></span><br/>

<span data-ttu-id="ef4f1-209">**FWPM \_ ACTRL \_ ENUMFWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-209">**FWPM\_ACTRL\_ENUMFWPM\_ACTRL\_READ**</span></span><br/>

[<span data-ttu-id="ef4f1-210">**FwpmFilterSubscribeChanges0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-210">**FwpmFilterSubscribeChanges0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscribechanges0)

<span data-ttu-id="ef4f1-211">Contenedor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-211">Container</span></span>

<span data-ttu-id="ef4f1-212">**suscripción a FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-212">**FWPM\_ACTRL\_SUBSCRIBE**</span></span>

[<span data-ttu-id="ef4f1-213">**FwpmFilterSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-213">**FwpmFilterSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfiltersubscriptionsget0)

<span data-ttu-id="ef4f1-214">Contenedor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-214">Container</span></span>

<span data-ttu-id="ef4f1-215">**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-215">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-216">**IPsecGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-216">**IPsecGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0)

<span data-ttu-id="ef4f1-217">BD de IPsec SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-217">IPsec SA DB</span></span>

<span data-ttu-id="ef4f1-218">**FWPM \_ ACTRL \_ leer \_ estadísticas**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-218">**FWPM\_ACTRL\_READ\_STATS**</span></span>

<span data-ttu-id="ef4f1-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-219">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0)[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0)</span></span><br/> [<span data-ttu-id="ef4f1-220">**IPsecSaContextAddInbound0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-220">**IPsecSaContextAddInbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0)<br/> [<span data-ttu-id="ef4f1-221">**IPsecSaContextAddOutbound0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-221">**IPsecSaContextAddOutbound0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0)<br/>

<span data-ttu-id="ef4f1-222">BD de IPsec SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-222">IPsec SA DB</span></span>

<span data-ttu-id="ef4f1-223">**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-223">**FWPM\_ACTRL\_ADD**</span></span>

<span data-ttu-id="ef4f1-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-224">[**IPsecSaContextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)[**IPsecSaContextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)</span></span><br/>

<span data-ttu-id="ef4f1-225">BD de IPsec SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-225">IPsec SA DB</span></span>

<span data-ttu-id="ef4f1-226">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-226">**DELETE**</span></span>

[<span data-ttu-id="ef4f1-227">**IPsecSaContextGetById0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-227">**IPsecSaContextGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0)

<span data-ttu-id="ef4f1-228">BD de IPsec SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-228">IPsec SA DB</span></span>

<span data-ttu-id="ef4f1-229">**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-229">**FWPM\_ACTRL\_READ**</span></span>

<span data-ttu-id="ef4f1-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-230">[**IPsecSaContextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)[**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)</span></span><br/>

<span data-ttu-id="ef4f1-231">BD de IPsec SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-231">IPsec SA DB</span></span>

<span data-ttu-id="ef4f1-232">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-232">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-233">**IkeextGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-233">**IkeextGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0)

<span data-ttu-id="ef4f1-234">BD DE IKE SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-234">IKE SA DB</span></span>

<span data-ttu-id="ef4f1-235">**FWPM \_ ACTRL \_ leer \_ estadísticas**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-235">**FWPM\_ACTRL\_READ\_STATS**</span></span>

[<span data-ttu-id="ef4f1-236">**IkeextSaDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-236">**IkeextSaDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsadeletebyid0)

<span data-ttu-id="ef4f1-237">BD DE IKE SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-237">IKE SA DB</span></span>

<span data-ttu-id="ef4f1-238">**DELETE**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-238">**DELETE**</span></span>

[<span data-ttu-id="ef4f1-239">**IkeextSaGetById0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-239">**IkeextSaGetById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsagetbyid0)

<span data-ttu-id="ef4f1-240">BD DE IKE SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-240">IKE SA DB</span></span>

<span data-ttu-id="ef4f1-241">**FWPM \_ ACTRL \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-241">**FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-242">**IkeextSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-242">**IkeextSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextsacreateenumhandle0)

<span data-ttu-id="ef4f1-243">BD DE IKE SA</span><span class="sxs-lookup"><span data-stu-id="ef4f1-243">IKE SA DB</span></span>

<span data-ttu-id="ef4f1-244">**FWPM \_ ACTRL \_ enum**  &  **FWPM \_ ACTRL \_ Read**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-244">**FWPM\_ACTRL\_ENUM** & **FWPM\_ACTRL\_READ**</span></span>

[<span data-ttu-id="ef4f1-245">**FwpmNetEventCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-245">**FwpmNetEventCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0)

<span data-ttu-id="ef4f1-246">Contenedor</span><span class="sxs-lookup"><span data-stu-id="ef4f1-246">Container</span></span>

<span data-ttu-id="ef4f1-247">**FWPM \_ ACTRL ( \_ enumeración)**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-247">**FWPM\_ACTRL\_ENUM**</span></span>

<span data-ttu-id="ef4f1-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span><span class="sxs-lookup"><span data-stu-id="ef4f1-248">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0)[**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)</span></span><br/>

<span data-ttu-id="ef4f1-249">Ninguna comprobación de acceso adicional más allá de las de los filtros y contextos de proveedor individuales</span><span class="sxs-lookup"><span data-stu-id="ef4f1-249">No additional access checks beyond those for the individual filters and provider contexts</span></span>



 

## <a name="related-topics"></a><span data-ttu-id="ef4f1-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ef4f1-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef4f1-251">**Derechos de acceso estándar**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-251">**Standard Access Rights**</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[<span data-ttu-id="ef4f1-252">Modelo de control de acceso de Windows</span><span class="sxs-lookup"><span data-stu-id="ef4f1-252">Windows access control model</span></span>](/windows/desktop/SecAuthZ/access-control-model)
</dt> <dt>

[<span data-ttu-id="ef4f1-253">**Identificadores de derechos de acceso de la plataforma de filtrado de Windows**</span><span class="sxs-lookup"><span data-stu-id="ef4f1-253">**Windows Filtering Platform Access Rights Identifiers**</span></span>](access-right-identifiers.md)
</dt> </dl>

 

