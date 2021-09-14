---
description: Contiene definiciones de términos de seguridad que comienzan por la letra M.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4c4402e9-7455-4868-978f-3899a8fd86c1
title: M (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db63fc76d4b8b803d523c46012dcb10ed5380e4a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361816"
---
# <a name="m-security-glossary"></a>M (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) H [](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) M [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_mac_gly"></span><span id="_SECURITY_MAC_GLY"></span>**MAC**
</dt> <dd>

Vea Código *de autenticación de mensajes.*

</dd> <dt>

<span id="_security_mac_key_gly"></span><span id="_SECURITY_MAC_KEY_GLY"></span>**Clave MAC**
</dt> <dd>

Una clave de código de autenticación de mensajes utilizada con [*protocolos Schannel.*](s-gly.md)

</dd> <dt>

<span id="_security_master_key_gly"></span><span id="_SECURITY_MASTER_KEY_GLY"></span>**clave maestra**
</dt> <dd>

Clave usada por el cliente y el servidor para toda la generación de claves de sesión. La clave maestra se usa para generar la clave de lectura de cliente, la clave de escritura de cliente, la clave de lectura del servidor y la clave de escritura del servidor. Las claves maestras se pueden exportar como blobs de clave simples.

</dd> <dt>

<span id="_security_md2_gly"></span><span id="_SECURITY_MD2_GLY"></span>**MD2**
</dt> <dd>

Nombre del algoritmo CryptoAPI para el algoritmo hash MD2. Otros algoritmos hash incluyen *MD4,* *MD5* y [*SHA.*](s-gly.md)

Consulte también el *algoritmo MD2*.

</dd> <dt>

<span id="_security_md2_algorithm_gly"></span><span id="_SECURITY_MD2_ALGORITHM_GLY"></span>**Algoritmo MD2**
</dt> <dd>

(MD2) Algoritmo hash que crea un valor hash de 128 bits. MD2 se ha optimizado para su uso con equipos de 8 bits. CryptoAPI hace referencia a este algoritmo por su tipo (CALG \_ MD2), nombre (MAC) y clase (ALG \_ CLASS \_ HASH). MD2 fue desarrollado por RSA Data Security, Inc.

Vea también *el algoritmo MD4*, *el algoritmo MD5*.

</dd> <dt>

<span id="_security_md4_gly"></span><span id="_SECURITY_MD4_GLY"></span>**MD4**
</dt> <dd>

Nombre del algoritmo CryptoAPI para el algoritmo hash MD4. Otros algoritmos hash incluyen *MD2,* *MD5* y [*SHA.*](s-gly.md)

Vea *el algoritmo MD4*.

</dd> <dt>

<span id="_security_md4_algorithm_gly"></span><span id="_SECURITY_MD4_ALGORITHM_GLY"></span>**Algoritmo MD4**
</dt> <dd>

(MD4) Algoritmo hash que crea un valor hash de 128 bits. MD4 se ha optimizado para equipos de 32 bits. Ahora se considera que se ha roto porque las colisiones se pueden encontrar de forma rápida y sencilla. MD4 fue desarrollado por RSA Data Security, Inc.

Vea también *el algoritmo MD2*, *el algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_gly"></span><span id="_SECURITY_MD5_GLY"></span>**MD5**
</dt> <dd>

Nombre del algoritmo CryptoAPI para el algoritmo hash MD5. Otros algoritmos hash incluyen *MD2,* *MD4* y [*SHA.*](s-gly.md)

Vea también el *algoritmo MD5*.

</dd> <dt>

<span id="_security_md5_algorithm_gly"></span><span id="_SECURITY_MD5_ALGORITHM_GLY"></span>**Algoritmo MD5**
</dt> <dd>

(MD5) Algoritmo hash que crea un valor hash de 128 bits. MD5 se ha optimizado para equipos de 32 bits. CryptoAPI hace referencia a este algoritmo por su identificador de algoritmo (CALG \_ MD5), name (MD5) y class (ALG \_ CLASS \_ HASH). MD5 fue desarrollado por RSA Data Security, Inc. y se especifica mediante los tipos de proveedor \_ PROV RSA \_ FULL, PROV \_ RSA \_ SIG, PROV \_ DSS, PROV \_ DSS DH y \_ PROV \_ MS \_ EXCHANGE.

Vea también *el algoritmo MD2*, *el algoritmo MD4*.

</dd> <dt>

<span id="_security_message_gly"></span><span id="_SECURITY_MESSAGE_GLY"></span>**Mensaje**
</dt> <dd>

Cualquier dato que se haya codificado para la transmisión a o recibido de una persona o entidad. Los mensajes se pueden cifrar por privacidad, firmar digitalmente con fines de autenticación o ambos.

</dd> <dt>

<span id="_security_message_digest_gly"></span><span id="_SECURITY_MESSAGE_DIGEST_GLY"></span>**síntesis del mensaje**
</dt> <dd>

Vea [*hash*](h-gly.md).

</dd> <dt>

<span id="_security_message_authentication_code_gly"></span><span id="_SECURITY_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Código de autenticación de mensajes**
</dt> <dd>

(MAC) Algoritmo hash con clave que usa una clave de sesión simétrica para ayudar a garantizar que un bloque de datos ha conservado su integridad desde el momento en que se enviaron hasta el momento en que se recibieron. Cuando se usa este tipo de algoritmo, la aplicación receptora también debe poseer la clave de sesión para volver a compilar el valor hash para que pueda comprobar que los datos base no han cambiado. CryptoAPI hace referencia a este algoritmo por su tipo \_ (CALG MAC), name (MAC) y class (ALG \_ CLASS \_ HASH).

</dd> <dt>

<span id="_security_message_encoding_type_gly"></span><span id="_SECURITY_MESSAGE_ENCODING_TYPE_GLY"></span>**tipo de codificación de mensajes**
</dt> <dd>

Define cómo se codifica el mensaje. El tipo de codificación del mensaje se almacena en la palabra de orden superior de la estructura del tipo de codificación. Los tipos de codificación definidos actualmente son: CRYPT \_ ASN \_ ENCODING, X509 \_ ASN \_ ENCODING y PKCS \_ 7 \_ ASN \_ ENCODING.

</dd> <dt>

<span id="_security_message_management_functions_gly"></span><span id="_SECURITY_MESSAGE_MANAGEMENT_FUNCTIONS_GLY"></span>**funciones de administración de mensajes**
</dt> <dd>

Funciones que proporcionan dos niveles de administración de mensajes: funciones de mensaje de bajo nivel y funciones de mensaje simplificadas. Las funciones de mensaje de bajo nivel proporcionan más flexibilidad que las funciones de mensaje simplificadas. sin embargo, requieren más llamadas de función.

</dd> <dt>

<span id="_security_message_signing_functions_gly"></span><span id="_SECURITY_MESSAGE_SIGNING_FUNCTIONS_GLY"></span>**funciones de firma de mensajes**
</dt> <dd>

Funciones que se usan para firmar mensajes y datos.

Consulte también funciones [*de mensaje simplificadas.*](s-gly.md)

</dd> <dt>

<span id="_security_mpr_gly"></span><span id="_SECURITY_MPR_GLY"></span>**MPR**
</dt> <dd>

Vea *Multiple Provider Router (Enrutador de varios proveedores).*

</dd> <dt>

<span id="_security_multiple_provider_router_gly"></span><span id="_SECURITY_MULTIPLE_PROVIDER_ROUTER_GLY"></span>**Enrutador de varios proveedores**
</dt> <dd>

(MPR) Componente del sistema que controla las comunicaciones entre el sistema y todos los proveedores de red. MpR llama a las funciones del proveedor de red que expone cada proveedor de red.

</dd> </dl>

 

 



