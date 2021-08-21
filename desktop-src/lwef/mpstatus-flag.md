---
title: MPSTATUS_FLAG enumeración (MpClient.h)
description: Posibles marcas de bits de estado general del producto.
ms.assetid: BF2E6506-E76A-4785-8E91-99937B413548
keywords:
- MPSTATUS_FLAG enumeración heredada de Windows environment
- PMPSTATUS_FLAG puntero de enumeración heredados Windows environment
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
ms.openlocfilehash: 4d850f0e8de9a3b0ed18a1a1353dfdef40d41bcb1ce4d17265ec245e82ba73f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747039"
---
# <a name="mpstatus_flag-enumeration"></a>Enumeración \_ MPSTATUS FLAG

Posibles marcas de bits de estado general del producto.

## <a name="syntax"></a>Syntax


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

<span id="MP_STATUS_FLAG_NONE"></span><span id="mp_status_flag_none"></span>**MARCA \_ DE ESTADO DE MP \_ \_ NONE**
</dt> <dd>

No hay marcas de estado establecidas (estado no inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_UNAVAILABLE"></span><span id="mp_status_flag_service_unavailable"></span>**SERVICIO DE \_ MARCA DE ESTADO DE MP NO \_ \_ \_ DISPONIBLE**
</dt> <dd>

El servicio no se está ejecutando.

</dd> <dt>

<span id="MP_STATUS_FLAG_MPENGINE_UNAVAILABLE"></span><span id="mp_status_flag_mpengine_unavailable"></span>**MP \_ STATUS \_ FLAG \_ MPENGINE \_ UNAVAILABLE**
</dt> <dd>

El servicio se inició sin ningún motor de protección contra malware.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_FULLSCAN_REQUIRED"></span><span id="mp_status_flag_threat_fullscan_required"></span>**MP \_ STATUS \_ FLAG \_ THREAT \_ FULLSCAN \_ REQUIRED**
</dt> <dd>

Examen completo pendiente debido a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_REBOOT_REQUIRED"></span><span id="mp_status_flag_threat_reboot_required"></span>**SE REQUIERE \_ EL REINICIO DE LA AMENAZA DE MARCA DE ESTADO DEL \_ \_ \_ \_ MP**
</dt> <dd>

Reinicio pendiente debido a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_MANUAL_STEPS_REQUIRED"></span><span id="mp_status_flag_threat_manual_steps_required"></span>**PASOS MANUALES \_ DE AMENAZAS DE MARCA DE ESTADO DE MP \_ \_ \_ \_ \_ REQUERIDOS**
</dt> <dd>

Pasos manuales pendientes debido a una acción de amenaza.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AV_SIGNATURE"></span><span id="mp_status_flag_due_av_signature"></span>**MARCA DE \_ ESTADO DE MP DUE AV \_ \_ \_ \_ SIGNATURE**
</dt> <dd>

Firmas de antivirus no actualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_AS_SIGNATURE"></span><span id="mp_status_flag_due_as_signature"></span>**MARCA DE \_ ESTADO DE MP DEBIDO COMO \_ \_ \_ \_ FIRMA**
</dt> <dd>

Firmas antispyware no actualizadas.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_QUICK_SCAN"></span><span id="mp_status_flag_due_quick_scan"></span>**MARCA DE \_ ESTADO DE MP DUE QUICK \_ \_ \_ \_ SCAN**
</dt> <dd>

No se ha producido ningún examen rápido durante un período especificado.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_FULL_SCAN"></span><span id="mp_status_flag_due_full_scan"></span>**MARCA DE \_ ESTADO DE MP DUE FULL \_ \_ \_ \_ SCAN**
</dt> <dd>

no se ha producido ningún examen completo durante un período especificado.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_SYSTEM_SCAN"></span><span id="mp_status_flag_inprogress_system_scan"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ SYSTEM \_ SCAN**
</dt> <dd>

Examen iniciado por el sistema en curso.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_ROUTINE_CLEANING"></span><span id="mp_status_flag_inprogress_routine_cleaning"></span>**LIMPIEZA \_ \_ RUTINARIA \_ DE MARCA DE \_ \_ ESTADO DE MP**
</dt> <dd>

Limpieza iniciada por el sistema en curso.

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_SAMPLES"></span><span id="mp_status_flag_due_samples"></span>**EJEMPLOS DE \_ MARCA DE ESTADO DE MP \_ \_ DUE \_**
</dt> <dd>

Hay ejemplos pendientes de envío.

</dd> <dt>

<span id="MP_STATUS_FLAG_EVALUATION_MODE"></span><span id="mp_status_flag_evaluation_mode"></span>**MODO DE \_ EVALUACIÓN DE MARCA DE ESTADO DE \_ \_ \_ MP**
</dt> <dd>

El producto se ejecuta en modo de evaluación.

</dd> <dt>

<span id="MP_STATUS_FLAG_NONGENUINE"></span><span id="mp_status_flag_nongenuine"></span>**MARCA \_ DE ESTADO DE MP \_ \_ NOGENUINE**
</dt> <dd>

El producto se ejecuta en modo de Windows original.

</dd> <dt>

<span id="MP_STATUS_FLAG_PRODUCT_EXPIRED"></span><span id="mp_status_flag_product_expired"></span>**PRODUCTO DE \_ MARCA DE ESTADO DE MP \_ \_ \_ EXPIRADO**
</dt> <dd>

El producto ha expirado.

</dd> <dt>

<span id="MP_STATUS_FLAG_THREAT_CALLISTO_REQUIRED"></span><span id="mp_status_flag_threat_callisto_required"></span>**MP \_ STATUS \_ FLAG \_ THREAT \_ CALLISTO \_ REQUIRED**
</dt> <dd>

Se requiere un examen fuera de línea de Callisto.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_ON_SYSTEM_SHUTDOWN"></span><span id="mp_status_flag_service_on_system_shutdown"></span>**SERVICIO DE \_ MARCA DE ESTADO DE MP AL APAGAR EL \_ \_ \_ \_ \_ SISTEMA**
</dt> <dd>

El servicio se está cerrando como parte del apagado del sistema.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_critical_failure"></span>**ERROR CRÍTICO \_ DEL SERVICIO DE MARCA DE ESTADO DE \_ \_ \_ \_ MP**
</dt> <dd>

Error crítico en la corrección de amenazas.

</dd> <dt>

<span id="MP_STATUS_FLAG_SERVICE_NON_CRITICAL_FAILURE"></span><span id="mp_status_flag_service_non_critical_failure"></span>**ERROR CRÍTICO \_ DEL SERVICIO DE MARCA DE ESTADO DE \_ \_ \_ \_ \_ MP**
</dt> <dd>

Error de corrección de amenazas no crítico.

</dd> <dt>

<span id="MP_STATUS_FLAG_HEALTH_INITIALIZED"></span><span id="mp_status_flag_health_initialized"></span>**ESTADO DEL \_ \_ MP: ESTADO \_ \_ INICIALIZADO**
</dt> <dd>

No hay marcas de estado establecidas (estado bien inicializado).

</dd> <dt>

<span id="MP_STATUS_FLAG_DUE_PLATFORM_UPDATE"></span><span id="mp_status_flag_due_platform_update"></span>**MP \_ STATUS \_ FLAG \_ DUE \_ PLATFORM \_ UPDATE**
</dt> <dd>

La plataforma no está actualizada.

</dd> <dt>

<span id="MP_STATUS_FLAG_INPROGRESS_PLATFORM_UPDATE"></span><span id="mp_status_flag_inprogress_platform_update"></span>**MP \_ STATUS \_ FLAG \_ INPROGRESS \_ PLATFORM \_ UPDATE**
</dt> <dd>

La actualización de la plataforma está en curso.

</dd> <dt>

<span id="MP_STATUS_FLAG_PLATFORM_ABOUT_TO_BE_OUTDATED"></span><span id="mp_status_flag_platform_about_to_be_outdated"></span>**PLATAFORMA DE \_ MARCA DE ESTADO DE MP A PUNTO DE ESTAR \_ \_ \_ \_ \_ \_ OBSOLETA**
</dt> <dd>

La plataforma está a punto de estar obsoleta

</dd> <dt>

<span id="MP_STATUS_FLAG_END_OF_LIFE"></span><span id="mp_status_flag_end_of_life"></span>**FIN \_ DEL CICLO DE VIDA DE LA MARCA DE ESTADO DEL \_ \_ \_ \_ MP**
</dt> <dd>

El final del ciclo de vida de la firma o plataforma es pasado o está pendiente.

</dd> <dt>

<span id="MP_STATUS_FLAG_MAX"></span><span id="mp_status_flag_max"></span>**MARCA \_ DE ESTADO DE MP \_ \_ MÁX.**
</dt> <dd>

Marca válida máxima.

</dd> <dt>

<span id="MP_STATUS_FLAG_ALL"></span><span id="mp_status_flag_all"></span>**MARCA \_ DE ESTADO DE MP \_ \_ ALL**
</dt> <dd>

Valor máximo posible.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                  |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





