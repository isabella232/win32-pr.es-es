---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Proveedores de almacenamiento de claves CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423671"
---
# <a name="cng-key-storage-providers"></a>Proveedores de almacenamiento de claves CNG

A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves (KSP). KSP se puede usar para crear, eliminar, exportar, importar, abrir y almacenar claves. En función de la implementación, también se pueden usar para el cifrado asimétrico, el acuerdo secreto y la firma. Microsoft instala los siguientes KSP a partir de Windows Vista y Windows Server 2008. Los proveedores pueden crear e instalar otros proveedores.

## <a name="microsoft-software-key-storage-provider"></a>Proveedor de almacenamiento de claves de software de Microsoft

Admite la creación y el almacenamiento de claves de software y los algoritmos siguientes.



| Algoritmo                                          | Propósito                           | Longitud de clave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acuerdo confidencial e intercambio de claves | de 512 a 4096 en incrementos de 64 bits  |
| Algoritmo de firma digital (DSA)                  | Prototipos                        | de 512 a 1024 en incrementos de 64 bits  |
| Diffie-Hellman de curva elíptica (ECDH)               | Acuerdo confidencial e intercambio de claves | P256, CLAVE P384, P521                  |
| Algoritmo de firma digital de curva elíptica (ECDSA) | Prototipos                        | P256, CLAVE P384, P521                  |
| RSA                                                | Firma y cifrado asimétrico | de 512 a 16384 en incrementos de 64 bits |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Proveedor de almacenamiento de claves de tarjeta inteligente de Microsoft

Admite la creación y el almacenamiento de claves de tarjeta inteligente y los algoritmos siguientes.



| Algoritmo                                          | Propósito                           | Longitud de clave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acuerdo confidencial e intercambio de claves | de 512 a 4096 en incrementos de 64 bits  |
| Diffie-Hellman de curva elíptica (ECDH)               | Acuerdo confidencial e intercambio de claves | P256, CLAVE P384, P521                  |
| Algoritmo de firma digital de curva elíptica (ECDSA) | Prototipos                        | P256, CLAVE P384, P521                  |
| RSA                                                | Firma y cifrado asimétrico | de 512 a 16384 en incrementos de 64 bits |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funciones de almacenamiento de claves CNG](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Descripción de los proveedores de servicios criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
