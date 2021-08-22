---
description: Contiene definiciones de términos de seguridad que comienzan por la letra R.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ce589e18-02ac-42c2-b76b-776deb686bbd
title: R (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a566a939746cd65c6336e8f31ff05a7ee3f0a3b7954e9d790d3f15a8163f138b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118895294"
---
# <a name="r-security-glossary"></a>R (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M N](m-gly.md) [](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q R [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_rc2_gly"></span><span id="_SECURITY_RC2_GLY"></span>**RC2**
</dt> <dd>

Nombre [*del algoritmo CryptoAPI*](c-gly.md) para el algoritmo RC2.

Consulte también algoritmo *de bloque RC2*.

</dd> <dt>

<span id="_security_rc2_block_algorithm_gly"></span><span id="_SECURITY_RC2_BLOCK_ALGORITHM_GLY"></span>**Algoritmo de bloque RC2**
</dt> <dd>

Algoritmo de [*cifrado de*](e-gly.md) datos basado en el cifrado de bloque simétrico RC2 de 64 bits. RC2 se especifica mediante los tipos de proveedor \_ PROV RSA \_ FULL. [*CryptoAPI hace*](c-gly.md) referencia a este algoritmo por su identificador (CALG \_ RC2), nombre (RC2) y clase (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rc4_gly"></span><span id="_SECURITY_RC4_GLY"></span>**RC4**
</dt> <dd>

Nombre [*del algoritmo CryptoAPI*](c-gly.md) para el algoritmo RC4.

Consulte también el *algoritmo de secuencia RC4*.

</dd> <dt>

<span id="_security_rc4_stream_algorithm_gly"></span><span id="_SECURITY_RC4_STREAM_ALGORITHM_GLY"></span>**Algoritmo de secuencia RC4**
</dt> <dd>

Algoritmo de [*cifrado de*](e-gly.md) datos basado en el cifrado de flujo simétrico RC4. Los tipos de proveedor \_ PROV RSA FULL especifican \_ RC4. [*CryptoAPI*](c-gly.md) hace referencia a este algoritmo por su identificador (CALG \_ RC4), nombre (RC4) y clase (ALG \_ CLASS DATA \_ \_ ENCRYPT).

</dd> <dt>

<span id="_security_rdn_gly"></span><span id="_SECURITY_RDN_GLY"></span>**Rdn**
</dt> <dd>

Vea *el nombre distintivo relativo*.

</dd> <dt>

<span id="_security_reader_gly"></span><span id="_SECURITY_READER_GLY"></span>**Lector**
</dt> <dd>

Un dispositivo estándar dentro del [*subsistema de tarjeta inteligente.*](s-gly.md) Un dispositivo de interfaz (IFD) que admite entrada/salida bidireccional a una tarjeta inteligente. Puede estar asociado a un sistema completo, a uno o varios grupos de lectores o a un terminal específico. El subsistema de tarjeta inteligente permite que un lector esté dedicado al terminal al que está asignado. Sin embargo, actualmente solo existe un terminal en un equipo.

</dd> <dt>

<span id="_security_reader_driver_gly"></span><span id="_SECURITY_READER_DRIVER_GLY"></span>**controlador de lector**
</dt> <dd>

Un controlador específico que asigna servicios de controlador a un dispositivo de lector de hardware específico. Debe comunicar eventos de inserción [](s-gly.md) y eliminación de tarjetas al controlador de clase de tarjeta inteligente para reenviarlos al administrador de recursos de tarjeta inteligente, y debe proporcionar funcionalidades de intercambio de datos a la tarjeta mediante cualquier protocolo sin formato, T=0, T=1 o PTS.

</dd> <dt>

<span id="_security_reader_group_gly"></span><span id="_SECURITY_READER_GROUP_GLY"></span>**grupo de lectores**
</dt> <dd>

Un grupo lógico de lectores. El sistema puede definir los grupos de lectores o los pueden crear usuarios o administradores. Los grupos de lectores se usan mediante funciones de tarjeta inteligente que pueden actuar sobre grupos de lectores. Para evitar conflictos de nomenclatura con grupos definidos por el usuario, Microsoft reserva el uso de cualquier nombre que contenga el signo de dólar ($).

</dd> <dt>

<span id="_security_reader_helper_driver_gly"></span><span id="_SECURITY_READER_HELPER_DRIVER_GLY"></span>**controlador del asistente de lector**
</dt> <dd>

Proporciona rutinas comunes de compatibilidad con controladores de tarjeta inteligente y compatibilidad adicional con los protocolos T=0 y T=1 para controladores específicos según sea necesario.

</dd> <dt>

<span id="_security_reference_count_gly"></span><span id="_SECURITY_REFERENCE_COUNT_GLY"></span>**recuento de referencias**
</dt> <dd>

Valor entero utilizado para realizar un seguimiento de un objeto COM. Cuando se crea un objeto, su recuento de referencias se establece en uno. Cada vez que una interfaz se enlaza al objeto , se incrementa su recuento de referencias; cuando se destruye la conexión de interfaz, se disminuye el recuento de referencias. El objeto se destruye cuando el recuento de referencias alcanza cero. Todas las interfaces de ese objeto no son válidas.

</dd> <dt>

<span id="_security_relative_distinguished_name_gly"></span><span id="_SECURITY_RELATIVE_DISTINGUISHED_NAME_GLY"></span>**nombre distintivo relativo**
</dt> <dd>

(RDN) Una entidad incluida como sujeto en una solicitud de certificado. Los elementos de un RDN se definen mediante sus atributos y no es necesario incluir un nombre. Con respecto a [*CryptoAPI,*](c-gly.md)un RDN se define mediante una estructura RDN cert, que a su vez apunta a una matriz de estructuras de atributo \_ \_ \_ ATTR de CERT RDN. Cada estructura de atributo especifica un único atributo.

</dd> <dt>

<span id="_security_relative_identifier_gly"></span><span id="_SECURITY_RELATIVE_IDENTIFIER_GLY"></span>**identificador relativo**
</dt> <dd>

(RID) Parte de un [*identificador de seguridad*](s-gly.md) (SID) que identifica un usuario o grupo en relación con la autoridad que emitió el SID.

</dd> <dt>

<span id="_security_relocated_store_gly"></span><span id="_SECURITY_RELOCATED_STORE_GLY"></span>**almacén reubicado**
</dt> <dd>

Un [*almacén de certificados*](c-gly.md) que se ha movido de su ubicación predeterminada del Registro a una ubicación diferente en el registro.

</dd> <dt>

<span id="_security_remote_store_gly"></span><span id="_SECURITY_REMOTE_STORE_GLY"></span>**almacén remoto**
</dt> <dd>

Un [*almacén de certificados*](c-gly.md) ubicado en otro equipo, como un servidor de archivos o algún otro equipo remoto compartido.

</dd> <dt>

<span id="_security_reply_apdu_gly"></span><span id="_SECURITY_REPLY_APDU_GLY"></span>**APDU de respuesta**
</dt> <dd>

Una [*unidad de datos de protocolo de*](a-gly.md) aplicación (APDU) enviada en respuesta a una APDU recibida.

</dd> <dt>

<span id="_security_repudiation_gly"></span><span id="_SECURITY_REPUDIATION_GLY"></span>**Repudio**
</dt> <dd>

La capacidad de un usuario de negar falsamente el haber realizado una acción cuando el resto de partes no pueden demostrar lo contrario. Por ejemplo, un usuario que eliminó un archivo y que puede denegar correctamente haberlo hecho.

</dd> <dt>

<span id="_security_resource_manager_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_GLY"></span>**Resource Manager**
</dt> <dd>

Módulo del subsistema [*de tarjetas inteligentes*](s-gly.md) que administra el acceso a varios lectores y tarjetas inteligentes. El administrador de recursos identifica y realiza un seguimiento de los recursos, asigna lectores y recursos en varias aplicaciones y admite primitivas de transacciones para acceder a los servicios disponibles en una tarjeta determinada.

</dd> <dt>

<span id="_security_resource_manager_api_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_API_GLY"></span>**API de Resource Manager**
</dt> <dd>

Conjunto de funciones Windows que proporcionan acceso directo a los servicios del administrador de recursos.

</dd> <dt>

<span id="_security_resource_manager_context_gly"></span><span id="_SECURITY_RESOURCE_MANAGER_CONTEXT_GLY"></span>**contexto del administrador de recursos**
</dt> <dd>

Contexto utilizado por el administrador de recursos al acceder a la base de datos de tarjeta inteligente. Las funciones de consulta y administración usan principalmente el contexto del administrador de recursos al acceder a la base de datos. El ámbito del contexto de Resource Manager puede ser el usuario actual o el sistema.

</dd> <dt>

<span id="_security_revocation_list_gly"></span><span id="_SECURITY_REVOCATION_LIST_GLY"></span>**lista de revocación**
</dt> <dd>

Vea [*Lista de revocación de certificados.*](c-gly.md)

</dd> <dt>

<span id="_security_rid_gly"></span><span id="_SECURITY_RID_GLY"></span>**Librar**
</dt> <dd>

Vea *el identificador relativo*.

</dd> <dt>

<span id="_security_root_authority_gly"></span><span id="_SECURITY_ROOT_AUTHORITY_GLY"></span>**autoridad raíz**
</dt> <dd>

La [*entidad de certificación*](c-gly.md) (CA) en la parte superior de una jerarquía de ca. La entidad emisora raíz certifica CA en el siguiente nivel de la jerarquía.

</dd> <dt>

<span id="_security_root_certificate_gly"></span><span id="_SECURITY_ROOT_CERTIFICATE_GLY"></span>**certificado raíz**
</dt> <dd>

Un certificado de entidad [*de certificación*](c-gly.md) (CA) autofirmado que identifica una entidad de certificación. Se denomina certificado raíz porque es el certificado de la CA raíz. La CA raíz debe firmar su propio certificado de entidad de certificación porque, por definición, no hay ninguna entidad de certificación superior para firmar su certificado de CA.

</dd> <dt>

<span id="_security_rsa_gly"></span><span id="_SECURITY_RSA_GLY"></span>**Rsa**
</dt> <dd>

RSA Data Security, Inc., un desarrollador y editor importante de [*estándares criptografía de clave pública*](p-gly.md) (PKCS). La "RSA" en el nombre representa los nombres de los tres desarrolladores y propietarios de la empresa: Elstst, Shamir y Adleman.

</dd> <dt>

<span id="_security_rsa_keyx_gly"></span><span id="_SECURITY_RSA_KEYX_GLY"></span>**RSA \_ KEYX**
</dt> <dd>

Nombre [*del algoritmo CryptoAPI*](c-gly.md) para el algoritmo de intercambio de claves RSA. CryptoAPI también hace referencia a este algoritmo por su identificador de algoritmo (CALG \_ RSA \_ KEYX) y la clase (ALG \_ CLASS KEY \_ \_ EXCHANGE).

</dd> <dt>

<span id="_security_rsa_sign_gly"></span><span id="_SECURITY_RSA_SIGN_GLY"></span>**RSA \_ SIGN**
</dt> <dd>

Nombre del algoritmo CryptoAPI para el algoritmo de firma RSA. CryptoAPI también hace referencia a este algoritmo por su identificador de algoritmo (CALG \_ RSA \_ SIGN) y la clase (ALG \_ CLASS \_ SIGNATURE).

</dd> <dt>

<span id="_security_rsa_public_key_algorithm_gly"></span><span id="_SECURITY_RSA_PUBLIC_KEY_ALGORITHM_GLY"></span>**Algoritmo de clave pública RSA**
</dt> <dd>

Un algoritmo de intercambio de claves y firma basado en el popular cifrado de clave pública RSA. Este algoritmo lo usan los tipos de proveedor \_ PROV RSA \_ FULL, PROV \_ RSA \_ SIG, PROV \_ MS \_ EXCHANGE y PROV \_ SSL. CryptoAPI hace referencia a este algoritmo por sus identificadores (CALG RSA KEYX y CALG RSA SIGN), nombres (RSA KEYX y RSA SIGN) y clase \_ \_ \_ \_ \_ \_ (ALG \_ CLASS \_ KEY \_ EXCHANGE).

</dd> </dl>

 

 



