---
description: El proveedor criptográfico RSA y AES mejorado de Microsoft admite las mismas funcionalidades que el proveedor criptográfico base de Microsoft, denominado proveedor base.
ms.assetid: a01bc5db-17b9-44fe-adf8-0c2954fcd369
title: Proveedor criptográfico AES de Microsoft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2449c53cb828a94c8dd596133c3a8c21c9b0388
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244089"
---
# <a name="microsoft-aes-cryptographic-provider"></a>Proveedor criptográfico AES de Microsoft

El proveedor criptográfico RSA y AES mejorado de Microsoft admite las mismas funcionalidades que el proveedor criptográfico base de Microsoft, denominado proveedor base. El proveedor de AES admite una mayor seguridad a través de claves más largas y algoritmos adicionales. Se puede usar con todas las versiones de CryptoAPI.

**Windows XP:** El proveedor criptográfico AES de Microsoft se denominaba Microsoft Enhanced RSA and AES Cryptographic Provider (Prototipo).

Para mantener la compatibilidad con versiones anteriores del proveedor, el nombre del proveedor, tal como se define en el archivo de encabezado Wincrypt.h, conserva la designación de la versión 1.0 aunque se hayan enviado versiones más recientes de este proveedor. Para determinar la versión del proveedor en uso, llame a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con el parámetro *dwParam* establecido en PP \_ VERSION. La versión 2.0 está en uso si 0x0200 se devuelve.

|                   | Value                    |
|-------------------|--------------------------|
| **Tipo de proveedor** | PROV \_ RSA \_ AES           |
| **Nombre del proveedor** | MS \_ ENH \_ RSA \_ AES \_ PROV  |



 

En la tabla siguiente se resaltan las diferencias entre el proveedor base, el proveedor fuerte y el proveedor de AES. Las [*longitudes de clave que*](../secgloss/k-gly.md) se muestran son las longitudes de clave predeterminadas.



| Algoritmo                                                                                | Longitud de clave del proveedor base | Longitud de clave de proveedor segura | Longitud de clave del proveedor de AES                     |
|------------------------------------------------------------------------------------------|--------------------------|----------------------------|---------------------------------------------|
| Algoritmo de firma de clave pública RSA                                                       | 512 bits                 | 1024 bits                 | 1024 bits                                  |
| Algoritmo de intercambio de claves públicas RSA                                                        | 512 bits                 | 1024 bits                 | 1024 bits                                  |
| Algoritmo de cifrado de bloques RC2                                                           | 40 bits                  | 128 bits                   | Se puede establecer una longitud de sal de 128 bits.<br/> |
| Algoritmo de cifrado de flujo RC4                                                          | 40 bits                  | 128 bits                   | Se puede establecer una longitud de sal de 128 bits.<br/> |
| DES                                                                                      | 56 bits                  | 56 bits                    | 56 bits                                     |
| [*Triple DES*](../secgloss/t-gly.md) (2 claves) | No compatible            | 112 bits                   | 112 bits                                    |
| Triple DES (3 claves)                                                                       | No compatible            | 168 bits                   | 168 bits                                    |



 

Para obtener una lista completa de los algoritmos admitidos, vea [Algoritmos de proveedor de AES](aes-provider-algorithms.md).

El proveedor fuerte, el proveedor mejorado y el proveedor de AES son compatibles con el proveedor base, salvo que los proveedores solo pueden generar claves RC2 o RC4 de longitud de clave predeterminada. La longitud predeterminada del proveedor base es de 40 bits. La longitud predeterminada del proveedor de AES es de 128 bits. Por lo tanto, el proveedor de AES no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor de AES puede importar claves RC2 y RC4 de hasta 128 bits. Por lo tanto, el proveedor de AES puede importar y usar claves de 40 bits generadas mediante el proveedor base.

 

 
