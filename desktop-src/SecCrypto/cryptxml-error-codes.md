---
description: A continuación se muestran los códigos de error en tiempo de ejecución, definidos en Cryptxml. h, que pueden ser devueltos por las funciones de CryptXML.
ms.assetid: c3678767-aab3-4771-b2f2-8d79545d420d
title: Códigos de error de CryptXML (Cryptxml. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5906c406f14081844ddce042f0e170668950e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669736"
---
# <a name="cryptxml-error-codes"></a>Códigos de error de CryptXML

A continuación se muestran los códigos de error en tiempo de ejecución, definidos en Cryptxml. h, que pueden ser devueltos por las funciones de CryptXML.



| Constante o valor                                                                                                                                                                                                                                                                             | Descripción                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_E_LARGE"></span><span id="crypt_xml_e_large"></span><dl> <dt>**Cifrado \_ XML \_ E \_**</dt> <dt>0x80092101L</dt> grande </dl>                                               | El valor proporcionado es demasiado grande.<br/>                                                                        |
| <span id="CRYPT_XML_E_ENCODING"></span><span id="crypt_xml_e_encoding"></span><dl> <dt>**Cifrado \_ \_Codificación E \_ codificación XML**</dt> <dt>0x80092103L</dt> </dl>                                      | No se admite la codificación XML especificada.<br/>                                                              |
| <span id="CRYPT_XML_E_ALGORITHM"></span><span id="crypt_xml_e_algorithm"></span><dl> <dt>**Cifrado \_ 0x80092104L \_ de \_ algoritmo XML E**</dt> <dt></dt> </dl>                                   | No se admite el algoritmo XML especificado.<br/>                                                             |
| <span id="CRYPT_XML_E_TRANSFORM"></span><span id="crypt_xml_e_transform"></span><dl> <dt>**Cifrado \_ XML \_ E \_ transformación**</dt> <dt>0x80092105L</dt> </dl>                                   | No se admite la transformación especificada.<br/>                                                                 |
| <span id="CRYPT_XML_E_HANDLE"></span><span id="crypt_xml_e_handle"></span><dl> <dt>**Cifrado \_ \_ \_ Identificador E**</dt> <dt>0x80092106L</dt> XML </dl>                                            | El identificador proporcionado no es válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_OPERATION"></span><span id="crypt_xml_e_operation"></span><dl> <dt>**Cifrado \_ \_ \_ Operación E**</dt> <dt>0x80092107L</dt> XML </dl>                                   | La operación no es válida.<br/>                                                                             |
| <span id="CRYPT_XML_E_UNRESOLVED_REFERENCE"></span><span id="crypt_xml_e_unresolved_reference"></span><dl> <dt>**Cifrado \_ \_ \_ \_ Referencia no resuelta de XML E**</dt> <dt>0x80092108L</dt> </dl> | No se puede resolver el elemento de **referencia** .<br/>                                                            |
| <span id="CRYPT_XML_E_INVALID_DIGEST"></span><span id="crypt_xml_e_invalid_digest"></span><dl> <dt>**Cifrado \_ XML \_ E 0x80092109L de \_ \_ Resumen no válidos**</dt> <dt></dt> </dl>                   | El valor de síntesis no es válido.<br/>                                                                          |
| <span id="CRYPT_XML_E_INVALID_SIGNATURE"></span><span id="crypt_xml_e_invalid_signature"></span><dl> <dt>**Cifrado \_ XML \_ E \_ \_ signatura no válida**</dt> <dt>0x8009210AL</dt> </dl>          | El valor de signatura no es válido.<br/>                                                                       |
| <span id="CRYPT_XML_E_HASH_FAILED"></span><span id="crypt_xml_e_hash_failed"></span><dl> <dt>**Cifrado \_ \_Error de \_ hash \_ de XML E**</dt> <dt>0x8009210BL</dt> </dl>                            | No se puede crear o calcular el hash.<br/>                                                                 |
| <span id="CRYPT_XML_E_SIGN_FAILED"></span><span id="crypt_xml_e_sign_failed"></span><dl> <dt>**Cifrado \_ \_Error de \_ signo \_ E de XML**</dt> <dt>0x8009210CL</dt> </dl>                            | Error en la operación de firma criptográfica.<br/>                                                           |
| <span id="CRYPT_XML_E_VERIFY_FAILED"></span><span id="crypt_xml_e_verify_failed"></span><dl> <dt>**Cifrado \_ \_Error de \_ comprobación \_ de XML E**</dt> <dt>0x8009210DL</dt> </dl>                      | Error en la comprobación de la firma.<br/>                                                                      |
| <span id="CRYPT_XML_E_TOO_MANY_SIGNATURES"></span><span id="crypt_xml_e_too_many_signatures"></span><dl> <dt>**Cifrado \_ XML \_ E \_ demasiadas \_ \_ firmas**</dt> <dt>0x8009210EL</dt> </dl>   | El número de elementos de **firma** del documento superó el límite máximo permitido para el procesamiento.<br/> |
| <span id="CRYPT_XML_E_INVALID_KEYVALUE"></span><span id="crypt_xml_e_invalid_keyvalue"></span><dl> <dt>**Cifrado \_ 0x8009210FL \_ \_ no válido de \_ KEYVALUE XML**</dt> <dt></dt> </dl>             | El valor de clave proporcionado no es válido.<br/>                                                           |
| <span id="CRYPT_XML_E_UNEXPECTED_XML"></span><span id="crypt_xml_e_unexpected_xml"></span><dl> <dt>**Cifrado \_ XML \_ E \_ inesperado \_ XML**</dt> <dt>0x80092110L</dt> </dl>                   | Se encontró XML no válido o inesperado.<br/>                                                              |
| <span id="CRYPT_XML_E_SIGNER"></span><span id="crypt_xml_e_signer"></span><dl> <dt>**Cifrado \_ XML \_ E \_ firmante**</dt> <dt>0x80092111L</dt> </dl>                                            | No se encuentra la clave del firmante.<br/>                                                                      |
| <span id="CRYPT_XML_E_NON_UNIQUE_ID"></span><span id="crypt_xml_e_non_unique_id"></span><dl> <dt>**Cifrado \_ \_ \_ \_ \_ Identificador no único de XML E**</dt> <dt>0x80092112L</dt> </dl>                     | Se encontró un atributo de **identificador** no único.<br/>                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                               |
| Encabezado<br/>                   | <dl> <dt>Cryptxml. h</dt> </dl> |



 

 




