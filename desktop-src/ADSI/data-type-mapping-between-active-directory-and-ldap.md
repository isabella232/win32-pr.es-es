---
title: Asignación de tipos de datos entre Active Directory y LDAP
description: En la tabla siguiente se asigna el nombre descriptivo de la sintaxis al OID de sintaxis LDAP correspondiente y al valor ADSTYPEENUM.
ms.assetid: 07952de0-0389-473a-84ca-b5f35fdc5b1f
ms.tgt_platform: multiple
keywords:
- asignación de tipos de datos entre Active Directory y ADSI LDAP
- Proveedor de servicios LDAP ADSI, asignación de tipos de datos entre Active Directory y LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45157fb7cefe1a993e6e16dffe28f101bc73759b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656188"
---
# <a name="data-type-mapping-between-active-directory-and-ldap"></a>Asignación de tipos de datos entre Active Directory y LDAP

En la tabla siguiente se asigna el nombre descriptivo de la sintaxis al OID de sintaxis LDAP correspondiente y al valor [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) .



| Nombre descriptivo de la sintaxis              | OID de sintaxis LDAP               | ADSTYPEENUM, tipo de datos                 |
|-----------------------------------|-------------------------------|---------------------------------------|
| AccessPointDN                     | 1.3.6.1.4.1.1466.115.121.1.2  | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| AttributeTypeDescription          | 1.3.6.1.4.1.1466.115.121.1.3  | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| Audio                             | 1.3.6.1.4.1.1466.115.121.1.4  | **ADSTYPE \_ cadena de octeto \_**            |
| Binary                            | 1.3.6.1.4.1.1466.115.121.1.5  | **ADSTYPE \_ cadena de octeto \_**            |
| BitString                         | 1.3.6.1.4.1.1466.115.121.1.6  | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| Boolean                           | 1.3.6.1.4.1.1466.115.121.1.7  | **ADSTYPE \_ booleano**                  |
| CaseExactString                   | 1.2.840.113556.1.4.1362       | **\_ \_ cadena exacta de caso ADSTYPE \_**      |
| CaseIgnoreString                  | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| Certificado                       | 1.3.6.1.4.1.1466.115.121.1.8  | **ADSTYPE \_ cadena de octeto \_**            |
| CertificateList                   | 1.3.6.1.4.1.1466.115.121.1.9  | **ADSTYPE \_ cadena de octeto \_**            |
| CertificatePair                   | 1.3.6.1.4.1.1466.115.121.1.10 | **ADSTYPE \_ cadena de octeto \_**            |
| País/región                    | 1.3.6.1.4.1.1466.115.121.1.11 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| DataQualitySyntax                 | 1.3.6.1.4.1.1466.115.121.1.13 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| DeliveryMethod                    | 1.3.6.1.4.1.1466.115.121.1.14 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| DirectoryString                   | 1.3.6.1.4.1.1466.115.121.1.15 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| DN                                | 1.3.6.1.4.1.1466.115.121.1.12 | **ADSTYPE \_ \_ cadena DN**               |
| DSAQualitySyntax                  | 1.3.6.1.4.1.1466.115.121.1.19 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| EnhancedGuide                     | 1.3.6.1.4.1.1466.115.121.1.21 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| FacsimileTelephoneNumber          | 1.3.6.1.4.1.1466.115.121.1.22 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| Fax                               | 1.3.6.1.4.1.1466.115.121.1.23 | **ADSTYPE \_ cadena de octeto \_**            |
| GeneralizedTime                   | 1.3.6.1.4.1.1466.115.121.1.24 | **\_hora UTC de ADSTYPE \_**                |
| Hora (solo el servidor de sitio lo hace) | 1.3.6.1.4.1.1466.115.121.1.24 | **\_hora UTC de ADSTYPE \_**                |
| Guía                             | 1.3.6.1.4.1.1466.115.121.1.25 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| IA5String                         | 1.3.6.1.4.1.1466.115.121.1.26 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| INTEGER                           | 1.3.6.1.4.1.1466.115.121.1.27 | **\_entero ADSTYPE**                  |
| INTEGER8 (no en LDAP, NTDS)      | 1.2.840.113556.1.4.906        | **\_entero grande de ADSTYPE \_**           |
| JPEG                              | 1.3.6.1.4.1.1466.115.121.1.28 | **ADSTYPE \_ cadena de octeto \_**            |
| MailPreference                    | 1.3.6.1.4.1.1466.115.121.1.32 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| NameAndOptionalUID                | 1.3.6.1.4.1.1466.115.121.1.34 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| NumericString                     | 1.3.6.1.4.1.1466.115.121.1.36 | **ADSTYPE \_ \_ cadena numérica**          |
| ObjectClassDescription            | 1.3.6.1.4.1.1466.115.121.1.37 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| OctetString (no en RFC)          | 1.3.6.1.4.1.1466.115.121.1.40 | **ADSTYPE \_ cadena de octeto \_**            |
| OID                               | 1.3.6.1.4.1.1466.115.121.1.38 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| ORName                            | 1.2.840.113556.1.4.1221       | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| OtherMailbox                      | 1.3.6.1.4.1.1466.115.121.1.39 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| PostalAddress                     | 1.3.6.1.4.1.1466.115.121.1.41 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| PresentationAddress               | 1.3.6.1.4.1.1466.115.121.1.43 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| PrintableString                   | 1.3.6.1.4.1.1466.115.121.1.44 | **ADSTYPE \_ cadena imprimible \_**        |
| ObjectSecurityDescriptor          | 1.2.840.113556.1.4.907        | **descriptor de seguridad de ADSTYPE \_ NT \_ \_** |
| TelephoneNumber                   | 1.3.6.1.4.1.1466.115.121.1.50 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| TeletexTerminalIdentifier         | 1.3.6.1.4.1.1466.115.121.1.51 | **ADSTYPE \_ cadena de octeto \_**            |
| TelexNumber                       | 1.3.6.1.4.1.1466.115.121.1.52 | **ADSTYPE \_ caso \_ omitir \_ cadena**     |
| UTCTime                           | 1.3.6.1.4.1.1466.115.121.1.53 | **\_hora UTC de ADSTYPE \_**                |



 

 

 




