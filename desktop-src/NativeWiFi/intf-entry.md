---
description: Contiene información detallada sobre una interfaz que requiere un cliente RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: INTF_ENTRY estructura (Wzcsapi.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 8e93a9a0214e9ca46e6ae6872e0d341cd703ed9331622dfbc27bd5a949ece61c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801315"
---
# <a name="intf_entry-structure"></a>Estructura INTF \_ ENTRY

\[**INTF \_ ENTRY** ya no se admite a partir de Windows Vista y Windows Server 2008. En su lugar, use [la API Wi-Fi nativa,](native-wifi-reference.md)que proporciona una funcionalidad similar. Para obtener más información, vea [Acerca de la API Wi-Fi nativa.](about-the-native-wifi-api.md)\]

Contiene información detallada sobre una interfaz que requiere un cliente RPC.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct {
  LPWSTR   wszGuid;
  LPWSTR   wszDescr;
  DWORD    dwContext;
  ULONG    ulMediaState;
  ULONG    ulMediaType;
  ULONG    ulPhysicalMediaType;
  INT      nInfraMode;
  INT      nAuthMode;
  INT      nWepStatus;
  DWORD    dwCtlFlags;
  DWORD    dwDynFlags;
  DWORD    dwCapabilities;
  RAW_DATA rdNicCapabilities;
  RAW_DATA rdSSID;
  RAW_DATA rdBSSID;
  RAW_DATA rdBSSIDList;
  RAW_DATA rdStSSIDList;
  RAW_DATA rdCtrlData;
} INTF_ENTRY, *PINTF_ENTRY;
```



## <a name="members"></a>Miembros

<dl> <dt>

**wszGuid**
</dt> <dd>

Puntero al GUID de interfaz representado como una cadena Unicode con el siguiente formato: "{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}".

</dd> <dt>

**wszDescr**
</dt> <dd>

Puntero a una cadena que contiene la descripción de la interfaz recuperada por el servicio configuración inalámbrica cero (WZCSVC).

</dd> <dt>

**dwContext**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**ulMediaState**
</dt> <dd>

Estado actual de conexión de medios NDIS para la interfaz. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                  | Significado                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **ESTADO \_ MULTIMEDIA \_ CONECTADO**</dt> <dt>1</dt> </dl>       | El medio está conectado.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**MEDIA \_ ESTADO \_ DESCONECTADO**</dt> <dt>0</dt> </dl> | El medio está desconectado.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**MEDIA \_ ESTADO \_ DESCONOCIDO**</dt> <dt>-1</dt> </dl>               | Se desconoce el estado del medio.<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

Los tipos de medios NDIS que usa actualmente la NIC. Cuando se consulta, el valor de este miembro es **NdisMedium802 \_ 3,** tal como se define en el archivo de encabezado *Ndispnp.h.*

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

Tipo de medio NDIS para la interfaz. Cuando se consulta, el valor de este miembro es **NdisPhysicalMediumWirelessLan,** tal como se define en el archivo de encabezado *Ndispnp.h.*

</dd> <dt>

**nInfraMode**
</dt> <dd>

El modo de infraestructura 802.11 actual establecido en la interfaz.

</dd> <dt>

**nAuthMode**
</dt> <dd>

El modo de autenticación 802.11 actual establecido en la interfaz .

En la tabla siguiente se muestran los valores posibles para el parámetro basándose en la enumeración AUTHENTICATION MODE de **NDIS \_ 802 \_ 11 \_ \_** definida en el archivo de encabezado *NtDDNdis.h.*



| Valor                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeAbrir**</dt> <dt>1</dt> </dl>                         | Autenticación del sistema abierto IEEE 802.11.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | Autenticación compartida IEEE 802.11 que usa una clave de privacidad equivalente cableada (WEP) previamente compartida. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | Modo de conmutación automática. Cuando se usa el modo de conmutación automática, la tarjeta de interfaz de red inalámbrica (NIC) intenta primero el modo de autenticación compartida. Si se produce un error en el modo compartido, la NIC intenta usar el modo de autenticación abierto. <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             | Seguridad de acceso protegido inalámbrico (WPA). La autenticación se realiza entre el servidor de suplicación, autenticador y autenticación a través de IEEE 802.1X. Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | Seguridad wpa mediante una clave pre shared. La autenticación se realiza entre el suplicante y el autenticador a través de IEEE 802.1X. Las claves de cifrado son dinámicas y se derivan a través de la clave previamente compartida usada por el suplicante y el autenticador. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | Seguridad de WPA. La autenticación se realiza mediante una clave previamente compartida sin autenticación IEEE 802.1X. Las claves de cifrado son estáticas y se derivan a través de la clave previamente compartida. Este modo solo es aplicable a los tipos de red ad hoc. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | Seguridad de WPA2. La autenticación se realiza entre el servidor de suplicación, autenticador y autenticación a través de IEEE 802.1X. Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | Especifica la seguridad wpa2. La autenticación se realiza entre el suplicante y el autenticador a través de IEEE 802 1X. Las claves de cifrado son dinámicas y se derivan a través de la clave previamente compartida usada por el suplicante y el autenticador. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | Valor máximo posible para el valor de **enumeración NDIS \_ 802 \_ 11 \_ AUTHENTICATION \_ MODE.** Este no es un valor legal para el modo de autenticación. <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

El modo de cifrado 802.11 actual establecido en la interfaz .

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

Valor de máscara de bits de marcas de control que indican cómo funciona WZCSVC en la interfaz.

En la tabla siguiente se muestran los valores de bits posibles.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_ Máscara \_ de CM**</dt> <dt>0x0007</dt> </dl>      | Máscara de bits para el modo de filtro de red. INTFCTL CM MASK & dwCtlFlags tiene como resultado un valor del tipo \_ \_ \_ NDIS 802 \_ 11 \_ NETWORK \_ INFRASTRUCTURE. El valor resultante indica si WZCSVC solo se conecta a redes de infraestructura, redes addhoc o a ambos tipos de redes.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_ HABILITADO**</dt> <dt>0x8000</dt> </dl>       | Indica si WZCSVC debe configurar la interfaz.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_ FallBACK**</dt> <dt>0x4000</dt> </dl>    | Si una red preferida no está disponible, este valor indica si WZCSVC debe configurar automáticamente la NIC para asociarla a cualquier red disponible.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | Indica si el controlador NIC admite todos los 802.11 OID requeridos por WZCSVC para funcionar.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **InTFCTL \_ VOLATILE**</dt> <dt>0x1000</dt> </dl> | Indica si los parámetros de servicio para esta interfaz deben conservarse en el Registro. <br/> Si se establece este valor, estos parámetros son volátiles y no deben conservarse en el Registro.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt> **Directiva de \_ INTFCTL**</dt> <dt>0x0800</dt> </dl>       | Indica si una directiva de grupo inserta los parámetros de servicio para esta interfaz.<br/> Si se establece este valor, la directiva de grupo inserta los parámetros de servicio en el equipo local.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | Indica si está habilitada la compatibilidad con 802.1X.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

Máscara de bits de marcas dinámicas que controlan el comportamiento dinámico (no persistente y no estático) en la interfaz.

Estos bits son útiles para desencadenar cambios dinámicos y temporales en la forma en que WZCSVC actúa en la interfaz. Ninguno de estos bits se conserva en el Registro, por lo que la configuración no sobrevivirá a un reinicio del sistema o a que un dispositivo deshabilite y habilite la secuencia.

En la tabla siguiente se muestran los posibles valores de bits.



| Valor                                                                                                                                                                                                                            | Significado                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt> </dl> | Indica que WZCSVC no debe solicitar que la interfaz realice un examen activo, sino que use los valores almacenados en caché en el controlador NIC.<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

Especifica las funcionalidades del controlador.



| Valor                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_ MAX \_ CIPHER \_ MASK**</dt> <dt>0x000000ff</dt> </dl> | Los bits de orden inferior de este miembro se usan para indicar el cifrado máximo admitido. Los valores posibles son algunos de los valores de enumeración definidos en la estructura **NDIS \_ 802 \_ 11 \_ WEP \_ STATUS** en el archivo de encabezado *NtDDNdis.h* incluido en el SDK de Windows.<br/> El valor Ndis802 \_ 11Encryption1Enabled (2) indica que se admite WEP. No se admiten TKIP y AES, y una clave de transmisión puede estar disponible o no. <br/> El valor Ndis802 \_ 11Encryption2Enabled (9) indica que se admiten TKIP y WEP. No se admite AES y hay disponible una clave de transmisión. <br/> El valor Ndis802 \_ 11Encryption3Enabled (11) indica que se admiten AES, TKIP y WEP, y hay disponible una clave de transmisión. <br/> Ndis802 11EncryptionNotSupported (8) indica que no se admite la clave \_ WEP. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_ SSN**</dt> <dt>0x00000100</dt> </dl>                                       | Indica la compatibilidad con Simple Secure Network (SSN), que es un subconjunto de 802.11i. <br/> SSN cambia la clave de cifrado periódicamente, en lugar del estándar WEP (Wired Equivalent Privacy), que usa una clave estática. Para que SSN funcione, el cifrado máximo admitido debe ser al menos TKIP. SSN fue desarrollado por un consorcio de proveedores en 2002 como un enfoque provisional para mejorar la seguridad de LAN inalámbrica mientras se completaba el estándar IEEE 802.11i.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | Indica la compatibilidad con el estándar IEEE 802.11i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

Un conjunto de funcionalidades para 802.11i.

La [**función WZCQueryInterface**](wzcqueryinterface.md) devuelve datos **rdNicCapabilities** cuando se llama a con la marca **CAPABILITIES de INTF \_** pasada en el *parámetro dwInflags.* Si la llamada a la función se realiza correctamente, el **miembro pData** de la **estructura RAW \_ DATA** contiene una estructura **CAPABILITY INTF \_ 80211. \_**

</dd> <dt>

**rdSSID**
</dt> <dd>

Datos binarios que contienen el SSID 802.11 configurado actualmente en la interfaz.

La [**función WZCQueryInterface**](wzcqueryinterface.md) devuelve datos **rdSSID** cuando se llama con la marca **INTF \_ SSID** pasada en el *parámetro dwInflags.* Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura **RAW \_ DATA** contiene el miembro **SsidLength** de una estructura **\_ \_ \_ SSID NDIS 802 11** y el miembro **pData** de la estructura **RAW \_ DATA** contiene el miembro **Ssid** de una estructura **\_ \_ \_ SSID NDIS 802 11.**

La **estructura \_ \_ \_ SSID NDIS 802 11** se define en el archivo de encabezado *Ntddndis.h.*

</dd> <dt>

**rdBSSID**
</dt> <dd>

Datos binarios que contienen el BSSID 802.11 configurado en la interfaz.

La [**función WZCQueryInterface**](wzcqueryinterface.md) devuelve datos **rdBSSID** cuando se llama con la marca **\_ BSSID de INTF** pasada en el *parámetro dwInflags.* Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura **RAW \_ DATA** contiene el tamaño de una estructura **NDIS \_ 802 \_ 11 \_ MAC \_ ADDRESS** y el miembro **pData** de la estructura **RAW \_ DATA** contiene la estructura **NDIS \_ 802 \_ 11 \_ MAC \_ ADDRESS.**

La **estructura NDIS \_ 802 \_ 11 \_ MAC \_ ADDRESS** se define en el archivo de encabezado *Ntddndis.h.*

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

Datos binarios que contienen la lista de SSID que WZCSVC recuperó por última vez.

La [**función WZCQueryInterface**](wzcqueryinterface.md) devuelve datos **rdBSSIDList** cuando se llama a con la marca **\_ INTF BSSIDLIST** pasada en el *parámetro dwInflags.* Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura **RAW \_ DATA** contiene la longitud del búfer con los datos devueltos y el miembro **pData** de la estructura **RAW \_ DATA** contiene la estructura CONFIG LIST de **WZC \_ 802 \_ \_ \_ 11.**

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

Datos binarios que contienen la lista de redes preferidas configuradas para esta interfaz.

La [**función WZCQueryInterface**](wzcqueryinterface.md) devuelve datos **rdStSSIDList** cuando se llama a con la marca **\_ PREFLIST de INTF** pasada en el *parámetro dwInflags.* Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura **RAW \_ DATA** contiene la longitud del búfer con los datos devueltos y el miembro **pData** de la estructura **RAW \_ DATA** contiene la estructura CONFIG LIST de **WZC \_ 802 \_ \_ \_ 11.**

Si una de las redes preferidas está conectada actualmente, el miembro **dwCtlFlags** de la estructura **\_ WZC WLAN \_ CONFIG** de la red tendrá el conjunto de bits **WZCCTL \_ MEDIA \_ CONNECTED** (0x0400).

</dd> <dt>

**rdCtrlData**
</dt> <dd>

Datos binarios usados con otras marcas de control, al establecer parámetros adicionales en la interfaz.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Las funciones [**WZCQueryInterface**](wzcqueryinterface.md) y [**WZCRefreshInterface**](wzcrefreshinterface.md) usan la estructura **INTF \_ ENTRY.**

La **estructura \_ RAW DATA** se define de la siguiente manera:


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



El *miembro pData* apunta a datos binarios. *dwDataLen indica* el número de bytes a los que apunta *pData.*

> [!Note]  
> El *archivo de encabezado Wzcsapi.h* no está disponible en Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP solo con aplicaciones de \[ escritorio sp2\]<br/>                                 |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Wzcsapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




