---
title: Función MpUpdateStart (MpClient.h)
description: Inicia una operación de actualización de firma.
ms.assetid: BB056356-17E5-42F0-9636-9E1C254361E4
keywords:
- Función MpUpdateStart Legacy Windows Environment Features
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
ms.openlocfilehash: a61cda213ecfbb23c9ef366fcce7b5c91e806f26f0f4ebe8b45dc596b63d1b5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975895"
---
# <a name="mpupdatestart-function"></a>Función MpUpdateStart

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

*hMpHandle* \[ En\]
</dt> <dd>

Tipo: **MPHANDLE**

Controlar la interfaz del administrador de protección contra malware. La función [**MpManagerOpen**](mpmanageropen.md) devuelve este identificador.

</dd> <dt>

*dwUpdateOptions* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Especifica la opción para la operación de actualización de firma. Puede ser uno de los siguientes valores:



| Value                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPUPDATE_OPTION_NONE"></span><span id="mpupdate_option_none"></span><dl> <dt>**OPCIÓN MPUPDATE \_ \_ NONE**</dt> </dl>                | No se solicita ninguna opción específica.<br/>                                                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_ASYNC"></span><span id="mpupdate_option_async"></span><dl> <dt>**OPCIÓN MPUPDATE \_ \_ ASYNC**</dt> </dl>             | La operación de actualización va a ser asincrónica, donde **MpUpdateStart** vuelve inmediatamente después del inicio correcto de la actualización de firma. (De forma predeterminada, la operación de actualización es sincrónica, lo que **significa que MpUpdateStart** solo devolverá una vez finalizada la actualización de la firma).<br/> |
| <span id="MPUPDATE_OPTION_PROGRESS"></span><span id="mpupdate_option_progress"></span><dl> <dt>**PROGRESO DE LA \_ OPCIÓN MPUPDATE \_**</dt> </dl>    | El autor de la llamada está interesado en recibir información de progreso de actualización de firma a través de una devolución de llamada.<br/>                                                                                                                                                                                           |
| <span id="MPUPDATE_OPTION_HTTP"></span><span id="mpupdate_option_http"></span><dl> <dt>**OPCIÓN MPUPDATE \_ \_ HTTP**</dt> </dl>                | La actualización de la firma se realiza descargando el paquete de firma completo desde el sitio del portal de seguridad de Microsoft. Se puede usar como opción de reserva si el cliente está experimentando un problema de descarga de firma a través de Microsoft Update.<br/>                                           |
| <span id="MPUPDATE_OPTION_UNC"></span><span id="mpupdate_option_unc"></span><dl> <dt>**OPCIÓN DE MPUPDATE \_ \_ UNC**</dt> </dl>                   | Realiza la actualización de firmas mediante la descarga directa desde recursos compartidos UNC.<br/>                                                                                                                                                                                                                      |
| <span id="MPUPDATE_OPTION_MANAGED"></span><span id="mpupdate_option_managed"></span><dl> <dt>**OPCIÓN MPUPDATE \_ \_ ADMINISTRADA**</dt> </dl>       | Realiza la actualización de firmas mediante EL WSUS del servicio administrado.<br/>                                                                                                                                                                                                                             |
| <span id="MPUPDATE_OPTION_UNMANAGED"></span><span id="mpupdate_option_unmanaged"></span><dl> <dt>**OPCIÓN MPUPDATE \_ \_ NO ADMINISTRADA**</dt> </dl> | Realiza la actualización de firmas mediante el servicio no administrado MU/WU.<br/>                                                                                                                                                                                                                          |



 

</dd> <dt>

*pCallbackInfo* \[ en, opcional\]
</dt> <dd>

Tipo: **PMPCALLBACK \_ INFO**

Puntero a la información de devolución de llamada utilizada para alimentar al cliente con cambios de estado de actualización de firma (como inicio y completado) e información de progreso. Los [**DATOS MPCALLBACK \_ pasados**](mpcallback-data.md) de vuelta en la función de devolución de llamada notifican el estado de actualización real y la información relacionada con el progreso. A continuación se muestra una lista de posibles devoluciones de llamada:



| Value                                                                                                                                                                                                                                | Significado                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPNOTIFY_SIGUPDATE_START"></span><span id="mpnotify_sigupdate_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ START**</dt> </dl>                                      | Operación de actualización iniciada.<br/>                                                                                                                                  |
| <span id="MPNOTIFY_SIGUPDATE_COMPLETE"></span><span id="mpnotify_sigupdate_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ COMPLETE**</dt> </dl>                             | Operación de actualización completada.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_START"></span><span id="mpnotify_sigupdate_search_start"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ START**</dt> </dl>                | Busque actualizaciones iniciadas.<br/>                                                                                                                                |
| <span id="MPNOTIFY_SIGUPDATE_SEARCH_COMPLETE"></span><span id="mpnotify_sigupdate_search_complete"></span><dl> <dt>**MPNOTIFY \_ SIGUPDATE \_ SEARCH \_ COMPLETE**</dt> </dl>       | Busque actualizaciones completadas. Hay información adicional disponible a través de [**la estructura DE DATOS MPSIGUPDATE. \_**](mpsigupdate-data.md)<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_START"></span><span id="mpnotify_sigupdate_download_start"></span><dl> <dt>**INICIO DE DESCARGA DE MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>          | Descargar para la actualización iniciada.<br/>                                                                                                                               |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_PROGRESS"></span><span id="mpnotify_sigupdate_download_progress"></span><dl> <dt>**PROGRESO DE DESCARGA DE MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl> | Descargue la información de progreso. Hay información adicional disponible a través de [**la estructura DE DATOS MPSIGUPDATE. \_**](mpsigupdate-data.md)<br/>                            |
| <span id="MPNOTIFY_SIGUPDATE_DOWNLOAD_COMPLETE"></span><span id="mpnotify_sigupdate_download_complete"></span><dl> <dt>**DESCARGA COMPLETA DE \_ MPNOTIFY SIGUPDATE \_ \_**</dt> </dl> | Descargue para completar la actualización. Hay información adicional disponible a través de [**la estructura DE DATOS MPSIGUPDATE. \_**](mpsigupdate-data.md)<br/>                             |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_START"></span><span id="mpnotify_sigupdate_install_start"></span><dl> <dt>**INICIO DE INSTALACIÓN DE MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>             | Se inició la instalación de la actualización.<br/>                                                                                                                            |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_PROGRESS"></span><span id="mpnotify_sigupdate_install_progress"></span><dl> <dt>**PROGRESO DE INSTALACIÓN DE MPNOTIFY \_ SIGUPDATE \_ \_**</dt> </dl>    | Información de progreso de la instalación. Hay información adicional disponible a través de [**la estructura DE DATOS MPSIGUPDATE. \_**](mpsigupdate-data.md)<br/>                        |
| <span id="MPNOTIFY_SIGUPDATE_INSTALL_COMPLETE"></span><span id="mpnotify_sigupdate_install_complete"></span><dl> <dt>**INSTALACIÓN COMPLETA DE \_ MPNOTIFY SIGUPDATE \_ \_**</dt> </dl>    | Instalación de la actualización completada. Hay información adicional disponible a través de [**la estructura DE DATOS MPSIGUPDATE. \_**](mpsigupdate-data.md)<br/>                         |
| <span id="MPNOTIFY_SIGUPDATE_REQUEST_PROCESSED"></span><span id="mpnotify_sigupdate_request_processed"></span><dl> <dt>**SOLICITUD DE \_ MPNOTIFY SIGUPDATE \_ \_ PROCESADA**</dt> </dl> | El servicio antimalware procesó una solicitud de actualización de firma. HResult indica un error o un resultado correcto *en* [**MPCALLBACK \_ DATA**](mpcallback-data.md).<br/> |
| <span id="MPNOTIFY_SIGUPDATE_REBOOT_REQUIRED"></span><span id="mpnotify_sigupdate_reboot_required"></span><dl> <dt>**SE REQUIERE EL \_ REINICIO DE MPNOTIFY SIGUPDATE \_ \_**</dt> </dl>       | Requiere reiniciar para completar la operación de actualización. HResult indica un error o un resultado correcto *en* [**MPCALLBACK \_ DATA**](mpcallback-data.md).<br/>             |
| <span id="MPNOTIFY_INTERNAL_FAILURE"></span><span id="mpnotify_internal_failure"></span><dl> <dt>**ERROR INTERNO DE \_ \_ MPNOTIFY**</dt> </dl>                                   | La operación de actualización de firmas ha detectado un error genérico. HResult *en* [**MPCALLBACK \_ DATA**](mpcallback-data.md) tiene el código de error específico.<br/>    |



 

</dd> <dt>

*phUpdateHandle* \[ out\]
</dt> <dd>

Tipo: **PMPHANDLE**

Identificador de actualización devuelto que identifica la operación de actualización de firma iniciada actualmente. Este identificador se puede usar en llamadas de función posteriores, como para controlar la operación de actualización de firma. El identificador debe cerrarse con la [**función MpHandleClose.**](mphandleclose.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si la función se realiza correctamente, el valor devuelto es **S \_ OK**.

Si se produce un error en la función, el valor devuelto es un **código HRESULT con** errores. El autor de la llamada puede usar [**la función MpErrorMessageFormat**](mperrormessageformat.md) para obtener una descripción genérica del mensaje de error.

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

[**DATOS DE \_ MPSIGUPDATE**](mpsigupdate-data.md)
</dt> </dl>

 

 





