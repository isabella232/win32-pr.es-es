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
# <a name="wmi-event-messages"></a>Mensajes de eventos WMI

En la lista siguiente se enumeran los eventos admitidos por los registros WMI en Windows Vista y sistemas operativos posteriores.

> [!Note]  
> La siguiente documentación está diseñada para desarrolladores y administradores de ti. Si está intentando resolver un mensaje de error de WMI en el sistema doméstico, consulte el sitio web de [soporte técnico de Microsoft](https://support.microsoft.com/) .

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**\_repositorio MC de WBEM \_ \_ incoherente**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



El servicio Instrumental de administración de Windows detectó una incoherencia con el repositorio WMI en el directorio *% WINDIR% \\ system32 \\ WBEM \\* y no pudo recuperarlo. Ahora se eliminará el repositorio WMI, se creará un nuevo repositorio basado en el mecanismo de recuperación automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**subsistema de proveedor de WBEM de la \_ \_ \_ \_ \_ carga del proveedor LOCALSYSTEM \_**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Un proveedor, %1, se ha registrado en el espacio de nombres Instrumental de administración de Windows %2 para usar la cuenta LocalSystem. Esta cuenta tiene privilegios y el proveedor puede producir una infracción de seguridad si no suplanta correctamente las solicitudes del usuario.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**\_no se cargó WBEM MC \_ MOF en la \_ \_ \_ \_ recuperación**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Error %1 al intentar cargar MOF %2 durante la recuperación. Archivo MOF marcado con Autorrecuperación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC \_ no puede \_ activar el \_ filtro**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



No se pudo reactivar el filtro de eventos con la consulta "%2" en el espacio de nombres "%1" debido al error %3. Los eventos no se pueden entregar a través de este filtro hasta que se corrija el problema.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**\_consulta de \_ proveedor de eventos no válido WBEM MC \_ \_ \_**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



El proveedor de eventos %1 intentó registrar una consulta no válida sintácticamente "%2". Se omitirá la consulta. La consulta se puede corregir examinando el repositorio WMI con CIM Studio y actualizando las suscripciones permanentes para el proveedor y la consulta de la lista. Si se crea la suscripción permanente con el archivo MOF que viene con un producto instalado, se debe contactar con el proveedor de la aplicación para corregir el registro defectuoso.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**\_ \_ \_ \_ consulta intrínseca de proveedor de eventos no \_ válido \_ WBEM MC**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



El proveedor de eventos %1 intentó registrar una consulta de evento intrínseco "%2" en el espacio de nombres %3 para el que no se pudo determinar el conjunto de clases de objeto de destino. Se omitirá la consulta.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**\_consulta de proveedor de eventos WBEM MC \_ \_ \_ \_ demasiado \_ amplia**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la consulta "%2" en el espacio de nombres %3, que es demasiado amplio. Los proveedores de eventos no pueden proporcionar eventos proporcionados por el sistema. Se omitirá la consulta. Póngase en contacto con el proveedor de la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**\_ \_ \_ \_ \_ no \_ se encontró la consulta del proveedor de eventos WBEM MC**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la consulta "%2" cuya clase de destino "%3" en el espacio de nombres "%4" no existe. Se omitirá la consulta.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**\_consulta de proveedor de eventos WBEM MC \_ \_ \_ \_ no \_ evento**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la consulta &quot; %2 &quot; cuya clase de destino &quot; %3 &quot; no es una clase de eventos. Se omitirá la consulta. Póngase en contacto con el proveedor de la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**\_error del \_ \_ núcleo WBEM \_ de WBEM**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



No se pudo inicializar el núcleo de WMI o el subsistema de proveedor o el subsistema de eventos con el número de error %1. Esto puede deberse a una versión de WMI mal instalada, un error de actualización del repositorio WMI, espacio insuficiente en disco o memoria insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**error de conexión de WBEM \_ MC \_ ADAP \_ \_**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Instrumental de administración de Windows ADAP no pudo conectarse al espacio de nombres %1 con el siguiente error %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**error de WBEM de \_ \_ \_ \_ PUTCLASS \_ de la**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Instrumental de administración de Windows ADAP no pudo guardar el objeto %1 en el espacio de nombres %2 debido al siguiente error: %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP \_ no se puede \_ \_ agregar \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Instrumental de administración de Windows ADAP no pudo crear la \_ clase base de rendimiento de Win32 en %1: resultado = %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP \_ no se puede \_ \_ agregar \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Instrumental de administración de Windows ADAP no pudo crear la \_ clase base PerfRawData de Win32% 1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**\_ \_ \_ no se pudo iniciar el repositorio \_ de WBEM MC \_**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



El servicio Instrumental de administración de Windows no pudo cargar los archivos de repositorio en el directorio *% WINDIR% \\ system32 WBEM del \\ \\ repositorio*. Esto puede deberse a daños en los archivos del repositorio, a la configuración de seguridad de este directorio, a la falta de espacio en disco o a otros problemas de recursos del sistema, como la falta de memoria. Si este error se produce cada vez que se reinicia el equipo, es posible que el administrador de este equipo necesite detener el servicio WMI, revisar la configuración de seguridad en esta carpeta y archivos de esta carpeta y ejecutar WMIDiag para validar el estado de Instrumental de administración de Windows.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM \_ requiere \_ cifrado \_ denegado**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



Se denegó el acceso al espacio de nombres %1 porque el espacio de nombres está marcado con RequiresEncryption, pero el script o la aplicación intentó conectarse a este espacio de nombres con un nivel de autenticación por debajo de la **\_ privacidad de PKT**. Cambie el nivel de autenticación a la **\_ privacidad PKT** y vuelva a ejecutar el script o la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM \_ requiere \_ cifrado \_ Async \_ DENIED**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Instrumental de administración de Windows servicio no pudo proporcionar los resultados de forma asincrónica para el espacio de nombres %1. El espacio de nombres está marcado con RequiresEncryption, pero WinMgmt no pudo volver a establecer una conexión segura con el equipo cliente. Asegúrese de que hay una relación de confianza entre los equipos cliente y servidor para que el cliente reconozca la cuenta del equipo servidor.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**\_host WBEM de WBEM MC \_ \_ \_ eliminado**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Instrumental de administración de Windows ha detenido WMIPRVSE.EXE porque una cuota alcanzó un valor de advertencia. Cuota: %1 valor: %2 valor máximo: %3 PID de WMIPRVSE: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Durante el inicio del servicio, el servicio Instrumental de administración de Windows no encontró los archivos del repositorio. Se creará un nuevo repositorio basado en el mecanismo de recuperación automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM se \_ inició \_ correctamente**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Instrumental de administración de Windows servicio se inició correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**\_ESS MC \_ WBEM \_ Core \_ PSS de WBEM \_ \_ inicializado**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Instrumental de administración de Windows subsistemas de servicio se inicializaron correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**\_error de \_ \_ \_ inicialización del \_ servicio WBEM de WBEM**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



Se devolvió el número de error %1 al intentar inicializar el servicio Instrumental de administración de Windows. Esto puede deberse a una versión de WMI mal instalada, un error de actualización del repositorio WMI, espacio insuficiente en disco o memoria insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**se \_ ha \_ \_ \_ recreado el repositorio WBEM de WBEM.**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Instrumental de administración de Windows repositorio se ha creado correctamente con el mecanismo de autorrecuperación.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Eventos WMI](wmi-events.md)
</dt> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 




