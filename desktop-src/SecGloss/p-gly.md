---
description: Contiene definiciones de términos de seguridad que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea06fef6f39c1cbee3adbb8f53870013da9cec52cceef6e318e679af42fd37ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117969963"
---
# <a name="p-security-glossary"></a>P (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](g-gly.md) [](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L M](l-gly.md) [N](m-gly.md) [O](n-gly.md) [](o-gly.md) P P [Q R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**Acolchado**
</dt> <dd>

Cadena que se suele agregar cuando el último bloque de texto simple es corto. Por ejemplo, si la longitud del bloque es de 64 bits y el último bloque solo contiene 40 bits, se deben agregar 24 bits de relleno al último bloque. La cadena de relleno puede contener ceros, ceros y unos alternos, o algún otro patrón. Las aplicaciones que [*usan CryptoAPI*](c-gly.md) no necesitan agregar relleno a su texto sin formato antes de cifrarse, ni tienen que quitarlo después de descifrarlo. Todo esto se controla automáticamente.

</dd> <dt>

<span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro de contraseña**
</dt> <dd>

Un archivo DLL que proporciona la aplicación de directivas de contraseñas y la notificación de cambio. La autoridad de seguridad local llama a las funciones implementadas por los filtros [*de contraseña.*](l-gly.md)

</dd> <dt>

<span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**almacenamiento persistente**
</dt> <dd>

Cualquier medio de almacenamiento que permanezca intacto cuando se desconecte la alimentación. Muchas bases [*de datos de almacén*](c-gly.md) de certificados son formas de almacenamiento persistente.

</dd> <dt>

<span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**Pkcs**
</dt> <dd>

Vea Public Key Cryptography Standards ( *Estándares de criptografía de clave pública).*

</dd> <dt>

<span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**
</dt> <dd>

Los estándares recomendados para la implementación de criptografía de clave pública basada en el algoritmo RSA, tal como se define [en RFC 3447](https://tools.ietf.org/html/rfc3447).

</dd> <dt>

<span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**
</dt> <dd>

El estándar de sintaxis Exchange personal, desarrollado y mantenido por RSA Data Security, Inc. Este estándar de sintaxis especifica un formato portátil para almacenar o transportar claves privadas, certificados y secretos varios de un usuario.

Vea también [*certificate and*](c-gly.md) Public Key Cryptography Standards ( *Estándares de criptografía de clave pública y certificado).*

</dd> <dt>

<span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**Datos firmados de PKCS \# 7**
</dt> <dd>

Objeto de datos firmado con public Key Cryptography Standard \# 7 (PKCS 7) y que encapsula la información utilizada para \# firmar un archivo. Normalmente, incluye el certificado del firmante y el [*certificado raíz*](r-gly.md).

</dd> <dt>

<span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**
</dt> <dd>

Estándar de sintaxis de mensajes criptográficos. Una sintaxis general para los datos a los que se puede aplicar la criptografía, como cifrado y firmas digitales. También proporciona una sintaxis para la difusión de certificados o listas de revocación de certificados y otros atributos de mensaje, como marcas de tiempo, al mensaje.

</dd> <dt>

<span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**CODIFICACIÓN DE \_ \_ ASN PKCS 7 \_**
</dt> <dd>

Tipo [*de codificación de mensajes*](m-gly.md). Los tipos de codificación de mensajes se almacenan en la palabra de orden superior de **un DWORD** (el valor es: 0x00010000).

</dd> <dt>

<span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**Plaintext**
</dt> <dd>

Un mensaje no cifrado. Los mensajes de texto simple se conocen a veces como mensajes texto sin cifrar.

</dd> <dt>

<span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Imagen portable ejecutable (PE)**
</dt> <dd>

El formato Windows ejecutable estándar.

</dd> <dt>

<span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**Prf**
</dt> <dd>

Vea *Pseudo-Random Function*.

</dd> <dt>

<span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenciales principales**
</dt> <dd>

El paquete de autenticación MsV1 0 define un valor de cadena de clave de credencial principal: la cadena de credenciales principales contiene las credenciales proporcionadas en el momento del inicio \_ de sesión inicial. Incluye el nombre de usuario y las formas que distinguen mayúsculas de minúsculas y no distinguen mayúsculas de minúsculas de la contraseña del usuario.

Consulte también [*las credenciales complementarias.*](s-gly.md)

</dd> <dt>

<span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**proveedor de servicios principal**
</dt> <dd>

Proveedor de servicios que proporciona las interfaces de control a la tarjeta. Cada tarjeta inteligente puede registrar su proveedor de servicios principal en la base de datos de tarjeta inteligente.

</dd> <dt>

<span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token principal**
</dt> <dd>

Token de acceso que normalmente solo crea el Windows kernel. Se puede asignar a un proceso para representar la información de seguridad predeterminada para ese proceso.

Consulte también [*token de acceso*](a-gly.md) y token de [*suplantación.*](i-gly.md)

</dd> <dt>

<span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**entidad de seguridad**
</dt> <dd>

Consulte la [*entidad de seguridad*](s-gly.md).

</dd> <dt>

<span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**Privacidad**
</dt> <dd>

La condición de estar aislado de la vista o el secreto. Con respecto a los mensajes, los mensajes privados son mensajes cifrados cuyo texto está oculto de la vista. Con respecto a las claves, una clave privada es una clave secreta oculta de otras.

</dd> <dt>

<span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**clave privada**
</dt> <dd>

La mitad secreta de un par de claves usado en un algoritmo de clave pública. Las claves privadas se utilizan normalmente para cifrar una clave de sesión simétrica, firmar digitalmente un mensaje o descifrar un mensaje cifrado con la clave pública correspondiente.

Consulte también *clave pública*.

</dd> <dt>

<span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**
</dt> <dd>

Blob de clave que contiene un par de claves pública y privada completo. Los programas administrativos usan blobs de clave privada para transportar pares de claves. Como la parte de clave privada del par de claves es extremadamente confidencial, estos BLOB normalmente se mantienen cifrados con un cifrado simétrico. Estas blobs clave también se pueden usar en aplicaciones avanzadas donde los pares de claves se almacenan dentro de la aplicación, en lugar de depender del mecanismo de almacenamiento del CSP. Se crea un blob de clave mediante una llamada a **la función CryptExportKey.**

</dd> <dt>

<span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**Privilegio**
</dt> <dd>

El derecho de un usuario para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar los controles de dispositivos o cambiar la hora del sistema. El token de acceso de un usuario contiene una lista de los privilegios que tiene el usuario o los grupos del usuario.

</dd> <dt>

<span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**Proceso**
</dt> <dd>

El contexto de seguridad bajo el que se ejecuta una aplicación. Normalmente, el contexto de seguridad está asociado a un usuario, por lo que todas las aplicaciones que se ejecutan bajo un proceso determinado toman los permisos y privilegios del usuario propietario.

</dd> <dt>

<span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV \_ DSS**
</dt> <dd>

Vea *Prov DSS provider type (Tipo de proveedor de \_ DSS de PROV).*

</dd> <dt>

<span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ de DSS prov**
</dt> <dd>

Tipo de proveedor predefinido que solo admite firmas digitales y hashes. Especifica el algoritmo de firma DSA y los algoritmos hash MD5 y SHA-1.

</dd> <dt>

<span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV \_ DSS \_ DH**
</dt> <dd>

Vea *PROV DSS DH provider type (Tipo \_ de proveedor de \_ DSS DH de PROV).*

</dd> <dt>

<span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ DSS DH de PROV \_**
</dt> <dd>

Tipo de proveedor predefinido que proporciona algoritmos hash, firma digital y intercambio de claves. Es similar al tipo de proveedor \_ de DSS de PROV.

</dd> <dt>

<span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV \_ FORTEZZA**
</dt> <dd>

Vea *PROV FORTEZZA provider type (Tipo de proveedor de \_ PROV FORTEZZA).*

</dd> <dt>

<span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ DE PROV FORTEZZA**
</dt> <dd>

Tipo de proveedor predefinido que proporciona algoritmos de intercambio de claves, firma digital, cifrado y hash. Los protocolos criptográficos y algoritmos especificados por este tipo de proveedor pertenecen al Instituto Nacional de Estándares y Tecnología (NIST).

</dd> <dt>

<span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV \_ MS \_ EXCHANGE**
</dt> <dd>

Vea Prov MS EXCHANGE provider type (Tipo *de proveedor de MS EXCHANGE de PROV). \_ \_*

</dd> <dt>

<span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ de MS EXCHANGE de PROV \_**
</dt> <dd>

Tipo de proveedor predefinido diseñado para las necesidades de Microsoft Exchange, así como otras aplicaciones compatibles con Microsoft Mail. Proporciona algoritmos de intercambio de claves, firma digital, cifrado y hash.

</dd> <dt>

<span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV \_ RSA \_ FULL**
</dt> <dd>

Vea PROV RSA FULL provider type (Tipo de *\_ proveedor DE PROV RSA \_ FULL).*

</dd> <dt>

<span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ PROV RSA \_ FULL**
</dt> <dd>

Tipo de proveedor predefinido definido por Microsoft y RSA Data Security, Inc. Este tipo de proveedor de uso general proporciona algoritmos de intercambio de claves, firma digital, cifrado y hash. Los algoritmos de intercambio de claves, firma digital y cifrado se basan en la criptografía de clave pública RSA.

</dd> <dt>

<span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV \_ RSA \_ SIG**
</dt> <dd>

Vea PROV RSA SIG provider type (Tipo de *proveedor DE SIG RSA \_ \_ de PROV).*

</dd> <dt>

<span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ DE PROV RSA \_ SIG**
</dt> <dd>

Tipo de proveedor predefinido definido por Microsoft y RSA Data Security. Este tipo de proveedor es un subconjunto de PROV RSA FULL que proporciona solo algoritmos hash y firma \_ \_ digital. El algoritmo de firma digital es un algoritmo de clave pública RSA.

</dd> <dt>

<span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV \_ SSL**
</dt> <dd>

Vea Prov SSL provider type (Tipo *de proveedor SSL \_ de PROV).*

</dd> <dt>

<span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor \_ DE PROV SSL**
</dt> <dd>

Tipo de proveedor predefinido que admite el protocolo Capa de sockets seguros (SSL). Este tipo proporciona algoritmos de cifrado de claves, firma digital, cifrado y hash. Una especificación que explica SSL está disponible en Netscape Communications Corp.

</dd> <dt>

<span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**Proveedor**
</dt> <dd>

Vea [*Proveedor de servicios criptográficos*](c-gly.md).

</dd> <dt>

<span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nombre del proveedor**
</dt> <dd>

Nombre que se usa para identificar un CSP. Por ejemplo, el proveedor criptográfico base de Microsoft versión 1.0. El nombre del proveedor se usa normalmente al llamar a la **función CryptAcquireContext** para conectarse a un CSP.

</dd> <dt>

<span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo de proveedor**
</dt> <dd>

Término que se usa para identificar un tipo de proveedor de servicios criptográficos (CSP). Los CSP se agrupan en diferentes tipos de proveedor que representan una familia específica de protocolos y formatos de datos estándar. A diferencia del nombre de proveedor único de un CSP, los tipos de proveedor no son únicos para un CSP determinado. El tipo de proveedor se usa normalmente al llamar a la **función CryptAcquireContext** para conectarse a un CSP.

</dd> <dt>

<span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**función pseudo aleatoria**
</dt> <dd>

(PRF) Función que toma una clave, etiqueta y valor de ed como entrada y, a continuación, genera una salida de longitud arbitraria.

</dd> <dt>

<span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**par de claves pública y privada**
</dt> <dd>

Un conjunto de claves criptográficas utilizado para la criptografía de clave pública. Para cada usuario, un CSP suele mantener dos pares de claves pública y privada: un par de claves de intercambio y un par de claves de firma digital. Ambos pares de claves se mantienen de una sesión a otra.

Vea [*par de claves de intercambio y*](e-gly.md) par de claves de [*firma.*](s-gly.md)

</dd> <dt>

<span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**clave pública**
</dt> <dd>

Una clave criptográfica utilizada normalmente al descifrar una clave de sesión o una firma digital. La clave pública también se puede utilizar para cifrar un mensaje, garantizando que solo la persona con la clave privada correspondiente puede descifrar el mensaje.

Consulte también *clave privada.*

</dd> <dt>

<span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo de clave pública**
</dt> <dd>

Cifrado asimétrico que usa dos claves, una para el cifrado, la clave pública y la otra para el descifrado, la clave privada. Según lo implícito en los nombres de clave, la clave pública que se usa para codificar texto no cifrado puede estar disponible para cualquier persona. Sin embargo, la clave privada debe permanecer secreta. Solo la clave privada puede descifrar el texto cifrado. El algoritmo de clave pública usado en este proceso es lento (en el orden de 1000 veces más lento que los algoritmos simétricos) y normalmente se usa para cifrar las claves de sesión o firmar digitalmente un mensaje.

Consulte también *clave pública* y *clave privada.*

</dd> <dt>

<span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**
</dt> <dd>

Blob que se usa para almacenar la parte de clave pública de un par de claves pública y privada. Los BLOB de clave pública no se cifran, ya que la clave pública contenida en no es secreta. Se crea un BLOB de clave pública mediante una llamada a la **función CryptExportKey.**

</dd> <dt>

<span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Estándares de criptografía de clave pública**
</dt> <dd>

(PKCS) Un conjunto de estándares de sintaxis para criptografía de clave pública que abarcan funciones de seguridad, incluidos métodos para firmar datos, intercambiar claves, solicitar certificados, cifrado y descifrado de claves públicas y otras funciones de seguridad.

</dd> <dt>

<span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**cifrado de clave pública**
</dt> <dd>

Cifrado que utiliza un par de claves, una clave para cifrar los datos y la otra clave para descifrar los datos. Por el contrario, los algoritmos de cifrado simétricos usan la misma clave para cifrado y descifrado. En la práctica, la criptografía de clave pública se usa normalmente para proteger la clave de sesión que usa un algoritmo de cifrado simétrico. En este caso, la clave pública se utiliza para cifrar la clave de sesión, que, a su vez, fue utilizada para cifrar algunos datos, y la clave privada se utiliza para el descifrado. Además de para proteger las claves de sesión, la criptografía de clave pública también se puede utilizar para firmar digitalmente un mensaje (mediante la clave privada) y validar la firma (mediante la clave pública).

Vea también *el algoritmo de clave pública*.

</dd> </dl>

 

 



