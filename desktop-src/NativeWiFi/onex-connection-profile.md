---
description: Contiene información sobre el perfil de conexión 802.1X que se usa actualmente para la autenticación 802.1X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: ONEX_CONNECTION_PROFILE estructura
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ONEX_CONNECTION_PROFILE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21e02a1f09d3439c64fb8124cd0cfc8140732be9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069454"
---
# <a name="onex_connection_profile-structure"></a>Estructura DE \_ PERFIL \_ DE CONEXIÓN ONEX

La **estructura ONEX \_ CONNECTION \_ PROFILE** contiene información sobre el perfil de conexión 802.1X que se usa actualmente para la autenticación 802.1X.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ONEX_CONNECTION_PROFILE {
  DWORD                dwVersion;
  DWORD                dwTotalLen;
  DWORD                fOneXSupplicantFlags  :1;
  DWORD                fsupplicantMode  :1;
  DWORD                fauthMode  :1;
  DWORD                fHeldPeriod  :1;
  DWORD                fAuthPeriod  :1;
  DWORD                fStartPeriod  :1;
  DWORD                fMaxStart  :1;
  DWORD                fMaxAuthFailures  :1;
  DWORD                fNetworkAuthTimeout  :1;
  DWORD                fAllowLogonDialogs  :1;
  DWORD                fNetworkAuthWithUITimeout  :1;
  DWORD                fUserBasedVLan  :1;
  DWORD                dwOneXSupplicantFlags;
  ONEX_SUPPLICANT_MODE supplicantMode;
  ONEX_AUTH_MODE       authMode;
  DWORD                dwHeldPeriod;
  DWORD                dwAuthPeriod;
  DWORD                dwStartPeriod;
  DWORD                dwMaxStart;
  DWORD                dwMaxAuthFailures;
  DWORD                dwNetworkAuthTimeout;
  DWORD                dwNetworkAuthWithUITimeout;
  BOOL                 bAllowLogonDialogs;
  BOOL                 bUserBasedVLan;
} ONEX_CONNECTION_PROFILE, *PONEX_CONNECTION_PROFILE;
```



## <a name="members"></a>Members

<dl> <dt>

**dwVersion**
</dt> <dd>

La versión de esta estructura **ONEX \_ CONNECTION \_ PROFILE.**

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Longitud, en bytes, de esta **estructura ONEX \_ CONNECTION \_ PROFILE.**

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwOneXSupplicantFlags.**

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro supplicantMode.**

</dd> <dt>

**fauthMode**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro authMode.**

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwHeldPeriod.**

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwAuthPeriod.**

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwStartPeriod.**

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwMaxStart.**

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwMaxAuthFailures.**

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwNetworkAuthTimeout.**

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en **el miembro bAllowLogonDialogs.**

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro dwNetworkAuthWithUITimeout.**

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indica si la estructura **ONEX \_ CONNECTION \_ PROFILE** contiene datos válidos en el **miembro bUserBasedVLan.**

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Conjunto de marcas 802.1X que pueden estar presentes en el perfil. El módulo de autenticación 802.1X reserva estas marcas para su uso interno.

</dd> <dt>

**supplicantMode**
</dt> <dd>

Elemento supplicantMode del esquema 802.1X que especifica el método de transmisión utilizado para EAPOL-Start mensajes. Para obtener más información, [**vea el elemento supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md) en el esquema 802.1X.



| Value                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | EAPOL-Start mensajes no se transmiten. Válido solo para perfiles de LAN cableadas.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | El cliente determina cuándo enviar paquetes EAPOL-Start en función de la funcionalidad de red. EAPOL-Start mensajes solo se envían cuando es necesario. Válido solo para perfiles de LAN cableadas.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start mensajes se transmiten según lo especificado por 802.1X. Válido para perfiles de LAN cableadas e inalámbricas.<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

Elemento authMode del esquema 802.1X que especifica el tipo de credenciales usadas para la autenticación 802.1X. Para obtener más información, vea [**el elemento authMode (OneX)**](onexschema-authmode-onex-element.md) en el esquema 802.1X.



| Value                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Use credenciales de máquina o usuario. Cuando un usuario ha iniciado sesión, las credenciales del usuario se usan para la autenticación. Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Use solo credenciales de máquina.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Use solo credenciales de usuario.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Use solo credenciales de invitado (vacías).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | No se especifican las credenciales que se van a usar.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

Elemento heldPeriod del esquema 802.1X que especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación con error. Para obtener más información, vea [**el elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md) en el esquema 802.1X.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

Elemento authPeriod del esquema 802.1X que especifica la longitud máxima de tiempo, en segundos, en la que un cliente espera una respuesta del autenticador. Si no se recibe una respuesta dentro del período especificado, el cliente asume que no hay ningún autenticador presente en la red. Para obtener más información, vea el elemento [**authPeriod (OneX)**](onexschema-authperiod-onex-element.md) en el esquema 802.1X.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

Elemento startPeriod del esquema 802.1X que especifica el tiempo, en segundos, que se debe esperar antes de que se envíe EAPOL-Start una aplicación. Se EAPOL-Start mensaje para iniciar el proceso de autenticación 802.1X. Para obtener más información, [**vea el elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md) del esquema 802.1X.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

Elemento maxStart del esquema 802.1X que especifica el número máximo de EAPOL-Start mensajes enviados. Una vez enviado el número máximo EAPOL-Start mensajes, el cliente asume que no hay ningún autenticador presente en la red. Para obtener más información, [**vea el elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md) en el esquema 802.1X.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

Elemento maxAuthFailures del esquema 802.1X que especifica el número máximo de errores de autenticación permitidos para un conjunto de credenciales. Para obtener más información, [**vea el elemento maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md) en el esquema 802.1X.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Tiempo, en segundos, que se debe esperar a la finalización de la autenticación 802.1X antes de que continúe el inicio de sesión normal. Este valor se usa en escenarios de inicio de sesión único (SSO). Este valor tiene como valor predeterminado 10 segundos en un perfil 802.1X. Para obtener más información, [**vea el elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) en el esquema 802.1X.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

El tiempo máximo de duración, en segundos, para esperar una conexión en caso de que se muestre un cuadro de diálogo de interfaz de usuario que requiera la entrada del usuario durante el inicio de sesión único por inicio de sesión.

En Windows Vista con SP1 y versiones posteriores, este valor se codifica de forma rígida a 10 minutos y no es configurable. En Windows versión de Vista para fabricación, este valor tiene como valor predeterminado 60 segundos en un perfil 802.1X y estaba controlado por el elemento **maxDelayWithAdditionalDialogs** del esquema.

En Windows Vista con SP1 y versiones posteriores, el elemento **maxDelayWithAdditionalDialogs** del esquema 802.1X se omite y está en desuso.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Valor que especifica si se deben permitir que se muestren diálogos EAP al usar sso previo al inicio de sesión único. Para obtener más información, **vea el elemento allowAdditionalDialogs** en el esquema 802.1X.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

Elemento userBasedVirtualLan del esquema 802.1X que especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario. Algunos dispositivos de servidor de acceso a la red (NAS) cambian la VLAN después de que un usuario se autentique. Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique. Para obtener más información, [**vea el elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) en el esquema 802.1X.

</dd> </dl>

## <a name="remarks"></a>Observaciones

El módulo 802.1X usa la estructura **ONEX \_ CONNECTION \_ PROFILE,** un nuevo componente de configuración inalámbrica compatible con Windows Vista y versiones posteriores.

[**ONEX \_ RESULT UPDATE DATA \_ \_ contiene**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) información sobre un cambio de estado a la autenticación 802.1X. La estructura **ONEX \_ RESULT UPDATE \_ \_ DATA** se devuelve cuando el miembro **NotificationSource** de la estructura DE DATOS DE NOTIFICACIÓN DE WLAN es **WLAN NOTIFICATION SOURCE \_ \_ \_ ONEX** y el **miembro NotificationCode** de la estructura DE DATOS DE NOTIFICACIÓN DE WLAN para la notificación recibida **es OneXNotificationTypeResultUpdate.** [**\_ \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) **\_ \_** Para esta notificación, el miembro **pData** de la estructura **WLAN NOTIFICATION \_ \_ DATA** apunta a una estructura **ONEX RESULT UPDATE \_ \_ \_ DATA** que contiene información sobre el cambio de estado de autenticación 802.1X.

Si se establece el miembro **fOneXAuthParams** de la estructura [**ONEX \_ RESULT UPDATE \_ \_ DATA,**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) el miembro **authParams** de la estructura **ONEX RESULT UPDATE \_ \_ \_ DATA** contiene una estructura [**\_ ONEX VARIABLE \_ BLOB**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una estructura [**ONEX \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) incrustada a partir del **miembro dwOffset** del **BLOB DE VARIABLE \_ \_ ONEX.** El **miembro oneXConnProfile** de la estructura **ONEX \_ AUTH \_ PARAMS** contiene una estructura **\_ \_ ONEX VARIABLE BLOB** con una estructura **ONEX CONNECTION \_ \_ PROFILE** incrustada a partir del **miembro dwOffset** de **ONEX VARIABLE \_ \_ BLOB.**

La **estructura ONEX \_ CONNECTION \_ PROFILE** no se define en un archivo de encabezado público.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Acerca de la arquitectura de ACM](about-the-acm-architecture.md)
</dt> <dt>

[Esquema de OneX](onexschema-schema.md)
</dt> <dt>

[**Elemento authMode (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**Elemento authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**Elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**elemento supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**ONEX \_ AUTH \_ PARAMS**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**TIPO DE \_ NOTIFICACIÓN \_ ONEX**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**DATOS DE ACTUALIZACIÓN \_ DE \_ RESULTADOS DE \_ ONEX**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**Elemento Schema de OneX**](onexschema-onex-element.md)
</dt> <dt>

[**BLOB DE \_ VARIABLE \_ ONEX**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**DATOS DE NOTIFICACIÓN DE WLAN \_ \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
