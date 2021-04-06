---
description: Contiene definiciones de términos de seguridad que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911249"
---
# <a name="p-security-glossary"></a>P (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) p Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**acolcha**
</dt> <dd>

Cadena que se suele agregar cuando el último bloque de texto simple es corto. Por ejemplo, si la longitud del bloque es de 64 bits y el último bloque contiene solo 40 bits, se deben agregar 24 bits de relleno al último bloque. La cadena de relleno puede contener ceros, alternar ceros y otros, o algún otro patrón. Las aplicaciones que usan [*CryptoAPI*](c-gly.md) no necesitan agregar relleno a su texto no cifrado antes de que se cifren, ni tampoco deben quitarlo después del descifrado. Esto se controla automáticamente.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro de contraseñas**
</dt> <dd>

Un archivo DLL que proporciona la aplicación de la Directiva de contraseñas y la notificación de cambios. La [*autoridad de seguridad local*](l-gly.md)llama a las funciones implementadas por los filtros de contraseña.

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**almacenamiento persistente**
</dt> <dd>

Cualquier medio de almacenamiento que permanezca intacto cuando se desconecte la alimentación. Muchas bases de datos del [*almacén de certificados*](c-gly.md) son formas de almacenamiento persistente.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**
</dt> <dd>

Consulte *estándares de criptografía de clave pública*.

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Los estándares recomendados para la implementación de la criptografía de clave pública basada en el algoritmo de RSA, tal como se define en [RFC 3447](https://tools.ietf.org/html/rfc3447).

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

Estándar de sintaxis de intercambio de información personal, desarrollado y mantenido por RSA Data Security, Inc. Este estándar de sintaxis especifica un formato portátil para almacenar o transportar claves privadas, certificados y secretos distintos de un usuario.

Vea también estándares de *criptografía de clave pública* y [*certificado*](c-gly.md) .

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Datos firmados PKCS 7**
</dt> <dd>

Un objeto de datos que se firma con el estándar de criptografía de clave pública \# 7 (PKCS \# 7) y que encapsula la información utilizada para firmar un archivo. Normalmente, incluye el certificado del firmante y el [*certificado raíz*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

Estándar de sintaxis de mensajes criptográficos. Una sintaxis general para los datos a los que se puede aplicar la criptografía, como cifrado y firmas digitales. También proporciona una sintaxis para la diseminación de certificados o listas de revocación de certificados y otros atributos de mensajes, como las marcas de tiempo, al mensaje.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**CODIFICACIÓN de ASN de PKCS \_ 7 \_ \_**
</dt> <dd>

[*Tipo de codificación de mensajes*](m-gly.md). Los tipos de codificación de mensajes se almacenan en la palabra de orden superior de un **DWORD** (el valor es: 0x00010000).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**texto**
</dt> <dd>

Un mensaje no cifrado. Los mensajes de texto simple se conocen a veces como mensajes texto sin cifrar.

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Imagen ejecutable portable (PE)**
</dt> <dd>

Formato de archivo ejecutable de Windows estándar.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**FICHERO**
</dt> <dd>

Vea *función pseudoaleatorios*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenciales principales**
</dt> <dd>

El \_ paquete de autenticación MsV1 0 define un valor de cadena de clave de credencial principal: la cadena de credenciales principal contiene las credenciales proporcionadas en la hora de inicio de sesión inicial. Incluye el nombre de usuario y las formas con distinción de mayúsculas y minúsculas y sin distinción de mayúsculas y minúsculas de la contraseña del usuario.

Vea también [*credenciales adicionales*](s-gly.md).

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**proveedor de servicios principal**
</dt> <dd>

Proveedor de servicios que proporciona las interfaces de control a la tarjeta. Cada tarjeta inteligente puede registrar su proveedor de servicios principal en la base de datos de tarjetas inteligentes.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token principal**
</dt> <dd>

Un token de acceso que normalmente solo crea el kernel de Windows. Se puede asignar a un proceso para representar la información de seguridad predeterminada para ese proceso.

Vea también token de [*acceso*](a-gly.md) y [*token de suplantación*](i-gly.md).

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**entidad**
</dt> <dd>

Consulte [*entidad de seguridad*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**Service**
</dt> <dd>

Condición de estar aislada de la vista o el secreto. Con respecto a los mensajes, los mensajes privados son mensajes cifrados cuyo texto está oculto en la vista. Con respecto a las claves, una clave privada es una clave secreta oculta de otras.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**clave privada**
</dt> <dd>

La mitad secreta de un par de claves usado en un algoritmo de clave pública. Las claves privadas se utilizan normalmente para cifrar una clave de sesión simétrica, firmar digitalmente un mensaje o descifrar un mensaje cifrado con la clave pública correspondiente.

Vea también *clave pública*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de clave privada**
</dt> <dd>

Un BLOB de clave que contiene un par de claves pública y privada completo. Los programas administrativos usan blobs de clave privada para transportar pares de claves. Como la parte de la clave privada del par de claves es extremadamente confidencial, estos blobs se suelen mantener cifrados con un cifrado simétrico. Estos blobs de clave también pueden usarse en aplicaciones avanzadas en las que los pares de claves se almacenan dentro de la aplicación, en lugar de depender del mecanismo de almacenamiento del CSP. Un BLOB de clave se crea mediante una llamada a la función **CryptExportKey** .

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilegia**
</dt> <dd>

El derecho de un usuario para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar los controles de dispositivos o cambiar la hora del sistema. El token de acceso de un usuario contiene una lista de los privilegios que mantiene el usuario o los grupos del usuario.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**Procese**
</dt> <dd>

El contexto de seguridad bajo el que se ejecuta una aplicación. Normalmente, el contexto de seguridad está asociado a un usuario, por lo que todas las aplicaciones que se ejecutan bajo un proceso determinado toman los permisos y privilegios del usuario propietario.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**DSS de PROV \_**
</dt> <dd>

Consulte *el \_ tipo de proveedor de DSS de Prov*.

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de DSS de PROV \_**
</dt> <dd>

Tipo de proveedor predefinido que solo admite firmas y hashes digitales. Especifica el algoritmo de firma de DSA y los algoritmos hash MD5 y SHA-1.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**de PROV \_ DSS \_ DH**
</dt> <dd>

Consulte *\_ tipo de \_ proveedor de la DSS DSS de Prov*.

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo de proveedor de DSS DSS \_ DH**
</dt> <dd>

Tipo de proveedor predefinido que proporciona intercambio de claves, firma digital y algoritmos hash. Es similar al tipo de proveedor de DSS de PROV \_ .

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**Fortezza de PROV \_**
</dt> <dd>

Vea *\_ tipo de proveedor de Fortezza de Prov*.

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de Fortezza de PROV \_**
</dt> <dd>

Tipo de proveedor predefinido que proporciona intercambio de claves, firma digital, cifrado y algoritmos hash. Los protocolos criptográficos y los algoritmos especificados por este tipo de proveedor pertenecen al National Institute of Standards and Technology (NIST).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**\_Microsoft \_ Exchange**
</dt> <dd>

Consulte *\_ tipo de \_ proveedor de Microsoft Exchange*.

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ proveedor de Microsoft Exchange**
</dt> <dd>

Tipo de proveedor predefinido diseñado para las necesidades de Microsoft Exchange, así como otras aplicaciones compatibles con Microsoft Mail. Proporciona intercambio de claves, firma digital, cifrado y algoritmos hash.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**aprovisionamiento \_ completo de RSA \_**
</dt> <dd>

Consulte *el \_ \_ tipo de proveedor completo RSA*.

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ proveedor completo RSA de Prov**
</dt> <dd>

Tipo de proveedor predefinido definido por Microsoft y RSA Data Security, Inc. Este tipo de proveedor de uso general proporciona intercambio de claves, firma digital, cifrado y algoritmos hash. El intercambio de claves, la firma digital y los algoritmos de cifrado se basan en la criptografía de clave pública RSA.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**\_firma RSA \_ SIG**
</dt> <dd>

Consulte *\_ tipo de \_ proveedor de RSA SIG de Prov*.

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo de proveedor de RSA SIG de Prov \_**
</dt> <dd>

Tipo de proveedor predefinido definido por Microsoft y RSA Data Security. Este tipo de proveedor es un subconjunto de aprovisionamiento de \_ RSA \_ completo que proporciona solo algoritmos de firma digital y hash. El algoritmo de firma digital es un algoritmo de clave pública RSA.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**SSL de PROV \_**
</dt> <dd>

Vea *\_ tipo de proveedor de SSL de Prov*.

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de SSL de PROV \_**
</dt> <dd>

Tipo de proveedor predefinido que admite el protocolo Capa de sockets seguros (SSL). Este tipo proporciona cifrado de claves, firma digital, cifrado y algoritmos hash. Una especificación que explica SSL está disponible en Netscape Communications Corp.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**presta**
</dt> <dd>

Vea [*proveedor de servicios de cifrado*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nombre del proveedor**
</dt> <dd>

Nombre usado para identificar un CSP. Por ejemplo, la versión 1,0 del proveedor de servicios criptográficos básicos de Microsoft. Normalmente, el nombre del proveedor se usa al llamar a la función **CryptAcquireContext** para conectarse a un CSP.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo de proveedor**
</dt> <dd>

Término usado para identificar un tipo de proveedor de servicios criptográficos (CSP). Los CSP se agrupan en diferentes tipos de proveedor que representan una familia específica de protocolos y formatos de datos estándar. A diferencia del nombre de proveedor único de un CSP, los tipos de proveedor no son únicos para un CSP determinado. Normalmente, el tipo de proveedor se usa al llamar a la función **CryptAcquireContext** para conectarse a un CSP.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**función pseudoaleatorios**
</dt> <dd>

FICHERO Una función que toma una clave, una etiqueta y una inicialización como entrada y, a continuación, genera una salida de longitud arbitraria.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**par de claves pública y privada**
</dt> <dd>

Un conjunto de claves criptográficas utilizado para la criptografía de clave pública. Para cada usuario, un CSP normalmente mantiene dos pares de claves pública y privada: un par de claves de intercambio y un par de claves de firma digital. Ambos pares de claves se mantienen de una sesión a otra.

Consulte par de claves de [*Exchange*](e-gly.md) y par de [*claves de firma*](s-gly.md).

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**clave pública**
</dt> <dd>

Una clave criptográfica utilizada normalmente al descifrar una clave de sesión o una firma digital. La clave pública también se puede utilizar para cifrar un mensaje, garantizando que solo la persona con la clave privada correspondiente puede descifrar el mensaje.

Vea también *clave privada*.

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo de clave pública**
</dt> <dd>

Cifrado asimétrico que usa dos claves, una para el cifrado, la clave pública y la otra para el descifrado, la clave privada. Como se trata de los nombres de clave, la clave pública que se usa para codificar texto no cifrado puede ponerse a disposición de cualquier usuario. Sin embargo, la clave privada debe permanecer secreta. Solo la clave privada puede descifrar el texto cifrado. El algoritmo de clave pública que se usa en este proceso es lento (en el orden de 1.000 veces más lento que los algoritmos simétricos) y normalmente se usa para cifrar las claves de sesión o firmar digitalmente un mensaje.

Vea también *clave pública* y *clave privada*.

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB de clave pública**
</dt> <dd>

Un BLOB que se usa para almacenar la parte de la clave pública de un par de claves pública y privada. Los blobs de clave pública no se cifran, ya que la clave pública incluida en no es secreta. Un BLOB de clave pública se crea mediante una llamada a la función **CryptExportKey** .

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Estándares de criptografía de clave pública**
</dt> <dd>

PKCS Un conjunto de estándares de sintaxis para la criptografía de clave pública que abarca las funciones de seguridad, incluidos los métodos para firmar datos, el intercambio de claves, la solicitud de certificados, el cifrado y descifrado de claves públicas y otras funciones de seguridad.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**cifrado de clave pública**
</dt> <dd>

Cifrado que utiliza un par de claves, una clave para cifrar los datos y la otra clave para descifrar los datos. Por el contrario, los algoritmos de cifrado simétricos usan la misma clave para cifrado y descifrado. En la práctica, la criptografía de clave pública se usa normalmente para proteger la clave de sesión utilizada por un algoritmo de cifrado simétrico. En este caso, la clave pública se utiliza para cifrar la clave de sesión, que, a su vez, fue utilizada para cifrar algunos datos, y la clave privada se utiliza para el descifrado. Además de para proteger las claves de sesión, la criptografía de clave pública también se puede utilizar para firmar digitalmente un mensaje (mediante la clave privada) y validar la firma (mediante la clave pública).

Vea también *algoritmo de clave pública*.

</dd> </dl>

 

 



