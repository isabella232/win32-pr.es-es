---
title: Códigos de retorno de TBS (TBS. h)
description: TBS usa los siguientes códigos para indicar el resultado de una llamada de función.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422334"
---
# <a name="tbs-return-codes"></a>Códigos de retorno de TBS

TBS usa los siguientes códigos para indicar el resultado de una llamada de función.



| Constante o valor                                                                                                                                                                                                                                                                                   | Descripción                                                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TBS_SUCCESS"></span><span id="tbs_success"></span><dl> <dt>**TBS \_ CORRECTO**</dt> <dt>0 (0X0)</dt> </dl>                                                                             | La función se ha realizado correctamente.<br/>                                                                                                                                                                                                         |
| <span id="TBS_E_INTERNAL_ERROR"></span><span id="tbs_e_internal_error"></span><dl> <dt>**TBS \_ \_ \_ ERROR interno**</dt> <dt>2150121473 (0x80284001)</dt> </dl>                                | Error interno de software.<br/>                                                                                                                                                                                            |
| <span id="TBS_E_BAD_PARAMETER"></span><span id="tbs_e_bad_parameter"></span><dl> <dt>**TBS \_ E \_ \_ parámetro incorrecto**</dt> <dt>2150121474 (0x80284002)</dt> </dl>                                   | Uno o varios valores de parámetro no son válidos.<br/>                                                                                                                                                                                     |
| <span id="TBS_E_INVALID_OUTPUT_POINTER"></span><span id="tbs_e_invalid_output_pointer"></span><dl> <dt>**TBS \_ E \_ \_ \_ puntero de salida no válido**</dt> <dt>2150121475 (0x80284003)</dt> </dl>       | Un puntero de salida especificado es incorrecto.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_INVALID_CONTEXT"></span><span id="tbs_e_invalid_context"></span><dl> <dt>**TBS \_ E \_ \_ contexto no válido**</dt> <dt>2150121476 (0x80284004)</dt> </dl>                             | El identificador de contexto especificado no hace referencia a un contexto válido.<br/>                                                                                                                                                                 |
| <span id="TBS_E_INSUFFICIENT_BUFFER"></span><span id="tbs_e_insufficient_buffer"></span><dl> <dt>**TBS \_ E \_ insuficiente \_ búfer**</dt> <dt>2150121477 (0x80284005)</dt> </dl>                 | El búfer de salida especificado es demasiado pequeño.<br/>                                                                                                                                                                                       |
| <span id="TBS_E_IOERROR"></span><span id="tbs_e_ioerror"></span><dl> <dt>**TBS \_ E \_ IOERROR**</dt> <dt>2150121478 (0x80284006)</dt> </dl>                                                      | Error al comunicarse con el TPM.<br/>                                                                                                                                                                             |
| <span id="TBS_E_INVALID_CONTEXT_PARAM"></span><span id="tbs_e_invalid_context_param"></span><dl> <dt>**TBS \_ E \_ no es válido el \_ \_ parámetro de contexto**</dt> <dt>2150121479 (0x80284007)</dt> </dl>          | Se pasó un parámetro de contexto no válido al intentar crear un contexto de TBS.<br/>                                                                                                                                       |
| <span id="TBS_E_SERVICE_NOT_RUNNING"></span><span id="tbs_e_service_not_running"></span><dl> <dt>**TBS \_ El \_ servicio E \_ no se \_ está ejecutando**</dt> <dt>2150121480 (0x80284008)</dt> </dl>                | El servicio TBS no se está ejecutando y no se pudo iniciar.<br/>                                                                                                                                                                        |
| <span id="TBS_E_TOO_MANY_TBS_CONTEXTS"></span><span id="tbs_e_too_many_tbs_contexts"></span><dl> <dt>**TBS \_ E \_ demasiados \_ \_ \_ contextos de TBS**</dt> <dt>2150121481 (0x80284009)</dt> </dl>         | No se pudo crear un nuevo contexto porque hay demasiados contextos abiertos.<br/>                                                                                                                                                    |
| <span id="TBS_E_TOO_MANY_RESOURCES"></span><span id="tbs_e_too_many_resources"></span><dl> <dt>**TBS \_ E \_ demasiados \_ \_ recursos**</dt> <dt>2150121482 (0x8028400A)</dt> </dl>                   | No se pudo crear un nuevo recurso virtual porque hay demasiados recursos virtuales abiertos.<br/>                                                                                                                                  |
| <span id="TBS_E_SERVICE_START_PENDING"></span><span id="tbs_e_service_start_pending"></span><dl> <dt>**TBS \_ E \_ Inicio de servicio \_ \_ pendiente**</dt> <dt>2150121483 (0x8028400B)</dt> </dl>          | El servicio TBS se ha iniciado pero aún no se está ejecutando.<br/>                                                                                                                                                                        |
| <span id="TBS_E_PPI_NOT_SUPPORTED"></span><span id="tbs_e_ppi_not_supported"></span><dl> <dt>**TBS \_ \_No se \_ \_ admiten PPP E**</dt> <dt>2150121484 (0x8028400C)</dt> </dl>                      | No se admite la interfaz de presencia física.<br/>                                                                                                                                                                               |
| <span id="TBS_E_COMMAND_CANCELED"></span><span id="tbs_e_command_canceled"></span><dl> <dt>**TBS \_ \_Comando E \_ cancelado**</dt> <dt>2150121485 (0x8028400D)</dt> </dl>                          | Se canceló el comando.<br/>                                                                                                                                                                                                       |
| <span id="TBS_E_BUFFER_TOO_LARGE"></span><span id="tbs_e_buffer_too_large"></span><dl> <dt>**TBS \_ \_Búfer E \_ demasiado \_ grande**</dt> <dt>2150121486 (0x8028400E)</dt> </dl>                         | El búfer de entrada o de salida es demasiado grande.<br/>                                                                                                                                                                                        |
| <span id="TBS_E_TPM_NOT_FOUND"></span><span id="tbs_e_tpm_not_found"></span><dl> <dt>**TBS \_ \_ \_ No \_ se encontró el TPM**</dt> <dt>2150121487 (0x8028400F)</dt> </dl>                                  | No se encuentra un dispositivo de seguridad de Módulo de plataforma segura compatible (TPM) en este equipo.<br/>                                                                                                                                    |
| <span id="TBS_E_SERVICE_DISABLED"></span><span id="tbs_e_service_disabled"></span><dl> <dt>**TBS \_ \_Servicio E \_ deshabilitado**</dt> <dt>2150121488 (0x80284010)</dt> </dl>                          | Se ha deshabilitado el servicio TBS.<br/>                                                                                                                                                                                              |
| <span id="TBS_E_NO_EVENT_LOG"></span><span id="tbs_e_no_event_log"></span><dl> <dt>**TBS \_ E \_ ningún \_ \_ registro de eventos**</dt> <dt>2150121489 (0x80284011)</dt> </dl>                                     | El registro de eventos de TBS no está disponible.<br/>                                                                                                                                                                                             |
| <span id="TBS_E_ACCESS_DENIED"></span><span id="tbs_e_access_denied"></span><dl> <dt>**TBS \_ E \_ acceso \_ denegado**</dt> <dt>2150121490 (0x80284012)</dt> </dl>                                   | El autor de la llamada no tiene los derechos adecuados para realizar la operación solicitada.<br/>                                                                                                                                             |
| <span id="TBS_E_PROVISIONING_NOT_ALLOWED"></span><span id="tbs_e_provisioning_not_allowed"></span><dl> <dt>**TBS \_ \_ \_ No se \_ permite el aprovisionamiento**</dt> de <dt>2150121491 (0x80284013)</dt> </dl> | Las marcas especificadas no permiten la acción de aprovisionamiento de TPM.<br/>                                                                                                                                                              |
| <span id="TBS_E_PPI_FUNCTION_UNSUPPORTED"></span><span id="tbs_e_ppi_function_unsupported"></span><dl> <dt>**TBS \_ \_Función PPI \_ \_ no compatible**</dt> <dt>2150121492 (0x80284014)</dt> </dl> | La interfaz de presencia física de este firmware no admite el método solicitado.<br/>                                                                                                                                         |
| <span id="TBS_E_OWNERAUTH_NOT_FOUND"></span><span id="tbs_e_ownerauth_not_found"></span><dl> <dt>**TBS \_ E \_ OWNERAUTH \_ no \_ encontrado**</dt> <dt>2150121493 (0x80284015)</dt> </dl>                | No se encontró el valor de OwnerAuth de TPM solicitado.<br/>                                                                                                                                                                                |
| <span id="TBS_E_PROVISIONING_INCOMPLETE"></span><span id="tbs_e_provisioning_incomplete"></span><dl> <dt>**TBS \_ E \_ aprovisionamiento \_ incompleto**</dt> <dt>2150121493 (0x80284015)</dt> </dl>     | No se completó el aprovisionamiento de TPM. Para obtener más información sobre cómo completar el aprovisionamiento, llame al método WMI [**\_ TPM de Win32**](/windows/desktop/SecProv/win32-tpm) para aprovisionar TPM (' provision ') y comprobar la información devuelta.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                   |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                             |
| Encabezado<br/>                   | <dl> <dt>TBS. h</dt> </dl> |



 

