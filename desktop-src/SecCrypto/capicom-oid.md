---
description: Proporciona los nombres de los identificadores de objeto CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: CAPICOM_OID enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_OID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8c008a77e11bd7803dfb09ed2e6ddf1f57ed8695f2de33655239eb73ac49a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879035"
---
# <a name="capicom_oid-enumeration"></a>CapiCOM \_ OID (enumeración)

La **enumeración \_ CAPICOM OID** proporciona los nombres de los identificadores de objeto CAPICOM.

El OID usa esta [**enumeración. Propiedad**](oid-name.md) Name.

## <a name="members"></a>Miembros



| Miembro                                                        | Descripción                                                                                                                                                                                                                                    | Value |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ OID \_ OTHER**                                       | El objeto no es uno de los tipos de objeto CAPICOM predefinidos.<br/>                                                                                                                                                                       | 0     |
| **EXTENSIÓN CAPICOM \_ OID \_ AUTHORITY KEY \_ \_ IDENTIFIER \_**       | El objeto es una extensión de certificado que contiene el identificador de clave pública de la entidad de certificación (CA).<br/>                                                                                                                  | 1     |
| **EXTENSIÓN CAPICOM \_ OID \_ KEY \_ ATTRIBUTES \_**                  | El objeto es una extensión de certificado que contiene atributos opcionales de una clave pública.<br/>                                                                                                                                            | 2     |
| **EXTENSIÓN CAPICOM \_ OID \_ CERT POLICIES \_ \_ 95 \_**               | El objeto es una extensión de certificado que contiene Windows de directiva de certificado 95.<br/>                                                                                                                                      | 3     |
| **EXTENSIÓN DE RESTRICCIÓN DE USO \_ DE CLAVE DE OID CAPICOM \_ \_ \_ \_**          | El objeto es una extensión de certificado que contiene restricciones sobre el uso de la clave pública de un certificado.<br/>                                                                                                                          | 4     |
| **EXTENSIÓN CAPICOM \_ OID \_ LEGACY \_ POLICY \_ MAPPINGS \_**         | El objeto es una extensión de certificado que contiene información de asignación de directivas heredada.<br/>                                                                                                                                              | 5     |
| **EXTENSIÓN CAPICOM \_ OID \_ SUBJECT ALT NAME \_ \_ \_ EXTENSION**               | El objeto es una extensión de certificado que contiene un nombre alternativo para el sujeto del certificado.<br/>                                                                                                                         | 6     |
| **EXTENSIÓN DE NOMBRE ALT DEL \_ EMISOR DE OID CAPICOM \_ \_ \_ \_**                | El objeto es una extensión de certificado que contiene un nombre alternativo para el emisor del certificado.<br/>                                                                                                                          | 7     |
| **EXTENSIÓN DE \_ RESTRICCIONES BÁSICAS DEL OID \_ \_ CAPICOM \_**               | El objeto es una extensión de certificado que indica si el sujeto certificado puede actuar como una entidad de certificación, una entidad final o ambos. <br/>                                                                                                        | 8     |
| **EXTENSIÓN CAPICOM \_ OID \_ SUBJECT KEY \_ \_ IDENTIFIER \_**         | El objeto es una extensión de certificado que contiene el identificador de clave del sujeto del certificado.<br/>                                                                                                                           | 9     |
| **EXTENSIÓN CAPICOM \_ OID \_ KEY \_ USAGE \_**                       | El objeto es una extensión de certificado que contiene información sobre el uso previsto de la clave pública de un certificado.<br/>                                                                                                               | 10    |
| **EXTENSIÓN DE PERÍODO \_ DE USO DE CLAVE PRIVADA DE CAPICOM OID \_ \_ \_ \_**        | El objeto es una extensión de certificado que contiene información sobre el período de tiempo durante el que se puede obtener acceso a la clave privada de un certificado.<br/>                                                                                           | 11    |
| **EXTENSIÓN CAPICOM \_ OID \_ SUBJECT ALT \_ \_ NAME2 \_**              | El objeto es una extensión de certificado que contiene un nombre alternativo para el sujeto del certificado.<br/>                                                                                                                         | 12    |
| **EXTENSIÓN CAPICOM \_ OID \_ ISSUER \_ ALT \_ NAME2 \_**               | El objeto es una extensión de certificado que contiene un nombre alternativo para el emisor del certificado.<br/>                                                                                                                          | 13    |
| **EXTENSIÓN CAPICOM \_ OID \_ BASIC \_ CONSTRAINTS2 \_**              | El objeto es una extensión de certificado que indica si el sujeto certificado puede actuar como una entidad de certificación, una entidad final o ambos. <br/>                                                                                                        | 14    |
| **EXTENSIÓN DE \_ RESTRICCIONES DE NOMBRE DE OID \_ \_ CAPICOM \_**                | El objeto es una extensión de certificado que contiene información sobre los certificados que se permiten o excluyen específicamente de la confianza.<br/>                                                                                          | 15    |
| **EXTENSIÓN CAPICOM \_ OID \_ CRL \_ DIST \_ \_ POINTS**                | El objeto es una extensión de certificado que contiene información que se usa para actualizar la lista de revocación de certificados (CRL).<br/>                                                                                                               | 16    |
| **EXTENSIÓN CAPICOM \_ OID \_ CERT \_ POLICIES \_**                   | El objeto es una extensión de certificado que contiene una lista de las directivas que admite el certificado.<br/>                                                                                                                           | 17    |
| **EXTENSIÓN CAPICOM \_ OID \_ POLICY \_ MAPPINGS \_**                 | El objeto es una extensión de certificado que proporciona asignaciones entre directivas en dominios diferentes.<br/>                                                                                                                                 | 18    |
| **EXTENSIÓN CAPICOM \_ OID \_ AUTHORITY KEY \_ \_ IDENTIFIER2 \_**      | El objeto es una extensión de certificado que contiene el identificador de clave pública de la CA.<br/>                                                                                                                                            | 19    |
| **EXTENSIÓN CAPICOM \_ OID \_ POLICY \_ CONSTRAINTS \_**              | El objeto es una extensión de certificado que contiene directivas establecidas para aceptar certificados como de confianza.<br/>                                                                                                                     | 20    |
| **EXTENSIÓN CAPICOM \_ OID \_ ENHANCED KEY \_ \_ USAGE \_**             | El objeto es una extensión de certificado que contiene información mejorada sobre el uso previsto de la clave pública de un certificado.<br/>                                                                                                      | 21    |
| **EXTENSIÓN DE PLANTILLA \_ DE CERTIFICADO OID \_ \_ CAPICOM \_**            | El objeto es una extensión de certificado que contiene una plantilla de certificado.<br/>                                                                                                                                                         | 22    |
| **EXTENSIÓN DE DIRECTIVAS DE CERTIFICADO DE APLICACIÓN \_ CAPICOM OID \_ \_ \_ \_**      | El objeto es una extensión de certificado que contiene la directiva de aplicación del certificado.<br/>                                                                                                                                      | 23    |
| **EXTENSIÓN CAPICOM \_ OID \_ APPLICATION POLICY \_ \_ MAPPINGS \_**    | El objeto es una extensión de certificado que contiene asignaciones entre distintas directivas de aplicación.<br/>                                                                                                                                | 24    |
| **EXTENSIÓN CAPICOM \_ OID \_ APPLICATION POLICY \_ \_ CONSTRAINTS \_** | El objeto es una extensión de certificado que contiene las restricciones de directiva de aplicación del certificado.<br/>                                                                                                                          | 25    |
| **EXTENSIÓN CAPICOM \_ OID \_ AUTHORITY INFO \_ \_ ACCESS \_**          | El objeto es una extensión de certificado que indica cómo acceder a la información y los servicios de ca para el emisor del certificado.<br/>                                                                                                   | 26    |
| **CAPICOM \_ OID \_ SERVER \_ AUTH \_ EKU**                           | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para autenticar un servidor.<br/>                                                                                                                | 100   |
| **CAPICOM \_ OID \_ CLIENT \_ AUTH \_ EKU**                           | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para autenticar un cliente.<br/>                                                                                                                | 101   |
| **CAPICOM \_ OID \_ CODE \_ SIGNING \_ EKU**                          | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para crear una firma digital.<br/>                                                                                                           | 102   |
| **CAPICOM \_ OID \_ EMAIL \_ PROTECTION \_ EKU**                      | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la protección de correo electrónico.<br/>                                                                                                                    | 103   |
| **CAPICOM \_ OID \_ IPSEC \_ END \_ SYSTEM \_ EKU**                     | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para un sistema final IPsec.<br/>                                                                                                                 | 104   |
| **CAPICOM \_ OID \_ IPSEC \_ TUNNEL \_ EKU**                          | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la tunelización de IPsec.<br/>                                                                                                                     | 105   |
| **CAPICOM \_ OID \_ IPSEC \_ USER \_ EKU**                            | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para un usuario de IPsec.<br/>                                                                                                                       | 106   |
| **CAPICOM \_ OID \_ TIME \_ STAMPING \_ EKU**                         | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la marca de tiempo.<br/>                                                                                                                       | 107   |
| **CAPICOM \_ OID \_ CTL \_ USAGE \_ SIGNING \_ EKU**                    | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para firmar la lista de confianza de certificados (CTL).<br/>                                                                                                | 108   |
| **EKU DE FIRMA DE MARCA DE TIEMPO DE \_ CAPICOM OID \_ \_ \_ \_**                   | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para firmar una marca de tiempo.<br/>                                                                                                                    | 109   |
| **CAPICOM \_ OID \_ SERVER \_ GATED \_ CRYPTO \_ EKU**                  | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la criptografía [*compuerta de servidor*](../secgloss/s-gly.md) (SGC).<br/> | 110   |
| **CAPICOM \_ OID \_ ENCRYPTING \_ FILE \_ SYSTEM \_ EKU**               | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para [*el Sistema de cifrado de archivos*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **CAPICOM \_ OID \_ EFS \_ RECOVERY \_ EKU**                          | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la recuperación de EFS.<br/>                                                                                                                 | 112   |
| **CAPICOM \_ OID \_ WHQL \_ CRYPTO \_ EKU**                           | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para Windows criptografía de Hardware Quality Labs (WHQL).<br/>                                                                                   | 113   |
| **CAPICOM \_ OID \_ NT5 \_ CRYPTO \_ EKU**                            | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para Windows Server 2003 y Windows criptografía XP.<br/>                                                                                     | 114   |
| **CAPICOM \_ OID \_ OEM \_ WHQL \_ CRYPTO \_ EKU**                      | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la criptografía WHQL de fabricantes de equipos originales (OEM).<br/>                                                                            | 115   |
| **CAPICOM \_ OID \_ EMBEDED \_ NT \_ CRYPTO \_ EKU**                    | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para Windows criptografía de NT Embedded.<br/>                                                                                                    | 116   |
| **CAPICOM \_ OID \_ ROOT \_ LIST \_ SIGNER \_ EKU**                     | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para firmar una lista raíz.<br/>                                                                                                                     | 117   |
| **CAPICOM \_ OID \_ QUALIFIED \_ SUBORDINATION \_ EKU**               | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la subordinación calificada.<br/>                                                                                                             | 118   |
| **CAPICOM \_ OID \_ KEY \_ RECOVERY \_ EKU**                          | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para la recuperación de claves.<br/>                                                                                                                        | 119   |
| **CAPICOM \_ OID \_ DIGITAL \_ RIGHTS \_ EKU**                        | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para los derechos digitales.<br/>                                                                                                                      | 120   |
| **CAPICOM \_ OID \_ LICENSES \_ EKU**                               | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para las licencias.<br/>                                                                                                                            | 121   |
| **CAPICOM \_ OID \_ LICENSE \_ SERVER \_ EKU**                        | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para un servidor de licencias.<br/>                                                                                                                    | 122   |
| **CAPICOM \_ OID \_ SMART \_ CARD \_ LOGON \_ EKU**                     | El objeto es un [**objeto EKU**](eku.md) que especifica que el certificado se puede usar para el inicio de sesión con tarjeta inteligente.<br/>                                                                                                                    | 123   |
| **CAPICOM \_ OID \_ PKIX \_ POLICY \_ QUALIFIER \_ CPS**                | El objeto es una instrucción de práctica de certificación (CPS) que se puede usar para el calificador de directiva de infraestructura de clave pública X.509 (PKIX).<br/>                                                                                            | 124   |
| **CAPICOM \_ OID \_ PKIX \_ POLICY \_ QUALIFIER \_ USERNOTICE**         | El objeto es un aviso de usuario que se puede usar para el calificador de directiva de infraestructura de clave pública X.509 (PKIX).<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
