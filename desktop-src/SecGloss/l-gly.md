---
description: Contiene definiciones de términos de seguridad que comienzan por la letra L.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b33ee054c2bcf414ef289cc381ac13ef970da6dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361817"
---
# <a name="l-security-glossary"></a>L (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](g-gly.md) [](h-gly.md) [I](i-gly.md) J [K](k-gly.md) L [M N](m-gly.md) [O](n-gly.md) [](o-gly.md) [P P](p-gly.md) [Q R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**LDAP**
</dt> <dd>

Consulte *Protocolo ligero de acceso a directorios*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Protocolo ligero de acceso a directorios**
</dt> <dd>

Subconjunto más fácil de implementar del estándar DAP X.500 para servicios de directorio.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**little-endian**
</dt> <dd>

Un formato de memoria o datos en el que el byte menos significativo se almacena en la dirección inferior o llega primero.

Consulte también [*big-endian*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**identificador único local**
</dt> <dd>

(LUID) Valor de 64 bits que se garantiza que es único en el sistema operativo que lo generó hasta que se reinicie el sistema.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**entidad de registro local**
</dt> <dd>

(LRA) Intermediario entre un publicador y una [*entidad de certificación*](c-gly.md) (CA). El LRA puede, por ejemplo, comprobar las credenciales de un publicador antes de enviarlas a la entidad de certificación.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Autoridad de seguridad local**
</dt> <dd>

(LSA) Subsistema protegido que autentica y registra a los usuarios en el sistema local. LSA también mantiene información sobre todos los aspectos de seguridad local en un sistema, que se conoce como directiva de seguridad local del sistema.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**almacén lógico**
</dt> <dd>

Consulte [*la tienda virtual*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**datos de inicio de sesión**
</dt> <dd>

Información presentada al sistema por una entidad de [*seguridad para*](s-gly.md) la autenticación.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**identificador de inicio de sesión**
</dt> <dd>

UN LUID que identifica una sesión *de inicio de sesión*. Un identificador de inicio de sesión es válido hasta que el usuario cierra la sesión. Un identificador de inicio de sesión es único mientras se ejecuta el equipo; ninguna otra sesión de inicio de sesión tendrá el mismo identificador de inicio de sesión. Sin embargo, el conjunto de posibles IDs de inicio de sesión se restablece cuando se inicia el equipo. Para recuperar el identificador de inicio de sesión de un [*token de*](a-gly.md)acceso, llame a la **función GetTokenInformation** para TokenStatistics; El identificador de inicio de sesión está en el **miembro AuthenticationId.**

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**sesión de inicio de sesión**
</dt> <dd>

Una sesión de inicio de sesión comienza cada vez que un usuario inicia sesión en un equipo. Todos los procesos de una sesión de inicio de sesión tienen el mismo [*token de acceso principal.*](a-gly.md) El token de acceso contiene información sobre el contexto de seguridad de la sesión de inicio de sesión, incluido el SID del usuario, el identificador de inicio de sesión y el *SID de inicio de sesión.*

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**SID de inicio de sesión**
</dt> <dd>

Identificador [*de seguridad*](s-gly.md) (SID) que identifica una sesión de inicio de *sesión*. Puede usar el SID de inicio de sesión en [*una DACL*](d-gly.md) para controlar el acceso durante una sesión de inicio de sesión. Un SID de inicio de sesión es válido hasta que el usuario cierra la sesión. Un SID de inicio de sesión es único mientras se ejecuta el equipo; ninguna otra sesión de inicio de sesión tendrá el mismo SID de inicio de sesión. Sin embargo, el conjunto de posibles SID de inicio de sesión se restablece cuando se inicia el equipo. Para recuperar el SID de inicio de sesión de un [*token de*](a-gly.md)acceso, llame a la **función GetTokenInformation** para TokenGroups.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**Funciones de mensaje de bajo nivel**
</dt> <dd>

Funciones de administración de mensajes que funcionan en un nivel superior al de las funciones criptográficas base. Estas funciones proporcionan funcionalidad para codificar datos para la transmisión y para la codificación de los datos que se han recibido. Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificadas, pero requieren más llamadas de función.

Vea también funciones [*de mensaje simplificadas.*](s-gly.md)

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**LSA**
</dt> <dd>

Vea *Autoridad de seguridad local*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

Vea *identificador único local.*

</dd> </dl>

 

 



