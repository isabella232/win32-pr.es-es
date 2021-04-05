---
title: Función MpScanStart (MpClient. h)
description: Inicia una operación de digitalización.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Función MpScanStart características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpScanStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d343787edc85a18dc7471d19165999a7252d18a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996659"
---
# <a name="mpscanstart-function"></a>MpScanStart función)

Inicia una operación de digitalización.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpScanStart(
  _In_     MPHANDLE          hMpHandle,
  _In_     MPSCAN_TYPE       ScanType,
  _In_     DWORD             dwScanOptions,
  _In_opt_ PMPSCAN_RESOURCES pScanResources,
  _In_opt_ PMPCALLBACK_INFO  pCallbackInfo,
  _Out_    PMPHANDLE         phScanHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*ScanType* \[ de\]
</dt> <dd>

Tipo: **[ **MPSCAN \_ Type**](mpscan-type.md)**

Especifica el tipo de examen. Este parámetro debe ser uno de los miembros del [**\_ tipo MPSCAN**](mpscan-type.md) enueration.

</dd> <dt>

*dwScanOptions* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Especifica varias opciones para la operación de examen.



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**opción de MPSCAN \_ \_ ninguna**</dt> </dl>                               | No se solicita ninguna opción específica.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**\_opción MPSCAN \_ Async**</dt> </dl>                            | La operación de examen es asincrónica, donde **MpScanStart** vuelve inmediatamente después del inicio correcto del examen. (De forma predeterminada, la operación de examen es sincrónica, lo que significa que **MpScanStart** solo devolverá una vez finalizada la exploración).<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**progreso de la \_ opción MPSCAN \_**</dt> </dl>                   | El autor de la llamada está interesado en recibir información de progreso del examen a través de una devolución de llamada.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**MPSCAN \_ opción \_ LOWPRIORITY**</dt> </dl>          | Realice el examen con prioridad baja. (De forma predeterminada, la operación de examen se realiza con prioridad normal).<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**MPSCAN \_ opción \_ PACKEDEXES**</dt> </dl>             | Examinar los ejecutables empaquetados en busca de posibles amenazas.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**\_archivos de opciones de MPSCAN \_**</dt> </dl>                   | Examinar el contenido del archivo en busca de posibles amenazas. Los archivos son archivos con extensiones como. zip,. cab o. tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**heurística de la \_ opción MPSCAN \_**</dt> </dl>             | Habilitar el examen basado en la heurística. Se buscarán amenazas con el tipo de detección establecido en heurística.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**MPSCAN \_ opción \_ REPORTFRIENDLY**</dt> </dl> | Notificar elementos descriptivos en un examen de recursos. Solo está pensado para uso interno.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**MPSCAN \_ opción \_ REPORTUNKNOWN**</dt> </dl>    | Notificar elementos desconocidos en un examen de recursos. Solo está pensado para uso interno.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**\_opción MPSCAN \_ noconsolidate**</dt> </dl>    | No consolide los resultados de los exámenes con la vista de amenazas global. Esto resulta útil para un cliente (por ejemplo, un cliente de correo electrónico) que desee controlar la experiencia de usuario de limpieza por sí misma en lugar de permitir la limpieza antimalware predeterminada. Solo está pensado para uso interno.<br/> |



 

</dd> <dt>

*pScanResources* \[ en, opcional\]
</dt> <dd>

Tipo: **\_ recursos PMPSCAN**

Puntero a la información de recurso de examen. Este parámetro debe ser **null** para un examen rápido. Se trata de un parámetro opcional para un examen completo. Para un examen de recursos, este parámetro debe especificarse con al menos una estructura de información de recursos. Para examinar recursos específicos, el llamador debe tener permiso de **\_ lectura genérico** para el recurso. Vea [**\_ recursos de MPSCAN**](mpscan-resources.md).

</dd> <dt>

*pCallbackInfo* \[ en, opcional\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ info**

Un puntero a la información de devolución de llamada que se usa para alimentar al cliente con los cambios de estado de exploración (como inicio y finalización) y la información de progreso. Los [**\_ datos de MPCALLBACK**](mpcallback-data.md) que se devuelven en la función de devolución de llamada notifican el estado de examen real y la información relacionada con el progreso. A continuación se muestra una lista de posibles devoluciones de llamada:



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**\_Inicio de examen de MPNOTIFY \_**</dt> </dl>                            | Operación de examen iniciada.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**examen de MPNOTIFY \_ \_ completado**</dt> </dl>                   | Operación de examen completada. Hay información adicional disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**examen de MPNOTIFY en \_ \_ pausa**</dt> </dl>                         | La operación de examen está en pausa.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**examen de MPNOTIFY \_ \_ reanudado**</dt> </dl>                      | La operación de examen se reanudó de la pausa.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**\_Cancelar examen de MPNOTIFY \_**</dt> </dl>                         | Se canceló la operación de examen.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**\_progreso del examen de MPNOTIFY \_**</dt> </dl>                   | Información de progreso de la exploración. La información adicional (como las estadísticas de recursos) está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**\_error de examen de MPNOTIFY \_**</dt> </dl>                            | Examinar la información de error de un recurso específico. La información de recursos específica está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**examen de MPNOTIFY \_ \_ infectado**</dt> </dl>                   | El examen encontró un recurso infectado. Tenga en cuenta que, en la mayoría de los casos, esto dará lugar a la notificación de alguna amenaza al final del examen. En ocasiones, es posible que no se materializa como amenaza debido a las exclusiones. La información adicional sobre los recursos infectados está disponible a través de la estructura de [**\_ datos MPSCAN**](mpscan-data.md) .<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ scan \_ MEMORYSTART**</dt> </dl>          | Se ha iniciado la parte de examen rápido del examen completo.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ scan \_ MEMORYCOMPLETE**</dt> </dl> | Se ha completado la parte de examen rápido del examen completo.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_error interno de MPNOTIFY \_**</dt> </dl>          | La operación de examen ha encontrado un error genérico. El *hResult* en [**los \_ datos de MPCALLBACK**](mpcallback-data.md) tiene el código de error específico.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ enuncia\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de examen devuelto que identifica el examen iniciado actualmente. Este identificador se puede usar en las llamadas de función subsiguientes, como para recuperar el resultado de un examen. El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se ejecuta correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un código **HRESULT** erróneo. El autor de la llamada puede usar la función [**MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>MpClient. h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerOpen**](mpmanageropen.md)
</dt> <dt>

[**datos de MPCALLBACK \_**](mpcallback-data.md)
</dt> <dt>

[**datos de MPSCAN \_**](mpscan-data.md)
</dt> <dt>

[**recursos de MPSCAN \_**](mpscan-resources.md)
</dt> <dt>

[**\_tipo MPSCAN**](mpscan-type.md)
</dt> </dl>

 

 





