---
title: Marcas de método EAP (Eaptypes. h)
description: Las marcas de método EAP se utilizan en las funciones suplicante, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.
ms.assetid: b6305349-3418-475e-8a37-2c06b399556e
topic_type:
- apiref
api_name:
- EAP_FLAG_Reserved1
- EAP_FLAG_NON_INTERACTIVE
- EAP_FLAG_LOGON
- EAP_FLAG_PREVIEW
- EAP_FLAG_Reserved2
- EAP_FLAG_MACHINE_AUTH
- EAP_FLAG_GUEST_ACCESS
- EAP_FLAG_Reserved3
- EAP_FLAG_Reserved4
- EAP_FLAG_RESUME_FROM_HIBERNATE
- EAP_FLAG_Reserved5
- EAP_FLAG_Reserved6
- EAP_FLAG_FULL_AUTH
- EAP_FLAG_PREFER_ALT_CREDENTIALS
- EAP_FLAG_Reserved7
- EAP_PEER_FLAG_HEALTH_STATE_CHANGE
- EAP_FLAG_SUPRESS_UI
- EAP_FLAG_PRE_LOGON
- EAP_FLAG_USER_AUTH
- EAP_FLAG_CONFG_READONLY
- EAP_FLAG_Reserved8
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34913c950f0bba981a96256e74d9a8c3c3ff5f04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488914"
---
# <a name="eap-method-flags"></a>Marcas de método EAP

Las marcas de método EAP se utilizan en las funciones suplicante, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**\_Marca EAP \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**\_marca EAP \_ no \_ interactiva**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



No mostrar una interfaz de usuario (UI).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**Inicio de sesión de \_ marca EAP \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Los datos de usuario se obtuvieron del inicio de sesión de Windows.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**\_ \_ vista previa de la marca EAP**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Mostrar la interfaz de usuario de credenciales antes de la autenticación, incluso si las credenciales almacenadas en caché están presentes.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ de MARCA \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**\_autenticación de \_ equipo de marca EAP \_**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Usar autenticación a nivel de equipo; Si no se establece esta marca, indica que se está usando la autenticación de nivel de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**\_acceso de \_ invitado de marca EAP \_**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indica una solicitud para proporcionar acceso de invitado.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**\_Marca EAP \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ de MARCA \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**\_marca EAP \_ reanudar \_ desde \_ hibernación**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indica que se trata de la primera llamada después de que la actividad del equipo se haya reanudado desde un período de hibernación.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ de MARCA \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**\_Marca EAP \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**\_ \_ autenticación completa de la marca EAP \_**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indica que los métodos de túnel deben realizar una autenticación completa en lugar de una versión abreviada, como la [reconexión rápida de EAP protegido (PEAP)](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**marca de EAP \_ \_ preferida de \_ \_ credenciales Alt**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que las credenciales que se pasan a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) son preferibles a todas las demás formas de recuperación de credenciales, incluso si los datos de configuración pasados a la función actual solicitan un modo diferente de recuperación de credenciales.

> [!Note]  
> Esta marca solo se usa en [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession).

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**\_Marca EAP \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**cambio de estado de mantenimiento de marca de EAP \_ del mismo nivel \_ \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indica que la causa de la reautenticación es una devolución de llamada de [protección de acceso a redes](/windows/desktop/NAP/network-access-protection-start-page) (NAP); NAP inició la sesión de autenticación porque cambió el estado de mantenimiento. Esta marca solo se debe enviar cuando se llama a esta función mediante una devolución de llamada de [*NotificationHandler*](/previous-versions/windows/desktop/api) específica de NAP proporcionada por una llamada anterior a esta función.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**\_marca EAP \_ suprimir \_ UI**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continúe la autenticación con la información disponible. Si la autenticación no puede continuar, se produce un error.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**\_Inicio de \_ sesión previo de marca EAP \_**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que EAPHost debe proporcionar el inicio de sesión único (SSO). Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**\_autenticación de \_ usuario de marca EAP \_**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica la autenticación de nivel de usuario para métodos heredados que no pueden establecer la autenticación del **\_ equipo de marca \_ \_ EAP**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**\_marca EAP \_ de \_ solo lectura**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indica que la configuración se puede ver pero no actualizar.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**\_Marca EAP \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de EAPHost comunes](common-eap-host-error-constants.md)
</dt> </dl>

