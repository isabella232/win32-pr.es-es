---
description: Estos son los códigos de error en tiempo de ejecución, definidos en Cryptxml.h, que pueden devolver las funciones CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Códigos de error CryptXML (Cryptxml.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccb4b06070ca77f8b55f96d3e6c4732abc22c26970b83b6a70c720b7bade8a84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767982"
---
# <a name="cryptxml-error-codes"></a>Códigos de error CryptXML

Estos son los códigos de error en tiempo de ejecución, definidos en Cryptxml.h, que pueden devolver las funciones CryptXML.



| Constante o valor                                                                                                                                                                                                                                                                             | Descripción                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**CRYPT \_ XML \_ E \_ LARGE**</dt> <dt>0x80092101L</dt> </dl>                                               | El valor proporcionado es demasiado grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**CRYPT \_ \_CODIFICACIÓN \_ XML E**</dt> <dt>0x80092103L</dt> </dl>                                      | No se admite la codificación XML especificada.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**CRYPT \_ XML \_ E \_ ALGORITHM**</dt> <dt>0x80092104L</dt> </dl>                                   | No se admite el algoritmo XML especificado.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**CRYPT \_ XML \_ E \_ TRANSFORM**</dt> <dt>0x80092105L</dt> </dl>                                   | No se admite la transformación especificada.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**CRYPT \_ IDENTIFICADOR \_ DE \_ E XML**</dt> <dt>0x80092106L</dt> </dl>                                            | El identificador proporcionado no es válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**CRYPT \_ XML \_ E \_ OPERATION**</dt> <dt>0x80092107L</dt> </dl>                                   | La operación no es válida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**CRYPT \_ REFERENCIA \_ XML E SIN \_ \_ RESOLVER**</dt> <dt>0x80092108L</dt> </dl> | No se puede resolver el **elemento Reference.**<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ DIGEST**</dt> <dt>0x80092109L</dt> </dl>                   | El valor de resumen no es válido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ SIGNATURE**</dt> <dt>0x8009210AL</dt> </dl>          | El valor de la firma no es válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**CRYPT \_ ERROR \_ HASH \_ XML \_ E**</dt> <dt>0x8009210BL</dt> </dl>                            | No se puede crear ni calcular el hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**CRYPT \_ ERROR \_ DE XML E \_ SIGN \_**</dt> <dt>0x8009210CL</dt> </dl>                            | Error en la operación de firma criptográfica.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**CRYPT \_ XML \_ E \_ VERIFY \_ FAILED**</dt> <dt>0x8009210DL</dt> </dl>                      | Error en la comprobación de la firma.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**CRYPT \_ XML \_ E \_ \_ \_ DEMASIADAS FIRMAS**</dt> <dt>0x8009210EL</dt> </dl>   | El número de **elementos Signature** del documento superó el límite máximo permitido para el procesamiento.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**CRYPT \_ XML \_ E \_ INVALID \_ KEYVALUE**</dt> <dt>0x8009210FL</dt> </dl>             | El valor de clave proporcionado no es válido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**CRYPT \_ XML \_ E \_ UNEXPECTED \_ XML**</dt> <dt>0x80092110L</dt> </dl>                   | Se encontró UN XML no válido o inesperado.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**CRYPT \_ XML \_ E \_ SIGNER**</dt> <dt>0x80092111L</dt> </dl>                                            | No se puede encontrar la clave del firmante.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**CRYPT \_ XML \_ E NON UNIQUE \_ \_ \_ ID**</dt> <dt>0x80092112L</dt> </dl>                     | Se encontró un atributo **id.** no único.<br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                               |
| Header<br/>                   | <dl> <dt>Cryptxml.h</dt> </dl> |



 

 




