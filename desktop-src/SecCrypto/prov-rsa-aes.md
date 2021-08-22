---
description: Admite firmas digitales y cifrado de datos. Se considera un proveedor de servicios criptográficos (CSP) de uso general.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796ac0b77b91b9cffebc6f04ae3812b1bc25aabd885295e7dd3e1715bb4efc04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901595"
---
# <a name="prov_rsa_aes"></a>PROV \_ RSA \_ AES

El tipo de proveedor \_ PROV RSA \_ AES admite firmas [digitales y](digital-signatures.md) cifrado de datos. Se considera un proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) de uso general. El algoritmo de [*clave pública RSA*](../secgloss/p-gly.md) se usa para todas las operaciones de [*clave*](../secgloss/p-gly.md) pública.

## <a name="algorithms-supported"></a>Algoritmos admitidos

Para obtener descripciones de cada uno de estos algoritmos, consulte el glosario.



| Propósito      | Algoritmos admitidos                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intercambio de claves | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Firma    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Cifrado   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Aplicación de algoritmo hash      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 y SHA-512)<br/> |



 

## <a name="related-documentation"></a>Documentación relacionada

Microsoft y RSA Data Security definen este tipo de proveedor. Se describe en los siguientes documentos:

-   *Guía del programador del proveedor de servicios criptográficos de Microsoft,* Microsoft, 1996.
-   Rsa Rsa, Public Key Cryptography Standards, RSA Data Security, noviembre de 1993.

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
