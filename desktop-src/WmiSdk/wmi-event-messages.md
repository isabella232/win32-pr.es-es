---
description: En la lista siguiente se enumeran los eventos admitidos por los registros wmi Windows Vista y sistemas operativos posteriores.
ms.assetid: ad8891cc-0b76-404d-81fc-961bcdbfae32
ms.tgt_platform: multiple
title: Mensajes de eventos WMI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 543e7131ac0c73a9f1e0f111dafe90197989a33d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967023"
---
# <a name="wmi-event-messages"></a>Mensajes de eventos WMI

En la lista siguiente se enumeran los eventos admitidos por los registros wmi Windows Vista y sistemas operativos posteriores.

> [!Note]  
> La siguiente documentación está diseñada para desarrolladores y administradores de TI. Si está intentando resolver un mensaje de error de WMI en el sistema principal, consulte el sitio [web Soporte técnico de Microsoft](https://support.microsoft.com/) wmi.

 

<dl> <dt>

<span id="WBEM_MC_REPOSITORY_INCONSISTENT"></span><span id="wbem_mc_repository_inconsistent"></span>**REPOSITORIO WBEM \_ MC \_ \_ INCOHERENTE**
</dt> <dd> <dl> <dt>

1073747424 (0x400015E0)
</dt> <dt>



El servicio de instrumentación de administración de Windows detectó una incoherencia con el repositorio WMI en el directorio *%windir% \\ system32 \\ wbem \\ repository* y no pudo recuperarlo. Ahora se eliminará el repositorio WMI; se creará un nuevo repositorio basado en el mecanismo de recuperación automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_PROVIDER_SUBSYSTEM_LOCALSYSTEM_PROVIDER_LOAD"></span><span id="wbem_mc_provider_subsystem_localsystem_provider_load"></span>**WBEM \_ MC \_ PROVIDER \_ SUBSYSTEM \_ LOCALSYSTEM \_ PROVIDER \_ LOAD**
</dt> <dd> <dl> <dt>

2147483711 (0x8000003F)
</dt> <dt>



Se ha registrado un proveedor, %1, en el espacio de nombres %2 Windows Management Instrumentation para usar la cuenta LocalSystem. Esta cuenta tiene privilegios y el proveedor puede producir una infracción de seguridad si no suplanta correctamente las solicitudes de usuario.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_MOF_NOT_LOADED_AT_RECOVERY"></span><span id="wbem_mc_mof_not_loaded_at_recovery"></span>**WBEM \_ MC \_ MOF NO CARGADO DURANTE LA \_ \_ \_ \_ RECUPERACIÓN**
</dt> <dd> <dl> <dt>

3221225476 (0xC0000004)
</dt> <dt>



Error %1 encontrado al intentar cargar MOF %2 al recuperar . Archivo MOF marcado con autorrecuperación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_CANNOT_ACTIVATE_FILTER"></span><span id="wbem_mc_cannot_activate_filter"></span>**WBEM \_ MC NO PUEDE ACTIVAR \_ \_ \_ FILTRO**
</dt> <dd> <dl> <dt>

3221225482 (0xC000000A)
</dt> <dt>



No se pudo reactivar el filtro de eventos con la consulta "%2" en el espacio de nombres "%1" debido al error %3. Los eventos no se pueden entregar a través de este filtro hasta que se corrija el problema.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_QUERY"></span><span id="wbem_mc_invalid_event_provider_query"></span>**WBEM \_ MC \_ INVALID \_ EVENT \_ PROVIDER \_ QUERY**
</dt> <dd> <dl> <dt>

3221225493 (0xC0000015)
</dt> <dt>



El proveedor de eventos %1 intentó registrar una consulta sintácticamente no válida "%2". La consulta se omitirá. La consulta se puede corregir examinando el repositorio WMI con CIM Studio y actualizando las suscripciones permanentes para el proveedor y la consulta enumerados. Si la suscripción permanente se crea con un archivo MOF que viene con un producto instalado, se debe ponerse en contacto con el proveedor de la aplicación para corregir el registro defectuoso.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_INVALID_EVENT_PROVIDER_INTRINSIC_QUERY"></span><span id="wbem_mc_invalid_event_provider_intrinsic_query"></span>**WBEM MC INVALID EVENT PROVIDER INTRINSIC QUERY (CONSULTA INTRÍNSECA DEL PROVEEDOR DE EVENTOS NO VÁLIDO DE WBEM \_ \_ \_ \_ \_ \_ MC)**
</dt> <dd> <dl> <dt>

3221225494 (0xC0000016)
</dt> <dt>



El proveedor de eventos %1 intentó registrar una consulta de eventos intrínseca "%2" en el espacio de nombres %3 para el que no se pudo determinar el conjunto de clases de objeto de destino. La consulta se omitirá.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_TOO_BROAD"></span><span id="wbem_mc_event_provider_query_too_broad"></span>**CONSULTA DEL PROVEEDOR DE EVENTOS WBEM \_ MC \_ DEMASIADO \_ \_ \_ \_ AMPLIA**
</dt> <dd> <dl> <dt>

3221225495 (0xC0000017)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la consulta "%2" en el espacio de nombres %3, que es demasiado amplio. Los proveedores de eventos no pueden proporcionar eventos proporcionados por el sistema. La consulta se omitirá. Póngase en contacto con el proveedor de la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_FOUND"></span><span id="wbem_mc_event_provider_query_not_found"></span>**NO SE ENCONTRÓ \_ LA CONSULTA DEL PROVEEDOR DE \_ \_ \_ EVENTOS \_ \_ WBEM MC**
</dt> <dd> <dl> <dt>

3221225496 (0xC0000018)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la consulta "%2" cuya clase de destino "%3" en el espacio de nombres %4 no existe. La consulta se omitirá.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_EVENT_PROVIDER_QUERY_NOT_EVENT"></span><span id="wbem_mc_event_provider_query_not_event"></span>**WBEM \_ MC \_ EVENT \_ PROVIDER \_ QUERY \_ NOT \_ EVENT**
</dt> <dd> <dl> <dt>

3221225497 (0xC0000019)
</dt> <dt>



El proveedor de eventos %1 intentó registrar la &quot; consulta %2 cuya clase de destino &quot; &quot; %3 &quot; no es una clase de eventos. La consulta se omitirá. Póngase en contacto con el proveedor de la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_FAILURE"></span><span id="wbem_mc_wbem_core_failure"></span>**WBEM \_ MC \_ WBEM \_ CORE \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225500 (0xC000001C)
</dt> <dt>



No se pudo inicializar wmi core o subsistema del proveedor o subsistema de eventos con el número de error %1. Esto podría deberse a una versión mal instalada de WMI, a un error de actualización del repositorio WMI, a un espacio en disco insuficiente o a una memoria insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_CONNECTION_FAILURE"></span><span id="wbem_mc_adap_connection_failure"></span>**WBEM \_ MC \_ ADAP \_ CONNECTION \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225515 (0xC000002B)
</dt> <dt>



Windows ADAP de instrumentación de administración no pudo conectarse al espacio de nombres %1 con el siguiente error %2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_PERFLIB_PUTCLASS_FAILURE"></span><span id="wbem_mc_adap_perflib_putclass_failure"></span>**WBEM \_ MC \_ ADAP \_ PERFLIB \_ PUTCLASS \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225520 (0xC0000030)
</dt> <dt>



Windows ADAP de instrumentación de administración no pudo guardar el objeto %1 en el espacio de nombres %2 debido al siguiente error %3.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERF"></span><span id="wbem_mc_adap_unable_to_add_win32perf"></span>**WBEM \_ MC \_ ADAP NO PUEDE AGREGAR \_ \_ \_ \_ WIN32PERF**
</dt> <dd> <dl> <dt>

3221225530 (0xC000003A)
</dt> <dt>



Windows ADAP de instrumentación de administración no pudo crear la clase base Perf de Win32 \_ en %1:Result=%2.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_ADAP_UNABLE_TO_ADD_WIN32PERFRAWDATA"></span><span id="wbem_mc_adap_unable_to_add_win32perfrawdata"></span>**WBEM \_ MC \_ ADAP NO PUEDE AGREGAR \_ \_ \_ \_ WIN32PERFRAWDATA**
</dt> <dd> <dl> <dt>

3221225531 (0xC000003B)
</dt> <dt>



Windows ADAP de instrumentación de administración no pudo crear la clase \_ base Win32 PerfRawData %1.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_REPOSITORY_FAILED_TO_START"></span><span id="wbem_mc_repository_failed_to_start"></span>**NO SE PUDO INICIAR EL REPOSITORIO WBEM \_ MC \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

3221231073 (0xC00015E1)
</dt> <dt>



El Windows management instrumentation service no pudo cargar los archivos del repositorio en el directorio *%windir% \\ system32 \\ wbem \\ repository*. Esto puede deberse a daños en los archivos del repositorio, la configuración de seguridad en este directorio, la falta de espacio en disco u otros problemas de recursos del sistema, como la falta de memoria. Si este error se produce cada vez que se reinicia el equipo, es posible que el administrador de este equipo tenga que detener el servicio WMI, revisar la configuración de seguridad en esta carpeta y los archivos de esta carpeta y ejecutar WMIDiag para validar el estado de Windows Management Instrumentation.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_denied"></span>**WBEM \_ MC \_ WBEM REQUIERE CIFRADO \_ \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

3221231077 (0xC00015E5)
</dt> <dt>



Se denegó el acceso al espacio de nombres %1 porque el espacio de nombres está marcado con RequiresEncryption, pero el script o la aplicación intentaron conectarse a este espacio de nombres con un nivel de autenticación por debajo de **Pkt \_ Privacy**. Cambie el nivel de autenticación a **Pkt \_ Privacy** y vuelva a ejecutar el script o la aplicación.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REQUIRES_ENCRYPTION_ASYNC_DENIED"></span><span id="wbem_mc_wbem_requires_encryption_async_denied"></span>**WBEM \_ MC \_ WBEM REQUIERE CIFRADO ASINCRÓNICO \_ \_ \_ \_ DENEGADO**
</dt> <dd> <dl> <dt>

3221231078 (0xC00015E6)
</dt> <dt>



Windows El servicio de instrumentación de administración no pudo entregar resultados de forma asincrónica para el espacio de nombres %1. El espacio de nombres está marcado con RequiresEncryption, pero WinMgmt no pudo establecer una conexión segura al equipo cliente. Asegúrese de que hay una relación de confianza entre los equipos cliente y servidor para que el cliente reconozca la cuenta de equipo del servidor.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_HOST_KILLED"></span><span id="wbem_mc_wbem_host_killed"></span>**WBEM \_ MC \_ WBEM \_ HOST \_ KILLED**
</dt> <dd> <dl> <dt>

3221231084 (0xC00015EC)
</dt> <dt>



Windows Management Instrumentation se ha detenido WMIPRVSE.EXE porque una cuota alcanzó un valor de advertencia. Cuota: %1 Valor: %2 Valor máximo: %3 WMIPRVSE PID: %4.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPFILESNOTFOUND"></span><span id="wbem_mc_wbem_repfilesnotfound"></span>**WBEM \_ MC \_ WBEM \_ REPFILESNOTFOUND**
</dt> <dd> <dl> <dt>

3221231086 (0xC00015EE)
</dt> <dt>



Durante el inicio del servicio, el Windows Management Instrumentation no pudo encontrar los archivos del repositorio. Se creará un nuevo repositorio basado en el mecanismo de recuperación automática.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_STARTED_SUCESSFULLY"></span><span id="wbem_mc_wbem_started_sucessfully"></span>**WBEM \_ MC \_ WBEM SE \_ INICIÓ \_ CORRECTAMENTE**
</dt> <dd> <dl> <dt>

3221231087 (0xC00015EF)
</dt> <dt>



Windows El servicio de instrumentación de administración se inició correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_CORE_PSS_ESS_INITIALIZED"></span><span id="wbem_mc_wbem_core_pss_ess_initialized"></span>**WBEM \_ MC \_ WBEM CORE \_ \_ PSS \_ ESS \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

3221231089 (0xC00015F1)
</dt> <dt>



Windows Subsistemas del servicio de instrumentación de administración inicializados correctamente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_SERVICE_INIT_FAILURE"></span><span id="wbem_mc_wbem_service_init_failure"></span>**WBEM \_ MC \_ WBEM \_ SERVICE \_ INIT \_ FAILURE**
</dt> <dd> <dl> <dt>

3221225501 (0xC000001D)
</dt> <dt>



Se devolvió el número de error %1 al intentar inicializar Windows Management Instrumentation Service. Esto podría deberse a una versión mal instalada de WMI, a un error de actualización del repositorio WMI, a un espacio en disco insuficiente o a una memoria insuficiente.


</dt> </dl> </dd> <dt>

<span id="WBEM_MC_WBEM_REPOSITORY_RECREATED"></span><span id="wbem_mc_wbem_repository_recreated"></span>**REPOSITORIO WBEM \_ MC \_ WBEM \_ \_ RECREADO**
</dt> <dd> <dl> <dt>

3221231088 (0xC00015F0)
</dt> <dt>



Windows Repositorio de instrumentación de administración que se ha creado correctamente mediante el mecanismo de recuperación automática.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Eventos WMI](wmi-events.md)
</dt> <dt>

[Solución de problemas de WMI](wmi-troubleshooting.md)
</dt> </dl>

 

 




