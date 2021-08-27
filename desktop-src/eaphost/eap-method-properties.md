---
title: Propiedades del método EAP (Eaptypes.h)
description: Lo usan los suplicadores y autenticadores para determinar los métodos EAP que se usarán con un suplicante o autenticador determinado. Las propiedades del método también especifican la configuración de un método.
ms.assetid: 10407b85-5d2c-4c75-9b65-a0d65d4cc7ab
topic_type:
- apiref
api_name:
- eapPropCipherSuiteNegotiation
- eapPropMutualAuth
- eapPropIntegrity
- eapPropReplayProtection
- eapPropConfidentiality
- eapPropKeyDerivation
- eapPropKeyStrength64
- eapPropKeyStrength128
- eapPropKeyStrength256
- eapPropKeyStrength512
- eapPropKeyStrength1024
- eapPropDictionaryAttackResistance
- eapPropFastReconnect
- eapPropCryptoBinding
- eapPropSessionIndependence
- eapPropFragmentation
- eapPropChannelBinding
- eapPropNap
- eapPropStandalone
- eapPropMppeEncryption
- eapPropTunnelMethod
- eapPropSupportsConfig
- eapPropCertifiedMethod
- eapPropmachineAuth
- eapPropUserAuth
- eapPropIdentityPrivacy
- eapPropMethodChaining
- eapPropSharedStateEquivalence
- eapPropReserved
api_location:
- eaptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c88c31d77b666e377cbd1911cde8b5df63d8f5c2fc750cd03a701b03af5b60ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120094405"
---
# <a name="eap-method-properties"></a>Propiedades del método EAP

Lo usan los suplicadores y autenticadores para determinar los métodos EAP que se usarán con un suplicante o autenticador determinado. Las propiedades del método también especifican la configuración de un método.

Por ejemplo, el suplicante [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) puede requerir que los métodos tengan ciertas propiedades para su uso con el suplicante [802.1X.](/previous-versions/windows/embedded/ms890287(v=msdn.10)) El material de clave, por ejemplo, es un requisito.

Se enumeran las propiedades admitidas por los métodos EAP. Las propiedades se almacenan como valores de clave del Registro. Para obtener más información, vea la sección Clave del Registro DLL del método del mismo nivel de EAP del tema Configuración del [Registro para métodos EAP.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



El método permite que el conjunto de cifrado se negocie para el cifrado de datos. Windows Server 2008 admite los siguientes [](/windows/desktop/SecAuthN/tls-cipher-suites)conjuntos de cifrado 3DES:

-   TLS \_ RSA \_ WITH \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   TLS \_ DHE \_ DSS \_ CON \_ 3DES \_ EDE \_ CBC SHA \_ (TLS & SSL 3)
-   SSL \_ CK \_ DES \_ 192 \_ EDE3 \_ CBC \_ WITH \_ MD5 (SSL 2 si está habilitado)

Para obtener más información sobre el protocolo de seguridad TLS 1.0, vea [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



El método proporciona un intercambio, en el que el autenticador autentica el elemento del mismo nivel y viceversa.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



El método proporciona autenticación de origen de datos y protección contra la modificación no autorizada de información para paquetes EAP, incluidas las solicitudes y respuestas de EAP. Al realizar esta notificación, una especificación de método debe especificar los paquetes EAP protegidos y los campos protegidos dentro de los paquetes EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



El método puede protegerse contra la reproducción de un método EAP o sus mensajes. No se pueden reproducir las indicaciones de resultados correctos y de error.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



El método puede cifrar mensajes EAP. Se cifran las solicitudes de EAP, las respuestas de EAP, las indicaciones de resultados de éxito y las indicaciones de resultados de error. Un método que realiza esta notificación debe admitir la protección de identidad.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



El método puede derivar material de clave exportable, como la clave de sesión maestra (MSK) y la clave de sesión maestra extendida (EMSK). MSK solo se usa para la derivación de claves posteriores, no directamente para la protección de la conversación eap o los datos posteriores. El uso de EMSK está reservado.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



La longitud mínima de clave admitida por el método EAP es de 64 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



La longitud mínima de clave admitida por el método EAP es de 128 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



La longitud mínima de clave admitida por el método EAP es de 256 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



La longitud mínima de clave admitida por el método EAP es de 512 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La longitud mínima de clave admitida por el método EAP es de 1024 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



El método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas del diccionario de un atacante. Cuando se usa la autenticación de contraseñas, las contraseñas se seleccionan normalmente de un conjunto pequeño (en comparación con un conjunto de claves de N bits), lo que genera una preocupación por los ataques de diccionario. Se puede decir que un método proporciona protección contra ataques de diccionario si, cuando usa una contraseña como secreto, el método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas del diccionario de un atacante.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



El método tiene la capacidad, en el caso de que se haya establecido previamente una asociación de seguridad, de crear una asociación de seguridad nueva o actualizada de forma más eficaz o en un número menor de recorridos de ida y vuelta.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



El método muestra al servidor EAP que una sola entidad ha actuado como el par EAP para todos los métodos ejecutados dentro de un método de túnel. El enlace también puede implicar que el servidor EAP demuestra al mismo nivel que una sola entidad ha actuado como servidor EAP para todos los métodos ejecutados dentro de un método de túnel. Si se ejecuta correctamente, el enlace sirve para mitigar las vulnerabilidades de tipo "Man in the middle".


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



El método muestra que los ataques pasivos (como la captura de la conversación eap) o los ataques activos (incluido el riesgo de MSK o EMSK) no pone en peligro los MSK o EMSK posteriores o anteriores.


</dt> </dl> </dd> <dt>

<span id="eapPropFragmentation"></span><span id="eappropfragmentation"></span><span id="EAPPROPFRAGMENTATION"></span>**eapPropFragmentation**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



El método puede admitir la fragmentación y el reensamblado si los paquetes EAP superan la MTU mínima (unidad de transmisión máxima) de 1020 octetos.


</dt> </dl> </dd> <dt>

<span id="eapPropChannelBinding"></span><span id="eappropchannelbinding"></span><span id="EAPPROPCHANNELBINDING"></span>**eapPropChannelBinding**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



El método puede comunicar propiedades de canal protegidas por integridad, como identificadores de punto de conexión, que se pueden comparar con valores que se comunican mediante mecanismos fuera de banda, como [autenticación,](https://go.microsoft.com/fwlink/p/?linkid=84063) autorización y contabilidad (AAA) o el protocolo de nivel inferior.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



El método admite protección de acceso a redes (NAP).


</dt> </dl> </dd> <dt>

<span id="eapPropStandalone"></span><span id="eappropstandalone"></span><span id="EAPPROPSTANDALONE"></span>**eapPropStandalone**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



El método se puede usar en un equipo independiente.


</dt> </dl> </dd> <dt>

<span id="eapPropMppeEncryption"></span><span id="eappropmppeencryption"></span><span id="EAPPROPMPPEENCRYPTION"></span>**eapPropMppeEncryption**
</dt> <dd> <dl> <dt>

 0x00080000
</dt> <dt>



El método admite el cifrado de protocolo de cifrado de punto a punto [(MPPE) de Microsoft.](https://go.microsoft.com/fwlink/p/?linkid=83915)


</dt> </dl> </dd> <dt>

<span id="eapPropTunnelMethod"></span><span id="eapproptunnelmethod"></span><span id="EAPPROPTUNNELMETHOD"></span>**eapPropTunnelMethod**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



El método admite la tunelización de otros métodos EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropSupportsConfig"></span><span id="eappropsupportsconfig"></span><span id="EAPPROPSUPPORTSCONFIG"></span>**eapPropSupportsConfig**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



El método admite propiedades configurables y tiene una interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



El método se certificó mediante el Programa de certificación eap. Este bit solo debe enviarse mediante métodos EAP que han pasado la certificación.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 o posterior: el método se puede usar para autenticar una máquina en una red con las credenciales de las máquinas.


</dt> </dl> </dd> <dt>

<span id="eapPropUserAuth"></span><span id="eappropuserauth"></span><span id="EAPPROPUSERAUTH"></span>**eapPropUserAuth**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



Windows 7 o posterior: el método se puede usar para autenticar a un usuario en una red con las credenciales de los usuarios.


</dt> </dl> </dd> <dt>

<span id="eapPropIdentityPrivacy"></span><span id="eappropidentityprivacy"></span><span id="EAPPROPIDENTITYPRIVACY"></span>**eapPropIdentityPrivacy**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



Windows 7 o posterior: el método admite el envío de la identidad del usuario en un canal protegido.


</dt> </dl> </dd> <dt>

<span id="eapPropMethodChaining"></span><span id="eappropmethodchaining"></span><span id="EAPPROPMETHODCHAINING"></span>**eapPropMethodChaining**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Windows 7 o posterior: el método es un método tunelizado y admite el encadenamiento de métodos EAP dentro del túnel.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 o posterior: el método admite la equivalencia de estado compartido tal como se define en [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Reservado. No se usa.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Eaptypes.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Claves del Registro para métodos EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Constantes comunes de EAPHost](common-eap-host-error-constants.md)
</dt> </dl>

