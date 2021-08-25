---
description: Los protocolos y conjuntos de cifrado admitidos se pueden enumerar mediante llamadas a CryptGetProvParam con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX.
ms.assetid: 8f0c2129-6841-4793-a404-bb6ee8f41683
title: Enumeración de protocolos admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d7236fe20901e9feb48e844deceea47e8f5936b9685580a653f1480b3b667c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874435"
---
# <a name="enumerating-supported-protocols"></a>Enumeración de protocolos admitidos

Los protocolos y conjuntos de cifrado admitidos se pueden enumerar mediante llamadas a [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con PP \_ ENUMALGS o PP \_ ENUMALGS \_ EX. El valor PP ENUMALGS EX funciona como PP ENUMALGS, pero devuelve una estructura \_ \_ \_ [**\_ PROV ENUMALGS \_ EX**](/windows/desktop/api/Wincrypt/ns-wincrypt-prov_enumalgs_ex) que contiene información más amplia sobre los algoritmos admitidos por el proveedor.

Para obtener más información sobre las marcas de protocolo definidas y sus valores, vea [Marcas de protocolo.](protocol-flags.md)

Dado que el miembro **hCryptProv** es [](../secgloss/c-gly.md) el identificador de un contexto criptográfico abierto adquirido mediante [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) con su parámetro *dwProvType* establecido en PROV [](../secgloss/h-gly.md) \_ RSA SCHANNEL, en el ejemplo siguiente se enumeran los nombres de todos los algoritmos disponibles en el \_ CSP.


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



En la tabla siguiente se enumeran algunos algoritmos devueltos por un CSP SCHANNEL RSA de PROV \_ \_ típico. Tenga en cuenta que el CSP no admite los MACs SHA SSL2 ni el cifrado DES SSL2 en este ejemplo.



| Identificador de algoritmo                                                                        | Longitud de clave mínima | Longitud máxima de clave | Protocolos | Nombre del algoritmo |
|---------------------------------------------------------------------------------------------|--------------------|--------------------|-----------|----------------|
| [*CALG \_ RSA \_ KEYX*](../secgloss/c-gly.md) | 512                | 2048               | 0x0007    | "RSA \_ KEYX"    |
| [*CALG \_ MD5*](../secgloss/c-gly.md)                 | 128                | 128                | 0x0007    | "MD5"          |
| [*CALG \_ SHA*](../secgloss/c-gly.md)                 | 160                | 160                | 0x0005    | "SHA"          |
| [*CALG \_ RC4*](../secgloss/c-gly.md)                 | 40                 | 128                | 0x0007    | "RC4"          |
| CALG \_ DES                                                                                   | 56                 | 56                 | 0x0005    | "DES"          |



 

Para prepararse para enviar mensajes ClientHello o ServerHello, el motor de [*protocoloSchannel*](../secgloss/s-gly.md) enumera los algoritmos y tamaños de clave admitidos por CSP y crea una lista internamente de los conjuntos de cifrado admitidos.

 

 
