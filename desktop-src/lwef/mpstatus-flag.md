---
title: Enumeración MPSTATUS_FLAG (MpClient. h)
description: Posibles marcas de bits de estado de producto generales.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG enumeración características de entorno heredado de Windows
- PMPSTATUS_FLAG el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSTATUS_FLAG
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c7175980c09c63938be04626091c31b53335756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665979"
---
# <a name="mpstatus_flag-enumeration"></a>\_Enumeración de marcas MPSTATUS

Posibles marcas de bits de estado de producto generales.

## <a name="syntax"></a>Sintaxis


```C++
typedef enum tagMPSTATUS_FLAG { 
  MP_STATUS_FLAG_NONE                           = 0,
  MP_STATUS_FLAG_SERVICE_UNAVAILABLE            = 1 << 0,
  MP_STATUS_FLAG_MPENGINE_UNAVAILABLE           = 1 << 1,
  MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED       = 1 << 2,
  MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED         = 1 << 3,
  MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED   = 1 << 4,
  MP_STATUS_FLAG_DUE_AV_SIGNATURE               = 1 << 5,
  MP_STATUS_FLAG_DUE_AS_SIGNATURE               = 1 << 6,
  MP_STATUS_FLAG_DUE_QUICK_SCAN                 = 1 << 7,
  MP_STATUS_FLAG_DUE_FULL_SCAN                  = 1 << 8,
  MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN         = 1 << 9,
  MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING    = 1 << 10,
  MP_STATUS_FLAG_DUE_SAMPLES                    = 1 << 11,
  MP_STATUS_FLAG_EVALUATION_MODE                = 1 << 12,
  MP_STATUS_FLAG_NONGENUINE                     = 1 << 13,
  MP_STATUS_FLAG_PRODUCT_EXPIRED                = 1 << 14,
  MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED       = 1 << 15,
  MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN     = 1 << 16,
  MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE       = 1 << 17,
  MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE   = 1 << 18,
  MP_STATUS_FLAG_HEALTH_INITIALIZED             = 1 << 19,
  MP_STATUS_FLAG_DUE_PLATFORM_UPDATE            = 1 << 20,
  MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE     = 1 << 21,
  MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED  = 1 << 22,
  MP_STATUS_FLAG_END_OF_LIFE                    = 1 << 23,
  MP_STATUS_FLAG_MAX                            = 1 << 23,
  MP_STATUS_FLAG_ALL                            = (1 << 24)-1
} MPSTATUS_FLAG, *PMPSTATUS_FLAG;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**marca de estado de MP \_ \_ \_ ninguno**
</dt> <dd>

No se ha establecido ninguna marca de estado (estado no inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**marca de estado de MP \_ \_ \_ servicio \_ no disponible**
</dt> <dd>

El servicio no se está ejecutando.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**marca de estado de MP \_ \_ \_ MPENGINE \_ no disponible**
</dt> <dd>

El servicio se inició sin ningún motor de protección contra malware.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**marca de estado de MP \_ \_ \_ amenaza \_ \_ requerida**
</dt> <dd>

Examen completo pendiente debido a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**marca de estado de MP se \_ \_ \_ \_ requiere reinicio de amenazas \_**
</dt> <dd>

Reinicio pendiente debido a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**marca de estado de MP \_ \_ \_ \_ pasos manuales de amenazas \_ \_ necesarios**
</dt> <dd>

Pasos manuales pendientes debidos a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**marca de estado de MP \_ \_ \_ por \_ firma de AV \_**
</dt> <dd>

Firmas de antivirus no actualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**\_ \_ marca de estado \_ de MP debida \_ como \_ firma**
</dt> <dd>

Firmas de AntiSpyware no actualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**detección de estado de MP \_ \_ debido a \_ \_ \_ examen rápido**
</dt> <dd>

No se ha producido ningún examen rápido durante un período especificado.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**marca de estado del módulo de administración \_ \_ debido a \_ \_ \_ examen completo**
</dt> <dd>

no se ha producido ningún examen completo durante un período especificado

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**marca de estado del módulo de administración \_ \_ \_ \_ examen del sistema en curso \_**
</dt> <dd>

Examen iniciado por el sistema en curso.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**marca de estado de MP \_ \_ limpieza de \_ rutina en curso \_ \_**
</dt> <dd>

Limpieza iniciada por el sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**marca de estado de MP \_ \_ \_ por \_ ejemplos**
</dt> <dd>

Hay ejemplos de envío pendientes.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**\_modo de \_ evaluación de marca de estado de MP \_ \_**
</dt> <dd>

El producto se está ejecutando en modo de evaluación.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**marca de estado de MP no \_ \_ \_ original**
</dt> <dd>

El producto se está ejecutando en modo Windows no original.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**marca de estado de MP \_ \_ \_ \_ expirada del producto**
</dt> <dd>

Producto expirado.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**marca de estado de MP \_ \_ \_ amenaza \_ Callisto \_ requerida**
</dt> <dd>

Se requiere un análisis sin conexión de Callisto.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**\_ \_ \_ servicio \_ de marca de estado de MP al \_ apagar el sistema \_**
</dt> <dd>

El servicio se está cerrando como parte del cierre del sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**\_ \_ \_ error crítico de servicio de indicador \_ de estado de MP \_**
</dt> <dd>

Error en la corrección de amenazas de forma crítica.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**error de servicio de indicador de estado de MP \_ \_ \_ \_ no \_ crítico \_**
</dt> <dd>

Error de corrección de amenazas no crítico.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**Estado de indicador de estado de MP \_ \_ \_ \_ inicializado**
</dt> <dd>

No se ha establecido ninguna marca de estado (estado bien inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**marca de estado de MP \_ \_ \_ debida \_ actualización de plataforma \_**
</dt> <dd>

La plataforma no está actualizada.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**marca de estado de MP \_ \_ actualización de \_ plataforma en curso \_ \_**
</dt> <dd>

La actualización de la plataforma está en curso.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**\_plataforma de marca de estado de MP \_ \_ \_ \_ a punto de \_ ser \_ obsoleto**
</dt> <dd>

La plataforma está a punto de estar obsoleta

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**\_ \_ marca de estado \_ de MP final \_ de \_ ciclo de vida**
</dt> <dd>

La firma o el final de la plataforma de la vida es posterior o está pendiente.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**marca de estado de MP \_ \_ \_ máx.**
</dt> <dd>

Marca válida máxima.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**marca de estado de MP \_ \_ \_ todos**
</dt> <dd>

Valor máximo posible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





