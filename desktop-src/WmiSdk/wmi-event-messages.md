---
description: En la lista siguiente se enumeran los eventos admitidos por los registros WMI en Windows Vista y sistemas operativos posteriores.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Mensajes de eventos WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715827"
---
# <a name="wmi-event-messages"></a><span data-ttu-id="fec0b-103">Mensajes de eventos WMI</span><span class="sxs-lookup"><span data-stu-id="fec0b-103">WMI Event Messages</span></span>

<span data-ttu-id="fec0b-104">En la lista siguiente se enumeran los eventos admitidos por los registros WMI en Windows Vista y sistemas operativos posteriores.</span><span class="sxs-lookup"><span data-stu-id="fec0b-104">The following list lists events supported by WMI logs in Windows Vista and later operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="fec0b-105">La siguiente documentación está diseñada para desarrolladores y administradores de ti.</span><span class="sxs-lookup"><span data-stu-id="fec0b-105">The following documentation is designed for developers and IT administrators.</span></span> <span data-ttu-id="fec0b-106">Si está intentando resolver un mensaje de error de WMI en el sistema doméstico, consulte el sitio web de [soporte técnico de Microsoft](https://support.microsoft.com/) .</span><span class="sxs-lookup"><span data-stu-id="fec0b-106">If you are attempting to resolve a WMI error message on your home system, please refer to the [Microsoft Support](https://support.microsoft.com/) website.</span></span>

 

<dl> <dt>

<span data-ttu-id="fec0b-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repositorio MC de WBEM \_ \_ incoherente**</span><span class="sxs-lookup"><span data-stu-id="fec0b-107"><span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**WBEM\_MC\_REPOSITORY\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-108">1073747424 (0x400015E0)</span><span class="sxs-lookup"><span data-stu-id="fec0b-108">1073747424 (0x400015E0)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-109">El servicio Instrumental de administración de Windows detectó una incoherencia con el repositorio WMI en el directorio *% WINDIR% \\ system32 \\ WBEM \\* y no pudo recuperarlo.</span><span class="sxs-lookup"><span data-stu-id="fec0b-109">The Windows Management Instrumentation Service detected an inconsistency with the WMI repository in the directory *%windir%\\system32\\wbem\\repository* and was not able to recover it.</span></span> <span data-ttu-id="fec0b-110">Ahora se eliminará el repositorio WMI, se creará un nuevo repositorio basado en el mecanismo de recuperación automática.</span><span class="sxs-lookup"><span data-stu-id="fec0b-110">The WMI repository will now be deleted, A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**subsistema de proveedor de WBEM de la \_ \_ \_ \_ \_ carga del proveedor LOCALSYSTEM \_**</span><span class="sxs-lookup"><span data-stu-id="fec0b-111"><span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM\_MC\_PROVIDER\_SUBSYSTEM\_LOCALSYSTEM\_PROVIDER\_LOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-112">2147483711 (0x8000003F)</span><span class="sxs-lookup"><span data-stu-id="fec0b-112">2147483711 (0x8000003F)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-113">Un proveedor, %1, se ha registrado en el espacio de nombres Instrumental de administración de Windows %2 para usar la cuenta LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="fec0b-113">A provider, %1, has been registered in the Windows Management Instrumentation namespace %2 to use the LocalSystem account.</span></span> <span data-ttu-id="fec0b-114">Esta cuenta tiene privilegios y el proveedor puede producir una infracción de seguridad si no suplanta correctamente las solicitudes del usuario.</span><span class="sxs-lookup"><span data-stu-id="fec0b-114">This account is privileged and the provider may cause a security violation if it does not correctly impersonate user requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_no se cargó WBEM MC \_ MOF en la \_ \_ \_ \_ recuperación**</span><span class="sxs-lookup"><span data-stu-id="fec0b-115"><span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM\_MC\_MOF\_NOT\_LOADED\_AT\_RECOVERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-116">3221225476 (0xC0000004)</span><span class="sxs-lookup"><span data-stu-id="fec0b-116">3221225476 (0xC0000004)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-117">Error %1 al intentar cargar MOF %2 durante la recuperación. Archivo MOF marcado con Autorrecuperación.</span><span class="sxs-lookup"><span data-stu-id="fec0b-117">Error %1 encountered when trying to load MOF %2 while recovering .MOF file marked with autorecover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ no puede \_ activar el \_ filtro**</span><span class="sxs-lookup"><span data-stu-id="fec0b-118"><span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM\_MC\_CANNOT\_ACTIVATE\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-119">3221225482 (0xC000000A)</span><span class="sxs-lookup"><span data-stu-id="fec0b-119">3221225482 (0xC000000A)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-120">No se pudo reactivar el filtro de eventos con la consulta "%2" en el espacio de nombres "%1" debido al error %3.</span><span class="sxs-lookup"><span data-stu-id="fec0b-120">Event filter with query "%2" could not be reactivated in namespace "%1" because of error %3.</span></span> <span data-ttu-id="fec0b-121">Los eventos no se pueden entregar a través de este filtro hasta que se corrija el problema.</span><span class="sxs-lookup"><span data-stu-id="fec0b-121">Events cannot be delivered through this filter until the problem is corrected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_consulta de \_ proveedor de eventos no válido WBEM MC \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fec0b-122"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-123">3221225493 (0xC0000015)</span><span class="sxs-lookup"><span data-stu-id="fec0b-123">3221225493 (0xC0000015)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-124">El proveedor de eventos %1 intentó registrar una consulta no válida sintácticamente "%2".</span><span class="sxs-lookup"><span data-stu-id="fec0b-124">Event provider %1 attempted to register a syntactically invalid query "%2".</span></span> <span data-ttu-id="fec0b-125">Se omitirá la consulta.</span><span class="sxs-lookup"><span data-stu-id="fec0b-125">The query will be ignored.</span></span> <span data-ttu-id="fec0b-126">La consulta se puede corregir examinando el repositorio WMI con CIM Studio y actualizando las suscripciones permanentes para el proveedor y la consulta de la lista.</span><span class="sxs-lookup"><span data-stu-id="fec0b-126">The query can be corrected by examining the WMI repository with CIM studio and updating the permanent subscriptions for the listed provider and query.</span></span> <span data-ttu-id="fec0b-127">Si se crea la suscripción permanente con el archivo MOF que viene con un producto instalado, se debe contactar con el proveedor de la aplicación para corregir el registro defectuoso.</span><span class="sxs-lookup"><span data-stu-id="fec0b-127">If the permanent subscription is created with MOF file coming with an installed product, the application vendor must be contacted to correct the faulty registration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ consulta intrínseca de proveedor de eventos no \_ válido \_ WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="fec0b-128"><span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM\_MC\_INVALID\_EVENT\_PROVIDER\_INTRINSIC\_QUERY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-129">3221225494 (0xC0000016)</span><span class="sxs-lookup"><span data-stu-id="fec0b-129">3221225494 (0xC0000016)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-130">El proveedor de eventos %1 intentó registrar una consulta de evento intrínseco "%2" en el espacio de nombres %3 para el que no se pudo determinar el conjunto de clases de objeto de destino.</span><span class="sxs-lookup"><span data-stu-id="fec0b-130">Event provider %1 attempted to register an intrinsic event query "%2" in %3 namespace for which the set of target object classes could not be determined.</span></span> <span data-ttu-id="fec0b-131">Se omitirá la consulta.</span><span class="sxs-lookup"><span data-stu-id="fec0b-131">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_consulta de proveedor de eventos WBEM MC \_ \_ \_ \_ demasiado \_ amplia**</span><span class="sxs-lookup"><span data-stu-id="fec0b-132"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_TOO\_BROAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-133">3221225495 (0xC0000017)</span><span class="sxs-lookup"><span data-stu-id="fec0b-133">3221225495 (0xC0000017)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-134">El proveedor de eventos %1 intentó registrar la consulta "%2" en el espacio de nombres %3, que es demasiado amplio.</span><span class="sxs-lookup"><span data-stu-id="fec0b-134">Event provider %1 attempted to register query "%2" in %3 namespace which is too broad.</span></span> <span data-ttu-id="fec0b-135">Los proveedores de eventos no pueden proporcionar eventos proporcionados por el sistema.</span><span class="sxs-lookup"><span data-stu-id="fec0b-135">Event providers cannot provide events that are provided by the system.</span></span> <span data-ttu-id="fec0b-136">Se omitirá la consulta.</span><span class="sxs-lookup"><span data-stu-id="fec0b-136">The query will be ignored.</span></span> <span data-ttu-id="fec0b-137">Póngase en contacto con el proveedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fec0b-137">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró la consulta del proveedor de eventos WBEM MC**</span><span class="sxs-lookup"><span data-stu-id="fec0b-138"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-139">3221225496 (0xC0000018)</span><span class="sxs-lookup"><span data-stu-id="fec0b-139">3221225496 (0xC0000018)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-140">El proveedor de eventos %1 intentó registrar la consulta "%2" cuya clase de destino "%3" en el espacio de nombres "%4" no existe.</span><span class="sxs-lookup"><span data-stu-id="fec0b-140">Event provider %1 attempted to register query "%2" whose target class "%3" in %4 namespace does not exist.</span></span> <span data-ttu-id="fec0b-141">Se omitirá la consulta.</span><span class="sxs-lookup"><span data-stu-id="fec0b-141">The query will be ignored.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_consulta de proveedor de eventos WBEM MC \_ \_ \_ \_ no \_ evento**</span><span class="sxs-lookup"><span data-stu-id="fec0b-142"><span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM\_MC\_EVENT\_PROVIDER\_QUERY\_NOT\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-143">3221225497 (0xC0000019)</span><span class="sxs-lookup"><span data-stu-id="fec0b-143">3221225497 (0xC0000019)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-144">El proveedor de eventos %1 intentó registrar la consulta &quot; %2 &quot; cuya clase de destino &quot; %3 &quot; no es una clase de eventos.</span><span class="sxs-lookup"><span data-stu-id="fec0b-144">Event provider %1 attempted to register query &quot;%2&quot; whose target class &quot;%3&quot; is not an event class.</span></span> <span data-ttu-id="fec0b-145">Se omitirá la consulta.</span><span class="sxs-lookup"><span data-stu-id="fec0b-145">The query will be ignored.</span></span> <span data-ttu-id="fec0b-146">Póngase en contacto con el proveedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fec0b-146">Contact the application vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_error del \_ \_ núcleo WBEM \_ de WBEM**</span><span class="sxs-lookup"><span data-stu-id="fec0b-147"><span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM\_MC\_WBEM\_CORE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-148">3221225500 (0xC000001C)</span><span class="sxs-lookup"><span data-stu-id="fec0b-148">3221225500 (0xC000001C)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-149">No se pudo inicializar el núcleo de WMI o el subsistema de proveedor o el subsistema de eventos con el número de error %1.</span><span class="sxs-lookup"><span data-stu-id="fec0b-149">Failed to Initialize WMI Core or Provider SubSystem or Event SubSystem with error number %1.</span></span> <span data-ttu-id="fec0b-150">Esto puede deberse a una versión de WMI mal instalada, un error de actualización del repositorio WMI, espacio insuficiente en disco o memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="fec0b-150">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**error de conexión de WBEM \_ MC \_ ADAP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fec0b-151"><span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM\_MC\_ADAP\_CONNECTION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-152">3221225515 (0xC000002B)</span><span class="sxs-lookup"><span data-stu-id="fec0b-152">3221225515 (0xC000002B)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-153">Instrumental de administración de Windows ADAP no pudo conectarse al espacio de nombres %1 con el siguiente error %2.</span><span class="sxs-lookup"><span data-stu-id="fec0b-153">Windows Management Instrumentation ADAP failed to connect to namespace %1 with the following error %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**error de WBEM de \_ \_ \_ \_ PUTCLASS \_ de la**</span><span class="sxs-lookup"><span data-stu-id="fec0b-154"><span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM\_MC\_ADAP\_PERFLIB\_PUTCLASS\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-155">3221225520 (0xC0000030)</span><span class="sxs-lookup"><span data-stu-id="fec0b-155">3221225520 (0xC0000030)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-156">Instrumental de administración de Windows ADAP no pudo guardar el objeto %1 en el espacio de nombres %2 debido al siguiente error: %3.</span><span class="sxs-lookup"><span data-stu-id="fec0b-156">Windows Management Instrumentation ADAP was unable to save object %1 in namespace %2 because of the following error %3.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ no se puede \_ \_ agregar \_ WIN32PERF**</span><span class="sxs-lookup"><span data-stu-id="fec0b-157"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-158">3221225530 (0xC000003A)</span><span class="sxs-lookup"><span data-stu-id="fec0b-158">3221225530 (0xC000003A)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-159">Instrumental de administración de Windows ADAP no pudo crear la \_ clase base de rendimiento de Win32 en %1: resultado = %2.</span><span class="sxs-lookup"><span data-stu-id="fec0b-159">Windows Management Instrumentation ADAP was unable to create the Win32\_Perf base class in %1:Result=%2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ no se puede \_ \_ agregar \_ WIN32PERFRAWDATA**</span><span class="sxs-lookup"><span data-stu-id="fec0b-160"><span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM\_MC\_ADAP\_UNABLE\_TO\_ADD\_WIN32PERFRAWDATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-161">3221225531 (0xC000003B)</span><span class="sxs-lookup"><span data-stu-id="fec0b-161">3221225531 (0xC000003B)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-162">Instrumental de administración de Windows ADAP no pudo crear la \_ clase base PerfRawData de Win32% 1.</span><span class="sxs-lookup"><span data-stu-id="fec0b-162">Windows Management Instrumentation ADAP was unable to create the Win32\_PerfRawData base class %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ no se pudo iniciar el repositorio \_ de WBEM MC \_**</span><span class="sxs-lookup"><span data-stu-id="fec0b-163"><span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**WBEM\_MC\_REPOSITORY\_FAILED\_TO\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-164">3221231073 (0xC00015E1)</span><span class="sxs-lookup"><span data-stu-id="fec0b-164">3221231073 (0xC00015E1)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-165">El servicio Instrumental de administración de Windows no pudo cargar los archivos de repositorio en el directorio *% WINDIR% \\ system32 WBEM del \\ \\ repositorio*.</span><span class="sxs-lookup"><span data-stu-id="fec0b-165">The Windows Management Instrumentation Service failed to load the repository files under the directory *%windir%\\system32\\wbem\\repository*.</span></span> <span data-ttu-id="fec0b-166">Esto puede deberse a daños en los archivos del repositorio, a la configuración de seguridad de este directorio, a la falta de espacio en disco o a otros problemas de recursos del sistema, como la falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="fec0b-166">This can be caused by a corruption in the repository files, security settings on this directory, lack of disk space, or other system resource issues such as lack of memory.</span></span> <span data-ttu-id="fec0b-167">Si este error se produce cada vez que se reinicia el equipo, es posible que el administrador de este equipo necesite detener el servicio WMI, revisar la configuración de seguridad en esta carpeta y archivos de esta carpeta y ejecutar WMIDiag para validar el estado de Instrumental de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fec0b-167">If this error occurs each time the computer is restarted then the administrator on this computer may need to stop WMI Service, review the security setting on this folder and files under this folder, and run WMIDiag to validate the health of Windows Management Instrumentation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ requiere \_ cifrado \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="fec0b-168"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-169">3221231077 (0xC00015E5)</span><span class="sxs-lookup"><span data-stu-id="fec0b-169">3221231077 (0xC00015E5)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-170">Se denegó el acceso al espacio de nombres %1 porque el espacio de nombres está marcado con RequiresEncryption, pero el script o la aplicación intentó conectarse a este espacio de nombres con un nivel de autenticación por debajo de la **\_ privacidad de PKT**.</span><span class="sxs-lookup"><span data-stu-id="fec0b-170">Access to the %1 namespace was denied because the namespace is marked with RequiresEncryption but the script or application attempted to connect to this namespace with an authentication level below **Pkt\_Privacy**.</span></span> <span data-ttu-id="fec0b-171">Cambie el nivel de autenticación a la **\_ privacidad PKT** y vuelva a ejecutar el script o la aplicación.</span><span class="sxs-lookup"><span data-stu-id="fec0b-171">Change the authentication level to **Pkt\_Privacy** and run the script or application again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ requiere \_ cifrado \_ Async \_ DENIED**</span><span class="sxs-lookup"><span data-stu-id="fec0b-172"><span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM\_MC\_WBEM\_REQUIRES\_ENCRYPTION\_ASYNC\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-173">3221231078 (0xC00015E6)</span><span class="sxs-lookup"><span data-stu-id="fec0b-173">3221231078 (0xC00015E6)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-174">Instrumental de administración de Windows servicio no pudo proporcionar los resultados de forma asincrónica para el espacio de nombres %1.</span><span class="sxs-lookup"><span data-stu-id="fec0b-174">Windows Management Instrumentation Service could not deliver results asynchronously for %1 namespace.</span></span> <span data-ttu-id="fec0b-175">El espacio de nombres está marcado con RequiresEncryption, pero WinMgmt no pudo volver a establecer una conexión segura con el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="fec0b-175">The namespace is marked with RequiresEncryption but WinMgmt could not establish a secure connection back to the client computer.</span></span> <span data-ttu-id="fec0b-176">Asegúrese de que hay una relación de confianza entre los equipos cliente y servidor para que el cliente reconozca la cuenta del equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="fec0b-176">Ensure there is a trust relationship between the client and server computers so that the client recognizes the server computer account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_host WBEM de WBEM MC \_ \_ \_ eliminado**</span><span class="sxs-lookup"><span data-stu-id="fec0b-177"><span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM\_MC\_WBEM\_HOST\_KILLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-178">3221231084 (0xC00015EC)</span><span class="sxs-lookup"><span data-stu-id="fec0b-178">3221231084 (0xC00015EC)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-179">Instrumental de administración de Windows ha detenido WMIPRVSE.EXE porque una cuota alcanzó un valor de advertencia.</span><span class="sxs-lookup"><span data-stu-id="fec0b-179">Windows Management Instrumentation has stopped WMIPRVSE.EXE because a quota reached a warning value.</span></span> <span data-ttu-id="fec0b-180">Cuota: %1 valor: %2 valor máximo: %3 PID de WMIPRVSE: %4.</span><span class="sxs-lookup"><span data-stu-id="fec0b-180">Quota: %1 Value: %2 Maximum value: %3 WMIPRVSE PID: %4.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**</span><span class="sxs-lookup"><span data-stu-id="fec0b-181"><span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM\_MC\_WBEM\_REPFILESNOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-182">3221231086 (0xC00015EE)</span><span class="sxs-lookup"><span data-stu-id="fec0b-182">3221231086 (0xC00015EE)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-183">Durante el inicio del servicio, el servicio Instrumental de administración de Windows no encontró los archivos del repositorio.</span><span class="sxs-lookup"><span data-stu-id="fec0b-183">During the service startup, the Windows Management Instrumentation service was unable to locate the repository files.</span></span> <span data-ttu-id="fec0b-184">Se creará un nuevo repositorio basado en el mecanismo de recuperación automática.</span><span class="sxs-lookup"><span data-stu-id="fec0b-184">A new repository will be created based on the auto-recovery mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM se \_ inició \_ correctamente**</span><span class="sxs-lookup"><span data-stu-id="fec0b-185"><span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM\_MC\_WBEM\_STARTED\_SUCESSFULLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-186">3221231087 (0xC00015EF)</span><span class="sxs-lookup"><span data-stu-id="fec0b-186">3221231087 (0xC00015EF)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-187">Instrumental de administración de Windows servicio se inició correctamente.</span><span class="sxs-lookup"><span data-stu-id="fec0b-187">Windows Management Instrumentation Service started successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**\_ESS MC \_ WBEM \_ Core \_ PSS de WBEM \_ \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="fec0b-188"><span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM\_MC\_WBEM\_CORE\_PSS\_ESS\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-189">3221231089 (0xC00015F1)</span><span class="sxs-lookup"><span data-stu-id="fec0b-189">3221231089 (0xC00015F1)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-190">Instrumental de administración de Windows subsistemas de servicio se inicializaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="fec0b-190">Windows Management Instrumentation Service subsystems initialized successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_error de \_ \_ \_ inicialización del \_ servicio WBEM de WBEM**</span><span class="sxs-lookup"><span data-stu-id="fec0b-191"><span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM\_MC\_WBEM\_SERVICE\_INIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-192">3221225501 (0xC000001D)</span><span class="sxs-lookup"><span data-stu-id="fec0b-192">3221225501 (0xC000001D)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-193">Se devolvió el número de error %1 al intentar inicializar el servicio Instrumental de administración de Windows.</span><span class="sxs-lookup"><span data-stu-id="fec0b-193">Error number %1 was returned in trying to initialize Windows Management Instrumentation Service.</span></span> <span data-ttu-id="fec0b-194">Esto puede deberse a una versión de WMI mal instalada, un error de actualización del repositorio WMI, espacio insuficiente en disco o memoria insuficiente.</span><span class="sxs-lookup"><span data-stu-id="fec0b-194">This could be due to a badly installed version of WMI, WMI repository upgrade failure, insufficient disk space or insufficient memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fec0b-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**se \_ ha \_ \_ \_ recreado el repositorio WBEM de WBEM.**</span><span class="sxs-lookup"><span data-stu-id="fec0b-195"><span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**WBEM\_MC\_WBEM\_REPOSITORY\_RECREATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fec0b-196">3221231088 (0xC00015F0)</span><span class="sxs-lookup"><span data-stu-id="fec0b-196">3221231088 (0xC00015F0)</span></span>
</dt> <dt>



<span data-ttu-id="fec0b-197">Instrumental de administración de Windows repositorio se ha creado correctamente con el mecanismo de autorrecuperación.</span><span class="sxs-lookup"><span data-stu-id="fec0b-197">Windows Management Instrumentation Repository successfully recreated using Autorecovery mechanism.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fec0b-198">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fec0b-198">Requirements</span></span>



| <span data-ttu-id="fec0b-199">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec0b-199">Requirement</span></span> | <span data-ttu-id="fec0b-200">Value</span><span class="sxs-lookup"><span data-stu-id="fec0b-200">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="fec0b-201">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec0b-201">Minimum supported client</span></span><br/> | <span data-ttu-id="fec0b-202">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fec0b-202">Windows Vista</span></span><br/>       |
| <span data-ttu-id="fec0b-203">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fec0b-203">Minimum supported server</span></span><br/> | <span data-ttu-id="fec0b-204">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fec0b-204">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fec0b-205">Vea también</span><span class="sxs-lookup"><span data-stu-id="fec0b-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec0b-206">Eventos WMI</span><span class="sxs-lookup"><span data-stu-id="fec0b-206">WMI Events</span></span>](wmi-events.md)
</dt> <dt>

[<span data-ttu-id="fec0b-207">Solución de problemas de WMI</span><span class="sxs-lookup"><span data-stu-id="fec0b-207">WMI Troubleshooting</span></span>](wmi-troubleshooting.md)
</dt> </dl>

 

 




