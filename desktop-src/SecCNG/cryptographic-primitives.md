---
description: La API de CNG proporciona un conjunto de funciones que realizan operaciones criptográficas básicas, como la creación de hashes o el cifrado y descifrado de datos. Para obtener más información sobre estas funciones, vea Funciones primitivas criptográficas de CNG.
ms.assetid: 925848ae-9f4f-444a-81ff-14a1997434b2
title: Primitivos criptográficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0f390b36bc500bf80b5b2ef0065651cf99f5e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073666"
---
# <a name="cryptographic-primitives"></a>Primitivos criptográficos

La API de CNG proporciona un conjunto de funciones que realizan operaciones criptográficas básicas, como la creación de hashes o el cifrado y descifrado de datos. Para obtener más información sobre estas funciones, vea [Funciones primitivas criptográficas de CNG](cng-cryptographic-primitive-functions.md).

CNG implementa numerosos algoritmos criptográficos. Cada algoritmo o clase de algoritmos expone su propia API primitiva. Se pueden instalar varias implementaciones de un algoritmo determinado al mismo tiempo; sin embargo, solo una implementación será el valor predeterminado en un momento dado.

Cada clase de algoritmo de CNG se representa mediante un enrutador primitivo. Las aplicaciones que usan las funciones primitivas de CNG se vincularán al archivo binario del enrutador Bcrypt.dll en modo de usuario o Ksecdd.sys en modo kernel antes de llamar a las funciones. Varias rutinas de enrutador administran todas las primitivas de algoritmo. Estos enrutadores realiza un seguimiento de cada implementación de algoritmo instalada en el sistema y enruta cada llamada de función al módulo de proveedor primitivo adecuado.

CNG proporciona primitivas para las siguientes clases de algoritmos.



| Clase Algorithm                                                                                                                                                  | Descripción                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span id="Random_number_generator"></span><span id="random_number_generator"></span><span id="RANDOM_NUMBER_GENERATOR"></span>Generador de números aleatorios<br/> | Generación de números aleatorios conectables (RNG).<br/>                                                         |
| <span id="Hashing"></span><span id="hashing"></span><span id="HASHING"></span>Hash<br/>                                                                 | Algoritmos usados para el hash, como SHA1 y SHA2.<br/>                                               |
| <span id="Symmetric_encryption"></span><span id="symmetric_encryption"></span><span id="SYMMETRIC_ENCRYPTION"></span>Cifrado simétrico<br/>             | Algoritmos usados para el cifrado simétrico, como AES, 3DES y RC4.<br/>                             |
| <span id="Asymmetric_encryption"></span><span id="asymmetric_encryption"></span><span id="ASYMMETRIC_ENCRYPTION"></span>Cifrado asimétrico<br/>         | Algoritmos asimétricos (clave pública) que admiten el cifrado, como RSA.<br/>                          |
| <span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma<br/>                                                         | Algoritmos de firma como DSA y ECDSA. Esta clase también se puede usar con RSA.<br/>                 |
| <span id="Secret_agreement"></span><span id="secret_agreement"></span><span id="SECRET_AGREEMENT"></span>Contrato secreto<br/>                             | Algoritmos de acuerdo secreto, como Diffie-Hellman (DH) y la curva elíptica Diffie-Hellman (ECDH).<br/> |



 

En la ilustración siguiente se muestra el diseño y la función de las primitivas criptográficas de CNG.

![diseño y función de primitivas criptográficas de cng](images/ssdk-cng1c.png)

El archivo de encabezado Bcrypt.h define la constante **MS \_ PRIMITIVE \_ PROVIDER** como "Proveedor primitivo de Microsoft". Para usar el proveedor primitivo de Microsoft, pase este valor a [**BCryptOpenAlgorithmProvider**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider).

 

 




