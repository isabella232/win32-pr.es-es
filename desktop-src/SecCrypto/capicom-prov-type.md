---
description: Especifica el tipo de proveedor de servicios criptográficos (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: CAPICOM_PROV_TYPE enumeración (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879025"
---
# <a name="capicom_prov_type-enumeration"></a>CAPICOM \_ PROV \_ TYPE (enumeración)

La **enumeración CAPICOM \_ PROV \_ TYPE** especifica el tipo de proveedor [*de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Miembros



| Miembro                             | Descripción                                                                                                                                                                                                                                                                                                                                                                        | Value |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ PROV \_ RSA \_ FULL**       | CSP [*de RSA*](../secgloss/r-gly.md) completo. Este tipo de proveedor admite firmas [*digitales y*](../secgloss/d-gly.md) cifrado de [*datos.*](../secgloss/e-gly.md)<br/>                                                            | 1     |
| **CAPICOM \_ PROV \_ RSA \_ SIG**        | Subconjunto del CSP de RSA que solo admite las funciones y algoritmos necesarios para hashes y firmas digitales.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ PROV \_ DSS**             | CSP [*de Digital Signature Standard*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **CAPICOM \_ PROV \_ FORTEZZA**        | CSP que contiene los protocolos criptográficos y algoritmos propiedad del Instituto [*Nacional de Estándares y Tecnología*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM \_ PROV \_ MS \_ EXCHANGE**    | CSP diseñado para las necesidades criptográficas de Exchange y otras aplicaciones compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ PROV \_ SSL**             | CSP que admite el protocolo [*Capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ PROV \_ RSA \_ SCHANNEL**   | CSP que admite los protocolos [*RSA*](../secgloss/r-gly.md) y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ PROV \_ DSS \_ DH**         | CSP que admite los protocolos DSS y [*Diffie-Hellman.*](../secgloss/d-gly.md)<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ SIG**  | CSP que admite las funciones y los algoritmos del algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ SIG**  | El CSP que admite las funciones y algoritmos de la curva elíptica Nyberg-Rueppel Analog (ECNRA) necesarias para las firmas digitales.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ PROV \_ EC \_ ECDSA \_ FULL** | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ PROV \_ EC \_ ECNRA \_ FULL** | CSP que admite la ECNRA completa.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ PROV \_ DH \_ SCHANNEL**    | CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel.*](../secgloss/s-gly.md)<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ PROV \_ SPYRUS \_ LYNKS**   | CSP que admite el dispositivo de tarjeta SPYRUS LYNKS.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ PROV \_ RNG**             | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ PROV \_ INTEL \_ SEC**      | CSP que proporciona la seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ PROV \_ REPLACE \_ OWF**    | CSP que admite la sustitución de la manera en que se generan formatos un solo sentido a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ PROV \_ RSA \_ AES**        | CSP que admite firmas digitales y cifrado de datos mediante el algoritmo Estándar de cifrado avanzado [*(AES).*](../secgloss/a-gly.md)<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Comentarios

Los métodos y propiedades siguientes usan la enumeración **\_ CAPICOM PROV \_ TYPE:**

-   [**Propiedad PrivateKey.ProviderType.**](privatekey-providertype.md)
-   [**Método PrivateKey.Open.**](privatekey-open.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Header<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
