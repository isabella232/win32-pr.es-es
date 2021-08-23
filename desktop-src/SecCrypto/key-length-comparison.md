---
description: El proveedor de servicios criptográficos mejorado de Microsoft proporciona una aplicación con mayor seguridad que la disponible actualmente con el proveedor criptográfico base de Microsoft. Una mayor longitud de clave proporciona a los usuarios más protección para la información confidencial.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparación de longitud de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c65615f6ffb9679b922600c4617e401067d565ac7dd62a258ae07a757d2cec7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622350"
---
# <a name="key-length-comparison"></a>Comparación de longitud de clave

El proveedor de servicios criptográficos mejorado de Microsoft proporciona una aplicación con mayor seguridad que la disponible actualmente con el proveedor criptográfico base de Microsoft. Una mayor longitud de clave proporciona a los usuarios más protección para la información confidencial.

En la tabla siguiente se enumeran las [*longitudes de clave predeterminadas admitidas*](../secgloss/k-gly.md) por el proveedor base y el proveedor mejorado para algoritmos estándar.



| Algoritmo                                                                                | Proveedor base | Proveedores seguros y mejorados |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| Clave RSA Exchange                                                                         | 512 bits       | 1024 bits                     |
| Firma RSA                                                                            | 512 bits       | 1024 bits                     |
| RC2                                                                                      | 40 bits        | 128 bits                       |
| RC4                                                                                      | 40 bits        | 128 bits                       |
| DES                                                                                      | No compatible | 56 bits                        |
| [*Triple DES*](../secgloss/t-gly.md) (2 claves) | No compatible | 112 bits                       |
| Triple DES (3 claves)                                                                       | No compatible | 168 bits                       |



 

[*Los algoritmos DES*](../secgloss/d-gly.md) [*y Triple DES*](../secgloss/t-gly.md) se admiten en el proveedor mejorado.

El proveedor mejorado es compatible con versiones anteriores con el proveedor base distribuido con versiones anteriores de CryptoAPI con la siguiente excepción. Tanto el proveedor base como el proveedor mejorado solo pueden generar claves de sesión de longitud de clave predeterminada. La longitud predeterminada de las claves de sesión para el proveedor base es de 40 bits. La longitud de clave predeterminada para el proveedor mejorado es de 128 bits. El proveedor mejorado no puede crear claves con longitudes de clave compatibles con el proveedor base. Sin embargo, el proveedor mejorado puede importar longitudes de clave de cualquier tamaño, hasta 128 bits.

 

 
