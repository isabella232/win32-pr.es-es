---
description: Contiene definiciones de términos de seguridad que comienzan por la letra H.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 4165b820-30fc-477e-a690-81109f161323
title: H (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 665cd90cfc8a849030b6a1cfd1cb4e6d6f687557
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361823"
---
# <a name="h-security-glossary"></a>H (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F G [H](g-gly.md) [I](i-gly.md) J [K](k-gly.md) L [M](l-gly.md) [N](m-gly.md) [O](n-gly.md) [](o-gly.md) [P P](p-gly.md) [Q R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_handle_gly"></span><span id="_SECURITY_HANDLE_GLY"></span>**Manejar**
</dt> <dd>

Token que se usa para identificar o acceder a un objeto, como el identificador de un proveedor criptográfico, un almacén de certificados, un mensaje o un par de claves.

</dd> <dt>

<span id="_security_hash_gly"></span><span id="_SECURITY_HASH_GLY"></span>**Hash**
</dt> <dd>

Resultado de tamaño fijo obtenido mediante la aplicación de una función matemática (el *algoritmo hash*) a una cantidad arbitraria de datos. (también conocido como "resumen del mensaje").

Vea también *funciones hash.*

</dd> <dt>

<span id="_security_hash_object_gly"></span><span id="_SECURITY_HASH_OBJECT_GLY"></span>**objeto hash**
</dt> <dd>

Objeto que se usa para hash de mensajes o claves de sesión. El objeto hash se crea mediante una llamada a **CryptCreateHash.** El CSP especificado en la llamada define la definición del objeto .

</dd> <dt>

<span id="_security_hashing_algorithm_gly"></span><span id="_SECURITY_HASHING_ALGORITHM_GLY"></span>**algoritmo hash**
</dt> <dd>

Un algoritmo utilizado para generar un valor hash de una parte de datos, como un mensaje o clave de sesión. Entre los algoritmos más comunes de hash se incluyen: MD2, MD4, MD5 y SHA-1.

</dd> <dt>

<span id="_security_hashing_functions_gly"></span><span id="_SECURITY_HASHING_FUNCTIONS_GLY"></span>**funciones hash**
</dt> <dd>

Conjunto de funciones que se usan para crear y destruir objetos hash, obtener o establecer los parámetros de un objeto hash y datos hash y claves de sesión.

</dd> <dt>

<span id="_security_hash_based_message_authentication_code_gly"></span><span id="_SECURITY_HASH_BASED_MESSAGE_AUTHENTICATION_CODE_GLY"></span>**Código de autenticación de mensajes basado en hash**
</dt> <dd>

(HMAC) Algoritmo hash con clave simétrica implementado por proveedores de servicios criptográficos de Microsoft. Un HMAC se usa para comprobar la integridad de los datos para ayudar a garantizar que no se han modificado durante el almacenamiento o el tránsito. Se puede usar con cualquier algoritmo hash criptográfico iterado, como MD5 o SHA-1. CryptoAPI hace referencia a este algoritmo por su identificador de algoritmo (CALG \_ HMAC) y la clase (ALG \_ CLASS \_ HASH).

Consulte también Código [*de autenticación de mensajes*](m-gly.md).

</dd> <dt>

<span id="_security_hcsbc_gly"></span><span id="_SECURITY_HCSBC_GLY"></span>**HCSBC**
</dt> <dd>

Tipo de datos que actúa como identificador de un contexto de copia de seguridad de Servicios de certificados. Su rol es mantener el estado de contexto entre el servidor y las API de copia de seguridad cuando se realiza una copia de seguridad.

</dd> <dt>

<span id="_security_hmac_gly"></span><span id="_SECURITY_HMAC_GLY"></span>**HMAC**
</dt> <dd>

Vea *Código de autenticación de mensajes basado en hash.*

</dd> </dl>

 

 



