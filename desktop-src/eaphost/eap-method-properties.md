---
title: Propiedades del método EAP (Eaptypes. h)
description: Lo usan los suplicantes y los autenticadores para determinar los métodos EAP que se van a usar con un solicitante o autenticador determinados. Las propiedades de método también especifican la configuración de un método.
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
ms.openlocfilehash: 844f897456ee21dfa93dfaa5b16b4f218ba5efb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802534"
---
# <a name="eap-method-properties"></a>Propiedades del método EAP

Lo usan los suplicantes y los autenticadores para determinar los métodos EAP que se van a usar con un solicitante o autenticador determinados. Las propiedades de método también especifican la configuración de un método.

Por ejemplo, el suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) puede requerir que los métodos tengan determinadas propiedades para su uso con el suplicante [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) . El material de creación de claves, por ejemplo, es un requisito.

Se enumeran las propiedades que admiten los métodos EAP. Las propiedades se almacenan como valores de clave del registro. Para obtener más información, consulte la sección clave del registro de la DLL del método EAP peer del tema [configuración del registro para los métodos EAP.](registry-keys-for-eap-methods.md)

<dl> <dt>

<span id="eapPropCipherSuiteNegotiation"></span><span id="eappropciphersuitenegotiation"></span><span id="EAPPROPCIPHERSUITENEGOTIATION"></span>**eapPropCipherSuiteNegotiation**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



El método permite negociar el conjunto de cifrado con el fin de cifrar los datos. Windows Server 2008 admite los siguientes [conjuntos de cifrado](/windows/desktop/SecAuthN/tls-cipher-suites)3DES:

-   TLS \_ RSA \_ con \_ 3DES \_ Ede \_ CBC \_ Sha (TLS & SSL 3)
-   TLS \_ DHE \_ DSS \_ con \_ 3DES \_ EDE \_ CBC \_ Sha (TLS & SSL 3)
-   SSL \_ CK \_ des \_ 192 \_ EDE3 \_ CBC \_ con \_ MD5 (SSL 2 Si está habilitado)

Para obtener más información acerca del Protocolo de seguridad TLS 1,0, consulte [RFC 2246](https://go.microsoft.com/fwlink/p/?linkid=84035).


</dt> </dl> </dd> <dt>

<span id="eapPropMutualAuth"></span><span id="eappropmutualauth"></span><span id="EAPPROPMUTUALAUTH"></span>**eapPropMutualAuth**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



El método proporciona un intercambio, en el que el autenticador autentica al par y viceversa.


</dt> </dl> </dd> <dt>

<span id="eapPropIntegrity"></span><span id="eappropintegrity"></span><span id="EAPPROPINTEGRITY"></span>**eapPropIntegrity**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



El método proporciona la autenticación del origen de datos y la protección contra la modificación no autorizada de la información de los paquetes EAP, incluidas las solicitudes EAP y las respuestas. Al efectuar esta declaración, una especificación de método debe especificar los paquetes EAP protegidos y los campos protegidos dentro de los paquetes EAP.


</dt> </dl> </dd> <dt>

<span id="eapPropReplayProtection"></span><span id="eappropreplayprotection"></span><span id="EAPPROPREPLAYPROTECTION"></span>**eapPropReplayProtection**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



El método puede protegerse frente a la reproducción de un método EAP o de sus mensajes. No se pueden reproducir las indicaciones de los resultados correctos y erróneos.


</dt> </dl> </dd> <dt>

<span id="eapPropConfidentiality"></span><span id="eappropconfidentiality"></span><span id="EAPPROPCONFIDENTIALITY"></span>**eapPropConfidentiality**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



El método puede cifrar los mensajes EAP. Se cifran las solicitudes de EAP, las respuestas de EAP, las indicaciones de resultados correctos y las indicaciones de resultados de error. Un método que realiza esta demanda debe admitir Identity Protection.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyDerivation"></span><span id="eappropkeyderivation"></span><span id="EAPPROPKEYDERIVATION"></span>**eapPropKeyDerivation**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



El método puede derivar material de creación de claves exportable, como la clave de sesión maestra (MSK) y la clave de sesión maestra extendida (EMSK). El MSK solo se usa para la derivación de claves adicionales, no directamente para la protección de la conversación EAP o los datos subsiguientes. El uso de EMSK está reservado.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength64"></span><span id="eappropkeystrength64"></span><span id="EAPPROPKEYSTRENGTH64"></span>**eapPropKeyStrength64**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



La longitud de clave mínima admitida por el método EAP es 64 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength128"></span><span id="eappropkeystrength128"></span><span id="EAPPROPKEYSTRENGTH128"></span>**eapPropKeyStrength128**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



La longitud de clave mínima admitida por el método EAP es 128 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength256"></span><span id="eappropkeystrength256"></span><span id="EAPPROPKEYSTRENGTH256"></span>**eapPropKeyStrength256**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



La longitud de clave mínima admitida por el método EAP es 256 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength512"></span><span id="eappropkeystrength512"></span><span id="EAPPROPKEYSTRENGTH512"></span>**eapPropKeyStrength512**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



La longitud de clave mínima admitida por el método EAP es 512 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropKeyStrength1024"></span><span id="eappropkeystrength1024"></span><span id="EAPPROPKEYSTRENGTH1024"></span>**eapPropKeyStrength1024**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



La longitud de clave mínima admitida por el método EAP es 1024 bits.


</dt> </dl> </dd> <dt>

<span id="eapPropDictionaryAttackResistance"></span><span id="eappropdictionaryattackresistance"></span><span id="EAPPROPDICTIONARYATTACKRESISTANCE"></span>**eapPropDictionaryAttackResistance**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



El método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas en el Diccionario de un atacante. En los casos en que se usa la autenticación de contraseña, las contraseñas se seleccionan normalmente a partir de un conjunto pequeño (en comparación con un conjunto de claves de N bits), lo que supone un problema sobre los ataques de diccionario. Se puede decir que un método proporciona protección contra ataques de diccionario si, cuando utiliza una contraseña como secreto, el método no permite un ataque sin conexión que tenga un factor de trabajo basado en el número de contraseñas en el Diccionario de un atacante.


</dt> </dl> </dd> <dt>

<span id="eapPropFastReconnect"></span><span id="eappropfastreconnect"></span><span id="EAPPROPFASTRECONNECT"></span>**eapPropFastReconnect**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



El método tiene la capacidad, en el caso de que se haya establecido previamente una asociación de seguridad, para crear una asociación de seguridad nueva o actualizada de forma más eficaz o en un número menor de recorridos de ida y vuelta.


</dt> </dl> </dd> <dt>

<span id="eapPropCryptoBinding"></span><span id="eappropcryptobinding"></span><span id="EAPPROPCRYPTOBINDING"></span>**eapPropCryptoBinding**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



El método muestra al servidor EAP que una sola entidad ha actuado como EAP del mismo nivel para todos los métodos que se ejecutan dentro de un método de túnel. El enlace también puede implicar que el servidor EAP muestra al sistema del mismo nivel que una sola entidad ha actuado como el servidor EAP para todos los métodos que se ejecutan dentro de un método de túnel. Si se ejecuta correctamente, el enlace sirve para mitigar las vulnerabilidades de tipo "Man in the Middle".


</dt> </dl> </dd> <dt>

<span id="eapPropSessionIndependence"></span><span id="eappropsessionindependence"></span><span id="EAPPROPSESSIONINDEPENDENCE"></span>**eapPropSessionIndependence**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



El método demuestra que los ataques pasivos (por ejemplo, la captura de la conversación EAP) o los ataques activos (incluido el riesgo de la MSK o EMSK) no ponen en peligro la MSKs o la EMSKs anterior o posterior.


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



El método puede comunicar propiedades de canal protegidas por integridad, como identificadores de punto de conexión, que se pueden comparar con valores comunicados mediante mecanismos fuera de banda, como la [autenticación, autorización y cuentas](https://go.microsoft.com/fwlink/p/?linkid=84063) (AAA) o el protocolo de nivel inferior.


</dt> </dl> </dd> <dt>

<span id="eapPropNap"></span><span id="eappropnap"></span><span id="EAPPROPNAP"></span>**eapPropNap**
</dt> <dd> <dl> <dt>

 0x00020000
</dt> <dt>



El método es compatible con la protección de acceso a redes (NAP).


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



El método admite el cifrado [de protocolo MPPE (cifrado punto a punto de Microsoft)](https://go.microsoft.com/fwlink/p/?linkid=83915) .


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



El método admite las propiedades configurables y tiene una interfaz de usuario.


</dt> </dl> </dd> <dt>

<span id="eapPropCertifiedMethod"></span><span id="eappropcertifiedmethod"></span><span id="EAPPROPCERTIFIEDMETHOD"></span>**eapPropCertifiedMethod**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



El método estaba certificado por el programa de Certificación EAP. Este bit solo debe ser enviado por métodos EAP que hayan pasado la certificación.


</dt> </dl> </dd> <dt>

<span id="eapPropmachineAuth"></span><span id="eappropmachineauth"></span><span id="EAPPROPMACHINEAUTH"></span>**eapPropmachineAuth**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Windows 7 o posterior: el método se puede usar para autenticar un equipo en una red con las credenciales de los equipos.


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



Windows 7 o posterior: el método es un método de túnel y admite el encadenamiento de métodos EAP dentro del túnel.


</dt> </dl> </dd> <dt>

<span id="eapPropSharedStateEquivalence"></span><span id="eappropsharedstateequivalence"></span><span id="EAPPROPSHAREDSTATEEQUIVALENCE"></span>**eapPropSharedStateEquivalence**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Windows 7 o posterior: el método admite la equivalencia de estado compartida tal y como se define en [RFC 4017](https://go.microsoft.com/fwlink/p/?linkid=90455).


</dt> </dl> </dd> <dt>

<span id="eapPropReserved"></span><span id="eappropreserved"></span><span id="EAPPROPRESERVED"></span>**eapPropReserved**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Reservado. No se utiliza.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Eaptypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Claves del registro para los métodos EAP](registry-keys-for-eap-methods.md)
</dt> <dt>

[Constantes de EAPHost comunes](common-eap-host-error-constants.md)
</dt> </dl>

