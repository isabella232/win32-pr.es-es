---
description: Se usa con las funciones BCryptGetProperty y BCryptSetProperty para identificar una propiedad.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propiedad primitivos de criptografía (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5452c6a55388998a08577cb19ef2fba6905faddbdf28f5f8051b7bc8d9d1c375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908226"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificadores de propiedad primitivos de criptografía

Los valores siguientes se usan con las [**funciones BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) y [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar una propiedad.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**NOMBRE DEL ALGORITMO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"AlgorithmName"
</dt> <dt>



Cadena Unicode terminada en NULL que contiene el nombre del algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**LONGITUD DE \_ ETIQUETA DE AUTENTICACIÓN \_ DE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"AuthTagLength"
</dt> <dt>



Longitudes de etiquetas de autenticación admitidas por el algoritmo. Esta propiedad es una [**estructura \_ STRUCT AUTH \_ TAG \_ LENGTHS \_ de BCRYPT.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Esta propiedad solo se aplica a los algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**LONGITUD DEL BLOQUE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"BlockLength"
</dt> <dt>



Tamaño, en bytes, de un bloque de cifrado para el algoritmo. Esta propiedad solo se aplica a los algoritmos de cifrado de bloques. Este tipo de datos es **DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT \_ BLOCK \_ SIZE \_ LIST**
</dt> <dd> <dl> <dt>

L"BlockSizeList"
</dt> <dt>



Lista de las longitudes de bloque admitidas por un algoritmo de cifrado. Este tipo de datos es una matriz **de DWORD.** El número de elementos de la matriz se puede determinar dividiendo el número de bytes recuperados por el tamaño de un **único DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**MODO DE \_ ENCADENAMIENTO DE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"ChainingMode"
</dt> <dt>



Puntero a una cadena Unicode terminada en NULL que representa el modo de encadenamiento del algoritmo de cifrado. Esta propiedad se puede establecer en un identificador de algoritmo o en un identificador de clave en uno de los valores siguientes.



| Identificador                   | Value                         | Descripción                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BCRYPT \_ CHAIN \_ MODE \_ CBC** | L"ChainingModeCBC"<br/> | Establece el modo de encadenamiento del algoritmo en [*el encadenamiento de bloques de cifrado.*](/windows/desktop/SecGloss/c-gly)<br/>            |
| **CCM del MODO \_ \_ DE CADENA \_ BCRYPT** | L"ChainingModeCCM"<br/> | Establece el modo de encadenamiento del algoritmo en contador con el modo CBC-MAC (CCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.<br/> <br/> |
| **BCRYPT \_ CHAIN \_ MODE \_ CFB** | L"ChainingModeCFB"<br/> | Establece el modo de encadenamiento del algoritmo para cifrar [*los comentarios*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **BCRYPT \_ CHAIN \_ MODE \_ ECB** | L"ChainingModeECB"<br/> | Establece el modo de encadenamiento del algoritmo en [*el cuaderno de códigos electrónico*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **BCRYPT \_ CHAIN \_ MODE \_ GCM** | L"ChainingModeGCM"<br/> | Establece el modo de encadenamiento del algoritmo en el modo Galois/counter (GCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.<br/> <br/>       |
| **BCRYPT \_ CHAIN \_ MODE \_ NA**  | L"ChainingModen/A"<br/> | El algoritmo no admite el encadenamiento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**PARÁMETROS DH DE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Especifica los parámetros que se usarán con Diffie-Hellman clave. Este tipo de datos es un puntero a una estructura [**\_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT \_ DSA \_ PARAMETERS**
</dt> <dd> <dl> <dt>

L"DSAParameters"
</dt> <dt>



Especifica los parámetros que se usarán con una clave DSA. Esta propiedad es una [**estructura \_ BCRYPT DSA \_ PARAMETER HEADER \_ o**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) [**BCRYPT \_ DSA \_ PARAMETER HEADER \_ \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.

**Windows 8:** A partir Windows 8, esta propiedad puede ser una estructura [**\_ BCRYPT DSA \_ PARAMETER HEADER \_ \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Use esta estructura si el tamaño de clave supera los 1024 bits y es menor o igual que 3072 bits. Si el tamaño de clave es mayor o igual que 512 pero menor o igual que 1024 bits, use la estructura DE ENCABEZADO DE PARÁMETRO [**\_ DSA \_ \_ de BCRYPT.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**LONGITUD DE \_ CLAVE EFECTIVA \_ DE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"EffectiveKeyLength"
</dt> <dt>



Tamaño, en bits, de la longitud efectiva de una clave RC2. Este tipo de datos es **DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**LONGITUD DEL \_ BLOQUE HASH \_ BCRYPT \_**
</dt> <dd> <dl> <dt>

L"HashBlockLength"
</dt> <dt>



Tamaño, en bytes, del bloque para un hash. Esta propiedad solo se aplica a los algoritmos hash. Este tipo de datos es **DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**LONGITUD DE HASH DE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"HashDigestLength"
</dt> <dt>



Tamaño, en bytes, del valor hash de un proveedor hash. Este tipo de datos es **DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT \_ HASH \_ OID \_ LIST**
</dt> <dd> <dl> <dt>

L"HashOIDList"
</dt> <dt>



Lista de identificadores de objetos hash (UNIDADES) [*codificados*](/windows/desktop/SecGloss/o-gly) por [*DER.*](/windows/desktop/SecGloss/d-gly) Esta propiedad es una [**estructura \_ BCRYPT OID \_ LIST.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Esta propiedad solo se puede leer.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**VECTOR DE \_ INICIALIZACIÓN DE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"IV"
</dt> <dt>



Contiene el [*vector de inicialización*](/windows/desktop/SecGloss/i-gly) (IV) de una clave. Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**LONGITUD DE \_ CLAVE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"KeyLength"
</dt> <dt>



Tamaño, en bits, del valor de clave de un proveedor de claves simétrico. Este tipo de datos es **DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**LONGITUDES \_ DE CLAVE \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"KeyLengths"
</dt> <dt>



Longitudes de clave admitidas por el algoritmo. Esta propiedad es una [**estructura \_ \_ \_ STRUCT BCRYPT KEY LENGTHS.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Esta propiedad solo se aplica a los algoritmos.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT \_ KEY \_ OBJECT \_ LENGTH**
</dt> <dd> <dl> <dt>

L"KeyObjectLength"
</dt> <dt>



No se usa esta propiedad. La **propiedad \_ BCRYPT OBJECT \_ LENGTH** se usa para obtener esta información.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**SEGURIDAD DE LA \_ CLAVE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"KeyStrength"
</dt> <dt>



Número de bits de la clave. Este tipo de datos es **DWORD.** Esta propiedad solo se aplica a las claves.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**LONGITUD DEL BLOQUE \_ DE \_ MENSAJES DE \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"MessageBlockLength"
</dt> <dt>



Esto se puede establecer en cualquier identificador de clave que tenga establecido el modo de encadenamiento CFB. De forma predeterminada, esta propiedad se establece en 1 para CFB de 8 bits. Si se establece en el tamaño de bloque en bytes, se usará CFB de bloque completo. Para las claves XTS se usa para establecer el tamaño, en bytes, de la unidad de datos XTS (normalmente 512 o 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**LONGITUD DE \_ VARIOS \_ OBJETOS DE \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"MultiObjectLength"
</dt> <dt>



Esta propiedad devuelve un [**\_ \_ \_ \_ STRUCT BCRYPT MULTI OBJECT LENGTH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contiene la información necesaria para calcular el tamaño de un búfer de objetos. Esta propiedad solo se admite en las versiones del sistema operativo que admiten [**la función BCryptCreateMultiHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**LONGITUD DEL OBJETO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"ObjectLength"
</dt> <dt>



Tamaño, en bytes, del subobjeto de un proveedor. Este tipo de datos es **DWORD.** Actualmente, los proveedores de algoritmos de cifrado hash y simétrico usan búferes asignados por el autor de la llamada para almacenar sus subobjetos. Por ejemplo, el proveedor de hash requiere que asigne memoria para el objeto hash obtenido con la [**función BCryptCreateHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) Esta propiedad proporciona el tamaño de búfer para el objeto de un proveedor para que pueda asignar memoria para el objeto creado por el proveedor.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**ESQUEMAS DE \_ RELLENO DE BCRYPT \_**
</dt> <dd> <dl> <dt>

L"PaddingSchemes"
</dt> <dt>



Representa el esquema de relleno del proveedor de algoritmos RSA. Este tipo de datos es **DWORD.** Puede ser uno de los siguientes valores.



| Identificador                             | Value      | Descripción                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **ENRUTADOR DE \_ \_ PANEL COMPATIBLE CON BCRYPT \_**     | 0x00000001 | El proveedor admite el relleno agregado por el enrutador.         |
| **BCRYPT \_ SUPPORTED \_ PAD \_ PKCS1 \_ ENC** | 0x00000002 | El proveedor admite el esquema de relleno de cifrado PKCS1. |
| **BCRYPT \_ SUPPORTED \_ PAD \_ PKCS1 \_ SIG** | 0x00000004 | El proveedor admite el esquema de relleno de firma PKCS1.  |
| **\_OAEP DE PANEL COMPATIBLE \_ \_ CON BCRYPT**       | 0x00000008 | El proveedor admite el esquema de relleno OAEP.             |
| **PSS \_ \_ DE PANEL COMPATIBLE CON \_ BCRYPT**        | 0x00000010 | El proveedor admite el esquema de relleno de PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**IDENTIFICADOR DEL PROVEEDOR DE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"ProviderHandle"
</dt> <dt>



Identificador del proveedor de CNG que creó el objeto pasado en el *parámetro hObject.* Este tipo de datos es **un identificador \_ de BCRYPT ALG \_**. Esta propiedad solo se puede recuperar; no se puede establecer.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**LONGITUD DE FIRMA DE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"SignatureLength"
</dt> <dt>



Tamaño, en bytes, de la longitud de una firma para una clave. Este tipo de datos es **DWORD.** Esta propiedad solo se aplica a las claves. Esta propiedad solo se puede recuperar; no se puede establecer.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                      |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



 

