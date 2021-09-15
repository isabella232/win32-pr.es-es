---
description: Los protocolos y conjuntos de cifrado admitidos se pueden enumerar mediante llamadas a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumeración de protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76976da7e3ab59e299d6ef0a8e9bcabce601c0b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476418"
---
# <a name="enumerating-supported-protocols"></a>Enumeración de protocolos admitidos

Los protocolos y conjuntos de cifrado admitidos se pueden enumerar mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX. El valor PP ENUMALGS EX funciona como \_ PP ENUMALGS, pero devuelve una estructura \_ \_ [**\_ ENUMALGS \_ EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) de PROV que contiene información más amplia sobre los algoritmos admitidos por el proveedor.

Para obtener más información sobre las marcas de protocolo definidas y sus valores, vea [Marcas de protocolo](protocol-flags.md).

Dado que el miembro **hCryptProv** es [](../secgloss/c-gly.md) el identificador de un contexto criptográfico abierto adquirido mediante [**CryptAcquireContext con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) su parámetro *dwProvType* establecido en PROV RSA [](../secgloss/h-gly.md) \_ \_ SCHANNEL, en el ejemplo siguiente se enumeran los nombres de todos los algoritmos disponibles en csp.


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



En la tabla siguiente se enumeran algunos algoritmos devueltos por un CSP \_ SCHANNEL RSA de PROV \_ típico. Tenga en cuenta que en este ejemplo no se admite el cifrado SSL2 SHA MACs ni SSL2 DES.



| Identificador de algoritmo                                                                        | Longitud mínima de clave | Longitud máxima de clave | Protocolos | Nombre del algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | "MD5"          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | "SHA"          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | "RC4"          |
| CALG \_ DES                                                                                   | 56                 | 56                 | 0x0005    | "DES"          |



 

Para prepararse para enviar mensajes ClientHello o ServerHello, el motor de [*protocoloSchannel*](../secgloss/s-gly.md) enumera los algoritmos y tamaños de clave admitidos por CSP y crea una lista internamente de conjuntos de cifrado admitidos.

 

 
