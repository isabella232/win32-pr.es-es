---
title: Asignación de tipos de datos entre Active Directory y LDAP
description: En la tabla siguiente se asigna el nombre descriptivo de la sintaxis al valor OID y ADSTYPEENUM de la sintaxis LDAP correspondiente.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- asignación de tipos de datos entre Active Directory y LDAP ADSI
- ADSI del proveedor de servicios LDAP, asignación de tipos de datos entre Active Directory y LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1aed0ff0071c55e381e1eb66f1f84e5a98aa8acf2c361816444533c6d0ad886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961974"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Asignación de tipos de datos entre Active Directory y LDAP

En la tabla siguiente se asigna el nombre descriptivo de la sintaxis al valor OID y [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) de la sintaxis LDAP correspondiente.



| Nombre descriptivo de la sintaxis              | OID de sintaxis LDAP               | Tipo de datos ADSTYPEENUM                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **ADSTYPE \_ OCTET \_ STRING**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **ADSTYPE \_ OCTET \_ STRING**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ BOOLEAN**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **CADENA EXACTA \_ DE MAYÚSCULAS \_ Y MINÚSCULAS ADSTYPE \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Certificado                       | 1.3.6.1.4.1.1466.115.121.1.8  | **ADSTYPE \_ OCTET \_ STRING**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **ADSTYPE \_ OCTET \_ STRING**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **ADSTYPE \_ OCTET \_ STRING**            |
| País/región                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **ADSTYPE \_ DN \_ STRING**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **ADSTYPE \_ OCTET \_ STRING**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ UTC \_ TIME**                |
| Hora (solo el servidor de sitio hace esto) | 1.3.6.1.4.1.1466.115.121.1.24 | **ADSTYPE \_ UTC \_ TIME**                |
| Guía                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **ADSTYPE \_ INTEGER**                  |
| INTEGER8 (no en LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **ADSTYPE \_ LARGE \_ INTEGER**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **ADSTYPE \_ OCTET \_ STRING**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **ADSTYPE \_ NUMERIC \_ STRING**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| OctetString (no en RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **ADSTYPE \_ OCTET \_ STRING**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **ADSTYPE \_ CADENA IMPRIMIBLE \_**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **ADSTYPE \_ NT \_ SECURITY \_ DESCRIPTOR** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **ADSTYPE \_ OCTET \_ STRING**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ CASE \_ IGNORE \_ STRING**     |
| HORA UTC                           | 1.3.6.1.4.1.1466.115.121.1.53 | **ADSTYPE \_ UTC \_ TIME**                |



 

 

 




