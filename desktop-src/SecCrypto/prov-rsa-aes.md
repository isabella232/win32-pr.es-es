---
description: Admite tanto firmas digitales como cifrado de datos. Se considera un proveedor de servicios criptográficos (CSP) de uso general.
ms.assetid: da0b50ec-25a6-40dd-af83-73500b4a4c08
title: PROV_RSA_AES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fa8d01e9fd212f2c39ab5615b12931738bc926
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083080"
---
# <a name="prov_rsa_aes"></a>\_AES de RSA \_

El \_ tipo de proveedor de RSA AES de Prov \_ es compatible con las [firmas digitales](digital-signatures.md) y el cifrado de datos. Se considera un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) de uso general. El [*algoritmo de clave pública*](../secgloss/p-gly.md) RSA se utiliza para todas las operaciones de [*clave pública*](../secgloss/p-gly.md) .

## <a name="algorithms-supported"></a>Algoritmos admitidos

Para obtener descripciones de cada uno de estos algoritmos, vea el glosario.



| Propósito      | Algoritmos admitidos                                                                                                                                                                                                                                                                                       |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intercambio de claves | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Firma    | [*RSA*](../secgloss/r-gly.md)<br/>                                                                                                                                                                                                                                     |
| Cifrado   | [*RC2*](../secgloss/r-gly.md)<br/> [*RC4*](../secgloss/r-gly.md)<br/> [*Estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES) <br/>                                                       |
| Aplicación de algoritmo hash      | [*MD2*](../secgloss/m-gly.md)<br/> [*MD4*](../secgloss/m-gly.md)<br/> [*MD5*](../secgloss/m-gly.md)<br/> [*SHA-1*](../secgloss/s-gly.md)<br/> SHA-2 (SHA-256, SHA-384 y SHA-512)<br/> |



 

## <a name="related-documentation"></a>Documentación relacionada

Este tipo de proveedor está definido por Microsoft y RSA Data Security. Se describe en los siguientes documentos:

-   *Guía del programador del proveedor de servicios criptográficos de Microsoft*, microsoft, 1996.
-   RSA Laboratories, estándares de criptografía de clave pública, RSA Data Security, noviembre de 1993.

> [!Note]  
> Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones.

 

 

 
