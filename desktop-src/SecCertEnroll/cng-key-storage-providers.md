---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores criptográficos de los proveedores de almacenamiento de claves (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Proveedores de claves Storage CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edef5858f4df370c7495c8796b552e00c080cc6a9da75e34fc21216bf2adc7bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670235"
---
# <a name="cng-key-storage-providers"></a>Proveedores de claves Storage CNG

A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores criptográficos de los proveedores de almacenamiento de claves (KSP). Los KSP se pueden usar para crear, eliminar, exportar, importar, abrir y almacenar claves. En función de la implementación, también se pueden usar para el cifrado asimétrico, el acuerdo secreto y la firma. Microsoft instala los siguientes KSP a partir de Windows Vista y Windows Server 2008. Los proveedores pueden crear e instalar otros proveedores.

## <a name="microsoft-software-key-storage-provider"></a>Proveedor de claves de software Storage Microsoft

Admite la creación y el almacenamiento de claves de software y los algoritmos siguientes.



| Algoritmo                                          | Propósito                           | Longitud de clave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acuerdo secreto e intercambio de claves | De 512 a 4096 en incrementos de 64 bits  |
| Algoritmo de firma digital (DSA)                  | Prototipos                        | De 512 a 1024 en incrementos de 64 bits  |
| Curva elíptica Diffie-Hellman (ECDH)               | Acuerdo secreto e intercambio de claves | P256, P384, P521                  |
| Algoritmo de firma digital de curva elíptica (ECDSA) | Prototipos                        | P256, P384, P521                  |
| RSA                                                | Cifrado y firma asimétricos | De 512 a 16384 en incrementos de 64 bits |



 

## <a name="microsoft-smart-card-key-storage-provider"></a>Proveedor de claves de tarjeta inteligente Storage Microsoft

Admite la creación y el almacenamiento de claves de tarjeta inteligente y los algoritmos siguientes.



| Algoritmo                                          | Propósito                           | Longitud de clave (bits)                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| Diffie-Hellman (DH)                                | Acuerdo secreto e intercambio de claves | De 512 a 4096 en incrementos de 64 bits  |
| Curva elíptica Diffie-Hellman (ECDH)               | Acuerdo secreto e intercambio de claves | P256, P384, P521                  |
| Algoritmo de firma digital de curva elíptica (ECDSA) | Prototipos                        | P256, P384, P521                  |
| RSA                                                | Cifrado y firma asimétricos | De 512 a 16384 en incrementos de 64 bits |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Identificadores de algoritmo CNG**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[Funciones de clave Storage CNG](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[Descripción de los proveedores criptográficos](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
