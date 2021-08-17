---
description: Las claves asimétricas, también conocidas como pares de claves públicas y privadas, se usan para el cifrado asimétrico. El cifrado asimétrico se usa principalmente para cifrar y descifrar claves de sesión y firmas digitales. El cifrado asimétrico usa algoritmos de cifrado de clave pública.
ms.assetid: f75e5e6c-0a84-47ac-97db-5063327f7931
title: Claves asimétricas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374ba5ae17610154e306f7bdafd895116e83371ea446babfa19b5c92c29a2247
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118901477"
---
# <a name="asymmetric-keys"></a>Claves asimétricas

[*Las claves asimétricas,*](../secgloss/a-gly.md)también conocidas como [*pares de claves públicas*](../secgloss/p-gly.md)y privadas, se usan para el cifrado asimétrico. El cifrado asimétrico se usa principalmente para cifrar y descifrar claves [*de sesión*](../secgloss/s-gly.md) y [*firmas digitales.*](../secgloss/d-gly.md) El cifrado asimétrico usa [*algoritmos de cifrado de clave*](../secgloss/p-gly.md) pública.

Los algoritmos de clave pública usan dos claves diferentes: [*una clave pública y*](../secgloss/p-gly.md) una clave [*privada.*](../secgloss/p-gly.md) El miembro de clave privada del par debe mantenerse privado y seguro. Sin embargo, la clave pública se puede distribuir a cualquier persona que lo solicite. La clave pública de un par de claves a menudo se distribuye mediante un [*certificado digital*](../secgloss/c-gly.md). Cuando se usa una clave de un par de claves para cifrar un mensaje, se requiere la otra clave de ese par para descifrar el mensaje. Por lo tanto, si la clave pública del usuario A se usa para cifrar los datos, solo el usuario A (o alguien que tenga acceso a la clave privada del usuario A) puede descifrar los datos. Si se usa la clave privada del usuario A para cifrar un fragmento de datos, solo la clave pública del usuario A descifrará los datos, lo que indica que el usuario A (o alguien con acceso a la clave privada del usuario A) hizo el cifrado.

Si la clave privada se usa para firmar un mensaje, se debe usar la clave pública de ese par para validar la firma. Por ejemplo, si Alice quiere enviar un mensaje firmado digitalmente a alguien, firmaría el mensaje con su clave privada y la otra persona podría comprobar su firma con su clave pública. Dado que, presumiblemente, solo Alice tiene acceso a su clave privada, el hecho de que la firma se pueda comprobar con la clave pública de Alice indica que Alice creó la firma.

Desafortunadamente, los algoritmos de clave pública son muy lentos, aproximadamente 1000 veces más lentos que los algoritmos simétricos. No es práctico usarlos para cifrar grandes cantidades de datos. En la práctica, los algoritmos de clave pública se usan para cifrar las [*claves de sesión*](../secgloss/s-gly.md). [*Los algoritmos simétricos*](../secgloss/s-gly.md) se usan para el cifrado y descifrado de la mayoría de los datos.

Del mismo modo, dado que firmar un mensaje, en efecto, cifra el mensaje, no es práctico usar algoritmos de firma de clave pública para firmar mensajes grandes. En su lugar, se realiza un [*hash*](../secgloss/h-gly.md) de longitud fija del mensaje y se firma el valor hash. Para obtener más información, [vea Hashes and Digital Signatures](hashes-and-digital-signatures.md).

Por lo general, cada usuario tiene dos [*pares de claves pública y privada.*](../secgloss/p-gly.md) Un par de claves se usa para cifrar las claves de sesión y el otro para crear [*firmas digitales.*](../secgloss/d-gly.md) Se conocen como el par [*de claves de intercambio de claves*](../secgloss/k-gly.md) y el par de claves de [*firma*](../secgloss/s-gly.md), respectivamente.

Tenga en cuenta que [](../secgloss/c-gly.md) aunque los contenedores de claves creados por la mayoría de los proveedores de servicios criptográficos (CSP) contienen dos pares de claves, esto no es necesario. Algunos CSP no almacenan ningún par [*de claves,*](../secgloss/k-gly.md) mientras que otros CSP almacenan más de dos pares.

Todas las claves de CryptoAPI se almacenan en LOSPS. Los CSP también son responsables de crear las claves, destruirlas y usarlas para realizar diversas operaciones criptográficas. La exportación de claves fuera del CSP para que se puedan enviar a otros usuarios se describe en [Clave criptográfica Storage](cryptographic-key-storage-and-exchange.md)y Exchange .

 

 
