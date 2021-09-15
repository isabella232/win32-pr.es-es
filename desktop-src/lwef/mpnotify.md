---
title: Enumeración MPNOTIFY (MpClient.h)
description: Posibles notificaciones de devolución de llamada.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Características heredadas del entorno de Windows MPNOTIFY
- Puntero de enumeración PMPNOTIFY Características heredadas Windows entorno
topic_type:
- apiref
api_name:
- MPNOTIFY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afa0eeb6cb1d610f28cc82f578617f7bd71cf886
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359747"
---
# <a name="mpnotify-enumeration"></a>Enumeración MPNOTIFY

Posibles notificaciones de devolución de llamada.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPNOTIFY { 
  MPNOTIFY_NONE,
  MPNOTIFY_CALL_START,
  MPNOTIFY_CALL_COMPLETE,
  MPNOTIFY_INTERNAL_FAILURE,
  MPNOTIFY_STATUS_SERVICE_START,
  MPNOTIFY_STATUS_SERVICE_RUNNING,
  MPNOTIFY_STATUS_SERVICE_STOP,
  MPNOTIFY_STATUS_COMPONENT,
  MPNOTIFY_STATUS_CHANGE,
  MPNOTIFY_STATUS_COMPONENT_CONFIGURATION,
  MPNOTIFY_STATUS_EXPIRATION_CHANGE,
  MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE,
  MPNOTIFY_SCAN_START,
  MPNOTIFY_SCAN_PAUSED,
  MPNOTIFY_SCAN_RESUMED,
  MPNOTIFY_SCAN_CANCEL,
  MPNOTIFY_SCAN_COMPLETE,
  MPNOTIFY_SCAN_PROGRESS,
  MPNOTIFY_SCAN_ERROR,
  MPNOTIFY_SCAN_INFECTED,
  MPNOTIFY_SCAN_MEMORYSTART,
  MPNOTIFY_SCAN_MEMORYCOMPLETE,
  MPNOTIFY_SCAN_SFC_BUILD_START,
  MPNOTIFY_SCAN_SFC_BUILD_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_START,
  MPNOTIFY_SCAN_FASTPATH_COMPLETE,
  MPNOTIFY_SCAN_FASTPATH_PROGRESS,
  MPNOTIFY_CLEAN_START,
  MPNOTIFY_CLEAN_COMPLETE,
  MPNOTIFY_CLEAN_RESTOREPOINT_START,
  MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED,
  MPNOTIFY_CLEAN_RESTOREPOINT_FAILED,
  MPNOTIFY_CLEAN_THREAT_START,
  MPNOTIFY_CLEAN_THREAT_SUCCEEDED,
  MPNOTIFY_CLEAN_THREAT_FAILED,
  MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED,
  MPNOTIFY_CLEAN_RESOURCE_FAILED,
  MPNOTIFY_CLEAN_THREAT_COMPLETE,
  MPNOTIFY_PRECHECK_START,
  MPNOTIFY_PRECHECK_COMPLETE,
  MPNOTIFY_PRECHECK_RESOURCE_BLOCKED,
  MPNOTIFY_THREAT_DETECTED,
  MPNOTIFY_THREAT_MODIFIED,
  MPNOTIFY_THREAT_CLEAN_SUCCEEDED,
  MPNOTIFY_THREAT_CLEAN_FAILED,
  MPNOTIFY_THREAT_ABANDONED,
  MPNOTIFY_THREAT_CLEAN_EVENT_START,
  MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE,
  MPNOTIFY_SIGUPDATE_START,
  MPNOTIFY_SIGUPDATE_SEARCH_START,
  MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE,
  MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_START,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS,
  MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE,
  MPNOTIFY_SIGUPDATE_INSTALL_START,
  MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS,
  MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE,
  MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED,
  MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED,
  MPNOTIFY_SIGUPDATE_COMPLETE,
  MPNOTIFY_SAMPLE_START,
  MPNOTIFY_SAMPLE_COMPLETE,
  MPNOTIFY_SAMPLE_ITEM_START,
  MPNOTIFY_SAMPLE_ITEM_SUCCEEDED,
  MPNOTIFY_SAMPLE_ITEM_FAILED,
  MPNOTIFY_RESERVED_DATA,
  MPNOTIFY_FASTPATH_SIG_ADDED,
  MPNOTIFY_FASTPATH_SIG_REMOVED,
  MPNOTIFY_NIS_PRIVATE,
  MPNOTIFY_HEALTH_CHANGE,
  MPNOTIFY_HEALTH_RECOVERY,
  MPNOTIFY_HEALTH_START,
  MPNOTIFY_ENDOFLIFE_CHANGE,
  MPNOTIFY_MALWARETOAST_DATA
} MPNOTIFY, *PMPNOTIFY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ NONE**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**MPNOTIFY \_ CALL \_ START**
</dt> <dd>

Inicio de la llamada de notificación.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**MPNOTIFY \_ CALL \_ COMPLETE**
</dt> <dd>

Llamada de notificación completada.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**ERROR INTERNO DE \_ \_ MPNOTIFY**
</dt> <dd>

Error interno genérico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**INICIO DEL SERVICIO \_ DE ESTADO \_ DE MPNOTIFY \_**
</dt> <dd>

Se ha iniciado el servicio de protección contra malware.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ RUNNING**
</dt> <dd>

Se está ejecutando el servicio de protección contra malware.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**MPNOTIFY \_ STATUS \_ SERVICE \_ STOP**
</dt> <dd>

El servicio de protección contra malware se ha detenido.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**COMPONENTE DE ESTADO \_ \_ MPNOTIFY**
</dt> <dd>

Estado de habilitación o deshabilitación de un componente determinado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**CAMBIO DE ESTADO \_ DE MPNOTIFY \_**
</dt> <dd>

El estado general del producto ha cambiado. Llame [**a MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) para obtener el estado actual.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**CONFIGURACIÓN DEL COMPONENTE \_ DE ESTADO \_ \_ MPNOTIFY**
</dt> <dd>

Un componente determinado ha cambiado la configuración.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**CAMBIO DE \_ EXPIRACIÓN DEL ESTADO DE \_ MPNOTIFY \_**
</dt> <dd>

El estado de expiración del producto ha cambiado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**CAMBIO DE EXAMEN \_ SIN CONEXIÓN DEL ESTADO \_ \_ DE \_ MPNOTIFY**
</dt> <dd>

Se ha cambiado el estado requerido del examen sin conexión.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**MPNOTIFY \_ SCAN \_ START**
</dt> <dd>

Examen iniciado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**MPNOTIFY \_ SCAN \_ PAUSED**
</dt> <dd>

Examen en pausa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**MPNOTIFY \_ SCAN \_ RESUMED**
</dt> <dd>

examen reanudado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**MPNOTIFY \_ SCAN \_ CANCEL**
</dt> <dd>

Examen cancelado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**MPNOTIFY \_ SCAN \_ COMPLETE**
</dt> <dd>

Examen completado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**PROGRESO DEL \_ EXAMEN DE MPNOTIFY \_**
</dt> <dd>

Notificación de progreso del recurso específico que se está analizando.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**MPNOTIFY \_ SCAN \_ ERROR**
</dt> <dd>

Error al examinar un recurso determinado. El examen continuará.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**MPNOTIFY \_ SCAN \_ INFECTED**
</dt> <dd>

El examen encontró un recurso infectado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ SCAN \_ MEMORYSTART**
</dt> <dd>

Se ha iniciado el examen del progreso para notificar a la parte del examen de memoria del examen del sistema.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**
</dt> <dd>

Progreso del examen para notificar que se ha completado la parte del examen de memoria del examen del sistema.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ START**
</dt> <dd>

Se ha iniciado el análisis del progreso para notificar a la parte de compilación de sfc.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ SCAN \_ SFC \_ BUILD \_ COMPLETE**
</dt> <dd>

Se ha completado el análisis del progreso para notificar a la parte de compilación de sfc.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ START**
</dt> <dd>

Ha comenzado el examen de fastpath spynet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ SCAN \_ FASTPATH \_ COMPLETE**
</dt> <dd>

Ha finalizado el examen de fastpath spynet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**PROGRESO DE \_ \_ FASTPATH DE MPNOTIFY SCAN \_**
</dt> <dd>

Notificación de progreso para los rescans de fastpath, usados internamente y convertidos en **MPNOTIFY \_ SCAN \_ PROGRESS** para externos.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**MPNOTIFY \_ CLEAN \_ START**
</dt> <dd>

Se inició la limpieza.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**MPNOTIFY \_ CLEAN \_ COMPLETE**
</dt> <dd>

Limpieza completada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ START**
</dt> <dd>

Empezó a crear un punto de restauración del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_ SUCCEEDED**
</dt> <dd>

Punto de restauración del sistema creado correctamente.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**ERROR DE MPNOTIFY \_ CLEAN \_ RESTOREPOINT \_**
</dt> <dd>

Error al crear el punto de restauración del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ START**
</dt> <dd>

La limpieza se inicia para una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ SUCCEEDED**
</dt> <dd>

La limpieza se realiza correctamente para una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**ERROR EN LA \_ AMENAZA DE \_ LIMPIEZA DE MPNOTIFY \_**
</dt> <dd>

No se pudo limpiar una amenaza determinada. **ERROR \_ El código de error \_ \_ NO \_ ENCONTRADO** DE AMENAZA DE MP indica que no se encontró la amenaza (y no se produjo un error al limpiar).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**MPNOTIFY \_ CLEAN \_ RESOURCE \_ SUCCEEDED**
</dt> <dd>

La limpieza se realiza correctamente para un recurso determinado.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**ERROR DE MPNOTIFY \_ CLEAN \_ RESOURCE \_**
</dt> <dd>

No se pudo limpiar un recurso determinado.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**MPNOTIFY \_ CLEAN \_ THREAT \_ COMPLETE**
</dt> <dd>

Se ha completado la limpieza de una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**MPNOTIFY \_ PRECHECK \_ START**
</dt> <dd>

Limpieza de la comprobación previa iniciada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**MPNOTIFY \_ PRECHECK \_ COMPLETE**
</dt> <dd>

Limpieza de la comprobación previa completada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY \_ PRECHECK \_ RESOURCE \_ BLOCKED**
</dt> <dd>

Se detectó un recurso bloqueado en la comprobación previa limpia.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**SE DETECTÓ UNA AMENAZA DE MPNOTIFY \_ \_**
</dt> <dd>

Nueva amenaza detectada en el sistema.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY \_ THREAT \_ MODIFIED**
</dt> <dd>

Información sobre amenazas modificada. Por ejemplo, se ha agregado un nuevo recurso.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ SUCCEEDED**
</dt> <dd>

Acción de limpieza correcta para una amenaza.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**ERROR DE LIMPIEZA \_ DE AMENAZAS \_ DE MPNOTIFY \_**
</dt> <dd>

Error en la acción de limpieza en caso de amenaza. **ERROR \_ El código de error \_ MP THREAT \_ NOT \_ FOUND** indica que no se encontró la amenaza (y no se produjo un error al limpiar).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY \_ THREAT \_ ABANDONED**
</dt> <dd>

No se produjo ninguna corrección antes de que se detuve el servicio.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**MPNOTIFY \_ THREAT \_ CLEAN \_ EVENT \_ START**
</dt> <dd>

Se ha iniciado una acción de limpieza.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**EVENTO MPNOTIFY \_ THREAT \_ CLEAN \_ \_ COMPLETADO**
</dt> <dd>

Finalizó una acción de limpieza.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**MPNOTIFY \_ SIGUPDATE \_ START**
</dt> <dd>

Se inició la actualización de firmas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ START**
</dt> <dd>

Busque actualizaciones iniciadas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ COMPLETE**
</dt> <dd>

Busque actualizaciones completadas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**ACTUALIZACIÓN DE SOFTWARE DE MPNOTIFY \_ SIGUPDATE \_ \_ \_ DISPONIBLE**
</dt> <dd>

Actualización de software disponible.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**INICIO DE DESCARGA DE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Se ha iniciado la descarga.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**PROGRESO DE DESCARGA DE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Descarga en curso. Los datos de devolución de llamada contienen progreso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**DESCARGA COMPLETA DE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Descarga completada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**INICIO DE INSTALACIÓN DE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Instalación iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**PROGRESO DE INSTALACIÓN DE MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Instalación en curso. Los datos de devolución de llamada contienen progreso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**INSTALACIÓN COMPLETA DE \_ MPNOTIFY SIGUPDATE \_ \_**
</dt> <dd>

Instalación completada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**SE REQUIERE EL \_ REINICIO DE MPNOTIFY SIGUPDATE \_ \_**
</dt> <dd>

La actualización requiere reiniciar.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**SOLICITUD DE \_ MPNOTIFY SIGUPDATE \_ \_ PROCESADA**
</dt> <dd>

El servicio procesó una solicitud de actualización de firma. HResult indica un error o un éxito **en** los datos de devolución de llamada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ COMPLETE**
</dt> <dd>

Actualización completada. **S \_ El** estado FALSE indica que no se necesitaron actualizaciones.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**INICIO DE EJEMPLO DE MPNOTIFY \_ \_**
</dt> <dd>

Se inició el envío de ejemplo.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**EJEMPLO DE MPNOTIFY \_ \_ COMPLETADO**
</dt> <dd>

Envío de ejemplo completado.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**INICIO DEL \_ ELEMENTO DE EJEMPLO \_ MPNOTIFY \_**
</dt> <dd>

Se inició el envío de elementos de ejemplo específicos. El índice de elemento de ejemplo está disponible [**en MPSAMPLE \_ DATA**](mpsample-data.md).

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**EL ELEMENTO DE EJEMPLO MPNOTIFY \_ \_ SE HA INSTALADO \_ CORRECTAMENTE**
</dt> <dd>

El envío de elementos de ejemplo específicos se ha publicado correctamente.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**ERROR EN EL \_ ELEMENTO DE \_ EJEMPLO MPNOTIFY \_**
</dt> <dd>

Error en el envío de elementos de ejemplo específicos. El código de error está disponible en [**MPCALLBACK \_ DATA**](mpcallback-data.md).

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ RESERVED \_ DATA**
</dt> <dd>

Datos reservados internos.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**SE HA AGREGADO \_ MPNOTIFY FASTPATH \_ SIG \_**
</dt> <dd>

Una firma fastpath ha agregado o deshabilitado una firma.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ QUITADO**
</dt> <dd>

Se ha quitado una firma FastPath.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ PRIVATE**
</dt> <dd>

Notifcations privados de NIS. Ningún asociado debe registrarse para ello.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**CAMBIO DE ESTADO \_ DE MPNOTIFY \_**
</dt> <dd>

El servicio AM ha entrado en un nuevo estado.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**MPNOTIFY \_ HEALTH \_ RECOVERY**
</dt> <dd>

El servicio AM se ha recuperado de un estado.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**MPNOTIFY \_ HEALTH \_ START**
</dt> <dd>

El servicio AM ha inicializado el estado del sistema.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**CAMBIO DE \_ MPNOTIFY \_ ENDOFLIFE**
</dt> <dd>

Las fechas de expiración del "final del ciclo de vida" del servicio AM han cambiado.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**MPNOTIFY \_ MALWARETOAST \_ DATA**
</dt> <dd>

El servicio AM ha detectado malware que podría haber provocado un cambio de configuración crítico en la máquina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**DATOS DE DEVOLUCIÓN DE \_ LLAMADA DE MP**](mpcallback-data.md)
</dt> <dt>

[**DATOS \_ MPSAMPLE**](mpsample-data.md)
</dt> </dl>

 

 





