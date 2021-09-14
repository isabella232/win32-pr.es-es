---
title: Códigos de retorno de TBS (Tbs.h)
description: TBS usa los códigos siguientes para indicar el resultado de una llamada de función.
ms.assetid: a3888263-aa00-4b31-b51d-c6d448c1edb7
topic_type:
- apiref
api_name:
- TBS_SUCCESS
- TBS_E_INTERNAL_ERROR
- TBS_E_BAD_PARAMETER
- TBS_E_INVALID_OUTPUT_POINTER
- TBS_E_INVALID_CONTEXT
- TBS_E_INSUFFICIENT_BUFFER
- TBS_E_IOERROR
- TBS_E_INVALID_CONTEXT_PARAM
- TBS_E_SERVICE_NOT_RUNNING
- TBS_E_TOO_MANY_TBS_CONTEXTS
- TBS_E_TOO_MANY_RESOURCES
- TBS_E_SERVICE_START_PENDING
- TBS_E_PPI_NOT_SUPPORTED
- TBS_E_COMMAND_CANCELED
- TBS_E_BUFFER_TOO_LARGE
- TBS_E_TPM_NOT_FOUND
- TBS_E_SERVICE_DISABLED
- TBS_E_NO_EVENT_LOG
- TBS_E_ACCESS_DENIED
- TBS_E_PROVISIONING_NOT_ALLOWED
- TBS_E_PPI_FUNCTION_UNSUPPORTED
- TBS_E_OWNERAUTH_NOT_FOUND
- TBS_E_PROVISIONING_INCOMPLETE
api_location:
- Tbs.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0271c323e4ea300f45817aa59d4f5f9779f9981
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127243770"
---
# <a name="tbs-return-codes"></a>Códigos de retorno de TBS

TBS usa los códigos siguientes para indicar el resultado de una llamada de función.



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ SUCCESS**</dt> <dt>0 (0x0)</dt> </dl>                                                                             | La función se ha realizado correctamente.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ E \_ ERROR \_ INTERNO**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Error interno de software.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ E \_ BAD \_ PARAMETER 2150121474**</dt> <dt>(0x80284002)</dt> </dl>                                   | Uno o varios valores de parámetro no son válidos.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ E \_ PUNTERO DE SALIDA \_ \_ NO**</dt> <dt>VÁLIDO 2150121475 (0x80284003)</dt> </dl>       | Un puntero de salida especificado es malo.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ E \_ CONTEXTO \_ NO**</dt> <dt>VÁLIDO 2150121476 (0x80284004)</dt> </dl>                             | El identificador de contexto especificado no hace referencia a un contexto válido.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ E \_ INSUFFICIENT \_ BUFFER**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | El búfer de salida especificado es demasiado pequeño.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Error al comunicarse con el TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ E \_ PARÁMETROS DE CONTEXTO \_ \_ NO**</dt> <dt>VÁLIDOs 2150121479 (0x80284007)</dt> </dl>          | Se pasó un parámetro de contexto que no es válido al intentar crear un contexto de TBS.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ E \_ SERVICE \_ NOT \_ RUNNING**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | El servicio TBS no se está ejecutando y no se pudo iniciar.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ E \_ \_ \_ DEMASIADOS CONTEXTOS \_ DE TBS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | No se pudo crear un nuevo contexto porque hay demasiados contextos abiertos.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ E \_ \_ DEMASIADOS \_ RECURSOS 2150121482**</dt> <dt>(0x8028400A)</dt> </dl>                   | No se pudo crear un nuevo recurso virtual porque hay demasiados recursos virtuales abiertos.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ E \_ SERVICE \_ START \_ PENDING**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | El servicio TBS se ha iniciado, pero aún no se está ejecutando.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ E \_ PPP NO \_ \_ COMPATIBLE**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | No se admite la interfaz de presencia física.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ E \_ COMMAND \_ CANCELED**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | El comando se canceló.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ E \_ BUFFER \_ TOO \_ LARGE**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | El búfer de entrada o salida es demasiado grande.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ E \_ TPM \_ NOT \_ FOUND**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | No se encuentra Módulo de plataforma segura dispositivo de seguridad de Módulo de plataforma segura (TPM) compatible en este equipo.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ E \_ SERVICE \_ DISABLED 2150121488**</dt> <dt>(0x80284010)</dt> </dl>                          | El servicio TBS se ha deshabilitado.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ NO EVENT LOG \_ \_ 2150121489**</dt> <dt>(0x80284011)</dt> </dl>                                     | El registro de eventos TBS no está disponible.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ ACCESO \_ \_ DENEGADO 2150121490**</dt> <dt>(0x80284012)</dt> </dl>                                   | El autor de la llamada no tiene los derechos adecuados para realizar la operación solicitada.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ E \_ NO SE PERMITE \_ \_ EL**</dt> <dt>2150121491 (0x80284013)</dt> </dl> | Las marcas especificadas no permiten la acción de aprovisionamiento de TPM.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ FUNCIÓN \_ E PPP NO \_ \_ 2150121492**</dt> <dt>(0x80284014)</dt> </dl> | La interfaz de presencia física de este firmware no admite el método solicitado.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ OWNERAUTH \_ NO SE \_ ENCUENTRA**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | No se encontró el valor de OwnerAuth de TPM solicitado.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ E \_ PROVISIONING \_ INCOMPLETE 2150121493**</dt> <dt>(0x80284015)</dt> </dl>     | El aprovisionamiento de TPM no se ha completado. Para obtener más información sobre cómo completar el aprovisionamiento, llame al método WMI de [**\_ Tpm Win32**](/windows/desktop/SecProv/win32-tpm) para aprovisionar el TPM ('Provision') y compruebe la información devuelta.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                   |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Tbs.h</dt> </dl> |



 

