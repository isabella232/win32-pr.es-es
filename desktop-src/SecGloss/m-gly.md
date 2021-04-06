---
description: Contiene definiciones de términos de seguridad que comienzan por la letra M.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002340"
---
# <a name="m-security-glossary"></a>M (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**Macintosh**
</dt> <dd>

Vea *código de autentificación de mensajes (Mac)*.

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Tecla MAC**
</dt> <dd>

Una clave de código de autenticación de mensajes utilizada con los protocolos [*Schannel*](s-gly.md) .

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**clave maestra**
</dt> <dd>

La clave utilizada por el cliente y el servidor para la generación de la clave de sesión. La clave maestra se usa para generar la clave de lectura de cliente, la clave de escritura de cliente, la clave de lectura de servidor y la clave de escritura de servidor. Las claves maestras se pueden exportar como blobs de clave simple.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

El nombre del algoritmo de CryptoAPI para el algoritmo hash MD2. Otros algoritmos hash incluyen *MD4*, *MD5* y [*Sha*](s-gly.md).

Vea también *algoritmo MD2*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**Algoritmo MD2**
</dt> <dd>

MD2 Algoritmo hash que crea un valor hash de 128 bits. MD2 se optimizó para su uso con equipos de 8 bits. CryptoAPI hace referencia a este algoritmo por su tipo (CALG \_ MD2), nombre (Mac) y clase ( \_ hash de clase alg \_ ). MD2 fue desarrollado por RSA Data Security, Inc.

Vea también *algoritmo MD4*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

El nombre del algoritmo de CryptoAPI para el algoritmo hash MD4. Otros algoritmos hash incluyen *MD2*, *MD5* y [*Sha*](s-gly.md).

Vea *algoritmo MD4*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**Algoritmo MD4**
</dt> <dd>

MD4 Algoritmo hash que crea un valor hash de 128 bits. MD4 se optimizó para equipos de 32 bits. Ahora se considera interrumpido porque las colisiones se pueden encontrar demasiado rápido y fácilmente. MD4 fue desarrollado por RSA Data Security, Inc.

Vea también *algoritmo MD2*, *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**MD5**
</dt> <dd>

El nombre del algoritmo de CryptoAPI para el algoritmo hash MD5. Otros algoritmos hash incluyen *MD2*, *MD4* y [*Sha*](s-gly.md).

Vea también *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**Algoritmo MD5**
</dt> <dd>

MD5 Algoritmo hash que crea un valor hash de 128 bits. MD5 se optimizó para equipos de 32 bits. CryptoAPI hace referencia a este algoritmo por su identificador de algoritmo (CALG \_ MD5), nombre (MD5) y clase ( \_ hash de clase alg \_ ). MD5 fue desarrollado por RSA Data Security, Inc. y lo especifican los \_ \_ tipos de proveedor RSA Full, Prov \_ RSA SIG, \_ Prov \_ DSS, Prov \_ DSS \_ DH y Prov \_ MS \_ Exchange.

Vea también *algoritmo MD2*, *algoritmo MD4*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Mensaje**
</dt> <dd>

Los datos que se han codificado para su transmisión o recepción de una persona o entidad. Los mensajes se pueden cifrar con fines de privacidad, firmados digitalmente para propósitos de autenticación o ambos.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**síntesis del mensaje**
</dt> <dd>

Consulte [*hash*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**código de autentificación de mensajes (MAC)**
</dt> <dd>

Macintosh Algoritmo hash con clave que utiliza una clave de sesión simétrica para garantizar que un bloque de datos ha conservado su integridad desde el momento en que se envió hasta el momento en que se recibió. Cuando se usa este tipo de algoritmo, la aplicación receptora también debe poseer la clave de sesión para volver a calcular el valor hash, de modo que pueda comprobar que los datos base no hayan cambiado. CryptoAPI hace referencia a este algoritmo por su tipo (CALG \_ Mac), nombre (Mac) y clase ( \_ hash de clase alg \_ ).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**tipo de codificación de mensajes**
</dt> <dd>

Define cómo se codifica el mensaje. El tipo de codificación de mensajes se almacena en la palabra de orden superior de la estructura de tipo de codificación. Los tipos de codificación definidos actualmente son: \_ \_ codificación de ASN de cifrado, codificación de ASN de X509 \_ \_ y codificación de ASN de PKCS \_ 7 \_ \_ .

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**funciones de administración de mensajes**
</dt> <dd>

Funciones que proporcionan dos niveles de administración de mensajes: funciones de mensaje de bajo nivel y funciones de mensaje simplificadas. Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificadas. sin embargo, requieren más llamadas a funciones.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**funciones de firma de mensajes**
</dt> <dd>

Funciones utilizadas para firmar mensajes y datos.

Vea también [*funciones de mensaje simplificadas*](s-gly.md).

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Vea *enrutador de varios proveedores*.

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Enrutador de varios proveedores**
</dt> <dd>

MPR Componente del sistema que controla las comunicaciones entre el sistema y todos los proveedores de red. El MPR llama a las funciones de proveedor de red que expone cada proveedor de red.

</dd> </dl>

 

 



