---
title: Constantes de error nap (WinError.h)
description: Las siguientes constantes de error nap se definen en WinError.h.
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
ms.openlocfilehash: 411500ea5f0fc3ba0f1d4067a6befe902a81af3154c91e76c36425c289616eb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620844"
---
# <a name="nap-error-constants"></a>Constantes de error nap

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

Las siguientes constantes de error nap se definen en WinError.h.

<dl> <dt>

<span id="NAP_E_INVALID_PACKET"></span><span id="nap_e_invalid_packet"></span>**NAP \_ E PAQUETE NO \_ \_ VÁLIDO**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270001L)
</dt> <dt>



El paquete [**de NAP SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) no es válido.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISSING_SOH"></span><span id="nap_e_missing_soh"></span>**NAP \_ E \_ MISSING \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270002L)
</dt> <dt>



Faltaba [**un SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) en el paquete NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_CONFLICTING_ID"></span><span id="nap_e_conflicting_id"></span>**NAP \_ E \_ CONFLICTING \_ ID**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270003L)
</dt> <dt>



El identificador de entidad entra en conflicto con un identificador de entidad ya registrado.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NO_CACHED_SOH"></span><span id="nap_e_no_cached_soh"></span>**NAP \_ E \_ NO \_ CACHED \_ SOH**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270004L)
</dt> <dt>



No hay [**soH almacenado en**](/windows/win32/api/naptypes/ns-naptypes-soh) caché.


</dt> </dl> </dd> <dt>

<span id="NAP_E_STILL_BOUND"></span><span id="nap_e_still_bound"></span>**NAP \_ E \_ TODAVÍA \_ ENLAZADO**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270005L)
</dt> <dt>



La entidad todavía está enlazada al sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_REGISTERED"></span><span id="nap_e_not_registered"></span>**NAP \_ E \_ NO \_ REGISTRADO**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270006L)
</dt> <dt>



La entidad no está registrada en el sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_INITIALIZED"></span><span id="nap_e_not_initialized"></span>**NAP \_ E \_ NO \_ INICIALIZADO**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270007L)
</dt> <dt>



La entidad no se inicializa con el sistema NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MISMATCHED_ID"></span><span id="nap_e_mismatched_id"></span>**IDENTIFICADOR \_ DE NAP E NO \_ \_ COINCIDENTE**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270008L)
</dt> <dt>



Los identificadores de correlación de la [**solicitud soH**](/windows/win32/api/naptypes/ns-naptypes-soh) y la **respuesta de SoH** no coinciden.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NOT_PENDING"></span><span id="nap_e_not_pending"></span>**NAP \_ E \_ NO \_ PENDIENTE**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270009L)
</dt> <dt>



La finalización se indicó en una solicitud que no está pendiente actualmente.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ID_NOT_FOUND"></span><span id="nap_e_id_not_found"></span>**ID. \_ DE NAP E NO \_ \_ \_ ENCONTRADO**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000AL)
</dt> <dt>



No se encontró el identificador del componente NAP.


</dt> </dl> </dd> <dt>

<span id="NAP_E_MAXSIZE_TOO_SMALL"></span><span id="nap_e_maxsize_too_small"></span>**NAP \_ E \_ MAXSIZE \_ TOO \_ SMALL**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000BL)
</dt> <dt>



El tamaño máximo de la conexión es demasiado pequeño para un paquete SoH.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SERVICE_NOT_RUNNING"></span><span id="nap_e_service_not_running"></span>**SERVICIO \_ NAP E NO EN \_ \_ \_ EJECUCIÓN**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000CL)
</dt> <dt>



El servicio NapAgent no se está ejecutando.


</dt> </dl> </dd> <dt>

<span id="NAP_S_CERT_ALREADY_PRESENT"></span><span id="nap_s_cert_already_present"></span>**EL \_ CERTIFICADO DE NAP YA ESTÁ \_ \_ \_ PRESENTE**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x0027000DL) 
</dt> <dt>



Un certificado ya está presente en el almacén de certificados.


</dt> </dl> </dd> <dt>

<span id="NAP_E_ENTITY_DISABLED"></span><span id="nap_e_entity_disabled"></span>**ENTIDAD \_ NAP E \_ \_ DESHABILITADA**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000EL)
</dt> <dt>



La entidad está deshabilitada con el servicio NapAgent.


</dt> </dl> </dd> <dt>

<span id="NAP_E_NETSH_GROUPPOLICY_ERROR"></span><span id="nap_e_netsh_grouppolicy_error"></span>**\_ERROR \_ \_ GROUPPOLICY DE NAP E NETSH \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x8027000FL)
</dt> <dt>



directiva de grupo no está configurado.


</dt> </dl> </dd> <dt>

<span id="NAP_E_TOO_MANY_CALLS"></span><span id="nap_e_too_many_calls"></span>**NAP \_ E \_ \_ DEMASIADAS \_ LLAMADAS**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270010L)
</dt> <dt>



Demasiadas llamadas simultáneas.


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_EXISTED"></span><span id="nap_e_shv_config_existed"></span>**EXISTÍA \_ LA CONFIGURACIÓN DE NAP E \_ SHV \_ \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270011L)
</dt> <dt>



La configuración de SHV ya existe.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_CONFIG_NOT_FOUND"></span><span id="nap_e_shv_config_not_found"></span>**NO \_ SE ENCONTRÓ LA CONFIGURACIÓN DE NAP E \_ SHV \_ \_ \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270012L)
</dt> <dt>



No se encuentra la configuración de SHV.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> <dt>

<span id="NAP_E_SHV_TIMEOUT"></span><span id="nap_e_shv_timeout"></span>**TIEMPO \_ DE ESPERA DE NAP E \_ SHV \_**
</dt> <dd> <dl> <dt>

\_HRESULT \_ TYPEDEF \_ (0x80270013L)
</dt> <dt>



Se ha producido un tiempo de espera de SHV en la solicitud.

> [!Note]  
> Compatible con Windows 7 o posterior.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>WinError.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Constantes nap**](nap-constants.md)
</dt> </dl>

 

 





