---
description: El proveedor de servicios criptográficos mejorados de Microsoft admite las mismas funcionalidades que el proveedor de servicios criptográficos básicos de Microsoft, pero admite una mayor seguridad gracias a claves más largas y algoritmos adicionales.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Proveedor de servicios criptográficos mejorados de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cadaa0b6325dc7d855aa0b7eeb8d7ff5f114cfd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001214"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Proveedor de servicios criptográficos mejorados de Microsoft

El proveedor de servicios criptográficos mejorados de Microsoft, denominado proveedor mejorado, admite las mismas capacidades que el proveedor de servicios criptográficos básicos de Microsoft, denominado proveedor base. El proveedor mejorado admite una mayor seguridad gracias a claves más largas y algoritmos adicionales. Se puede usar con todas las versiones de CryptoAPI.

Para mantener la compatibilidad con las versiones anteriores del proveedor, el nombre del proveedor, tal como se define en el archivo de encabezado Wincrypt. h, conserva la designación de la versión 1,0. Sin embargo, la versión 2,0 de este proveedor se está distribuyendo actualmente. Para determinar la versión del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **la \_ versión PP**. La versión 2,0 está en uso si se devuelve 0x0200.

|                |                        |
|----------------|------------------------|
| Tipo de proveedor: | **aprovisionamiento \_ completo de RSA \_**    |
| Nombre del proveedor: | **Microsoft \_ Enhanced \_ Prov** |



 

En la tabla siguiente se resaltan las diferencias entre el proveedor base, el proveedor seguro y el proveedor mejorado. Las longitudes de clave que se muestran son las longitudes de clave predeterminadas.



| Algoritmo                                                                                | Longitud de clave del proveedor base | Longitud de clave de proveedor fuerte | Longitud de clave de proveedor mejorada                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de firma de clave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de intercambio de claves públicas RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de cifrado de bloques RC2                                                           | 40 bits                  | 128 bits                   | se puede establecer la longitud del valor Salt de bits 128.<br/> |
| Algoritmo de cifrado de flujo RC4                                                          | 40 bits                  | 128 bits                   | se puede establecer la longitud del valor Salt de bits 128.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 tecla) | No compatible            | 112 bits                   | 112 bits                                    |
| Triple DES (3 tecla)                                                                       | No compatible            | 168 bits                   | 168 bits                                    |



 

El proveedor seguro y el proveedor mejorado son compatibles con el proveedor base, salvo que los proveedores solo pueden generar claves RC2 o RC4 de longitud de [*clave*](../secgloss/k-gly.md)predeterminada. La longitud predeterminada del proveedor base es 40 bits. La longitud predeterminada del proveedor mejorado es 128 bits. Por lo tanto, el proveedor mejorado no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor mejorado puede importar claves RC2 y RC4 de hasta 128 bits. Por lo tanto, el proveedor mejorado puede importar y usar las claves de 40 bits generadas mediante el proveedor base.

 

 
