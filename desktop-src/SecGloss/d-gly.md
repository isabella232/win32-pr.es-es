---
description: Contiene definiciones de términos de seguridad que comienzan por la letra D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d007cbb9-b547-4dc7-bc22-b526f650f7c2
title: D (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f81a17b2ba2c34b6d5367c1f920ad4b2a4048b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667903"
---
# <a name="d-security-glossary"></a>D (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) D [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_dac_gly"></span><span id="_SECURITY_DAC_GLY"></span>**DAC**
</dt> <dd>

Consulte *control de acceso dinámico*.

</dd> <dt>

<span id="_security_dacl_gly"></span><span id="_SECURITY_DACL_GLY"></span>**DACL**
</dt> <dd>

Vea *lista de control de acceso discrecional*.

</dd> <dt>

<span id="_security_data_content_type_gly"></span><span id="_SECURITY_DATA_CONTENT_TYPE_GLY"></span>**tipo de contenido de datos**
</dt> <dd>

Un tipo de contenido base definido por PKCS \# 7. El contenido de datos es simplemente una cadena de octeto (bytes).

</dd> <dt>

<span id="_security_data_encryption_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_GLY"></span>**cifrado de datos**
</dt> <dd>

Consulte [*cifrado*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_function_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_FUNCTION_GLY"></span>**función de cifrado de datos**
</dt> <dd>

Consulte [*funciones de cifrado y descifrado*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_standard_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_STANDARD_GLY"></span>**Estándar de cifrado de datos**
</dt> <dd>

DES Un cifrado de bloques que cifra los datos en bloques de 64 bits. DES es un algoritmo simétrico que usa el mismo algoritmo y la misma clave para el cifrado y el descifrado.

Desarrollado a comienzos de la década de 1970, DES también se conoce como DEA (algoritmo de cifrado de datos) por ANSI y DEA-1 por ISO.

</dd> <dt>

<span id="_security_datagram_gly"></span><span id="_SECURITY_DATAGRAM_GLY"></span>**diagrama**
</dt> <dd>

Un canal de comunicación que usa la información que se enruta a través de una red de conmutación de paquetes. Esta información incluye paquetes independientes de información y la información de entrega asociada a esos paquetes, como la dirección de destino. En una red de conmutación de paquetes, los paquetes de datos se enrutan de forma independiente entre sí y pueden seguir rutas diferentes. También pueden llegar en un orden diferente al del que se enviaron.

</dd> <dt>

<span id="_security_decoding_gly"></span><span id="_SECURITY_DECODING_GLY"></span>**descodificación**
</dt> <dd>

Proceso de traducir un objeto codificado (como un certificado) o datos de nuevo a su formato original.

En términos generales, el nivel de codificación y descodificación del Protocolo de comunicación descodifica los datos. Los certificados se descodifican mediante una llamada a la función **CryptDecodeObject** .

</dd> <dt>

<span id="_security_decryption_gly"></span><span id="_SECURITY_DECRYPTION_GLY"></span>**descifrado**
</dt> <dd>

Proceso de convertir texto cifrado en texto no cifrado. El descifrado es lo contrario del cifrado.

</dd> <dt>

<span id="_security_default_mode_gly"></span><span id="_SECURITY_DEFAULT_MODE_GLY"></span>**modo predeterminado**
</dt> <dd>

Configuración predeterminada, como el modo de cifrado de cifrado de bloqueo o el método de relleno de cifrado de bloque.

</dd> <dt>

<span id="_security_der_gly"></span><span id="_SECURITY_DER_GLY"></span>**DER**
</dt> <dd>

Vea *reglas de codificación distinguida*.

</dd> <dt>

<span id="_security_derived_key_gly"></span><span id="_SECURITY_DERIVED_KEY_GLY"></span>**clave derivada**
</dt> <dd>

Una clave criptográfica creada mediante una llamada a la función **CryptDeriveKey** . Una clave derivada se puede crear a partir de una contraseña o de cualquier otro dato de usuario. Las claves derivadas permiten a las aplicaciones crear claves de sesión según sea necesario, lo que elimina la necesidad de almacenar una clave determinada.

</dd> <dt>

<span id="_security_des_gly"></span><span id="_SECURITY_DES_GLY"></span>**DES**
</dt> <dd>

Consulte *estándar de cifrado de datos*.

</dd> <dt>

<span id="_security_dh_gly"></span><span id="_SECURITY_DH_GLY"></span>**DH**
</dt> <dd>

Vea *algoritmo de Diffie-Hellman*.

</dd> <dt>

<span id="_security_dh_keyx_gly"></span><span id="_SECURITY_DH_KEYX_GLY"></span>**\_KEYX DH**
</dt> <dd>

El nombre del algoritmo de CryptoAPI para el algoritmo de intercambio de claves de Diffie-Hellman.

Vea también *algoritmo Diffie-Hellman*.

</dd> <dt>

<span id="_security_diffie_hellman_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_ALGORITHM_GLY"></span>**Algoritmo Diffie-Hellman**
</dt> <dd>

DH Algoritmo de clave pública que se usa para el intercambio de claves seguro. No se puede usar Diffie-Hellman para el cifrado de datos. Este algoritmo se especifica como el algoritmo de intercambio de claves para los tipos de proveedor de PROV \_ DSS \_ DH.

Vea también *Diffie-Hellman (almacenar y reenviar) el algoritmo de intercambio de claves* y el *algoritmo de intercambio de claves Diffie-Hellman (efímero)*.

</dd> <dt>

<span id="_security_diffie_hellman_store_and_forward_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_STORE_AND_FORWARD_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algoritmo de intercambio de claves Diffie-Hellman (almacenamiento y reenvío)**
</dt> <dd>

Un algoritmo de Diffie-Hellman en el que se conservan los valores de clave de intercambio (en el CSP) después de que se haya destruido el identificador de clave.

Vea también *algoritmo de intercambio de claves Diffie-Hellman (efímero)*.

</dd> <dt>

<span id="_security_diffie_hellman_ephemeral_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_EPHEMERAL_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algoritmo de intercambio de claves Diffie-Hellman (efímero)**
</dt> <dd>

Diffie-Hellman algoritmo en el que el valor de clave de intercambio se elimina del CSP cuando se destruye el identificador de clave.

Vea también *el algoritmo de intercambio de claves Diffie-Hellman (almacenamiento y reenvío)*.

</dd> <dt>

<span id="_security_digested_data_gly"></span><span id="_SECURITY_DIGESTED_DATA_GLY"></span>**datos de síntesis**
</dt> <dd>

Un tipo de contenido de datos definido por PKCS \# 7 que consta de cualquier tipo de datos más un hash de mensaje (síntesis) del contenido.

</dd> <dt>

<span id="_security_digital_certificate_gly"></span><span id="_SECURITY_DIGITAL_CERTIFICATE_GLY"></span>**certificado digital**
</dt> <dd>

Vea [*certificado*](c-gly.md).

</dd> <dt>

<span id="_security_digital_envelope_gly"></span><span id="_SECURITY_DIGITAL_ENVELOPE_GLY"></span>**sobre digital**
</dt> <dd>

Mensajes privados cifrados mediante la clave pública del destinatario. Los mensajes con doble cifrado solo se pueden descifrar mediante la clave privada del destinatario, lo que permite que solo el destinatario entienda el mensaje.

</dd> <dt>

<span id="_security_digital_signature_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_GLY"></span>**firma digital**
</dt> <dd>

Datos que enlazan la identidad de un remitente con la información que se está enviando. Una firma digital se puede empaquetar junto con cualquier mensaje, archivo o cualquier otra información codificada o transmitida por separado. Las firmas digitales se utilizan en entornos de claves públicas y proporcionan servicios de integridad y autenticación.

</dd> <dt>

<span id="_security_digital_signature_algorithm_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_ALGORITHM_GLY"></span>**Algoritmo de firma digital**
</dt> <dd>

ALGORITMO Algoritmo de clave pública especificado por el estándar de firma digital (DSS). DSA solo se usa para generar firmas digitales. No se puede usar para el cifrado de datos.

</dd> <dt>

<span id="_security_digital_signature_key_pair_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_KEY_PAIR_GLY"></span>**par de claves de firma digital**
</dt> <dd>

Vea [*par de claves de firma*](s-gly.md).

</dd> <dt>

<span id="_security_digital_signature_standard_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_STANDARD_GLY"></span>**Firma digital estándar**
</dt> <dd>

DSS Estándar que especifica el algoritmo de firma digital (DSA) para el algoritmo de firma y SHA-1 como algoritmo hash de mensaje. DSA es un cifrado de clave pública que solo se usa para generar firmas digitales y no se puede usar para el cifrado de datos. DSS se especifica mediante los \_ tipos de proveedor de DSS DSS, Prov \_ DSS \_ DH y Prov \_ Fortezza.

</dd> <dt>

<span id="_security_discretionary_access_control_list_gly"></span><span id="_SECURITY_DISCRETIONARY_ACCESS_CONTROL_LIST_GLY"></span>**lista de control de acceso discrecional**
</dt> <dd>

DACL Una lista de control de acceso controlada por el propietario de un objeto y que especifica el acceso que los usuarios o grupos concretos pueden tener al objeto.

Consulte también [*lista de control de acceso*](a-gly.md) y [*lista de control de acceso del sistema*](s-gly.md).

</dd> <dt>

<span id="_security_distinguished_encoding_rules_gly"></span><span id="_SECURITY_DISTINGUISHED_ENCODING_RULES_GLY"></span>**reglas de codificación distinguida**
</dt> <dd>

DER Conjunto de reglas para codificar los datos definidos por ASN. 1 como una secuencia de bits para la transmisión o el almacenamiento externo. Cada objeto ASN. 1 tiene exactamente una codificación DER correspondiente. DER se define en la recomendación de CCITt X. 509, sección 8,7. Éste es uno de los dos métodos de codificación que usa actualmente CryptoAPI.

</dd> <dt>

<span id="_security_dll_gly"></span><span id="_SECURITY_DLL_GLY"></span>**DLL**
</dt> <dd>

Vea *biblioteca de vínculos dinámicos*.

</dd> <dt>

<span id="_security_dsa_gly"></span><span id="_SECURITY_DSA_GLY"></span>**ALGORITMO**
</dt> <dd>

Vea *algoritmo de firma digital*.

</dd> <dt>

<span id="_security_dss_gly"></span><span id="_SECURITY_DSS_GLY"></span>**DSS**
</dt> <dd>

Consulte *estándar de firma digital*.

</dd> <dt>

<span id="_security_dynamic_access_control_gly"></span><span id="_SECURITY_DYNAMIC_ACCESS_CONTROL_GLY"></span>**Access Control dinámico**
</dt> <dd>

DAC La capacidad de especificar directivas de control de acceso basadas en notificaciones de usuario, dispositivo y recursos. Esto hace que la autenticación sea más flexible para las aplicaciones, a la vez que mantiene los requisitos de seguridad y cumplimiento.

</dd> <dt>

<span id="_security_dynamic_link_library_gly"></span><span id="_SECURITY_DYNAMIC_LINK_LIBRARY_GLY"></span>**Biblioteca de vínculos dinámicos**
</dt> <dd>

(DLL) archivo que contiene rutinas ejecutables a las que se puede llamar desde otras aplicaciones.

</dd> </dl>

 

 



