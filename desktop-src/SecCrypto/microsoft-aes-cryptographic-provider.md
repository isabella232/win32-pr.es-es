---
description: El proveedor de servicios criptográficos RSA y AES mejorado de Microsoft admite las mismas funcionalidades que el proveedor de servicios criptográficos de base de Microsoft, denominado proveedor base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Proveedor de servicios criptográficos AES de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb4c774eb2cb9d01bcb3a12f5550537abe44b364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666525"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Proveedor de servicios criptográficos AES de Microsoft

El proveedor de servicios criptográficos RSA y AES mejorado de Microsoft admite las mismas funcionalidades que el proveedor de servicios criptográficos de base de Microsoft, denominado proveedor base. El proveedor AES admite una mayor seguridad gracias a claves más largas y algoritmos adicionales. Se puede usar con todas las versiones de CryptoAPI.

**Windows XP:** El proveedor de servicios criptográficos AES de Microsoft tenía el nombre Microsoft Enhanced RSA y AES Cryptographic Provider (Prototype).

Para mantener la compatibilidad con las versiones anteriores del proveedor, el nombre del proveedor, tal como se define en el archivo de encabezado Wincrypt. h, conserva la designación de la versión 1,0, aunque se hayan enviado las versiones más recientes de este proveedor. Para determinar la versión del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el parámetro *dwParam* establecido en la \_ versión PP. La versión 2,0 está en uso si se devuelve 0x0200.

|                |                             |
|----------------|-----------------------------|
| Tipo de proveedor: | **\_AES de RSA \_**          |
| Nombre del proveedor: | **Microsoft \_ Enh \_ RSA \_ AES \_ Prov** |



 

En la tabla siguiente se resaltan las diferencias entre el proveedor base, el proveedor seguro y el proveedor AES. Las [*longitudes de clave*](../secgloss/k-gly.md) que se muestran son las longitudes de clave predeterminadas.



| Algoritmo                                                                                | Longitud de clave del proveedor base | Longitud de clave de proveedor fuerte | Longitud de clave del proveedor de AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de firma de clave pública RSA                                                       | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de intercambio de claves públicas RSA                                                        | 512 bits                 | 1.024 bits                 | 1.024 bits                                  |
| Algoritmo de cifrado de bloques RC2                                                           | 40 bits                  | 128 bits                   | se puede establecer la longitud del valor Salt de bits 128.<br/> |
| Algoritmo de cifrado de flujo RC4                                                          | 40 bits                  | 128 bits                   | se puede establecer la longitud del valor Salt de bits 128.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple des*](../secgloss/t-gly.md) (2 tecla) | No compatible            | 112 bits                   | 112 bits                                    |
| Triple DES (3 tecla)                                                                       | No compatible            | 168 bits                   | 168 bits                                    |



 

Para obtener una lista completa de los algoritmos admitidos, consulte [algoritmos de proveedor de AES](aes-provider-algorithms.md).

El proveedor seguro, el proveedor mejorado y el proveedor AES son compatibles con el proveedor base, salvo que los proveedores pueden generar únicamente claves RC2 o RC4 de longitud de clave predeterminada. La longitud predeterminada del proveedor base es 40 bits. La longitud predeterminada del proveedor AES es 128 bits. Por lo tanto, el proveedor de AES no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor AES puede importar claves RC2 y RC4 de hasta 128 bits. Por lo tanto, el proveedor de AES puede importar y usar claves de 40 bits generadas mediante el proveedor base.

 

 
