---
description: Contiene definiciones de términos de seguridad que comienzan por la letra A.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 0baaa937-f635-4500-8dcd-9dbbd6f4cd02
title: A (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a3c9bd82d68a80d5a014c19e6c81dddf5e2b2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069026"
---
# <a name="a-security-glossary"></a>A (Glosario de seguridad)

A [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_absolute_security_descriptor_gly"></span><span id="_SECURITY_ABSOLUTE_SECURITY_DESCRIPTOR_GLY"></span>**descriptor de seguridad absoluto**
</dt> <dd>

Estructura de descriptor de seguridad que contiene punteros a la información de seguridad asociada a un objeto .

Vea también descriptor [*de seguridad*](s-gly.md) y descriptor de seguridad [*auto relative*](s-gly.md).

</dd> <dt>

<span id="_security_abstract_syntax_notation_one_gly"></span><span id="_SECURITY_ABSTRACT_SYNTAX_NOTATION_ONE_GLY"></span>**Abstract Syntax Notation One**
</dt> <dd>

(ASN.1) Método que se usa para especificar objetos abstractos que están diseñados para la transmisión en serie.

</dd> <dt>

<span id="_security_access_block_gly"></span><span id="_SECURITY_ACCESS_BLOCK_GLY"></span>**bloque de acceso**
</dt> <dd>

Blob de clave que contiene la clave del cifrado simétrico utilizado para cifrar un archivo o mensaje. El bloque de acceso solo se puede abrir con una clave privada.

</dd> <dt>

<span id="_security_access_control_entry_gly"></span><span id="_SECURITY_ACCESS_CONTROL_ENTRY_GLY"></span>**entrada de control de acceso**
</dt> <dd>

(ACE) Entrada en una lista de control de acceso (ACL). Una ACE contiene un conjunto de derechos de acceso y un identificador de seguridad (SID) que identifica a un administrador de confianza para el que se permiten, deniegan o auditan los derechos.

Consulte también la *lista de control de acceso,* el identificador [*de*](s-gly.md)seguridad y el administrador [*de confianza.*](t-gly.md)

</dd> <dt>

<span id="_security_access_control_list_gly"></span><span id="_SECURITY_ACCESS_CONTROL_LIST_GLY"></span>**lista de control de acceso**
</dt> <dd>

(ACL) Lista de protecciones de seguridad que se aplican a un objeto . (Un objeto puede ser un archivo, un proceso, un evento o cualquier otra cosa que tenga un descriptor de seguridad). Una entrada de una lista de control de acceso (ACL) es una entrada de control de acceso (ACE). Hay dos tipos de lista de control de acceso, discrecional y de sistema.

Consulte también entrada *de control de acceso,* [*lista de control de acceso discrecional,*](d-gly.md) [*descriptor de seguridad*](s-gly.md)y lista de control de acceso [*del sistema*](s-gly.md).

</dd> <dt>

<span id="_security_access_mask_gly"></span><span id="_SECURITY_ACCESS_MASK_GLY"></span>**máscara de acceso**
</dt> <dd>

Valor de 32 bits que especifica los derechos que se permiten o deniegan en una entrada de control de acceso (ACE). Una máscara de acceso también se usa para solicitar derechos de acceso cuando se abre un objeto.

Consulte también la *entrada de control de acceso*.

</dd> <dt>

<span id="_security_access_token_gly"></span><span id="_SECURITY_ACCESS_TOKEN_GLY"></span>**token de acceso**
</dt> <dd>

Un token de acceso contiene la información de seguridad para una sesión de inicio. El sistema crea un token de acceso cuando un usuario inicia sesión, y cada proceso ejecutado en nombre del usuario tiene una copia del token. El token identifica al usuario, los grupos del usuario y los privilegios del usuario. El sistema utiliza el token para controlar el acceso a los objetos que se pueden proteger y controlar la capacidad del usuario para realizar varias operaciones relacionadas con el sistema en el equipo local. Hay dos tipos de token de acceso, principal y suplantación.

Consulte también [*token de suplantación, token*](i-gly.md) [*principal,*](p-gly.md) [*privilegio,*](p-gly.md) [*proceso*](p-gly.md)e identificador [*de seguridad.*](s-gly.md)

</dd> <dt>

<span id="_security_ace_gly"></span><span id="_SECURITY_ACE_GLY"></span>**AS**
</dt> <dd>

Consulte la *entrada de control de acceso*.

</dd> <dt>

<span id="_security_acl_gly"></span><span id="_SECURITY_ACL_GLY"></span>**ACL**
</dt> <dd>

Consulte la *lista de control de acceso*.

</dd> <dt>

<span id="_security_aes_gly"></span><span id="_SECURITY_AES_GLY"></span>**Estándar de cifrado avanzado**
</dt> <dd>

(AES) Algoritmo criptográfico especificado por el Instituto Nacional de Estándares y Tecnología (NIST) para proteger la información confidencial.

</dd> <dt>

<span id="_security_alg_class_data_encrypt_gly"></span><span id="_SECURITY_ALG_CLASS_DATA_ENCRYPT_GLY"></span>**ALG \_ CLASS \_ DATA \_ ENCRYPT**
</dt> <dd>

La clase de algoritmo CryptoAPI para algoritmos de cifrado de datos. Los algoritmos de cifrado de datos típicos incluyen RC2 y RC4.

</dd> <dt>

<span id="_security_alg_class_hash_gly"></span><span id="_SECURITY_ALG_CLASS_HASH_GLY"></span>**HASH DE LA CLASE ALG \_ \_**
</dt> <dd>

La clase de algoritmo CryptoAPI para algoritmos hash. Los algoritmos hash típicos incluyen MD2, MD5, SHA-1 y MAC.

</dd> <dt>

<span id="_security_alg_class_key_exchange_gly"></span><span id="_SECURITY_ALG_CLASS_KEY_EXCHANGE_GLY"></span>**INTERCAMBIO DE CLAVES \_ DE \_ CLASE DE \_ ALG**
</dt> <dd>

La clase de algoritmo CryptoAPI para algoritmos de intercambio de claves. Un algoritmo de intercambio de claves típico es RSA \_ KEYX.

</dd> <dt>

<span id="_security_alg_class_signature_gly"></span><span id="_SECURITY_ALG_CLASS_SIGNATURE_GLY"></span>**FIRMA DE CLASE ALG \_ \_**
</dt> <dd>

La clase de algoritmo CryptoAPI para algoritmos de firma. Un algoritmo de firma digital típico es RSA \_ SIGN.

</dd> <dt>

<span id="_security_apdu_gly"></span><span id="_SECURITY_APDU_GLY"></span>**APDU**
</dt> <dd>

Consulte la *unidad de datos del protocolo de aplicación*.

</dd> <dt>

<span id="_security_application_protocol_data_unit_gly"></span><span id="_SECURITY_APPLICATION_PROTOCOL_DATA_UNIT_GLY"></span>**unidad de datos del protocolo de aplicación**
</dt> <dd>

(APDU) Secuencia de comandos (una unidad de datos del protocolo de aplicación) que puede enviarse mediante la tarjeta inteligente o devolverla la aplicación.

Consulte también [*responder a APDU.*](r-gly.md)

</dd> <dt>

<span id="_security_application_protocol_gly"></span><span id="_SECURITY_APPLICATION_PROTOCOL_GLY"></span>**protocolo de aplicación**
</dt> <dd>

Protocolo que normalmente reside sobre la capa de transporte. Por ejemplo, HTTP, TELNET, FTP y SMTP son todos protocolos de aplicación.

</dd> <dt>

<span id="_security_asn.1_gly"></span><span id="_SECURITY_ASN.1_GLY"></span>**ASN.1**
</dt> <dd>

Vea *Abstract Syntax Notation One*.

</dd> <dt>

<span id="_security_ascii_gly"></span><span id="_SECURITY_ASCII_GLY"></span>**ASCII**
</dt> <dd>

American Standard Code for Information Interchange. Esquema de codificación que asigna valores numéricos a letras, números, signos de puntuación y otros caracteres.

</dd> <dt>

<span id="_security_asymmetric_algorithm_gly"></span><span id="_SECURITY_ASYMMETRIC_ALGORITHM_GLY"></span>**algoritmo asimétrico**
</dt> <dd>

Vea el [*algoritmo de clave pública*](p-gly.md).

</dd> <dt>

<span id="_security_asymmetric_key_gly"></span><span id="_SECURITY_ASYMMETRIC_KEY_GLY"></span>**clave asimétrica**
</dt> <dd>

Una de un par de claves usadas con un algoritmo criptográfico asimétrico. Este algoritmo usa dos claves criptográficas: una "clave pública" para el cifrado y una "clave privada" para el descifrado. En la firma y la comprobación, los roles se invierten: la clave pública se usa para la comprobación y la clave privada se usa para la generación de firmas. La característica más importante de estos algoritmos es que su seguridad no depende de mantener el secreto de clave pública (aunque puede requerir cierta garantía de autenticidad de las claves públicas, por ejemplo, que se obtienen de un origen de confianza). Se requiere confidencialidad de la clave privada. Algunos ejemplos de algoritmos de clave pública son el algoritmo de firma [*digital (DSA),*](d-gly.md)el algoritmo de firma digital de curva elíptica (ECDSA) y la familia de algoritmosZierst-Shamir-Adleman (RSA).

</dd> <dt>

<span id="_security_atr_string_gly"></span><span id="_SECURITY_ATR_STRING_GLY"></span>**Cadena ATR**
</dt> <dd>

Secuencia de bytes devuelta desde una tarjeta inteligente cuando está activada. Estos bytes se usan para identificar la tarjeta en el sistema.

</dd> <dt>

<span id="_security_attribute_gly"></span><span id="_SECURITY_ATTRIBUTE_GLY"></span>**Atributo**
</dt> <dd>

Elemento de un nombre distintivo relativo (RDN). Algunos atributos típicos incluyen el nombre común, el apellido, la dirección de correo electrónico, la dirección postal y el nombre del país o región.

</dd> <dt>

<span id="_security_attribute_blob_gly"></span><span id="_SECURITY_ATTRIBUTE_BLOB_GLY"></span>**attribute BLOB**
</dt> <dd>

Representación codificada de la información de atributo almacenada en una solicitud de certificado.

</dd> <dt>

<span id="_security_audit_security_object_gly"></span><span id="_SECURITY_AUDIT_SECURITY_OBJECT_GLY"></span>**Auditar objeto de seguridad**
</dt> <dd>

Descriptor de seguridad que controla el acceso al subsistema de directivas de auditoría.

</dd> <dt>

<span id="_security_authentication_gly"></span><span id="_SECURITY_AUTHENTICATION_GLY"></span>**Autenticación**
</dt> <dd>

El proceso para comprobar que un usuario, equipo, servicio o proceso es quién o lo que dice ser.

</dd> <dt>

<span id="_security_authentication_package_gly"></span><span id="_SECURITY_AUTHENTICATION_PACKAGE_GLY"></span>**paquete de autenticación**
</dt> <dd>

Un archivo DLL que encapsula la lógica de autenticación utilizada para determinar si se permite que un usuario inicie sesión. LSA autentica un inicio de sesión de usuario mediante el envío de la solicitud a un paquete de autenticación. A continuación, el paquete de autenticación examina la información de inicio de sesión y autentica o rechaza el intento de inicio de sesión del usuario.

</dd> <dt>

<span id="_security_authenticode_gly"></span><span id="_SECURITY_AUTHENTICODE_GLY"></span>**Authenticode**
</dt> <dd>

Una característica de seguridad de Internet Explorer. Authenticode permite a los proveedores de código ejecutable descargable (complementos o controles ActiveX, por ejemplo) adjuntar certificados digitales a sus productos para garantizar a los usuarios finales que el código es del desarrollador original y no se ha modificado. Authenticode permite a los usuarios finales decidir por sí mismos si aceptan o rechazan los componentes de software publicados en Internet antes de comenzar la descarga.

</dd> </dl>

 

 



