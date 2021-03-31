---
description: Se usa con las funciones BCryptGetProperty y BCryptSetProperty para identificar una propiedad.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propiedad primitiva de criptografía (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907651"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificadores de propiedad primitiva de criptografía

Los valores siguientes se usan con las funciones [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) y [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar una propiedad.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nombre del algoritmo BCRYPT \_**
</dt> <dd> <dl> <dt>

L "AlgorithmName"
</dt> <dt>



Una cadena Unicode terminada en null que contiene el nombre del algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_longitud de \_ etiqueta de autenticación de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "AuthTagLength"
</dt> <dt>



Longitudes de las etiquetas de autenticación admitidas por el algoritmo. Esta propiedad es una estructura de [**struct de longitud de \_ etiquetas de autenticación \_ \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Esta propiedad solo se aplica a los algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_longitud del bloque BCRYPT \_**
</dt> <dd> <dl> <dt>

L "BlockLength"
</dt> <dt>



Tamaño, en bytes, de un bloque de cifrado para el algoritmo. Esta propiedad solo se aplica a los algoritmos de cifrado de bloques. Este tipo de datos es un **valor DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_lista de \_ tamaños de bloque BCRYPT \_**
</dt> <dd> <dl> <dt>

L "BlockSizeList"
</dt> <dt>



Una lista de las longitudes de bloque que admite un algoritmo de cifrado. Este tipo de datos es una matriz de **DWords**. El número de elementos de la matriz se puede determinar dividiendo el número de bytes recuperados por el tamaño de un único **DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modo de encadenamiento BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ChainingMode"
</dt> <dt>



Puntero a una cadena Unicode terminada en null que representa el modo de encadenamiento del algoritmo de cifrado. Esta propiedad se puede establecer en un identificador de algoritmo o en un identificador de clave para uno de los valores siguientes.



| Identificador                   | Value                         | Descripción                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_modo de cadena BCRYPT \_ \_ CBC** | L "ChainingModeCBC"<br/> | Establece el modo de encadenamiento del algoritmo en el [*encadenamiento de bloques de cifrado*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **\_CCM del \_ modo de cadena BCRYPT \_** | L "ChainingModeCCM"<br/> | Establece el modo de encadenamiento del algoritmo en el modo CBC-MAC (CCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.<br/> <br/> |
| **\_modo de cadena BCRYPT \_ \_ CFB** | L "ChainingModeCFB"<br/> | Establece el modo de encadenamiento del algoritmo en los [*comentarios de cifrado*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **\_ECB del \_ modo de cadena BCRYPT \_** | L "ChainingModeECB"<br/> | Establece el modo de encadenamiento del algoritmo en [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **\_modo de cadena BCRYPT \_ \_ GCM** | L "ChainingModeGCM"<br/> | Establece el modo de encadenamiento del algoritmo en el modo de Galois/contador (GCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.<br/> <br/>       |
| **\_modo de cadena BCRYPT \_ \_ na**  | L "ChainingModeN/A"<br/> | El algoritmo no admite el encadenamiento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_parámetros DH de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Especifica los parámetros que se van a usar con una clave de Diffie-Hellman. Este tipo de datos es un puntero a una estructura de [**\_ encabezado de \_ parámetro \_ de BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parámetros DSA de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "DSAParameters"
</dt> <dt>



Especifica los parámetros que se van a usar con una clave DSA. Esta propiedad es un [**\_ encabezado de \_ parámetro \_ DSA de bcrypt**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) o una estructura de [**encabezado del \_ parámetro DSA de bcrypt \_ \_ \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.

**Windows 8:** A partir de Windows 8, esta propiedad puede ser una estructura de [**\_ encabezado del parámetro DSA de BCRYPT \_ \_ \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Use esta estructura si el tamaño de clave supera los 1024 bits y es menor o igual que 3072 bits. Si el tamaño de la clave es mayor o igual que 512 pero menor o igual que 1024 bits, use la estructura de [**\_ \_ \_ encabezado del parámetro DSA de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_longitud de \_ clave \_ efectiva BCRYPT**
</dt> <dd> <dl> <dt>

L "EffectiveKeyLength"
</dt> <dt>



Tamaño, en bits, de la longitud efectiva de una clave RC2. Este tipo de datos es un **valor DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_longitud del \_ bloque \_ hash de BCRYPT**
</dt> <dd> <dl> <dt>

L "HashBlockLength"
</dt> <dt>



Tamaño, en bytes, del bloque de un valor hash. Esta propiedad solo se aplica a los algoritmos hash. Este tipo de datos es un **valor DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_longitud del hash de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "HashDigestLength"
</dt> <dt>



Tamaño, en bytes, del valor hash de un proveedor hash. Este tipo de datos es un **valor DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_lista de \_ OID \_ hash de BCRYPT**
</dt> <dd> <dl> <dt>

L "HashOIDList"
</dt> <dt>



Lista de [*identificadores de objeto*](/windows/desktop/SecGloss/o-gly) hash (OID) con codificación [*der*](/windows/desktop/SecGloss/d-gly). Esta propiedad es una estructura de [**\_ \_ lista de OID de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) . Esta propiedad solo se puede leer.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_Vector de inicialización de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Contiene el [*Vector de inicialización*](/windows/desktop/SecGloss/i-gly) (IV) para una clave. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**longitud de la \_ clave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyLength"
</dt> <dt>



Tamaño, en bits, del valor de clave de un proveedor de claves simétricas. Este tipo de datos es un **valor DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_longitudes de clave de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyLengths"
</dt> <dt>



Longitudes de clave admitidas por el algoritmo. Esta propiedad es una estructura de [**\_ \_ \_ struct de longitudes de clave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Esta propiedad solo se aplica a los algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_longitud del \_ objeto de clave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyObjectLength"
</dt> <dt>



No se usa esta propiedad. La propiedad de **\_ \_ longitud del objeto BCRYPT** se usa para obtener esta información.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_nivel de clave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "KeyStrength"
</dt> <dt>



Número de bits de la clave. Este tipo de datos es un **valor DWORD**. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_longitud del \_ bloque de mensajes BCRYPT \_**
</dt> <dd> <dl> <dt>

L "MessageBlockLength"
</dt> <dt>



Se puede establecer en cualquier identificador de clave que tenga establecido el modo de encadenamiento CFB. De forma predeterminada, esta propiedad se establece en 1 para CFB de 8 bits. Si se establece en el tamaño de bloque en bytes, se usará CFB de bloque completo. En el caso de las claves XTS, se usa para establecer el tamaño, en bytes, de la unidad de datos XTS (normalmente 512 o 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_longitud de varios \_ objetos \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "MultiObjectLength"
</dt> <dt>



Esta propiedad devuelve una [**\_ estructura de \_ \_ longitud \_ de varios objetos BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contiene la información necesaria para calcular el tamaño de un búfer de objetos. Esta propiedad solo se admite en las versiones de sistema operativo que admiten la función [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_longitud del objeto BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ObjectLength"
</dt> <dt>



Tamaño, en bytes, del subobjeto de un proveedor. Este tipo de datos es un **valor DWORD**. Actualmente, los proveedores de algoritmos hash y algoritmos de cifrado simétrico utilizan búferes asignados por el autor de la llamada para almacenar sus subobjetos. Por ejemplo, el proveedor hash requiere que asigne memoria para el objeto hash obtenido con la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Esta propiedad proporciona el tamaño de búfer para el objeto de un proveedor, de modo que pueda asignar memoria para el objeto creado por el proveedor.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_esquemas de relleno de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "PaddingSchemes"
</dt> <dt>



Representa el esquema de relleno del proveedor de algoritmos RSA. Este tipo de datos es un **valor DWORD**. Puede ser uno de los valores siguientes.



| Identificador                             | Value      | Descripción                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **el \_ \_ enrutador de controlador compatible con BCRYPT \_**     | 0x00000001 | El proveedor admite el relleno agregado por el enrutador.         |
| **El \_ controlador compatible con BCRYPT \_ \_ PKCS1 \_ enc** | 0x00000002 | El proveedor admite el esquema de relleno de cifrado PKCS1. |
| **BCRYPT \_ compatible con la \_ almohadilla \_ PKCS1 \_** | 0x00000004 | El proveedor admite el esquema de relleno de firmas PKCS1.  |
| **se \_ admitía el \_ panel \_ OAEP**       | 0x00000008 | El proveedor admite el esquema de relleno OAEP.             |
| **\_controlador compatible con BCRYPT \_ \_ PSS**        | 0x00000010 | El proveedor admite el esquema de relleno de PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_identificador del proveedor de BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ProviderHandle"
</dt> <dt>



Identificador del proveedor de CNG que creó el objeto pasado en el parámetro *hObject* . Este tipo de datos es **un \_ \_ identificador ALG de BCRYPT**. Esta propiedad solo se puede recuperar; no se puede establecer.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**longitud de la firma de BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "SignatureLength"
</dt> <dt>



Tamaño, en bytes, de la longitud de una firma para una clave. Este tipo de datos es un **valor DWORD**. Esta propiedad solo se aplica a las claves. Esta propiedad solo se puede recuperar; no se puede establecer.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                      |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



 

