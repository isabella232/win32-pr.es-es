---
description: Especifica el tipo de proveedor de servicios criptográficos (CSP).
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: Enumeración CAPICOM_PROV_TYPE (CAPICOM. h)
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
ms.openlocfilehash: d9c701b453656a68573fe391775c5b27fdd2461a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649931"
---
# <a name="capicom_prov_type-enumeration"></a>CAPICOM \_ Prov \_ Type (enumeración)

La enumeración de **\_ \_ tipo** de servicio CAPICOM especifica el tipo de [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

## <a name="members"></a>Miembros



| Miembro                             | Descripción                                                                                                                                                                                                                                                                                                                                                                        | Value |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **RSA de CAPICOM \_ Prov \_ \_ completo**       | El CSP [*RSA*](../secgloss/r-gly.md) completo. Este tipo de proveedor es compatible con las [*firmas digitales*](../secgloss/d-gly.md) y el [*cifrado*](../secgloss/e-gly.md)de datos.<br/>                                                            | 1     |
| **\_ \_ \_ firma RSA SIG de CAPICOM**        | Subconjunto del CSP de RSA que admite solo las funciones y algoritmos necesarios para los hashes y las firmas digitales.<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ Prov \_ DSS**             | El CSP [*estándar de firma digital*](../secgloss/d-gly.md) (DSS). Este tipo de proveedor solo admite hashes y firmas digitales. DSS usa el [*algoritmo de firma digital*](../secgloss/d-gly.md) (DSA).<br/> | 3     |
| **multiprov de CAPICOM \_ \_**        | El CSP que contiene los protocolos criptográficos y los algoritmos que pertenecen al [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/>                                                                                      | 4     |
| **CAPICOM \_ de \_ MS \_ Exchange**    | El CSP que se diseñó para las necesidades criptográficas de Exchange y otras aplicaciones compatibles con Microsoft Mail.<br/>                                                                                                                                                                                                                                       | 5     |
| **SSL de CAPICOM \_ \_**             | CSP que admite el protocolo [*capa de sockets seguros*](../secgloss/s-gly.md) (SSL).<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ de \_ RSA \_ Schannel**   | El CSP que admite los protocolos [*RSA*](../secgloss/r-gly.md) y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ de \_ DSS de DSS \_**         | El CSP que admite los protocolos DSS y [*Diffie-Hellman*](../secgloss/d-gly.md) .<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ Prov \_ EC \_ ECDSA \_**  | El CSP que admite las funciones y los algoritmos del algoritmo de firma digital de curva elíptica (ECDSA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                  | 14    |
| **\_ \_ \_ ECNRA \_ SIG de CAPICOM de EC**  | El CSP que admite la curva elíptica Nyberg-Rueppel funciones y algoritmos analógicos (ECNRA) necesarios para las firmas digitales.<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ Prov \_ EC \_ \_ completo** | CSP que admite la ECDSA completa.<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **ECNRA de CAPICOM de \_ \_ EC \_ \_ completo** | CSP que admite el ECNRA completo.<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ Prov \_ DH \_ Schannel**    | El CSP que admite los protocolos [*Diffie-Hellman*](../secgloss/d-gly.md) y [*Schannel*](../secgloss/s-gly.md) .<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ Prov \_ SPYRUS \_ LYNKS**   | El CSP que admite el dispositivo de tarjeta LYNKS de SPYRUS.<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **no es RNG de CAPICOM \_ \_**             | CSP que controla la generación de números aleatorios.<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **CAPICOM \_ Prov \_ Intel \_ s**      | El CSP que proporciona la seguridad de Intel.<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ Prov \_ reemplazar \_ OWF**    | El CSP que admite la sustitución de la manera en que se generan los formatos unidireccionales a partir de contraseñas.<br/>                                                                                                                                                                                                                                                                  | 23    |
| **\_AES de \_ RSA de CAPICOM \_**        | CSP que admite tanto firmas digitales como cifrado de datos mediante el algoritmo Estándar de cifrado avanzado ([*AES*](../secgloss/a-gly.md)).<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>Observaciones

Los siguientes métodos y propiedades utilizan la enumeración de **\_ \_ tipo** de la propiedad CAPICOM:

-   Propiedad [**privatekey. ProviderType**](privatekey-providertype.md) .
-   Método [**privatekey. Open**](privatekey-open.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|--------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                |
| Encabezado<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
