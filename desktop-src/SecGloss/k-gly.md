---
description: Contiene definiciones de términos de seguridad que comienzan por la letra K.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f17042c3-ba1a-408f-af55-5f171b0dee33
title: K (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c92abf9b3df1eb49f0caaee90ccbce8755d003478683aba35570d9ea99fa2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895598"
---
# <a name="k-security-glossary"></a>K (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [](h-gly.md) [I](i-gly.md) J K [L](l-gly.md) [M N](m-gly.md) [O](n-gly.md) [](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_kca_gly"></span><span id="_SECURITY_KCA_GLY"></span>**Kca**
</dt> <dd>

Consulte la *entidad de certificación clave*.

</dd> <dt>

<span id="_security_kdc_gly"></span><span id="_SECURITY_KDC_GLY"></span>**Kdc**
</dt> <dd>

Vea *Centro de distribución de claves*.

</dd> <dt>

<span id="_security_kea_gly"></span><span id="_SECURITY_KEA_GLY"></span>**Kea**
</dt> <dd>

Consulte el *algoritmo de intercambio de claves*.

</dd> <dt>

<span id="_security_kerberos_protocol_gly"></span><span id="_SECURITY_KERBEROS_PROTOCOL_GLY"></span>**Protocolo Kerberos**
</dt> <dd>

Un protocolo que define cómo los clientes interactúan con un servicio de autenticación de red. Los clientes obtienen vales del Centro de distribución de claves Kerberos (KDC) y presentan estos vales a los servidores cuando se establecen las conexiones. Los vales de Kerberos representan las credenciales de red del cliente.

</dd> <dt>

<span id="_security_key_blob_gly"></span><span id="_SECURITY_KEY_BLOB_GLY"></span>**blob de clave**
</dt> <dd>

Blob que contiene una clave privada cifrada. Los blobs en claves proporcionan una manera de almacenar claves fuera del CSP. Los BLOB de clave se crean mediante la exportación de una clave existente desde el CSP mediante una llamada a la **función CryptExportKey.** Más adelante, el blob de clave se puede importar en un proveedor (a menudo un CSP diferente en un equipo diferente) mediante una llamada a la **función CryptImportKey.** Esto crea una clave en el CSP que es un duplicado del que se exportó.

Consulte también [*blob de clave simple,*](s-gly.md) [*blob de clave pública*](p-gly.md)y blob de [*clave privada.*](p-gly.md)

</dd> <dt>

<span id="_security_key_blob_format_gly"></span><span id="_SECURITY_KEY_BLOB_FORMAT_GLY"></span>**formato blob de clave**
</dt> <dd>

Formato del BLOB de clave cuando se exporta una clave de sesión o pública desde un CSP. El formato se especifica mediante el tipo de proveedor del CSP de exportación. Se crea un BLOB de clave mediante una **llamada a CryptExportKey**.

Consulte también [*blob de clave pública*](p-gly.md) y blob de clave [*simple.*](s-gly.md)

</dd> <dt>

<span id="_security_key_certification_authority_gly"></span><span id="_SECURITY_KEY_CERTIFICATION_AUTHORITY_GLY"></span>**entidad de certificación clave**
</dt> <dd>

(KCA) Una entidad de confianza que normalmente mantiene una base de datos segura de mensajes compuestos firmados con la clave privada del KCA. En implementaciones prácticas, los mensajes compuestos constan del nombre del usuario, la clave pública del usuario y cualquier otra información importante sobre el usuario. Cuando la aplicación receptora recibe un mensaje firmado de un usuario, la aplicación puede comprobar la clave pública recibida con el mensaje comparándolo con la clave pública almacenada en la base de datos de KCA.

</dd> <dt>

<span id="_security_key_container_gly"></span><span id="_SECURITY_KEY_CONTAINER_GLY"></span>**contenedor de claves**
</dt> <dd>

Una parte de la base de datos de claves que contiene todos los pares de claves (pares de claves de intercambio y firma) que pertenecen a un usuario específico. Cada contenedor tiene un nombre único que se usa al llamar a la **función CryptAcquireContext** para obtener un identificador para el contenedor.

</dd> <dt>

<span id="_security_key_database_gly"></span><span id="_SECURITY_KEY_DATABASE_GLY"></span>**base de datos de claves**
</dt> <dd>

Base de datos que contiene las claves criptográficas persistentes para un CSP específico. La base de datos contiene uno o varios contenedores de claves, que almacenan individualmente todos los pares de claves criptográficas para un usuario específico.

Consulte también contenedor *de claves*.

</dd> <dt>

<span id="_security_key_distribution_center_gly"></span><span id="_SECURITY_KEY_DISTRIBUTION_CENTER_GLY"></span>**Centro de distribución de claves**
</dt> <dd>

(KDC) Un servicio de red que proporciona vales de sesión y claves de sesión temporales que se usan en el protocolo de autenticación Kerberos V5. El KDC se ejecuta como un proceso con privilegios en todos los controladores de dominio.

Consulte también el *protocolo Kerberos*.

</dd> <dt>

<span id="_security_key_exchange_algorithm_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_GLY"></span>**algoritmo de intercambio de claves**
</dt> <dd>

Algoritmo que se usa para cifrar y descifrar claves de intercambio (claves de sesión simétricas). Algunos algoritmos comunes de intercambio de claves incluyen Diffie-Hellman y KEA, el algoritmo de intercambio de claves especificado por un tipo de proveedor \_ FORTEZZA de PROV. El algoritmo KEA es una versión mejorada del algoritmo Diffie-Hellman estándar. Cada tipo de proveedor solo puede especificar un algoritmo de intercambio de claves.

</dd> <dt>

<span id="_security_key_exchange_algorithm_name_gly"></span><span id="_SECURITY_KEY_EXCHANGE_ALGORITHM_NAME_GLY"></span>**Algoritmo de Exchange clave**
</dt> <dd>

(KEA) Algoritmo de intercambio de claves especificado por un tipo de proveedor \_ FORTEZZA de PROV. Este algoritmo es una versión mejorada del algoritmo Diffie-Hellman datos.

</dd> <dt>

<span id="_security_key_exchange_certificate_gly"></span><span id="_SECURITY_KEY_EXCHANGE_CERTIFICATE_GLY"></span>**certificado de intercambio de claves**
</dt> <dd>

Certificado que se usa para cifrar la información enviada a otra parte. Un cliente puede usar el certificado de intercambio de claves de la entidad de certificación (CA) para cifrar la información enviada a la entidad de certificación.

</dd> <dt>

<span id="_security_key_exchange_functions_gly"></span><span id="_SECURITY_KEY_EXCHANGE_FUNCTIONS_GLY"></span>**funciones de intercambio de claves**
</dt> <dd>

Conjunto de funciones que se usan para intercambiar o transmitir claves. Las funciones de intercambio de claves también se pueden usar para implementar intercambios de claves de tres fases totalmente autenticados.

</dd> <dt>

<span id="_security_key_exchange_key_pair_gly"></span><span id="_SECURITY_KEY_EXCHANGE_KEY_PAIR_GLY"></span>**par de claves de intercambio de claves**
</dt> <dd>

Vea [*Par de claves de intercambio.*](e-gly.md)

</dd> <dt>

<span id="_security_key_exchange_private_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PRIVATE_KEY_GLY"></span>**clave privada de intercambio de claves**
</dt> <dd>

Clave privada de un par de claves de intercambio.

Vea también exchange key pair ( [*Par de claves de intercambio).*](e-gly.md)

</dd> <dt>

<span id="_security_key_exchange_protocol_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PROTOCOL_GLY"></span>**protocolo de intercambio de claves**
</dt> <dd>

Protocolo por el que dos partes intercambian información para establecer un secreto compartido. A continuación, el secreto compartido se usa normalmente como una clave de cifrado simétrica.

</dd> <dt>

<span id="_security_key_exchange_public_key_gly"></span><span id="_SECURITY_KEY_EXCHANGE_PUBLIC_KEY_GLY"></span>**clave pública de intercambio de claves**
</dt> <dd>

Clave pública de un par de claves de intercambio.

Vea también exchange key pair ( [*Par de claves de intercambio).*](e-gly.md)

</dd> <dt>

<span id="_security_key_generation_functions_gly"></span><span id="_SECURITY_KEY_GENERATION_FUNCTIONS_GLY"></span>**funciones de generación de claves**
</dt> <dd>

Conjunto de funciones que usan las aplicaciones para generar y personalizar claves criptográficas. Estas funciones incluyen compatibilidad total para cambiar los modos de encadenamiento, los vectores de inicialización y otras características de cifrado.

</dd> <dt>

<span id="_security_key_length_gly"></span><span id="_SECURITY_KEY_LENGTH_GLY"></span>**longitud de clave**
</dt> <dd>

Valores especificados por algunos proveedores que indican la longitud de los pares de claves pública y privada y las claves de sesión que se usan con ese proveedor.

</dd> <dt>

<span id="_security_key_pair_gly"></span><span id="_SECURITY_KEY_PAIR_GLY"></span>**par de claves**
</dt> <dd>

Una clave privada y su clave pública relacionada.

</dd> <dt>

<span id="_security_key_storage_provider_gly"></span><span id="_SECURITY_KEY_STORAGE_PROVIDER_GLY"></span>**proveedor de almacenamiento de claves**
</dt> <dd>

(KSP) Módulo de software independiente que implementa la funcionalidad para crear, administrar, almacenar y recuperar [*claves privadas.*](p-gly.md)

</dd> <dt>

<span id="_security_ksp_gly"></span><span id="_SECURITY_KSP_GLY"></span>**Ksp**
</dt> <dd>

Consulte proveedor *de almacenamiento de claves.*

</dd> </dl>

 

 



