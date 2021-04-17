---
description: Enumera los proveedores de servicios de cifrado disponibles en Microsoft.
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Proveedores de servicios criptográficos de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 294d00660cbfa89c6113e6e9fcf2600b2f745e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686862"
---
# <a name="microsoft-cryptographic-service-providers"></a>Proveedores de servicios criptográficos de Microsoft

Los siguientes [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) (CSP) están disponibles actualmente en Microsoft.



| Proveedor                                                                                                                                 | Descripción                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Proveedor de servicios criptográficos básicos de Microsoft](microsoft-base-cryptographic-provider.md)                                                       | Un amplio conjunto de funciones criptográficas básicas que se pueden exportar a otros países o regiones.                                                                                                                                                     |
| [Proveedor de servicios criptográficos seguros de Microsoft](microsoft-strong-cryptographic-provider.md)                                                   | Una extensión del proveedor de servicios criptográficos de base de Microsoft disponible con Windows XP y versiones posteriores.                                                                                                                                                           |
| [Proveedor de servicios criptográficos mejorados de Microsoft](microsoft-enhanced-cryptographic-provider.md)                                               | Proveedor de servicios criptográficos básicos de Microsoft con a través de claves más largas y algoritmos adicionales.                                                                                                                                                                |
| [Proveedor de servicios criptográficos AES de Microsoft](microsoft-aes-cryptographic-provider.md)                                                         | Proveedor de servicios criptográficos mejorados de Microsoft compatible con los algoritmos de cifrado AES.                                                                                                                                                                    |
| [Proveedor de servicios criptográficos de Microsoft DSS](microsoft-dss-cryptographic-provider.md)                                                         | Proporciona funciones de hash, firma de datos y comprobación de firmas mediante el algoritmo hash seguro ([*Sha*](../secgloss/s-gly.md)) y los algoritmos estándar de firma digital (DSS). |
| [Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | Un superconjunto del proveedor de servicios criptográficos DSS que también admite el intercambio de claves Diffie-Hellman, el hash, la firma de datos y la comprobación de firmas mediante los algoritmos de algoritmo hash seguro (SHA) y estándar de firma digital (DSS).                    |
| [Microsoft Enhanced DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | Admite el intercambio de claves Diffie-Hellman (un derivado DES de 40 bits), hash SHA, firma de datos DSS y comprobación de firma DSS.                                                                                                                           |
| [Proveedor de servicios criptográficos de Microsoft DSS y Diffie-Hellman/Schannel](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | Admite el hash, la firma de datos con DSS, la generación de claves Diffie-Hellman (D-H), el intercambio de claves D-H y la exportación de una tecla D-H. Este CSP admite la derivación de claves para los protocolos SSL3 y TLS1.                                                           |
| [Proveedor de servicios criptográficos de Microsoft RSA/Schannel](microsoft-rsa-schannel-cryptographic-provider.md)                                       | Admite el hash, la firma de datos y la comprobación de la firma. El identificador de algoritmo CALG \_ SSL3 \_ SHAMD5 se usa para la autenticación de cliente SSL 3,0 y TLS 1,0. Este CSP admite la derivación de claves para los protocolos SSL2, PCT1, SSL3 y TLS1.             |
| [Proveedor de servicios criptográficos de firmas RSA de Microsoft](microsoft-rsa-signature-cryptographic-provider.md)                                     | Proporciona firma de datos y comprobación de la firma.                                                                                                                                                                                                        |



 

 

 
