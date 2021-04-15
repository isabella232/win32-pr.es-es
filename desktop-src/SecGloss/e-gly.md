---
description: Contiene definiciones de términos de seguridad que comienzan por la letra E.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f1caccd2-3453-448e-b194-bf899eff8091
title: E (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed30465ef5764d4553ceb03e1094b73d940f85f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546115"
---
# <a name="e-security-glossary"></a>E (Glosario de seguridad)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) E F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**BCE**
</dt> <dd>

Consulte *Electronic Codebook*.

</dd> <dt>

<span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**ECC**
</dt> <dd>

Consulte *criptografía de curva elíptica*.

</dd> <dt>

<span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**EFS**
</dt> <dd>

Vea *sistema de cifrado de archivos*.

</dd> <dt>

<span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**
</dt> <dd>

Consulte *uso mejorado de claves*.

</dd> <dt>

<span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**Codebook electrónico**
</dt> <dd>

BCE Un modo de cifrado de bloques (cada bloque se cifra individualmente) que no usa ningún comentario. Esto significa que cualquier bloque de texto simple que sea idéntico (ya sea en el mismo mensaje o en un mensaje diferente que esté cifrado con la misma clave) se transforma en bloques de texto cifrado idénticos. Los vectores de inicialización no se pueden usar con este modo de cifrado. Si un solo bit del bloque de texto cifrado es ilegible, todo el bloque de texto no cifrado correspondiente también es ilegible.

</dd> <dt>

<span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**criptografía de curva elíptica**
</dt> <dd>

ECC Un enfoque para la criptografía de clave pública basado en las propiedades de las curvas elípticas. La principal ventaja de ECC es la eficacia, lo que es importante, ya que los dispositivos se vuelven más pequeños y los requisitos de seguridad se consumen más. Por ejemplo, las claves ECC entre 163 bits y 512 bits son de la sexta a la trigésima el tamaño de las claves RSA de nivel de seguridad equivalentes. A medida que el tamaño de clave aumenta la eficiencia relativa de los aumentos ECC.

</dd> <dt>

<span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**codificación**
</dt> <dd>

El proceso de convertir datos en una secuencia de bits. La codificación es parte del proceso de serialización que convierte datos en una secuencia de unos y ceros.

</dd> <dt>

<span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**tipo de codificación**
</dt> <dd>

Hace referencia al tipo de codificación que se usa para el certificado y la codificación de mensajes. Los tipos de codificación se especifican como **DWORD**, con el tipo de codificación de certificado almacenada en la palabra de orden inferior y el tipo de codificación de mensajes almacenada en la palabra de orden superior. Aunque algunas funciones o campos de estructura requieren solo uno de los tipos de codificación, siempre es aceptable especificar ambos.

</dd> <dt>

<span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**cifra**
</dt> <dd>

Proceso de convertir texto sin formato en texto cifrado para evitar que una entidad no autorizada pueda leerlo y entenderlo. El cifrado es lo contrario del descifrado.

</dd> <dt>

<span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**datos cifrados**
</dt> <dd>

Datos que se han convertido de texto sin formato en texto cifrado. Los mensajes cifrados se usan para disfrazar el contenido de un mensaje cuando se envía o se almacena.

</dd> <dt>

<span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**Sistema de cifrado de archivos**
</dt> <dd>

EFS Característica del sistema operativo Windows que permite a los usuarios cifrar archivos y carpetas en un disco de volumen NTFS para que se puedan proteger contra el acceso a los intrusos.

</dd> <dt>

<span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**funciones de cifrado y descifrado**
</dt> <dd>

Funciones de mensaje simplificadas utilizadas para codificar y cifrar (o descodificar y descifrar) los datos. Como conjunto, estas funciones incluyen compatibilidad para cifrar y descifrar datos simultáneamente.

Vea también [*funciones de mensaje simplificadas*](s-gly.md).

</dd> <dt>

<span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**tipo de contenido mejorado**
</dt> <dd>

Una clase de datos contenida en un \# mensaje PKCS 7 que contiene datos (posiblemente cifrados), además de mejoras criptográficas, como los valores hash o las firmas. Entre los tipos de datos mejorados definidos por PKCS \# 7 se incluyen los datos firmados, los datos con doble cifrado, los datos con doble cifrado y los datos con signo (hash).

</dd> <dt>

<span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**uso mejorado de clave**
</dt> <dd>

EKU Una extensión de certificado y un valor de propiedad extendida de certificado. Un EKU especifica los usos para los que un certificado es válido.

</dd> <dt>

<span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**tipo de contenido de datos con doble cifrado**
</dt> <dd>

\#Contenido mejorado PKCS 7 que consta de contenido cifrado (de cualquier tipo) y claves de cifrado de contenido (para uno o más destinatarios). La combinación de contenido cifrado y clave de cifrado para un destinatario se denomina *sobre digital* para ese destinatario. Este tipo de mensaje debe usarse cuando se desea mantener el contenido del mensaje secreto y permitir que solo las personas o entidades especificadas recuperen el contenido.

</dd> <dt>

<span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**clave de intercambio**
</dt> <dd>

Consulte *par de claves de Exchange*.

</dd> <dt>

<span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**par de claves de intercambio**
</dt> <dd>

Un par de claves pública/privada usada para cifrar claves de sesión para que se puedan almacenar e intercambiar con otros usuarios de forma segura. Los pares de claves de Exchange se crean mediante una llamada a la función **CryptGenKey** .

[*Par de claves*](s-gly.md)de la firma de comparación.

</dd> <dt>

<span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**almacén externo**
</dt> <dd>

Almacén de certificados que mantiene sus certificados, CRL y CTL en una ubicación externa a la memoria caché, como en una base de datos de un servidor de red. Un almacén externo no lee ni descodifica sus certificados, CRL y CTL cuando se llama a la función **CertOpenStore** . La lectura y la descodificación se aplazan hasta que se llama a un método de enumeración o búsqueda.

</dd> </dl>

 

 



