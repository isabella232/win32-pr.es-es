---
description: Microsoft Enhanced Cryptographic Provider proporciona una aplicación con una seguridad más segura que la que actualmente está disponible con el proveedor de servicios criptográficos de base de Microsoft. Una mayor longitud de clave proporciona a los usuarios más protección para los datos confidenciales.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparación de longitud de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913630"
---
# <a name="key-length-comparison"></a>Comparación de longitud de clave

Microsoft Enhanced Cryptographic Provider proporciona una aplicación con una seguridad más segura que la que actualmente está disponible con el proveedor de servicios criptográficos de base de Microsoft. Una mayor longitud de clave proporciona a los usuarios más protección para los datos confidenciales.

En la tabla siguiente se enumeran las [*longitudes de clave*](../secgloss/k-gly.md) predeterminadas admitidas por el proveedor base y el proveedor mejorado para los algoritmos estándar.



| Algoritmo                                                                                | Proveedor base | Proveedores sólidos y mejorados |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Intercambio de claves RSA                                                                         | 512 bits       | 1.024 bits                     |
| Firma RSA                                                                            | 512 bits       | 1.024 bits                     |
| RC2                                                                                      | 40 bits        | 128 bits                       |
| RC4                                                                                      | 40 bits        | 128 bits                       |
| DES                                                                                      | No compatible | 56 bits                        |
| [*Triple des*](../secgloss/t-gly.md) (2 teclas) | No compatible | 112 bits                       |
| Triple DES (3 teclas)                                                                       | No compatible | 168 bits                       |



 

Los algoritmos [*des*](../secgloss/d-gly.md) y [*triple des*](../secgloss/t-gly.md) se admiten en el proveedor mejorado.

El proveedor mejorado es compatible con versiones anteriores del proveedor base distribuido con versiones anteriores de CryptoAPI con la siguiente excepción. Tanto el proveedor base como el proveedor mejorado solo pueden generar claves de sesión de longitud de clave predeterminada. La longitud predeterminada de las claves de sesión para el proveedor base es 40 bits. La longitud de clave predeterminada para el proveedor mejorado es 128 bits. El proveedor mejorado no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor mejorado puede importar longitudes de clave de cualquier tamaño, hasta 128 bits.

 

 
