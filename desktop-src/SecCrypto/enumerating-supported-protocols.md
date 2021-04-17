---
description: Los protocolos admitidos y los conjuntos de cifrado se pueden enumerar mediante llamadas a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumerar protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666950"
---
# <a name="enumerating-supported-protocols"></a>Enumerar protocolos admitidos

Los protocolos admitidos y los conjuntos de cifrado se pueden enumerar mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ ex. El valor de PP \_ ENUMALGS \_ ex funciona como PP \_ ENUMALGS, pero devuelve una estructura [**Prov \_ ENUMALGS \_ ex**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) que contiene información más amplia sobre los algoritmos admitidos por el proveedor.

Para obtener más información sobre las marcas de protocolo definidas y sus valores, vea [marcas de protocolo](protocol-flags.md).

Dado que el miembro **hCryptProv** es el [*identificador*](../secgloss/h-gly.md) de un [*contexto*](../secgloss/c-gly.md) criptográfico abierto adquirido mediante [**CRYPTACQUIRECONTEXT**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) con su parámetro *dwProvType* establecido en Prov \_ RSA \_ Schannel, en el ejemplo siguiente se enumeran los nombres de todos los algoritmos disponibles en el CSP.


```C++
PROV_ENUMALGS_EX EnumAlgs;     //   Structure to hold information on 
                               //   a supported algorithm
DWORD dFlag = CRYPT_FIRST;     //   Flag indicating that the first
                               //   supported algorithm is to be
                               //   enumerated. Changed to 0 after the
                               //   first call to the function.
cbData = sizeof(PROV_ENUMALGS_EX);

while( CryptGetProvParam(
    hCryptProv,          // handle to an open cryptographic provider
    PP_ENUMALGS_EX, 
    (BYTE *)&EnumAlgs,  // information on the next algorithm
    &cbData,            // number of bytes in the PROV_ENUMALGS_EX
    dFlag))             // flag to indicate whether this is a first or
                        // subsequent algorithm supported by the
                        // CSP.
{
    printf("Supported Algorithm name %s\n", EnumAlgs.szName);
    dFlag = CRYPT_NEXT;          // Set to CRYPT_NEXT after the first call,
} //  end of while loop. When all of the supported algorithms have
  //  been enumerated, the function returns FALSE.
```



En la tabla siguiente se enumeran algunos de los algoritmos devueltos por un CSP de canal de provisión de RSA interno típico \_ \_ . Tenga en cuenta que el CSP no admite ni SSL2 SHA Mac ni cifrado DES SSL2 en este ejemplo.



| Identificador de algoritmo                                                                        | Longitud de clave mínima | Longitud máxima de la clave | Protocolos | Nombre del algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | MD5          |
| [*CALG \_ Sha*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | Sha          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | RC4          |
| CALG \_ des                                                                                   | 56                 | 56                 | 0x0005    | DES          |



 

Para prepararse para enviar mensajes ClientHello o ServerHello, el motor de protocolo [*Schannel*](../secgloss/s-gly.md) enumera los algoritmos y los tamaños de clave admitidos por el CSP y crea una lista internamente de los conjuntos de cifrado admitidos.

 

 
