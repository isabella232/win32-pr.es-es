---
title: Enumeración MPNOTIFY (MpClient. h)
description: Posibles notificaciones de devolución de llamada.
ms.assetid: CCD0CD89-2C6E-453F-9437-E6ED87AD9F29
keywords:
- Enumeración MPNOTIFY características de entorno heredado de Windows
- Puntero de enumeración PMPNOTIFY características de entorno heredado de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105705153"
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

<span id="MPNOTIFY_NONE"></span><span id="mpnotify_none"></span>**MPNOTIFY \_ ninguno**
</dt> <dd></dd> <dt>

<span id="MPNOTIFY_CALL_START"></span><span id="mpnotify_call_start"></span>**\_Inicio de llamada de MPNOTIFY \_**
</dt> <dd>

Inicio de la llamada de notificación.

</dd> <dt>

<span id="MPNOTIFY_CALL_COMPLETE"></span><span id="mpnotify_call_complete"></span>**llamada de MPNOTIFY \_ \_ completada**
</dt> <dd>

Llamada de notificación completada.

</dd> <dt>

<span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span>**\_error interno de MPNOTIFY \_**
</dt> <dd>

Error interno genérico.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_START"></span><span id="mpnotify_status_service_start"></span>**\_Inicio del \_ servicio de estado de MPNOTIFY \_**
</dt> <dd>

El servicio de protección contra malware se ha iniciado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_RUNNING"></span><span id="mpnotify_status_service_running"></span>**servicio de estado de MPNOTIFY en \_ \_ \_ ejecución**
</dt> <dd>

El servicio de protección contra malware se está ejecutando.

</dd> <dt>

<span id="MPNOTIFY_STATUS_SERVICE_STOP"></span><span id="mpnotify_status_service_stop"></span>**\_detención del \_ servicio de estado de MPNOTIFY \_**
</dt> <dd>

El servicio de protección contra malware se ha detenido.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT"></span><span id="mpnotify_status_component"></span>**\_componente de estado MPNOTIFY \_**
</dt> <dd>

Componente determinado habilitar o deshabilitar el estado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_CHANGE"></span><span id="mpnotify_status_change"></span>**\_cambio de estado de MPNOTIFY \_**
</dt> <dd>

El estado general del producto ha cambiado. Llame a [**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md) para obtener el estado actual.

</dd> <dt>

<span id="MPNOTIFY_STATUS_COMPONENT_CONFIGURATION"></span><span id="mpnotify_status_component_configuration"></span>**\_configuración del \_ componente de estado MPNOTIFY \_**
</dt> <dd>

Un componente determinado ha cambiado la configuración.

</dd> <dt>

<span id="MPNOTIFY_STATUS_EXPIRATION_CHANGE"></span><span id="mpnotify_status_expiration_change"></span>**\_cambio de \_ expiración de estado de MPNOTIFY \_**
</dt> <dd>

El estado de expiración del producto ha cambiado.

</dd> <dt>

<span id="MPNOTIFY_STATUS_OFFLINE_SCAN_CHANGE"></span><span id="mpnotify_status_offline_scan_change"></span>**Estado de MPNOTIFY \_ \_ cambio de examen sin conexión \_ \_**
</dt> <dd>

Cambio de Estado requerido del examen sin conexión.

</dd> <dt>

<span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span>**\_Inicio de examen de MPNOTIFY \_**
</dt> <dd>

Examen iniciado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span>**examen de MPNOTIFY en \_ \_ pausa**
</dt> <dd>

Examen en pausa.

</dd> <dt>

<span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span>**examen de MPNOTIFY \_ \_ reanudado**
</dt> <dd>

examen reanudado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span>**\_Cancelar examen de MPNOTIFY \_**
</dt> <dd>

Examen cancelado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span>**examen de MPNOTIFY \_ \_ completado**
</dt> <dd>

Examen completado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span>**\_progreso del examen de MPNOTIFY \_**
</dt> <dd>

Notificación de progreso del recurso específico que se está examinando.

</dd> <dt>

<span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span>**\_error de examen de MPNOTIFY \_**
</dt> <dd>

Error al examinar un recurso determinado. El examen continuará.

</dd> <dt>

<span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span>**examen de MPNOTIFY \_ \_ infectado**
</dt> <dd>

El examen encontró un recurso infectado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span>**MPNOTIFY \_ scan \_ MEMORYSTART**
</dt> <dd>

Se inició el progreso de la notificación en la parte de análisis de la memoria del examen del sistema.

</dd> <dt>

<span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span>**MPNOTIFY \_ scan \_ MEMORYCOMPLETE**
</dt> <dd>

Examinar el progreso para notificar a la parte de análisis de memoria del análisis del sistema se ha completado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_START"></span><span id="mpnotify_scan_sfc_build_start"></span>**MPNOTIFY \_ examinar el inicio de la \_ compilación de SFC \_ \_**
</dt> <dd>

Progreso del examen para notificar que la parte de la compilación de SFC se ha iniciado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_SFC_BUILD_COMPLETE"></span><span id="mpnotify_scan_sfc_build_complete"></span>**MPNOTIFY \_ examinar la \_ compilación de SFC \_ \_ completada**
</dt> <dd>

Progreso del examen para notificar que la parte de la compilación de SFC ha finalizado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_START"></span><span id="mpnotify_scan_fastpath_start"></span>**MPNOTIFY \_ scan \_ FASTPATH \_ Start**
</dt> <dd>

Se ha iniciado la exploración de FastPATH SpyNet.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_COMPLETE"></span><span id="mpnotify_scan_fastpath_complete"></span>**MPNOTIFY \_ examen de \_ FASTPATH \_ completado**
</dt> <dd>

La exploración de FastPATH SpyNet ha finalizado.

</dd> <dt>

<span id="MPNOTIFY_SCAN_FASTPATH_PROGRESS"></span><span id="mpnotify_scan_fastpath_progress"></span>**\_progreso de \_ FASTPATH de examen de MPNOTIFY \_**
</dt> <dd>

Notificación de progreso para los nuevos análisis de FastPATH, que se usan internamente y se convierten en el **\_ \_ progreso de examen de MPNOTIFY** para los externos.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_START"></span><span id="mpnotify_clean_start"></span>**\_Inicio limpio de MPNOTIFY \_**
</dt> <dd>

Limpieza iniciada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_COMPLETE"></span><span id="mpnotify_clean_complete"></span>**limpieza de MPNOTIFY \_ \_ completada**
</dt> <dd>

Limpieza completada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_START"></span><span id="mpnotify_clean_restorepoint_start"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Start**
</dt> <dd>

Se inició para crear un punto de restauración del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_SUCCEEDED"></span><span id="mpnotify_clean_restorepoint_succeeded"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ Succeeded**
</dt> <dd>

Punto de restauración del sistema creado correctamente.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESTOREPOINT_FAILED"></span><span id="mpnotify_clean_restorepoint_failed"></span>**MPNOTIFY \_ Clean \_ RESTOREPOINT \_ failed**
</dt> <dd>

No se pudo crear el punto de restauración del sistema.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_START"></span><span id="mpnotify_clean_threat_start"></span>**Inicio de la amenaza de limpieza de MPNOTIFY \_ \_ \_**
</dt> <dd>

La limpieza se inicia para una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_SUCCEEDED"></span><span id="mpnotify_clean_threat_succeeded"></span>**la amenaza de limpieza de MPNOTIFY se \_ \_ \_ realizó correctamente**
</dt> <dd>

La limpieza se realiza correctamente para una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_FAILED"></span><span id="mpnotify_clean_threat_failed"></span>**error de la amenaza de limpieza de MPNOTIFY \_ \_ \_**
</dt> <dd>

Error en la limpieza de una amenaza determinada. **Error \_ de El código de error de la amenaza de MP \_ \_ no \_ encontrada** indica que no se encontró la amenaza (y no se pudo limpiar).

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_SUCCEEDED"></span><span id="mpnotify_clean_resource_succeeded"></span>**el recurso de limpieza de MPNOTIFY se \_ \_ \_ realizó correctamente**
</dt> <dd>

La limpieza se realiza correctamente para un recurso determinado.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_RESOURCE_FAILED"></span><span id="mpnotify_clean_resource_failed"></span>**\_ \_ \_ no se pudo limpiar el recurso MPNOTIFY**
</dt> <dd>

Error en la limpieza de un recurso determinado.

</dd> <dt>

<span id="MPNOTIFY_CLEAN_THREAT_COMPLETE"></span><span id="mpnotify_clean_threat_complete"></span>**amenaza de limpieza de MPNOTIFY \_ \_ \_ completada**
</dt> <dd>

La limpieza se ha completado para una amenaza determinada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_START"></span><span id="mpnotify_precheck_start"></span>**Inicio de la comprobación de MPNOTIFY \_ \_**
</dt> <dd>

Se inició la comprobación previamente limpia.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_COMPLETE"></span><span id="mpnotify_precheck_complete"></span>**\_comprobación de MPNOTIFY \_ completada**
</dt> <dd>

Comprobación de limpieza completada.

</dd> <dt>

<span id="MPNOTIFY_PRECHECK_RESOURCE_BLOCKED"></span><span id="mpnotify_precheck_resource_blocked"></span>**MPNOTIFY \_ precomprobar \_ recurso \_ bloqueado**
</dt> <dd>

La precomprobación limpia detectó un recurso bloqueado.

</dd> <dt>

<span id="MPNOTIFY_THREAT_DETECTED"></span><span id="mpnotify_threat_detected"></span>**\_amenaza MPNOTIFY \_ detectada**
</dt> <dd>

Se ha detectado una nueva amenaza en el sistema.

</dd> <dt>

<span id="MPNOTIFY_THREAT_MODIFIED"></span><span id="mpnotify_threat_modified"></span>**MPNOTIFY \_ amenaza \_ modificada**
</dt> <dd>

Información de amenazas modificada. Por ejemplo, se ha agregado un nuevo recurso.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_SUCCEEDED"></span><span id="mpnotify_threat_clean_succeeded"></span>**limpieza de la amenaza de MPNOTIFY \_ \_ \_ correcta**
</dt> <dd>

Acción de limpieza correcta para una amenaza.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_FAILED"></span><span id="mpnotify_threat_clean_failed"></span>**\_ \_ error al limpiar la amenaza de MPNOTIFY \_**
</dt> <dd>

No se pudo limpiar la acción de una amenaza. **Error \_ de El código de error de la amenaza de MP \_ \_ no \_ encontrada** indica que no se encontró la amenaza (y no se pudo limpiar).

</dd> <dt>

<span id="MPNOTIFY_THREAT_ABANDONED"></span><span id="mpnotify_threat_abandoned"></span>**MPNOTIFY \_ amenaza \_ abandonada**
</dt> <dd>

No se ha producido ninguna corrección antes de que se detuviera el servicio.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_START"></span><span id="mpnotify_threat_clean_event_start"></span>**\_Inicio de \_ evento de limpieza de amenazas MPNOTIFY \_ \_**
</dt> <dd>

Se ha iniciado una acción de limpieza.

</dd> <dt>

<span id="MPNOTIFY_THREAT_CLEAN_EVENT_COMPLETE"></span><span id="mpnotify_threat_clean_event_complete"></span>**evento de limpieza de la amenaza de MPNOTIFY \_ \_ \_ \_ completado**
</dt> <dd>

Ha finalizado una acción de limpieza.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span>**Inicio de MPNOTIFY \_ SIGUPDATE \_**
</dt> <dd>

Actualización de firma iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span>**Inicio de la búsqueda de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Buscar actualizaciones iniciadas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ Search \_ completado**
</dt> <dd>

Buscar actualizaciones completadas.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_SOFTWARE_UPDATE_AVAILABLE"></span><span id="mpnotify_sigupdate_software_update_available"></span>**actualización de software de MPNOTIFY \_ SIGUPDATE \_ \_ \_ disponible**
</dt> <dd>

Actualización de software disponible.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span>**Inicio de la descarga de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Descarga iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span>**progreso de descarga de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Descarga en curso. Los datos de devolución de llamada contienen progreso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span>**descarga de MPNOTIFY \_ SIGUPDATE \_ \_ completado**
</dt> <dd>

Descarga completada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span>**Inicio de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Instalación iniciada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span>**progreso de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**
</dt> <dd>

Instalación en curso. Los datos de devolución de llamada contienen progreso.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span>**instalación de MPNOTIFY \_ SIGUPDATE \_ \_ completado**
</dt> <dd>

Instalación completada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span>**se \_ \_ requiere un reinicio de MPNOTIFY SIGUPDATE \_**
</dt> <dd>

La actualización requiere un reinicio.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span>**solicitud de MPNOTIFY \_ SIGUPDATE \_ \_ procesada**
</dt> <dd>

El servicio procesó una solicitud de actualización de firma. El error o el éxito se indica mediante **hResult** en los datos de devolución de llamada.

</dd> <dt>

<span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span>**MPNOTIFY \_ SIGUPDATE \_ completado**
</dt> <dd>

Actualización completada. **S \_** El estado False indica que no se necesita ninguna actualización.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_START"></span><span id="mpnotify_sample_start"></span>**\_Inicio del ejemplo MPNOTIFY \_**
</dt> <dd>

Se inició el envío de ejemplo.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_COMPLETE"></span><span id="mpnotify_sample_complete"></span>**ejemplo de MPNOTIFY \_ \_ completado**
</dt> <dd>

Envío de ejemplo completado.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_START"></span><span id="mpnotify_sample_item_start"></span>**\_Inicio del \_ elemento de ejemplo MPNOTIFY \_**
</dt> <dd>

Se inició el envío del elemento de ejemplo específico. El índice de elemento de ejemplo está disponible en los [**\_ datos de MPSAMPLE**](mpsample-data.md).

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_SUCCEEDED"></span><span id="mpnotify_sample_item_succeeded"></span>**el \_ elemento de ejemplo MPNOTIFY se \_ \_ realizó correctamente**
</dt> <dd>

El envío del elemento de ejemplo específico se realizó correctamente.

</dd> <dt>

<span id="MPNOTIFY_SAMPLE_ITEM_FAILED"></span><span id="mpnotify_sample_item_failed"></span>**error en el \_ elemento de ejemplo MPNOTIFY \_ \_**
</dt> <dd>

Error en el envío del elemento de ejemplo específico. El código de error está disponible en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).

</dd> <dt>

<span id="MPNOTIFY_RESERVED_DATA"></span><span id="mpnotify_reserved_data"></span>**MPNOTIFY \_ \_ datos reservados**
</dt> <dd>

Datos reservados internos.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_ADDED"></span><span id="mpnotify_fastpath_sig_added"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ Added**
</dt> <dd>

Una firma FastPath ha agregado o deshabilitado una firma.

</dd> <dt>

<span id="MPNOTIFY_FASTPATH_SIG_REMOVED"></span><span id="mpnotify_fastpath_sig_removed"></span>**MPNOTIFY \_ FASTPATH \_ SIG \_ quitado**
</dt> <dd>

Se ha quitado una firma de FastPath.

</dd> <dt>

<span id="MPNOTIFY_NIS_PRIVATE"></span><span id="mpnotify_nis_private"></span>**MPNOTIFY \_ NIS \_ privado**
</dt> <dd>

Notificaciones privado NIS. No se debe registrar ningún socio para esto.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_CHANGE"></span><span id="mpnotify_health_change"></span>**\_cambio de estado de MPNOTIFY \_**
</dt> <dd>

El servicio AM entró en un estado nuevo.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_RECOVERY"></span><span id="mpnotify_health_recovery"></span>**\_recuperación de mantenimiento de MPNOTIFY \_**
</dt> <dd>

El servicio AM se ha recuperado de un estado.

</dd> <dt>

<span id="MPNOTIFY_HEALTH_START"></span><span id="mpnotify_health_start"></span>**\_Inicio de estado de MPNOTIFY \_**
</dt> <dd>

El servicio AM ha inicializado el estado del sistema.

</dd> <dt>

<span id="MPNOTIFY_ENDOFLIFE_CHANGE"></span><span id="mpnotify_endoflife_change"></span>**cambio de MPNOTIFY \_ ENDOFLIFE \_**
</dt> <dd>

Las fechas de expiración del "final del ciclo de vida" del servicio AM han cambiado.

</dd> <dt>

<span id="MPNOTIFY_MALWARETOAST_DATA"></span><span id="mpnotify_malwaretoast_data"></span>**datos de MPNOTIFY \_ MALWARETOAST \_**
</dt> <dd>

El servicio AM ha detectado malware que podría haber provocado un cambio de configuración crítico en el equipo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpManagerStatusQueryEx**](mpmanagerstatusqueryex.md)
</dt> <dt>

[**datos de MPCALLBACK \_**](mpcallback-data.md)
</dt> <dt>

[**datos de MPSAMPLE \_**](mpsample-data.md)
</dt> </dl>

 

 





