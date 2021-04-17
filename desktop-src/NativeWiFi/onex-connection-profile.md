---
description: Contiene información sobre el perfil de conexión de 802.1 X que se usa actualmente para la autenticación de 802.1 X.
ms.assetid: ec494c74-bc79-445a-8889-a6f441e95ac5
title: Estructura de ONEX_CONNECTION_PROFILE
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687433"
---
# <a name="onex_connection_profile-structure"></a>Estructura de Perfil de \_ conexión Onex \_

La estructura de **\_ \_ Perfil de conexión Onex** contiene información sobre el perfil de conexión de 802.1 x que se usa actualmente para la autenticación de 802.1 x.

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



## <a name="members"></a>Miembros

<dl> <dt>

**dwVersion**
</dt> <dd>

La versión de esta estructura de **\_ \_ Perfil de conexión Onex** .

</dd> <dt>

**dwTotalLen**
</dt> <dd>

Longitud, en bytes, de esta estructura **de \_ \_ Perfil de conexión Onex** .

</dd> <dt>

**fOneXSupplicantFlags**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwOneXSupplicantFlags** .

</dd> <dt>

**fsupplicantMode**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **supplicantMode** .

</dd> <dt>

**fauthMode**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **authMode** .

</dd> <dt>

**fHeldPeriod**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwHeldPeriod** .

</dd> <dt>

**fAuthPeriod**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwAuthPeriod** .

</dd> <dt>

**fStartPeriod**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwStartPeriod** .

</dd> <dt>

**fMaxStart**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwMaxStart** .

</dd> <dt>

**fMaxAuthFailures**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwMaxAuthFailures** .

</dd> <dt>

**fNetworkAuthTimeout**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwNetworkAuthTimeout** .

</dd> <dt>

**fAllowLogonDialogs**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **bAllowLogonDialogs** .

</dd> <dt>

**fNetworkAuthWithUITimeout**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **dwNetworkAuthWithUITimeout** .

</dd> <dt>

**fUserBasedVLan**
</dt> <dd>

Indica si la estructura del **\_ \_ Perfil de conexión Onex** contiene datos válidos en el miembro **bUserBasedVLan** .

</dd> <dt>

**dwOneXSupplicantFlags**
</dt> <dd>

Un conjunto de marcas 802.1 X que pueden estar presentes en el perfil. Estas marcas están reservadas para uso interno por parte del módulo de autenticación 802.1 X.

</dd> <dt>

**supplicantMode**
</dt> <dd>

El elemento supplicantMode en el esquema 802.1 X que especifica el método de transmisión utilizado para los mensajes de EAPOL-Start. Para obtener más información, vea el [**elemento supplicantMode (Onex)**](onexschema-supplicantmode-onex-element.md) en el esquema 802.1 x.



| Value                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXSupplicantModeInhibitTransmission"></span><span id="onexsupplicantmodeinhibittransmission"></span><span id="ONEXSUPPLICANTMODEINHIBITTRANSMISSION"></span><dl> <dt>**OneXSupplicantModeInhibitTransmission**</dt> <dt>0</dt> </dl> | No se transmiten los mensajes de EAPOL-Start. Válido solo para perfiles de LAN con cable.<br/>                                                                                             |
| <span id="OneXSupplicantModeLearn"></span><span id="onexsupplicantmodelearn"></span><span id="ONEXSUPPLICANTMODELEARN"></span><dl> <dt>**OneXSupplicantModeLearn**</dt> <dt>1</dt> </dl>                                                         | El cliente determina cuándo se deben enviar los paquetes de EAPOL-Start en función de la capacidad de la red. EAPOL-Start mensajes solo se envían cuando es necesario. Válido solo para perfiles de LAN con cable.<br/> |
| <span id="OneXSupplicantModeCompliant"></span><span id="onexsupplicantmodecompliant"></span><span id="ONEXSUPPLICANTMODECOMPLIANT"></span><dl> <dt>**OneXSupplicantModeCompliant**</dt> <dt>2</dt> </dl>                                         | EAPOL-Start mensajes se transmiten según lo especificado por 802.1 X. Válido para perfiles de LAN inalámbrica y cableada.<br/>                                                             |



 

</dd> <dt>

**authMode**
</dt> <dd>

El elemento authMode en el esquema 802.1 X que especifica el tipo de credenciales usado para la autenticación 802.1 X. Para obtener más información, vea el [**elemento authMode (Onex)**](onexschema-authmode-onex-element.md) en el esquema 802.1 x.



| Value                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OneXAuthModeMachineOrUser"></span><span id="onexauthmodemachineoruser"></span><span id="ONEXAUTHMODEMACHINEORUSER"></span><dl> <dt>**OneXAuthModeMachineOrUser**</dt> <dt>0</dt> </dl> | Usar credenciales de equipo o de usuario. Cuando un usuario ha iniciado sesión, se usan las credenciales del usuario para la autenticación. Cuando ningún usuario ha iniciado sesión, se usan las credenciales del equipo.<br/> |
| <span id="OneXAuthModeMachineOnly"></span><span id="onexauthmodemachineonly"></span><span id="ONEXAUTHMODEMACHINEONLY"></span><dl> <dt>**OneXAuthModeMachineOnly**</dt> <dt>1</dt> </dl>         | Usar solo credenciales de equipo.<br/>                                                                                                                                           |
| <span id="OneXAuthModeUserOnly"></span><span id="onexauthmodeuseronly"></span><span id="ONEXAUTHMODEUSERONLY"></span><dl> <dt>**OneXAuthModeUserOnly**</dt> <dt>2</dt> </dl>                     | Usar solo credenciales de usuario.<br/>                                                                                                                                              |
| <span id="OneXAuthModeGuest"></span><span id="onexauthmodeguest"></span><span id="ONEXAUTHMODEGUEST"></span><dl> <dt>**OneXAuthModeGuest**</dt> <dt>3</dt> </dl>                                 | Usar solo credenciales de invitado (vacío).<br/>                                                                                                                                     |
| <span id="OneXAuthModeUnspecified"></span><span id="onexauthmodeunspecified"></span><span id="ONEXAUTHMODEUNSPECIFIED"></span><dl> <dt>**OneXAuthModeUnspecified**</dt> <dt>4</dt> </dl>         | No se especifican las credenciales que se van a usar.<br/>                                                                                                                                   |



 

</dd> <dt>

**dwHeldPeriod**
</dt> <dd>

El elemento heldPeriod en el esquema 802.1 X que especifica el período de tiempo, en segundos, en el que un cliente no volverá a intentar la autenticación después de un intento de autenticación erróneo. Para obtener más información, vea el [**elemento heldPeriod (Onex)**](onexschema-heldperiod-onex-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwAuthPeriod**
</dt> <dd>

El elemento authPeriod en el esquema 802.1 X que especifica el período de tiempo máximo, en segundos, en el que un cliente espera una respuesta del autenticador. Si no se recibe una respuesta dentro del período especificado, el cliente da por supuesto que no hay ningún autenticador presente en la red. Para obtener más información, vea el [**elemento authPeriod (Onex)**](onexschema-authperiod-onex-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwStartPeriod**
</dt> <dd>

El elemento startPeriod en el esquema 802.1 X que especifica el período de tiempo, en segundos, que hay que esperar antes de que se envíe un EAPOL-Start. Se envía un mensaje de EAPOL-Start para iniciar el proceso de autenticación de 802.1 X. Para obtener más información, vea el [**elemento startPeriod (Onex)**](onexschema-startperiod-onex-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwMaxStart**
</dt> <dd>

El elemento maxStart en el esquema 802.1 X que especifica el número máximo de mensajes EAPOL-Start enviados. Una vez enviado el número máximo de mensajes EAPOL-Start, el cliente supone que no hay ningún autenticador presente en la red. Para obtener más información, vea el [**elemento maxStart (Onex)**](onexschema-maxstart-onex-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwMaxAuthFailures**
</dt> <dd>

El elemento maxAuthFailures en el esquema 802.1 X que especifica el número máximo de errores de autenticación permitido para un conjunto de credenciales. Para obtener más información, vea el elemento [**maxAuthFailures (Onex)**](onexschema-maxauthfailures-onex-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwNetworkAuthTimeout**
</dt> <dd>

Tiempo, en segundos, que se va a esperar a que se complete la autenticación de 802.1 X antes de que continúe el inicio de sesión normal. Este valor se usa en escenarios de inicio de sesión único (SSO). El valor predeterminado es 10 segundos en un perfil de 802.1 X. Para obtener más información, vea el [**elemento maxDelay (singleSignOn)**](onexschema-maxdelay-singlesignon-element.md) en el esquema 802.1 x.

</dd> <dt>

**dwNetworkAuthWithUITimeout**
</dt> <dd>

Tiempo de espera máximo, en segundos, que se debe esperar para una conexión en caso de que se muestre un cuadro de diálogo de la interfaz de usuario que requiera la intervención del usuario durante el inicio de sesión único.

En Windows Vista con SP1 y versiones posteriores, este valor está codificado en 10 minutos y no es configurable. En la versión de Windows Vista a fabricación, este valor tiene como valor predeterminado 60 segundos en un perfil de 802.1 X y se controla mediante el elemento **maxDelayWithAdditionalDialogs** en el esquema.

En Windows Vista con SP1 y versiones posteriores, el elemento **maxDelayWithAdditionalDialogs** del esquema 802.1 x se omite y se deja en desuso.

</dd> <dt>

**bAllowLogonDialogs**
</dt> <dd>

Valor que especifica si se permiten mostrar cuadros de diálogo EAP cuando se usa el inicio de sesión único de SSO. Para obtener más información, vea el elemento **allowAdditionalDialogs** en el esquema 802.1 x.

</dd> <dt>

**bUserBasedVLan**
</dt> <dd>

El elemento userBasedVirtualLan en el esquema 802.1 X que especifica si la LAN virtual (VLAN) usada por el dispositivo cambia en función de las credenciales del usuario. Algunos dispositivos del servidor de acceso a la red (NAS) cambian la VLAN después de que un usuario se autentique. Cuando userBasedVirtualLan es TRUE, el NAS puede cambiar la VLAN de un dispositivo después de que un usuario se autentique. Para obtener más información, vea el [**elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md) en el esquema 802.1 x.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La estructura de **\_ \_ Perfil de conexión Onex** la usa el módulo 802.1 x, un nuevo componente de configuración inalámbrica compatible con Windows Vista y versiones posteriores.

Los [**\_ datos de \_ actualización \_ de resultados de Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) contienen información sobre un cambio de estado para la autenticación de 802.1 x. La estructura de **datos de \_ \_ actualización \_ de resultados Onex** se devuelve cuando el miembro **NotificationSource** de la estructura de [**datos de \_ notificación \_ de WLAN**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85)) es  Onex de **origen de notificación de WLAN \_ \_ \_** y el miembro NotificationCode de la estructura de **datos de \_ notificación \_ de WLAN** para la notificación recibida es **OneXNotificationTypeResultUpdate**. En esta notificación, el miembro **pdata** de la estructura de **\_ \_ datos de notificación de WLAN** apunta a una estructura de **\_ \_ \_ datos de actualización de resultados Onex** que contiene información sobre el cambio de estado de autenticación de 802.1 x.

Si se establece el miembro **fOneXAuthParams** de la estructura de [**datos de \_ \_ actualización \_ de resultados Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data) , el miembro **authParams** de la estructura de **datos de \_ \_ actualización \_ de resultados Onex** contiene una estructura de [**\_ \_ BLOB de variable Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob) con una estructura de [**\_ \_ parámetros de autenticación Onex**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params) insertada a partir del miembro **dwOffset** del BLOB de la **\_ variable \_ Onex**. El **miembro oneXConnProfile** de la estructura de **\_ \_ parámetros de autenticación Onex** contiene una estructura de **\_ \_ BLOB de variable Onex** con una estructura de **\_ \_ Perfil de conexión Onex** insertada a partir del miembro **dwOffset** del BLOB de la **\_ variable \_ Onex**.

La estructura de **\_ \_ Perfil de conexión Onex** no está definida en un archivo de encabezado público.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Acerca de la arquitectura ACM](about-the-acm-architecture.md)
</dt> <dt>

[Esquema OneX](onexschema-schema.md)
</dt> <dt>

[**Elemento authMode (OneX)**](onexschema-authmode-onex-element.md)
</dt> <dt>

[**Elemento authPeriod (OneX)**](onexschema-authperiod-onex-element.md)
</dt> <dt>

[**Elemento heldPeriod (OneX)**](onexschema-heldperiod-onex-element.md)
</dt> <dt>

[**maxAuthFailures (OneX)**](onexschema-maxauthfailures-onex-element.md)
</dt> <dt>

[**Elemento maxStart (OneX)**](onexschema-maxstart-onex-element.md)
</dt> <dt>

[**Elemento startPeriod (OneX)**](onexschema-startperiod-onex-element.md)
</dt> <dt>

[**Elemento supplicantMode (OneX)**](onexschema-supplicantmode-onex-element.md)
</dt> <dt>

[**Elemento userBasedVirtualLan (singleSignOn)**](onexschema-userbasedvirtuallan-singlesignon-element.md)
</dt> <dt>

[**\_parámetros de autenticación Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_auth_params)
</dt> <dt>

[**\_tipo de notificación Onex \_**](/windows/desktop/api/dot1x/ne-dot1x-onex_notification_type)
</dt> <dt>

[**\_datos de \_ actualización de resultados de Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_result_update_data)
</dt> <dt>

[**OneX (elemento de esquema)**](onexschema-onex-element.md)
</dt> <dt>

[**\_BLOB de variable de Onex \_**](/windows/desktop/api/dot1x/ns-dot1x-onex_variable_blob)
</dt> <dt>

[**\_datos de notificación de WLAN \_**](/previous-versions/windows/desktop/legacy/ms706902(v=vs.85))
</dt> <dt>

[**WlanRegisterNotification**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
</dt> </dl>

 

 
