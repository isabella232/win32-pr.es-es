---
title: Constantes de error de NAP (WinError. h)
description: Las siguientes constantes de error de NAP se definen en WinError. h.
ms.assetid: b2fba990-75d9-4153-8058-c01e97700d00
topic_type:
- apiref
api_name:
- NAP_E_INVALID_PACKET
- NAP_E_MISSING_SOH
- NAP_E_CONFLICTING_ID
- NAP_E_NO_CACHED_SOH
- NAP_E_STILL_BOUND
- NAP_E_NOT_REGISTERED
- NAP_E_NOT_INITIALIZED
- NAP_E_MISMATCHED_ID
- NAP_E_NOT_PENDING
- NAP_E_ID_NOT_FOUND
- NAP_E_MAXSIZE_TOO_SMALL
- NAP_E_SERVICE_NOT_RUNNING
- NAP_S_CERT_ALREADY_PRESENT
- NAP_E_ENTITY_DISABLED
- NAP_E_NETSH_GROUPPOLICY_ERROR
- NAP_E_TOO_MANY_CALLS
- NAP_E_SHV_CONFIG_EXISTED
- NAP_E_SHV_CONFIG_NOT_FOUND
- NAP_E_SHV_TIMEOUT
api_location:
- WinError.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b871d6f00174f05ab580aad54395851fa70af877
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996888"
---
# <a name="nap-error-constants"></a>Constantes de error de NAP

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las siguientes constantes de error de NAP se definen en WinError. h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**\_paquete NAP E \_ no válido \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270001L)
</dt> <dt>



El paquete [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) de NAP no es válido.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**falta el SOH de NAP \_ E \_ \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270002L)
</dt> <dt>



Falta un [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) en el paquete NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**\_ \_ identificador conflictivo de NAP \_ E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270003L)
</dt> <dt>



El identificador de entidad entra en conflicto con un identificador de entidad ya registrado.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**\_no se \_ ha \_ almacenado en caché el \_ SOH de NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270004L)
</dt> <dt>



No hay ningún [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) en caché presente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ todavía \_ enlazado**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270005L)
</dt> <dt>



La entidad sigue estando enlazada al sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ no \_ registrado**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270006L)
</dt> <dt>



La entidad no está registrada con el sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ no \_ inicializado**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270007L)
</dt> <dt>



La entidad no se ha inicializado con el sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**identificador de NAP \_ E no \_ coincidente \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270008L)
</dt> <dt>



Los identificadores de correlación de la solicitud de [**SOH**](/windows/win32/api/naptypes/ns-naptypes-soh) y la respuesta de **SOH** no coinciden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ no \_ pendiente**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270009L)
</dt> <dt>



La finalización se indicó en una solicitud que no está pendiente actualmente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador de NAP E**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x8027000AL)
</dt> <dt>



No se encontró el identificador del componente NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**tamaño de NAP \_ E \_ MaxSize \_ demasiado \_ pequeño**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x8027000BL)
</dt> <dt>



El tamaño máximo de la conexión es demasiado pequeño para un paquete SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**el \_ servicio NAP E \_ \_ no se \_ está ejecutando**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x8027000CL)
</dt> <dt>



El servicio NapAgent no se está ejecutando.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**\_certificado NAP \_ S \_ ya \_ presente**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x0027000DL) 
</dt> <dt>



Ya existe un certificado en el almacén de certificados.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**\_entidad E de NAP \_ \_ deshabilitada**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x8027000EL)
</dt> <dt>



La entidad se deshabilita con el servicio NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**ERROR de NAP \_ E \_ netsh \_ GROUPPOLICY \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x8027000FL)
</dt> <dt>



Directiva de grupo no está configurado.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ demasiadas \_ \_ llamadas**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270010L)
</dt> <dt>



Demasiadas llamadas simultáneas.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**\_existe la \_ configuración de SHV E \_ NAP \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270011L)
</dt> <dt>



La configuración de SHV ya existe.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**\_ \_ \_ \_ no se encontró la configuración \_ de SHV de NAP**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270012L)
</dt> <dt>



No se encuentra la configuración de SHV.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**tiempo de espera de NAP \_ E \_ SHV \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ \_ (TYPEDEF) (0x80270013L)
</dt> <dt>



SHV agotó el tiempo de espera en la solicitud.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>WinError. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes de NAP**](nap-constants.md)
</dt> </dl>

 

 





