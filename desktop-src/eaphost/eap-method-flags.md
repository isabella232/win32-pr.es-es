---
title: Marcas del método EAP (Eaptypes.h)
description: Las marcas del método EAP se usan dentro de las funciones de suplicación, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252945"
---
# <a name="eap-method-flags"></a>Marcas del método EAP

Las marcas del método EAP se usan dentro de las funciones de suplicación, autenticador y del mismo nivel para especificar los comportamientos de una sesión de autenticación EAP.

<dl> <dt>

<span id="EAP_FLAG_Reserved1"></span><span id="eap_flag_reserved1"></span><span id="EAP_FLAG_RESERVED1"></span>**EAP \_ FLAG \_ Reserved1**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_NON_INTERACTIVE"></span><span id="eap_flag_non_interactive"></span>**EAP FLAG NON INTERACTIVE (MARCA DE EAP \_ NO \_ \_ INTERACTIVA)**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



No muestre una interfaz de usuario (UI).


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_LOGON"></span><span id="eap_flag_logon"></span>**INICIO DE \_ SESIÓN DE MARCA DE \_ EAP**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Los datos de usuario se han obtenido de Windows inicio de sesión.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREVIEW"></span><span id="eap_flag_preview"></span>**VERSIÓN PRELIMINAR \_ DE LA MARCA DE \_ EAP**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Mostrar la interfaz de usuario de credenciales antes de la autenticación, incluso si las credenciales almacenadas en caché están presentes.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved2"></span><span id="_eap_flag_reserved2"></span><span id="_EAP_FLAG_RESERVED2"></span>**EAP \_ FLAG \_ Reserved2**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_MACHINE_AUTH"></span><span id="eap_flag_machine_auth"></span>**AUTENTICACIÓN \_ DE LA MÁQUINA DE LA MARCA DE \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Usar autenticación de nivel de máquina; no establecer esta marca indica que se está utilizando la autenticación de nivel de usuario.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_GUEST_ACCESS"></span><span id="eap_flag_guest_access"></span>**ACCESO DE \_ INVITADO DE LA MARCA \_ \_ EAP**
</dt> <dd> <dl> <dt>

 0x00000040
</dt> <dt>



Indica una solicitud para proporcionar acceso de invitado.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved3"></span><span id="eap_flag_reserved3"></span><span id="EAP_FLAG_RESERVED3"></span>**EAP \_ FLAG \_ Reserved3**
</dt> <dd> <dl> <dt>

0x00000080 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved4__"></span><span id="_eap_flag_reserved4__"></span><span id="_EAP_FLAG_RESERVED4__"></span>**EAP \_ FLAG \_ Reserved4** 
</dt> <dd> <dl> <dt>

0x00000100 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_RESUME_FROM_HIBERNATE"></span><span id="eap_flag_resume_from_hibernate"></span>**EAP \_ FLAG \_ RESUME \_ FROM \_ HIBERNATE**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Indica que esta es la primera llamada después de que la actividad de la máquina se haya reanudado desde un período de hibernación.


</dt> </dl> </dd> <dt>

<span id="_EAP_FLAG_Reserved5"></span><span id="_eap_flag_reserved5"></span><span id="_EAP_FLAG_RESERVED5"></span>**EAP \_ FLAG \_ Reserved5**
</dt> <dd> <dl> <dt>

0x00000400 
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved6________________"></span><span id="eap_flag_reserved6________________"></span><span id="EAP_FLAG_RESERVED6________________"></span>**EAP \_ FLAG \_ Reserved6** 
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_FULL_AUTH"></span><span id="eap_flag_full_auth"></span>**AUTENTICACIÓN \_ COMPLETA DE LA MARCA DE \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Indica que los métodos de túnel deben realizar una autenticación completa en lugar de una versión abreviada, como La reconexión rápida de [EAP protegido (PEAP).](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10))


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PREFER_ALT_CREDENTIALS"></span><span id="eap_flag_prefer_alt_credentials"></span>**MARCA EAP \_ \_ \_ PREFERIR CREDENCIALES \_ ALT**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Indica que las credenciales que se pasan a [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) son preferibles a todas las demás formas de recuperación de credenciales, incluso si los datos de configuración pasados a la función actual solicitan un modo diferente de recuperación de credenciales.

> [!Note]  
> [**EapPeerBeginSession**](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession)solo usa esta marca.

 


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved7"></span><span id="eap_flag_reserved7"></span><span id="EAP_FLAG_RESERVED7"></span>**EAP \_ FLAG \_ Reserved7**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> <dt>

<span id="EAP_PEER_FLAG_HEALTH_STATE_CHANGE"></span><span id="eap_peer_flag_health_state_change"></span>**CAMBIO \_ DE ESTADO DE MANTENIMIENTO DE LA MARCA DEL MISMO NIVEL DE \_ \_ \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Indica que la causa de la re autenticación es una devolución de llamada de [Protección](/windows/desktop/NAP/network-access-protection-start-page) de acceso a redes (NAP); NAP inició la sesión de autenticación porque el estado de mantenimiento cambió. Esta marca solo se debe enviar cuando se llama a esta función mediante una devolución de llamada [*NotificationHandler*](/previous-versions/windows/desktop/api) específica de NAP proporcionada por una llamada anterior a esta función.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_SUPRESS_UI"></span><span id="eap_flag_supress_ui"></span>**INTERFAZ DE \_ USUARIO \_ DE SUPRESS DE LA MARCA EAP \_**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Continúe la autenticación con la información disponible. Si la autenticación no puede continuar, se producirá un error.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_PRE_LOGON"></span><span id="eap_flag_pre_logon"></span>**INICIO DE \_ SESIÓN PREVIO DE LA MARCA \_ \_ DE EAP**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indica que EAPHost debe proporcionar inicio de sesión único (SSO). Para más información, consulte [SSO y PLAP.](understanding-sso-and-plap.md)


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_USER_AUTH"></span><span id="eap_flag_user_auth"></span>**AUTENTICACIÓN \_ DE USUARIO DE LA MARCA DE \_ \_ EAP**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Indica la autenticación de nivel de usuario para los métodos heredados que no pueden establecer **eap \_ flag machine \_ \_ AUTH**.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_CONFG_READONLY"></span><span id="eap_flag_confg_readonly"></span>**EAP \_ FLAG \_ CONFG \_ READONLY**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



Indica que la configuración se puede ver pero no actualizar.


</dt> </dl> </dd> <dt>

<span id="EAP_FLAG_Reserved8"></span><span id="eap_flag_reserved8"></span><span id="EAP_FLAG_RESERVED8"></span>**EAP \_ FLAG \_ Reserved8**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



No debe usarse. Reservado para uso futuro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Constantes comunes de EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

