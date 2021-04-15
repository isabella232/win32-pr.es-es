---
description: Contiene información detallada sobre una interfaz requerida por un cliente RPC.
ms.assetid: 92e734f3-eacb-44dc-9016-88dc6e9f04b6
title: INTF_ENTRY estructura (wzcsapi. h)
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
ms.openlocfilehash: e08efc8c95374f268efe21f963357e9c4f34ae35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543558"
---
# <a name="intf_entry-structure"></a>\_Estructura de entrada Intf

\[**Intf \_ La entrada** ya no se admite en Windows Vista y Windows Server 2008. En su lugar, use la [API WiFi nativa](native-wifi-reference.md), que proporciona una funcionalidad similar. Para obtener más información, consulte [acerca de la API WiFi nativa](about-the-native-wifi-api.md).\]

Contiene información detallada sobre una interfaz requerida por un cliente RPC.

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

Puntero al GUID de la interfaz que se representa como una cadena Unicode en el siguiente formato: "{xxxxxxxx-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".

</dd> <dt>

**wszDescr**
</dt> <dd>

Un puntero a una cadena que contiene la descripción de la interfaz recuperada por el servicio de configuración inalámbrica rápida (WZCSVC).

</dd> <dt>

**dwContext**
</dt> <dd>

Reservado para uso interno.

</dd> <dt>

**ulMediaState**
</dt> <dd>

Estado actual de conexión multimedia de NDIS para la interfaz. En la siguiente tabla se muestran los valores posibles.



| Valor                                                                                                                                                                                                                                                  | Significado                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="MEDIA_STATE_CONNECTED_"></span><span id="media_state_connected_"></span><dl> <dt> **\_ Estado multimedia \_ conectado**</dt> <dt>1</dt> </dl>       | El medio está conectado.<br/>     |
| <span id="MEDIA_STATE_DISCONNECTED"></span><span id="media_state_disconnected"></span><dl> <dt>**Medios \_ de ESTADO \_ desconectado**</dt> <dt>0</dt> </dl> | El medio está desconectado.<br/>  |
| <span id="MEDIA_STATE_UNKNOWN"></span><span id="media_state_unknown"></span><dl> <dt>**Medios \_ de ESTADO \_ desconocido**</dt> <dt>-1</dt> </dl>               | No se conoce el estado del medio.<br/> |



 

</dd> <dt>

**ulMediaType**
</dt> <dd>

Los tipos de medios NDIS que usa actualmente la NIC. Cuando se consulta, el valor de este miembro es **NdisMedium802 \_ 3** , tal y como se define en el archivo de encabezado *Ndispnp. h* .

</dd> <dt>

**ulPhysicalMediaType**
</dt> <dd>

El tipo de medio NDIS para la interfaz. Cuando se consulta, el valor de este miembro es **NdisPhysicalMediumWirelessLan** , tal y como se define en el archivo de encabezado *Ndispnp. h* .

</dd> <dt>

**nInfraMode**
</dt> <dd>

El modo de infraestructura 802,11 actual establecido en la interfaz.

</dd> <dt>

**nAuthMode**
</dt> <dd>

El modo de autenticación 802,11 actual establecido en la interfaz.

En la tabla siguiente se muestran los posibles valores para el parámetro basado en la enumeración del **\_ modo de autenticación NDIS 802 \_ 11 \_ \_** definida en el archivo de encabezado *NtDDNdis. h* .



| Value                                                                                                                                                                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Ndis802_11AuthModeOpen"></span><span id="ndis802_11authmodeopen"></span><span id="NDIS802_11AUTHMODEOPEN"></span><dl> <dt>**Ndis802 \_ 11AuthModeOpen**</dt> <dt>1</dt> </dl>                         | IEEE 802,11 Open System Authentication.<br/>                                                                                                                                                                                                      |
| <span id="Ndis802_11AuthModeShared"></span><span id="ndis802_11authmodeshared"></span><span id="NDIS802_11AUTHMODESHARED"></span><dl> <dt>**Ndis802 \_ 11AuthModeShared**</dt> <dt>2</dt> </dl>                 | Autenticación compartida IEEE 802,11 que usa una clave de privacidad equivalente por cable (WEP) previamente compartida. <br/>                                                                                                                                                |
| <span id="Ndis802_11AuthModeAutoSwitch"></span><span id="ndis802_11authmodeautoswitch"></span><span id="NDIS802_11AUTHMODEAUTOSWITCH"></span><dl> <dt>**Ndis802 \_ 11AuthModeAutoSwitch**</dt> <dt>3</dt> </dl> | Modo de cambio automático. Al usar el modo de conmutador automático, la tarjeta de interfaz de red inalámbrica (NIC) intenta en primer lugar el modo de autenticación compartida. Si se produce un error en el modo compartido, la NIC intenta usar el modo de autenticación abierta. <br/>                                    |
| <span id="Ndis802_11AuthModeWPA"></span><span id="ndis802_11authmodewpa"></span><span id="NDIS802_11AUTHMODEWPA"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA**</dt> <dt>4</dt> </dl>                             | Seguridad de acceso protegido inalámbrico (WPA). La autenticación se realiza entre el solicitante, el autenticador y el servidor de autenticación a través de IEEE 802.1 X. Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación. <br/>     |
| <span id="Ndis802_11AuthModeWPAPSK"></span><span id="ndis802_11authmodewpapsk"></span><span id="NDIS802_11AUTHMODEWPAPSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPAPSK**</dt> <dt>5</dt> </dl>                 | Seguridad de WPA mediante una clave previamente compartida. La autenticación se realiza entre el solicitante y el autenticador a través de IEEE 802.1 X. Las claves de cifrado son dinámicas y se derivan de la clave previamente compartida utilizada por el solicitante y el autenticador. <br/> |
| <span id="Ndis802_11AuthModeWPANone"></span><span id="ndis802_11authmodewpanone"></span><span id="NDIS802_11AUTHMODEWPANONE"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPANone**</dt> <dt>6</dt> </dl>             | Seguridad de WPA. La autenticación se realiza mediante una clave previamente compartida sin la autenticación IEEE 802.1 X. Las claves de cifrado son estáticas y se derivan de la clave previamente compartida. Este modo solo es aplicable a los tipos de red ad hoc. <br/>             |
| <span id="Ndis802_11AuthModeWPA2"></span><span id="ndis802_11authmodewpa2"></span><span id="NDIS802_11AUTHMODEWPA2"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2**</dt> <dt>7</dt> </dl>                         | Seguridad de WPA2. La autenticación se realiza entre el solicitante, el autenticador y el servidor de autenticación a través de IEEE 802.1 X. Las claves de cifrado son dinámicas y se derivan a través del proceso de autenticación. <br/>                               |
| <span id="Ndis802_11AuthModeWPA2PSK"></span><span id="ndis802_11authmodewpa2psk"></span><span id="NDIS802_11AUTHMODEWPA2PSK"></span><dl> <dt>**Ndis802 \_ 11AuthModeWPA2PSK**</dt> <dt>8</dt> </dl>             | Especifica la seguridad de WPA2. La autenticación se realiza entre el solicitante y el autenticador a través de IEEE 802 1X. Las claves de cifrado son dinámicas y se derivan de la clave previamente compartida utilizada por el solicitante y el autenticador. <br/>             |
| <span id="Ndis802_11AuthModeMax"></span><span id="ndis802_11authmodemax"></span><span id="NDIS802_11AUTHMODEMAX"></span><dl> <dt>**Ndis802 \_ 11AuthModeMax**</dt> <dt>9</dt> </dl>                             | El valor máximo posible para el valor de enumeración del **\_ modo de autenticación NDIS 802 \_ 11 \_ \_** . Este no es un valor válido para el modo de autenticación. <br/>                                                                                        |



 

</dd> <dt>

**nWepStatus**
</dt> <dd>

El modo de cifrado de 802,11 actual establecido en la interfaz.

</dd> <dt>

**dwCtlFlags**
</dt> <dd>

Un valor de máscara de máscara de marcas de control que indica cómo funciona WZCSVC en la interfaz.

En la tabla siguiente se muestran los posibles valores de bit.



| Value                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCTL_CM_MASK"></span><span id="intfctl_cm_mask"></span><dl> <dt>**INTFCTL \_ \_Máscara de cm**</dt> <dt>0x0007</dt> </dl>      | Máscara de red para el modo de filtro de red. INTFCTL \_ cm \_ Mask & dwCtlFlags generan un valor del tipo \_ infraestructura de red NDIS \_ 802 \_ 11 \_ . El valor resultante indica si WZCSVC solo se conecta a redes de infraestructura, redes ad hoc o a ambos tipos de redes.<br/> |
| <span id="INTFCTL_ENABLED"></span><span id="intfctl_enabled"></span><dl> <dt>**INTFCTL \_ HABILITAdo**</dt> <dt>0x8000</dt> </dl>       | Indica si WZCSVC debe configurar la interfaz.<br/>                                                                                                                                                                                                                         |
| <span id="INTFCTL_FALLBACK"></span><span id="intfctl_fallback"></span><dl> <dt>**INTFCTL \_**</dt> <dt>0X4000</dt> de reserva </dl>    | Si una red preferida no está disponible, este valor indica si WZCSVC debe configurar automáticamente la NIC para asociar a cualquier red disponible.<br/>                                                                                                                       |
| <span id="INTFCTL_OIDSSUPP_"></span><span id="intfctl_oidssupp_"></span><dl> <dt> **INTFCTL \_ OIDSSUPP**</dt> <dt>0x2000</dt> </dl> | Indica si el controlador NIC admite todos los OID 802,11 requeridos por WZCSVC para funcionar.<br/>                                                                                                                                                                                    |
| <span id="INTFCTL_VOLATILE_"></span><span id="intfctl_volatile_"></span><dl> <dt> **INTFCTL \_ volatile**</dt> <dt>0x1000</dt> </dl> | Indica si los parámetros de servicio de esta interfaz se deben conservar en el registro. <br/> Si se establece este valor, estos parámetros son volátiles y no deben conservarse en el registro.<br/>                                                                 |
| <span id="INTFCTL_POLICY_"></span><span id="intfctl_policy_"></span><dl> <dt>0x0800</dt> de <dt> **\_ Directiva de INTFCTL**</dt> </dl>       | Indica si una directiva de grupo inserta los parámetros de servicio para esta interfaz.<br/> Si se establece este valor, la Directiva de grupo inserta los parámetros del servicio en el equipo local.<br/>                                                                         |
| <span id="INTFCTL_8021XSUPP"></span><span id="intfctl_8021xsupp"></span><dl> <dt>**INTFCTL \_ 8021XSUPP**</dt> <dt>0x1000</dt> </dl> | Indica si la compatibilidad con 802.1 X está habilitada.<br/>                                                                                                                                                                                                                                     |



 

</dd> <dt>

**dwDynFlags**
</dt> <dd>

Máscara de bits de marcas dinámicas que controlan el comportamiento dinámico (no persistente y no estático) en la interfaz.

Estos bits son útiles para desencadenar cambios temporales y dinámicos en la forma en que el WZCSVC actúa en la interfaz. Ninguno de estos bits se conserva en el registro, por lo que la configuración no sobrevive al reinicio del sistema o a una secuencia de deshabilitación y habilitación de dispositivos.

En la tabla siguiente se muestran los posibles valores de bit.



| Value                                                                                                                                                                                                                            | Significado                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFDYN_NOSCAN"></span><span id="intfdyn_noscan"></span><dl> <dt>**INTFDYN \_ Noscan**</dt> <dt>0x00000001</dt> </dl> | Indica que WZCSVC no debe solicitar que la interfaz realice un examen activo, sino que use los valores almacenados en caché del controlador NIC.<br/> |



 

</dd> <dt>

**dwCapabilities**
</dt> <dd>

Especifica las capacidades del controlador.



| Value                                                                                                                                                                                                                                                         | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTFCAP_MAX_CIPHER_MASK"></span><span id="intfcap_max_cipher_mask"></span><dl> <dt>**INTFCAP \_ \_ \_ Máscara de cifrado máxima**</dt> <dt>0x000000ff</dt> </dl> | Los bits de orden inferior de este miembro se utilizan para indicar el cifrado máximo que se admite. Los valores posibles son algunos de los valores de enumeración definidos en la estructura de **\_ \_ \_ \_ Estado WEP 802 11 de NDIS** en el archivo de encabezado *NtDDNdis. h* incluido en el Windows SDK.<br/> El valor de 11Encryption1Enabled de Ndis802 \_ (2) indica que se admite WEP. TKIP y AES no se admiten, y es posible que una clave de transmisión esté disponible o no. <br/> El valor de 11Encryption2Enabled de Ndis802 \_ (9) indica que se admiten TKIP y WEP. No se admite AES y está disponible una clave de transmisión. <br/> El valor de 11Encryption3Enabled de Ndis802 \_ (11) indica que se admiten AES, TKIP y WEP, y que hay disponible una clave de transmisión. <br/> Ndis802 \_ 11EncryptionNotSupported (8) indica que no se admite la clave WEP. <br/> |
| <span id="INTFCAP_SSN"></span><span id="intfcap_ssn"></span><dl> <dt>**INTFCAP \_ SSN**</dt> <dt>0x00000100</dt> </dl>                                       | Indica compatibilidad con la red segura simple (SSN), que es un subconjunto de 802.11 i. <br/> SSN cambia la clave de cifrado periódicamente, en lugar de la estándar WEP (privacidad equivalente por cable), que usa una clave estática. Para que SSN funcione, el cifrado máximo admitido debe ser al menos TKIP. SSN fue desarrollado por un consorcio de proveedores en 2002 como un enfoque provisional para mejorar la seguridad de LAN inalámbrica mientras se completaba la norma IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="INTFCAP_80211I"></span><span id="intfcap_80211i"></span><dl> <dt>**INTFCAP \_ 80211I**</dt> <dt>0x00000200</dt> </dl>                              | Indica compatibilidad con el estándar IEEE 802.11 i.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

</dd> <dt>

**rdNicCapabilities**
</dt> <dd>

Un conjunto de funcionalidades para 802.11 i.

La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdNicCapabilities** cuando se llama con la marca de **\_ funcionalidades Intf** que se pasa en el parámetro *dwInflags* . Si la llamada de función se realiza correctamente, el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene una estructura de **capacidad de Intf \_ 80211 \_** .

</dd> <dt>

**rdSSID**
</dt> <dd>

Datos binarios que contienen el SSID 802,11 actualmente configurado en la interfaz.

La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdSSID** cuando se llama con la marca **Intf \_ SSID** pasada en el parámetro *dwInflags* . Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene el miembro **SsidLength** de una estructura de **SSID de NDIS \_ 802 \_ \_ 11** y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene el miembro **SSID** de una estructura de **\_ \_ \_ SSID 802 11 de NDIS** .

La estructura de **\_ \_ \_ SSID NDIS 802 11** se define en el archivo de encabezado *Ntddndis. h* .

</dd> <dt>

**rdBSSID**
</dt> <dd>

Datos binarios que contienen el valor de BSSID 802,11 configurado en la interfaz.

La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdBSSID** cuando se llama con la marca **\_ BSSID Intf** pasada en el parámetro *dwInflags* . Si la llamada a la función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene el tamaño de una estructura de **\_ \_ \_ \_ direcciones MAC NDIS 802 11** y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de **\_ \_ \_ \_ dirección Mac de NDIS 802 11** .

La estructura de **\_ \_ \_ \_ direcciones MAC NDIS 802 11** se define en el archivo de encabezado *Ntddndis. h* .

</dd> <dt>

**rdBSSIDList**
</dt> <dd>

Datos binarios que contienen la lista de BSSIDs que el WZCSVC recuperó por última vez.

La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdBSSIDList** cuando se llama con la marca **Intf \_ BSSIDLIST** pasada en el parámetro *dwInflags* . Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene la longitud del búfer con los datos devueltos y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de la **lista de configuración de WZC \_ 802 \_ 11 \_ \_** .

</dd> <dt>

**rdStSSIDList**
</dt> <dd>

Datos binarios que contienen la lista de redes preferidas configuradas para esta interfaz.

La función [**WZCQueryInterface**](wzcqueryinterface.md) devuelve los datos de **rdStSSIDList** cuando se llama con la marca **Intf \_ PREFLIST** pasada en el parámetro *dwInflags* . Si la llamada de función se realiza correctamente, el miembro **dwDataLen** de la estructura de **\_ datos sin procesar** contiene la longitud del búfer con los datos devueltos y el miembro **pdata** de la estructura de **\_ datos sin procesar** contiene la estructura de la **lista de configuración de WZC \_ 802 \_ 11 \_ \_** .

Si una de las redes preferidas está conectada actualmente, el miembro **dwCtlFlags** de la estructura de **configuración de \_ WLAN \_ de WZC** para la red tendrá establecido el bit **WZCCTL \_ media \_ Connected** (0x0400).

</dd> <dt>

**rdCtrlData**
</dt> <dd>

Datos binarios usados con otras marcas de control, al establecer parámetros adicionales en la interfaz.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Las funciones [**WZCQueryInterface**](wzcqueryinterface.md) y [**WZCRefreshInterface**](wzcrefreshinterface.md) usan la estructura de **\_ entrada Intf** .

La estructura de **\_ datos sin procesar** se define de la siguiente manera:


```C++
typedef struct
{
    DWORD   dwDataLen;
    LPBYTE  pData;
} RAW_DATA, *PRAW_DATA;
```



El miembro *pdata* apunta a datos binarios. *DwDataLen* indica el número de bytes señalado por *pdata*.

> [!Note]  
> El archivo de encabezado *wzcsapi. h* no está disponible en el Windows SDK.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP con SP2 \[\]<br/>                                 |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP con SP3<br/>                                                       |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Wzcsapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 




