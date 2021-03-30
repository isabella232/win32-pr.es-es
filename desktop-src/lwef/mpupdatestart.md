---
title: Función MpUpdateStart (MpClient. h)
description: Inicia una operación de actualización de firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Función MpUpdateStart características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MpUpdateStart
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39867525529339c6b354ae771b070589ca52acfa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492628"
---
# <a name="mpupdatestart-function"></a>MpUpdateStart función)

Inicia una operación de actualización de firma.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI MpUpdateStart(
  _In_     MPHANDLE         hMpHandle,
  _In_     DWORD            dwUpdateOptions,
  _In_opt_ PMPCALLBACK_INFO pCallbackInfo,
  _Out_    PMPHANDLE        phUpdateHandle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hMpHandle* \[ de\]
</dt> <dd>

Tipo: **MPHANDLE**

Identificador de la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*dwUpdateOptions* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Especifica la opción para la operación de actualización de la firma. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**opción de MPUPDATE \_ \_ ninguna**</dt> </dl>                | No se solicita ninguna opción específica.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**\_opción MPUPDATE \_ Async**</dt> </dl>             | La operación de actualización es asincrónica, donde **MpUpdateStart** vuelve inmediatamente después de que se iniciase correctamente la actualización de la firma. (De forma predeterminada, la operación de actualización es sincrónica, lo que significa que **MpUpdateStart** solo devolverá una vez finalizada la actualización de la firma).<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**progreso de la \_ opción MPUPDATE \_**</dt> </dl>    | El autor de la llamada está interesado en recibir información de progreso de actualización de firmas a través de una devolución de llamada.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**\_opción MPUPDATE \_ http**</dt> </dl>                | La actualización de la firma se realiza mediante la descarga del paquete de firmas completo desde el sitio del portal de seguridad de Microsoft. Se puede usar como opción de reserva si el cliente tiene un problema de descarga de la firma a través de Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**MPUPDATE \_ , opción \_ UNC**</dt> </dl>                   | Realiza una actualización de firmas mediante la descarga directa desde recursos compartidos UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**\_opción MPUPDATE \_ administrada**</dt> </dl>       | Realiza una actualización de firmas mediante el servicio administrado WSUS.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**\_opción MPUPDATE \_ no administrada**</dt> </dl> | Realiza una actualización de firmas mediante el servicio no administrado MU/WU.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ en, opcional\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ info**

Un puntero a la información de devolución de llamada que se usa para suministrar al cliente los cambios de estado de actualización de firma (como inicio y finalización) y la información de progreso. Los [**\_ datos de MPCALLBACK**](mpcallback-data.md) que se devuelven en la función de devolución de llamada notifican el estado de actualización real y la información relacionada con el progreso. A continuación se muestra una lista de posibles devoluciones de llamada:



| Value                                                                                                                                                                                                                                | Significado                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**Inicio de MPNOTIFY \_ SIGUPDATE \_**</dt> </dl>                                      | Operación de actualización iniciada.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ completado**</dt> </dl>                             | Operación de actualización completada.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**Inicio de la búsqueda de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>                | Buscar actualizaciones iniciadas.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ Search \_ completado**</dt> </dl>       | Buscar actualizaciones completadas. Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**Inicio de la descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Descarga de la actualización iniciada.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**progreso de descarga de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl> | Descargar información de progreso. Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**descarga de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</dt> </dl> | Descarga para completar la actualización. Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**Inicio de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>             | Se inició la instalación de la actualización.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**progreso de la instalación de MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Información sobre el progreso de la instalación. Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**instalación de MPNOTIFY \_ SIGUPDATE \_ \_ completado**</dt> </dl>    | Se completó la instalación de la actualización. Hay información adicional disponible a través de la estructura de [**\_ datos MPSIGUPDATE**](mpsigupdate-data.md) .<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**solicitud de MPNOTIFY \_ SIGUPDATE \_ \_ procesada**</dt> </dl> | El servicio antimalware procesó una solicitud de actualización de firma. El error o el éxito se indica mediante *hResult* en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**se \_ \_ requiere un reinicio de MPNOTIFY SIGUPDATE \_**</dt> </dl>       | Requiere un reinicio para completar la operación de actualización. El error o el éxito se indica mediante *hResult* en los [**\_ datos de MPCALLBACK**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**\_error interno de MPNOTIFY \_**</dt> </dl>                                   | La operación de actualización de firma ha encontrado un error genérico. El *hResult* en [**los \_ datos de MPCALLBACK**](mpcallback-data.md) tiene el código de error específico.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ enuncia\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de actualización devuelto que identifica la operación de actualización de firmas iniciada actualmente. Este identificador se puede usar en las llamadas de función subsiguientes, como para controlar la operación de actualización de la firma. El identificador debe cerrarse con la función [**MpHandleClose**](mphandleclose.md) .

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

[**datos de MPSIGUPDATE \_**](mpsigupdate-data.md)
</dt> </dl>

 

 





