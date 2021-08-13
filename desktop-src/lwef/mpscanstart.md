---
title: Función MpScanStart (MpClient.h)
description: Inicia una operación de examen.
ms.assetid: 3AF147C8-A41F-4193-AE28-72C1FBD18BA2
keywords:
- Función MpScanStart Legacy Windows Environment Features
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
ms.openlocfilehash: 34d56f6814ecdd13b2db4f698e8cc122d4d15e325bda17d82d56a5796d8590fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450245"
---
# <a name="mpscanstart-function"></a>Función MpScanStart

Inicia una operación de examen.

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

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controlar la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*ScanType* \[ En\]
</dt> <dd>

Tipo: **[ **MPSCAN \_ TYPE**](mpscan-type.md)**

Especifica el tipo de examen. Este parámetro debe ser uno de los miembros de la [**enueration \_ MPSCAN TYPE.**](mpscan-type.md)

</dd> <dt>

*dwScanOptions* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Especifica varias opciones para la operación de examen.



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPSCAN_OPTION_NONE"></span><span id="mpscan_option_none"></span><dl> <dt>**OPCIÓN MPSCAN \_ \_ NONE**</dt> </dl>                               | No se solicita ninguna opción específica.<br/>                                                                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_ASYNC"></span><span id="mpscan_option_async"></span><dl> <dt>**MPSCAN \_ OPTION \_ ASYNC**</dt> </dl>                            | La operación de examen va a ser asincrónica, donde **MpScanStart** vuelve inmediatamente después del inicio correcto del examen. (De forma predeterminada, la operación de examen es sincrónica, lo que **significa que MpScanStart** solo devolverá una vez finalizado el examen).<br/>      |
| <span id="MPSCAN_OPTION_PROGRESS"></span><span id="mpscan_option_progress"></span><dl> <dt>**PROGRESO DE LA \_ OPCIÓN MPSCAN \_**</dt> </dl>                   | El autor de la llamada está interesado en recibir información de progreso del examen a través de una devolución de llamada.<br/>                                                                                                                                                                            |
| <span id="MPSCAN_OPTION_LOWPRIORITY"></span><span id="mpscan_option_lowpriority"></span><dl> <dt>**OPCIÓN DE MPSCAN \_ \_ LOWPRIORITY**</dt> </dl>          | Realice el examen con prioridad baja. (De forma predeterminada, la operación de examen se realiza con prioridad normal).<br/>                                                                                                                                                     |
| <span id="MPSCAN_OPTION_PACKEDEXES"></span><span id="mpscan_option_packedexes"></span><dl> <dt>**OPCIÓN MPSCAN \_ \_ PACKEDEXES**</dt> </dl>             | Examinar archivos ejecutables empaquetados en busca de posibles amenazas.<br/>                                                                                                                                                                                                              |
| <span id="MPSCAN_OPTION_ARCHIVES"></span><span id="mpscan_option_archives"></span><dl> <dt>**ARCHIVOS DE OPCIONES DE MPSCAN \_ \_**</dt> </dl>                   | Examinar el contenido del archivo en busca de posibles amenazas. Los archivos son archivos con extensiones como .zip, .cab o .tar.<br/>                                                                                                                                                |
| <span id="MPSCAN_OPTION_HEURISTICS"></span><span id="mpscan_option_heuristics"></span><dl> <dt>**\_HEURÍSTICA DE LA OPCIÓN \_ MPSCAN**</dt> </dl>             | Habilite el examen basado en heurística. Esto buscará amenazas con el tipo de detección establecido en heurística.<br/>                                                                                                                                                        |
| <span id="MPSCAN_OPTION_REPORTFRIENDLY"></span><span id="mpscan_option_reportfriendly"></span><dl> <dt>**MPSCAN \_ OPTION \_ REPORTFRIENDLY**</dt> </dl> | Informe de elementos descriptivos en un examen de recursos. Está pensado solo para uso interno.<br/>                                                                                                                                                                          |
| <span id="MPSCAN_OPTION_REPORTUNKNOWN"></span><span id="mpscan_option_reportunknown"></span><dl> <dt>**MPSCAN \_ OPTION \_ REPORTUNKNOWN**</dt> </dl>    | Informe de elementos desconocidos en un examen de recursos. Está pensado solo para uso interno.<br/>                                                                                                                                                                           |
| <span id="MPSCAN_OPTION_NOCONSOLIDATE"></span><span id="mpscan_option_noconsolidate"></span><dl> <dt>**OPCIÓN DE MPSCAN \_ \_ NOCONSOLIDATE**</dt> </dl>    | No consolide los resultados del examen con la vista de amenazas global. Esto es útil para un cliente (por ejemplo, un cliente de correo electrónico) que desea controlar la limpieza de la experiencia de usuario por sí mismo en lugar de permitir la limpieza predeterminada de la experiencia de usuario antimalware. Está pensado solo para uso interno.<br/> |



 

</dd> <dt>

*pScanResources* \[ en, opcional\]
</dt> <dd>

Tipo: **\_ PMPSCAN RESOURCES**

Puntero a la información del recurso de examen. Este parámetro debe ser **NULL para** un examen rápido. Se trata de un parámetro opcional para un examen completo. Para un examen de recursos, este parámetro debe especificarse con al menos una estructura de información de recursos. Para examinar recursos específicos, el autor de la llamada debe tener el permiso **\_ GENERIC READ** para el recurso. Consulte MPSCAN RESOURCES ( [**RECURSOS DE \_ MPSCAN).**](mpscan-resources.md)

</dd> <dt>

*pCallbackInfo* \[ en, opcional\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ INFO**

Puntero a la información de devolución de llamada utilizada para alimentar al cliente con cambios de estado de examen (como inicio y completado) e información de progreso. Los [**DATOS MPCALLBACK \_ pasados**](mpcallback-data.md) de vuelta en la función de devolución de llamada notifican el estado real del examen y la información relacionada con el progreso. A continuación se muestra una lista de posibles devoluciones de llamada:



| Value                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SCAN_START"></span><span id="mpnotify_scan_start"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ START**</dt> </dl>                            | Se inició la operación de examen.<br/>                                                                                                                                                                                                                                                                                       |
| <span id="MPNOTIFY_SCAN_COMPLETE"></span><span id="mpnotify_scan_complete"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ COMPLETE**</dt> </dl>                   | Operación de examen completada. Hay información adicional disponible a través de [**la estructura \_ MPSCAN DATA.**](mpscan-data.md)<br/>                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_PAUSED"></span><span id="mpnotify_scan_paused"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ PAUSED**</dt> </dl>                         | La operación de examen está en pausa.<br/>                                                                                                                                                                                                                                                                                     |
| <span id="MPNOTIFY_SCAN_RESUMED"></span><span id="mpnotify_scan_resumed"></span><dl> <dt>**EXAMEN DE MPNOTIFY \_ \_ REANUDADO**</dt> </dl>                      | La operación de examen se reanudó desde la pausa.<br/>                                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_SCAN_CANCEL"></span><span id="mpnotify_scan_cancel"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ CANCEL**</dt> </dl>                         | Se canceló la operación de examen.<br/>                                                                                                                                                                                                                                                                                 |
| <span id="MPNOTIFY_SCAN_PROGRESS"></span><span id="mpnotify_scan_progress"></span><dl> <dt>**PROGRESO DEL EXAMEN DE MPNOTIFY \_ \_**</dt> </dl>                   | Examinar la información de progreso. Hay información adicional (como estadísticas de recursos) disponible a través de la [**estructura DE DATOS \_ MPSCAN.**](mpscan-data.md)<br/>                                                                                                                                                               |
| <span id="MPNOTIFY_SCAN_ERROR"></span><span id="mpnotify_scan_error"></span><dl> <dt>**ERROR DE EXAMEN DE MPNOTIFY \_ \_**</dt> </dl>                            | Examinar la información de error de un recurso específico. La información de recursos específica está disponible a través de [**la estructura \_ MPSCAN DATA.**](mpscan-data.md)<br/>                                                                                                                                                             |
| <span id="MPNOTIFY_SCAN_INFECTED"></span><span id="mpnotify_scan_infected"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ INFECTADO**</dt> </dl>                   | El examen encontró un recurso infectado. Tenga en cuenta que, en la mayoría de los casos, esto dará lugar a alguna amenaza notificada al final del examen. A veces, es posible que no se materialice como una amenaza debido a exclusiones. Hay información adicional sobre los recursos infectados disponible a través de [**la estructura \_ MPSCAN DATA.**](mpscan-data.md)<br/> |
| <span id="MPNOTIFY_SCAN_MEMORYSTART"></span><span id="mpnotify_scan_memorystart"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYSTART**</dt> </dl>          | Se ha iniciado la parte del examen rápido del examen completo.<br/>                                                                                                                                                                                                                                                              |
| <span id="MPNOTIFY_SCAN_MEMORYCOMPLETE"></span><span id="mpnotify_scan_memorycomplete"></span><dl> <dt>**MPNOTIFY \_ SCAN \_ MEMORYCOMPLETE**</dt> </dl> | Se ha completado la parte del examen rápido del examen completo.<br/>                                                                                                                                                                                                                                                            |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**ERROR INTERNO DE \_ \_ MPNOTIFY**</dt> </dl>          | La operación de examen ha detectado un error genérico. HResult *en* [**MPCALLBACK \_ DATA**](mpcallback-data.md) tiene el código de error específico.<br/>                                                                                                                                                                   |



 

</dd> <dt>

*phScanHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de examen devuelto que identifica el examen iniciado actualmente. Este identificador se puede usar en llamadas de función posteriores, como para recuperar un resultado de examen. El identificador debe cerrarse con la [**función MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT** con errores. El autor de la llamada puede [**usar la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Header<br/>                   | <dl> <dt>MpClient.h</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MpClient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MpErrorMessageFormat**](mperrormessageformat.md)
</dt> <dt>

[**MpHandleClose**](mphandleclose.md)
</dt> <dt>

[**MpManagerAbrir**](mpmanageropen.md)
</dt> <dt>

[**DATOS DE DEVOLUCIÓN DE \_ LLAMADA DE MP**](mpcallback-data.md)
</dt> <dt>

[**DATOS \_ DE MPSCAN**](mpscan-data.md)
</dt> <dt>

[**RECURSOS DE \_ MPSCAN**](mpscan-resources.md)
</dt> <dt>

[**TIPO \_ MPSCAN**](mpscan-type.md)
</dt> </dl>

 

 





