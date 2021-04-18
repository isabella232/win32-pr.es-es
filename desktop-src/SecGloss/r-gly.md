---
description: Contiene definiciones de términos de seguridad que comienzan por la letra R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc85a0da8aa4a0b985b8be040ef95e37068e8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687901"
---
# <a name="r-security-glossary"></a>R (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q R [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

El nombre del algoritmo de [*CryptoAPI*](c-gly.md) para el algoritmo RC2.

Vea también *algoritmo de bloque RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo de bloque RC2**
</dt> <dd>

Algoritmo de [*cifrado*](e-gly.md) de datos basado en el cifrado de bloques simétricos de 64 bits de RC2. RC2 se especifica mediante los \_ tipos de proveedor completo de RSA de Prov \_ . [*CryptoAPI*](c-gly.md) hace referencia a este algoritmo mediante su identificador (CALG \_ RC2), el nombre (RC2) y la clase (tipo de datos de la \_ clase alg \_ \_ ).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

El nombre del algoritmo de [*CryptoAPI*](c-gly.md) para el algoritmo RC4.

Vea también *algoritmo de flujo RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo de secuencia RC4**
</dt> <dd>

Algoritmo de [*cifrado*](e-gly.md) de datos basado en el cifrado de flujo simétrico RC4. RC4 lo especifican los \_ \_ tipos de proveedores completos de RSA. [*CryptoAPI*](c-gly.md) hace referencia a este algoritmo mediante su identificador (CALG \_ RC4), el nombre (RC4) y la clase (tipo de datos de la \_ clase alg \_ \_ ).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**RDN**
</dt> <dd>

Vea *nombre distintivo relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**omisión**
</dt> <dd>

Un dispositivo estándar dentro del subsistema de [*tarjeta inteligente*](s-gly.md) . Un dispositivo de interfaz (IFD) que admite entrada/salida bidireccional en una tarjeta inteligente. Puede estar asociado a un sistema completo, a uno o varios grupos de lectores o a un terminal específico. El subsistema de tarjeta inteligente permite que un lector esté dedicado al terminal al que está asignado. Sin embargo, actualmente solo existe un terminal en un equipo.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**controlador de lector**
</dt> <dd>

Un controlador específico que asigna los servicios de controlador a un dispositivo lector de hardware específico. Debe comunicar los eventos de inserción y eliminación de tarjeta al controlador de clase de [*tarjeta inteligente*](s-gly.md) para reenviarlos al administrador de recursos de tarjeta inteligente y debe proporcionar funciones de intercambio de datos a la tarjeta por cualquier protocolo RAW, t = 0, t = 1 o pts.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**Grupo de lectores**
</dt> <dd>

Grupo lógico de lectores. Los grupos de lectores pueden ser definidos por el sistema o creados por usuarios o administradores. Los grupos de lectores son utilizados por las funciones de tarjetas inteligentes que pueden actuar en grupos de lectores. Para evitar colisiones de nombres con grupos definidos por el usuario, Microsoft se reserva el uso de cualquier nombre que contenga el signo de dólar ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**controlador auxiliar de lector**
</dt> <dd>

Proporciona rutinas comunes de compatibilidad con controladores de tarjetas inteligentes y la compatibilidad con el protocolo T = 0 y T = 1 para controladores específicos según sea necesario.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**recuento de referencias**
</dt> <dd>

Valor entero que se usa para realizar un seguimiento de un objeto COM. Cuando se crea un objeto, su recuento de referencias se establece en uno. Cada vez que una interfaz se enlaza al objeto, se incrementa su recuento de referencias; Cuando se destruye la conexión de la interfaz, se reduce el recuento de referencias. El objeto se destruye cuando el recuento de referencias llega a cero. Todas las interfaces a ese objeto no son válidas.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nombre distintivo relativo**
</dt> <dd>

RDN Entidad incluida como asunto en una solicitud de certificado. Los elementos de un RDN se definen mediante sus atributos y no es necesario incluir un nombre. Con respecto a [*CryptoAPI*](c-gly.md), un RDN se define mediante una \_ estructura de certificado RDN, que a su vez apunta a una matriz de \_ estructuras de atributo RDN de CERT \_ . Cada estructura de atributo especifica un atributo único.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificador relativo**
</dt> <dd>

LIBRA La parte de un [*identificador de seguridad*](s-gly.md) (SID) que identifica a un usuario o grupo en relación con la entidad que emitió el SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**almacén reubicado**
</dt> <dd>

Un [*almacén de certificados*](c-gly.md) que se ha pasado de la ubicación del registro predeterminada a otra ubicación en el registro.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**almacén remoto**
</dt> <dd>

Un [*almacén de certificados*](c-gly.md) ubicado en otro equipo, como un servidor de archivos o algún otro equipo remoto compartido.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**APDU de respuesta**
</dt> <dd>

Una [*unidad de datos de protocolo de aplicación*](a-gly.md) (APDU) enviada como respuesta a una APDU recibida.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**repudio**
</dt> <dd>

La capacidad de un usuario de negar falsamente el haber realizado una acción cuando el resto de partes no pueden demostrar lo contrario. Por ejemplo, un usuario que eliminó un archivo y que puede denegarlo correctamente.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Administrador de recursos**
</dt> <dd>

Módulo del subsistema de [*tarjeta inteligente*](s-gly.md) que administra el acceso a varios lectores y tarjetas inteligentes. El administrador de recursos identifica y realiza un seguimiento de los recursos, asigna lectores y recursos entre varias aplicaciones y admite primitivas de transacción para tener acceso a los servicios disponibles en una tarjeta determinada.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API de Resource Manager**
</dt> <dd>

Un conjunto de funciones de Windows que proporcionan acceso directo a los servicios del administrador de recursos.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contexto de Resource Manager**
</dt> <dd>

Contexto utilizado por el administrador de recursos al tener acceso a la base de datos de la tarjeta inteligente. El contexto de Resource Manager se usa principalmente en las funciones de consulta y administración al obtener acceso a la base de datos. El ámbito del contexto del administrador de recursos puede ser el usuario actual o el sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**lista de revocación**
</dt> <dd>

Consulte [*lista de revocación de certificados*](c-gly.md).

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**LIBRA**
</dt> <dd>

Vea *identificador relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**entidad de certificación raíz**
</dt> <dd>

La [*entidad de certificación*](c-gly.md) (CA) en la parte superior de una jerarquía de CA. La entidad emisora raíz certifica CA en el siguiente nivel de la jerarquía.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificado raíz**
</dt> <dd>

Un certificado de [*entidad de certificación*](c-gly.md) (CA) autofirmado que identifica una CA. Se denomina certificado raíz porque es el certificado de la CA raíz. La entidad de certificación raíz debe firmar su propio certificado de CA porque, por definición, no hay ninguna entidad de certificación superior para firmar su certificado de CA.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**RSA**
</dt> <dd>

RSA Data Security, Inc., un desarrollador principal y un editor de [*estándares de criptografía de clave pública*](p-gly.md) (PKCS). La "RSA" en el nombre representa los nombres de los tres desarrolladores de la empresa y los propietarios: Rivest, Shamir y Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**\_KEYX RSA**
</dt> <dd>

El nombre del algoritmo de [*CryptoAPI*](c-gly.md) para el algoritmo de intercambio de claves RSA. CryptoAPI también hace referencia a este algoritmo mediante su identificador de algoritmo (CALG \_ RSA \_ KEYX) y la clase ( \_ intercambio de claves de clase alg \_ \_ ).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**\_firma RSA**
</dt> <dd>

El nombre del algoritmo de CryptoAPI para el algoritmo de firma RSA. CryptoAPI también hace referencia a este algoritmo mediante su identificador de algoritmo (CALG \_ RSA \_ Sign) y la clase ( \_ signatura de clase alg \_ ).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo de clave pública RSA**
</dt> <dd>

Un algoritmo de intercambio de claves y firma basado en el conocido cifrado de clave pública RSA. Este algoritmo lo usan los \_ tipos de \_ proveedor RSA Full, Prov \_ RSA \_ SIG, PROV \_ MS \_ Exchange y Prov \_ SSL. CryptoAPI hace referencia a este algoritmo mediante sus identificadores (CALG \_ RSA \_ KEYX y CALG \_ RSA \_ Sign), los nombres (RSA \_ KEYX y RSA \_ Sign) y la clase ( \_ intercambio de claves de clase alg \_ \_ ).

</dd> </dl>

 

 



