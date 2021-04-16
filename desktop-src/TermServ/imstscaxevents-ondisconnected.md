---
title: IMsTscAxEvents método OnDisconnect
description: Se llama cuando el control de cliente se ha desconectado del servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Método OnDisconnection Servicios de Escritorio remoto
- Método OnDisconnection Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnDisconnect
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676820"
---
# <a name="imstscaxeventsondisconnected-method"></a>IMsTscAxEvents:: OnDisconnection (método)

Se llama cuando el control de cliente se ha desconectado del servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*discReason* \[ de\]
</dt> <dd>

Especifica el motivo de la desconexión. A continuación se muestra una lista de códigos de error. Algunos de estos códigos de error se definen en Wincred. h.

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))


</dt> <dd>

Socket cerrado.

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0X3))


</dt> <dd>

Desconexión remota por servidor. No es un código de error.

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))


</dt> <dd>

Error de descompresión.

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))


</dt> <dd>

La conexión ha agotado el tiempo de espera.

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))


</dt> <dd>

Error de descifrado.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))


</dt> <dd>

Error de búsqueda de nombre DNS.

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))


</dt> <dd>

Error de búsqueda de DNS.

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))


</dt> <dd>

Error de cifrado.

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))


</dt> <dd>

Error en la llamada [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) de Windows Sockets.

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))


</dt> <dd>

Error de host no encontrado.

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))


</dt> <dd>

Error interno.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))


</dt> <dd>

Error de seguridad interno.

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))


</dt> <dd>

Error de seguridad interno.

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))


</dt> <dd>

El método de cifrado especificado no es válido.

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))


</dt> <dd>

Se especificó una dirección IP incorrecta.

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))


</dt> <dd>

Los datos de seguridad del servidor no son válidos.

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))


</dt> <dd>

Los datos de seguridad no son válidos.

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))


</dt> <dd>

La dirección IP especificada no es válida.

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))


</dt> <dd>

Error de negociación de licencia.

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))


</dt> <dd>

Tiempo de espera de licencia.

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))


</dt> <dd>

Desconexión local. No es un código de error.

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0X0))


</dt> <dd>

No hay información disponible.

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))


</dt> <dd>

Memoria insuficiente

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))


</dt> <dd>

Memoria insuficiente

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))


</dt> <dd>

Memoria insuficiente

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0X2))


</dt> <dd>

Desconexión remota por usuario. No es un código de error.

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))


</dt> <dd>

No se pudo desempaquetar el certificado de servidor.

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))


</dt> <dd>

Error de conexión de Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))


</dt> <dd>

Error en la llamada de [**recepción**](/windows/desktop/api/winsock/nf-winsock-recv) de Windows Sockets.

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))


</dt> <dd>

Se agotó el tiempo de espera.

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))


</dt> <dd>

Error de temporizador interno.

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))


</dt> <dd>

Error en la llamada de [**envío**](/windows/desktop/api/winsock2/nf-winsock2-send) de Windows Sockets.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_ de Cuenta de ERR \_ \_ deshabilitada** (2823 (0xB07))


</dt> <dd>

La cuenta está deshabilitada.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_ de Cuenta de ERR \_ \_ expirada** (3591 (0xE07))


</dt> <dd>

La cuenta ha expirado.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_ de Cuenta de ERR \_ \_ bloqueada \_** (3335 (0xD07))


</dt> <dd>

Se ha bloqueado la cuenta.

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_ de \_ \_ Restricción** de la cuenta de ERR (3079 (0xC07))


</dt> <dd>

La cuenta está restringida.

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ de ERR \_ CERT \_ Expired** (6919 (0x1B07))


</dt> <dd>

El certificado recibido expiró.

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_ de \_ \_ Directiva de delegación de ERR** (5639) (0x1607)


</dt> <dd>

La Directiva no admite la delegación de credenciales en el servidor de destino.

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_ de ERROR \_ \_ de credenciales actualizadas \_ solicitadas \_ por el \_ servidor** (8455 (0x2107))


</dt> <dd>

La Directiva de autenticación de servidor no permite solicitudes de conexión con credenciales guardadas. El usuario debe escribir nuevas credenciales.

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_ de \_ \_ Error de inicio de sesión** de error (2055) (0x807)


</dt> <dd>

Error de inicio de sesión.

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_ de NO se pudo \_ \_ autenticar la \_ entidad de autenticación** (6151 (0x1807))


</dt> <dd>

No se pudo establecer contacto con ninguna autoridad para la autenticación. El nombre de dominio de la entidad de autenticación podría ser incorrecto, el dominio podría estar inaccesible o podría haber un error de relación de confianza.

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_ de NO se ha podido \_ \_ este \_ usuario** (2567 (0xA07))


</dt> <dd>

El usuario especificado no tiene ninguna cuenta.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_ de Contraseña de error \_ \_ expirada** (3847 (0xF07))


</dt> <dd>

La contraseña ha expirado.

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_ de La \_ contraseña de Err \_ debe \_ cambiar** (4615 (0x1207))


</dt> <dd>

Se debe cambiar la contraseña del usuario antes de iniciar sesión por primera vez.

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ de \_Directiva de \_ Err \_ solo NTLM** (5895 (0x1707))


</dt> <dd>

No se permite la delegación de credenciales en el servidor de destino a menos que se haya logrado la autenticación mutua.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_ de \_Tarjeta inteligente de error \_ \_ bloqueada** (8711 (0x2207))


</dt> <dd>

La tarjeta inteligente está bloqueada.

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_ de PIN de error de \_ tarjeta inteligente \_ errónea \_** (7175 (0x1C07))


</dt> <dd>

Se presentó un PIN incorrecto a la tarjeta inteligente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Para recuperar una descripción del error de desconexión, llame al método [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) y pásele el parámetro *discReason* y la propiedad [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) de la interfaz [**IMsRdpClient**](imsrdpclient-interface.md) .

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsTscAxEvents se define como 336d5562-efa8-482e-8cb3-c5c0fc7a7db6<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

