---
description: Las interfaces siguientes se pueden usar para crear atributos de certificado.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfaces de atributos de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63cbd7b5e80fbb787a0d2aadcfb1617cb7972d7eed200da9184607ad0598031e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902928"
---
# <a name="certificate-attribute-interfaces"></a>Interfaces de atributos de certificado

Las interfaces siguientes se pueden usar para crear atributos de certificado.



| Interfaz                                                                    | Descripción                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | Representa un atributo criptográfico en una solicitud de certificado.                                                                              |
| [**ICryptAttributes**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | Administra una colección de [**objetos ICryptAttribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                                                 |
| [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | Representa un atributo en una solicitud de certificado PKCS \# 7, PKCS \# 10 o CMC.                                                               |
| [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | Representa un atributo que se puede usar para identificar el cliente que generó una solicitud de certificado.                                       |
| [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | Representa las extensiones de certificado en una solicitud de certificado.                                                                             |
| [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | Representa un atributo que contiene una clave privada cifrada que una entidad de certificación va a archivar.                                 |
| [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | Representa un atributo que contiene un hash SHA-1 de la clave privada cifrada que debe archivar una entidad de certificación.                |
| [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | Representa un atributo que identifica el proveedor criptográfico utilizado por la entidad que solicita el certificado.                           |
| [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | Representa un atributo que contiene información de versión sobre el sistema operativo cliente en el que se generó la solicitud de certificado. |
| [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | Representa un atributo que contiene el certificado que se va a renovar.                                                                        |
| [**IX509Attributes**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | Administra una colección de [**objetos IX509Attribute.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                                                   |
| [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | Representa un par nombre-valor genérico.                                                                                                       |
| [**IX509NameValuePairs**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | Administra una colección de [**objetos IX509NameValuePair.**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CertEnroll Interfaces](certenroll-interfaces.md)
</dt> </dl>

 

 



