---
description: Proporciona los nombres de los identificadores de objeto de CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: Enumeración CAPICOM_OID (CAPICOM. h)
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
ms.openlocfilehash: 4cedd7c039212b7bae3e681d7e0d594d3e1b8de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649699"
---
# <a name="capicom_oid-enumeration"></a>CAPICOM \_ OID (enumeración)

La enumeración de **CAPICOM \_ OID** proporciona los nombres de los identificadores de objeto de CAPICOM.

El OID usa esta enumeración [**. Propiedad nombre**](oid-name.md) .

## <a name="members"></a>Miembros



| Miembro                                                        | Descripción                                                                                                                                                                                                                                    | Value |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ OID \_ other**                                       | El objeto no es uno de los tipos de objeto CAPICOM predefinidos.<br/>                                                                                                                                                                       | 0     |
| **\_extensión de \_ \_ identificador de clave de entidad de certificación CAPICOM \_ \_**       | El objeto es una extensión de certificado que contiene el identificador de clave pública de la entidad de certificación (CA).<br/>                                                                                                                  | 1     |
| **CAPICOM \_ OID \_ key \_ attributes \_ Extension**                  | El objeto es una extensión de certificado que contiene atributos opcionales de una clave pública.<br/>                                                                                                                                            | 2     |
| **\_ \_ \_ Extensión 95 de directivas de certificados \_ de CAPICOM OID \_**               | El objeto es una extensión de certificado que contiene información de la Directiva de certificado de Windows 95.<br/>                                                                                                                                      | 3     |
| **\_extensión de \_ restricción de uso de claves \_ \_ de CAPICOM OID \_**          | El objeto es una extensión de certificado que contiene restricciones en el uso de la clave pública de un certificado.<br/>                                                                                                                          | 4     |
| **\_extensión de \_ \_ asignaciones de directivas heredadas de CAPICOM \_ OID \_**         | El objeto es una extensión de certificado que contiene información de asignación de directiva heredada.<br/>                                                                                                                                              | 5     |
| **\_extensión de \_ \_ nombre alternativo \_ de asunto del OID de \_ CAPICOM**               | El objeto es una extensión de certificado que contiene un nombre alternativo para el firmante del certificado.<br/>                                                                                                                         | 6     |
| **\_extensión de \_ \_ nombre alternativo del emisor de \_ CAPICOM OID \_**                | El objeto es una extensión de certificado que contiene un nombre alternativo para el emisor del certificado.<br/>                                                                                                                          | 7     |
| **\_extensión de \_ \_ Restricciones básicas \_ de CAPICOM OID**               | El objeto es una extensión de certificado que indica si el sujeto certificado puede actuar como una entidad de certificación, una entidad final o ambas. <br/>                                                                                                        | 8     |
| **\_extensión de \_ identificador de clave de sujeto \_ de \_ CAPICOM OID \_**         | El objeto es una extensión de certificado que contiene el identificador de clave del sujeto del certificado.<br/>                                                                                                                           | 9     |
| **\_extensión de \_ uso de claves \_ \_ de CAPICOM OID**                       | El objeto es una extensión de certificado que contiene información sobre el uso previsto de la clave pública de un certificado.<br/>                                                                                                               | 10    |
| **\_extensión de \_ período de uso de PRIVATEKEY \_ \_ de CAPICOM OID \_**        | El objeto es una extensión de certificado que contiene información sobre el período de tiempo durante el cual se puede usar la clave privada de un certificado.<br/>                                                                                           | 11    |
| **\_Extensión del \_ sujeto alternativo de CAPICOM OID \_ ALT \_ \_**              | El objeto es una extensión de certificado que contiene un nombre alternativo para el firmante del certificado.<br/>                                                                                                                         | 12    |
| **La \_ \_ extensión del emisor \_ ALT \_ de CAPICOM OID \_**               | El objeto es una extensión de certificado que contiene un nombre alternativo para el emisor del certificado.<br/>                                                                                                                          | 13    |
| **Extensión CONSTRAINTS2 de CAPICOM \_ OID \_ Basic \_ \_**              | El objeto es una extensión de certificado que indica si el sujeto certificado puede actuar como una entidad de certificación, una entidad final o ambas. <br/>                                                                                                        | 14    |
| **\_extensión de \_ restricciones de nombre de OID de CAPICOM \_ \_**                | El objeto es una extensión de certificado que contiene información sobre los certificados que se permiten específicamente o se excluyen de la confianza.<br/>                                                                                          | 15    |
| **\_extensión de \_ puntos de distribución de CRL \_ \_ de CAPICOM OID \_**                | El objeto es una extensión de certificado que contiene la información utilizada para actualizar la lista de revocación de certificados (CRL).<br/>                                                                                                               | 16    |
| **\_extensión de \_ directivas de certificado \_ \_ de CAPICOM OID**                   | El objeto es una extensión de certificado que contiene una lista de las directivas admitidas por el certificado.<br/>                                                                                                                           | 17    |
| **\_extensión de \_ asignaciones de directiva de CAPICOM OID \_ \_**                 | El objeto es una extensión de certificado que proporciona asignaciones entre directivas en dominios diferentes.<br/>                                                                                                                                 | 18    |
| **CAPICOM \_ OID \_ Authority \_ clave \_ identificador2 \_ Extension**      | El objeto es una extensión de certificado que contiene el identificador de clave pública de la CA.<br/>                                                                                                                                            | 19    |
| **\_extensión de \_ restricciones de directiva de CAPICOM OID \_ \_**              | El objeto es una extensión de certificado que contiene las directivas establecidas para aceptar certificados como de confianza.<br/>                                                                                                                     | 20    |
| **\_extensión de \_ uso mejorado de \_ clave \_ \_ de CAPICOM OID**             | El objeto es una extensión de certificado que contiene información mejorada sobre el uso previsto de la clave pública de un certificado.<br/>                                                                                                      | 21    |
| **\_extensión de \_ plantilla de certificado \_ \_ de CAPICOM OID**            | El objeto es una extensión de certificado que contiene una plantilla de certificado.<br/>                                                                                                                                                         | 22    |
| **\_extensión de \_ directivas de certificado de aplicación \_ \_ de CAPICOM OID \_**      | El objeto es una extensión de certificado que contiene la Directiva de aplicación del certificado.<br/>                                                                                                                                      | 23    |
| **\_extensión de \_ asignaciones de directiva de aplicación \_ de \_ CAPICOM OID \_**    | El objeto es una extensión de certificado que contiene asignaciones entre diferentes directivas de aplicación.<br/>                                                                                                                                | 24    |
| **extensión de restricciones de la Directiva de aplicación de CAPICOM \_ OID \_ \_ \_ \_** | El objeto es una extensión de certificado que contiene las restricciones de la Directiva de aplicación del certificado.<br/>                                                                                                                          | 25    |
| **\_extensión de \_ \_ \_ acceso a información \_ de la entidad de certificación CAPICOM**          | El objeto es una extensión de certificado que indica cómo tener acceso a la información y los servicios de la entidad de certificación para el emisor del certificado.<br/>                                                                                                   | 26    |
| **\_EKU de \_ autenticación del servidor \_ \_ de CAPICOM OID**                           | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para autenticar un servidor.<br/>                                                                                                                | 100   |
| **\_EKU de \_ autenticación de cliente \_ \_ de CAPICOM OID**                           | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para autenticar un cliente.<br/>                                                                                                                | 101   |
| **\_EKU de \_ firma de código \_ \_ de CAPICOM OID**                          | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para crear una firma digital.<br/>                                                                                                           | 102   |
| **\_EKU de \_ protección de correo electrónico de CAPICOM OID \_ \_**                      | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para la protección del correo electrónico.<br/>                                                                                                                    | 103   |
| **\_EKU de \_ \_ sistema final \_ IPSec \_ de CAPICOM OID**                     | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para un sistema final de IPSec.<br/>                                                                                                                 | 104   |
| **\_EKU de \_ \_ túnel IPSec \_ de CAPICOM OID**                          | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para el túnel IPSec.<br/>                                                                                                                     | 105   |
| **\_EKU de \_ usuario de IPSec \_ \_ de CAPICOM OID**                            | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para un usuario de IPSec.<br/>                                                                                                                       | 106   |
| **\_EKU de \_ marca de tiempo de CAPICOM OID \_ \_**                         | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para la marca de tiempo.<br/>                                                                                                                       | 107   |
| **\_EKU de \_ \_ firma de uso CTL \_ \_ de CAPICOM OID**                    | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para firmar la lista de certificados de confianza (CTL).<br/>                                                                                                | 108   |
| **\_EKU de \_ firma de marca de tiempo \_ \_ de CAPICOM OID \_**                   | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para firmar una marca de tiempo.<br/>                                                                                                                    | 109   |
| **\_EKU de \_ \_ \_ cifrado controlado \_ por el servidor OID de CAPICOM**                  | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para la [*Criptografía controlada por servidor*](../secgloss/s-gly.md) (SGC).<br/> | 110   |
| **\_ \_ \_ \_ EKU del sistema de cifrado de archivos de CAPICOM OID \_**               | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para el [*sistema de cifrado de archivos*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **\_EKU de \_ recuperación de EFS \_ \_ de CAPICOM OID**                          | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para la recuperación de EFS.<br/>                                                                                                                 | 112   |
| **\_EKU de \_ Crypto con WHQL \_ \_ de CAPICOM OID**                           | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para la criptografía de laboratorios de calidad de hardware de Windows (WHQL).<br/>                                                                                   | 113   |
| **EKU criptográfico de CAPICOM \_ OID \_ NT5 \_ \_**                            | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para windows Server 2003 y la criptografía de Windows XP.<br/>                                                                                     | 114   |
| **\_EKU de \_ \_ \_ cifrado de OEM WHQL \_ de CAPICOM OID**                      | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para la criptografía WHQL de fabricantes de equipos originales (OEM).<br/>                                                                            | 115   |
| **\_EKU de \_ \_ \_ cifrado NT criptográfico \_ de CAPICOM**                    | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para la criptografía de Windows NT Embedded.<br/>                                                                                                    | 116   |
| **\_EKU de \_ \_ firmante de lista raíz \_ \_ de CAPICOM OID**                     | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para firmar una lista raíz.<br/>                                                                                                                     | 117   |
| **\_EKU de \_ \_ subordinación \_ calificado de CAPICOM OID**               | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para la subordinación cualificada.<br/>                                                                                                             | 118   |
| **\_EKU de \_ recuperación de claves \_ \_ de CAPICOM OID**                          | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede utilizar para la recuperación de claves.<br/>                                                                                                                        | 119   |
| **\_EKU de \_ \_ derechos digitales \_ de CAPICOM OID**                        | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para los derechos digitales.<br/>                                                                                                                      | 120   |
| **EKU de licencias de CAPICOM \_ OID \_ \_**                               | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para las licencias.<br/>                                                                                                                            | 121   |
| **\_EKU del \_ servidor de licencias CAPICOM OID \_ \_**                        | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para un servidor de licencias.<br/>                                                                                                                    | 122   |
| **\_EKU de \_ Inicio \_ de \_ sesión de tarjeta inteligente \_ de CAPICOM OID**                     | El objeto es un objeto [**EKU**](eku.md) que especifica que el certificado se puede usar para el inicio de sesión de tarjeta inteligente.<br/>                                                                                                                    | 123   |
| **\_CPS de \_ \_ \_ calificador de \_ Directiva de CAPICOM OID PKIX**                | El objeto es una declaración de prácticas de certificación (CPS) que se puede usar para el calificador de directivas X. 509 (PKIX) de infraestructura de clave pública.<br/>                                                                                            | 124   |
| **\_calificador de directiva de CAPICOM OID \_ PKIX \_ \_ \_ USERNOTICE**         | El objeto es un aviso de usuario que se puede usar para el calificador de directiva X. 509 (PKIX) de infraestructura de clave pública.<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
