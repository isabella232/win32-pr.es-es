---
description: El proveedor de servicios criptográficos mejorado de Microsoft admite las mismas funcionalidades que el proveedor de servicios criptográficos base de Microsoft, pero admite una mayor seguridad a través de claves más largas y algoritmos adicionales.
ms.assetid: 87d0c865-8b29-439c-81aa-a40dc0034e3b
title: Proveedor de servicios criptográficos mejorado de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d60dbe254f9f22623a61de51b044b58df3a52f19f8a0b4f283caba3f59db7974
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425515"
---
# <a name="microsoft-enhanced-cryptographic-provider"></a>Proveedor de servicios criptográficos mejorado de Microsoft

El proveedor de servicios criptográficos mejorado de Microsoft, denominado proveedor mejorado, admite las mismas funcionalidades que el proveedor de servicios criptográficos base de Microsoft, denominado proveedor base. El proveedor mejorado admite una mayor seguridad a través de claves más largas y algoritmos adicionales. Se puede usar con todas las versiones de CryptoAPI.

Para mantener la compatibilidad con versiones anteriores del proveedor, el nombre del proveedor, tal como se define en el archivo de encabezado Wincrypt.h, conserva la designación de la versión 1.0. Sin embargo, la versión 2.0 de este proveedor se está enviando actualmente. Para determinar la versión del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el argumento *dwParam* establecido en **PP \_ VERSION**. La versión 2.0 está en uso si 0x0200 se devuelve.

|                   | Value               |
|-------------------|---------------------|
| **Tipo de proveedor** | PROV \_ RSA \_ FULL     |
| **Nombre del proveedor** | MS \_ ENHANCED \_ PROV  |



 

En la tabla siguiente se resaltan las diferencias entre el proveedor base, el proveedor fuerte y el proveedor mejorado. Las longitudes de clave que se muestran son las longitudes de clave predeterminadas.



| Algoritmo                                                                                | Longitud de clave del proveedor base | Longitud de clave del proveedor fuerte | Longitud de clave del proveedor mejorada                |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de firma de clave pública RSA                                                       | 512 bits                 | 1024 bits                 | 1024 bits                                  |
| Algoritmo de intercambio de claves públicas RSA                                                        | 512 bits                 | 1024 bits                 | 1024 bits                                  |
| Algoritmo de cifrado de bloques RC2                                                           | 40 bits                  | 128 bits                   | Se puede establecer una longitud de sal de 128 bits.<br/> |
| Algoritmo de cifrado de secuencias RC4                                                          | 40 bits                  | 128 bits                   | Se puede establecer una longitud de sal de 128 bits.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 clave) | No compatible            | 112 bits                   | 112 bits                                    |
| Triple DES (3 claves)                                                                       | No compatible            | 168 bits                   | 168 bits                                    |



 

El proveedor fuerte y el proveedor mejorado son compatibles con el proveedor base, salvo que los proveedores solo pueden generar claves RC2 o RC4 de longitud [*de clave predeterminada.*](../secgloss/k-gly.md) La longitud predeterminada del proveedor base es de 40 bits. La longitud predeterminada del proveedor mejorado es de 128 bits. Por lo tanto, el proveedor mejorado no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor mejorado puede importar claves RC2 y RC4 de hasta 128 bits. Por lo tanto, el proveedor mejorado puede importar y usar claves de 40 bits generadas mediante el proveedor base.

 

 
