---
description: Después de crear o importar una clave maestra, tanto RSA/Schannel como Diffie-Hellman/Schannel informan al CSP del tipo de claves de cifrado masivo y de las claves MAC que se derivarán de la clave maestra.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Especificar los algoritmos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f5d329486c655fbc347d35870cfe81335678cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648215"
---
# <a name="specifying-the-algorithms"></a>Especificar los algoritmos

Después de crear o importar una [*clave maestra*](../secgloss/m-gly.md) , tanto [*RSA*](../secgloss/r-gly.md)/Schannel como [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel informan al [*CSP*](../secgloss/c-gly.md) del tipo de [*claves de cifrado masivo*](../secgloss/b-gly.md) y de [*las claves Mac*](../secgloss/m-gly.md) que se derivarán de la clave maestra. En el ejemplo siguiente se especifican estos algoritmos. Se usa el mismo código para el cliente y el servidor.


```C++
#include <windows.h>
#include <stdio.h>

typedef struct _SCHANNEL_ALG 
{
    DWORD  dwUse;
    ALG_ID Algid;
    DWORD  cBits;
    DWORD  dwFlags;
    DWORD  dwReserved;
} SCHANNEL_ALG, *PSCHANNEL_ALG;

SCHANNEL_ALG Algorithm;

//--------------------------------------------------------------------
// Algorithms for the SCHANNEL_ALG structure

#define SCHANNEL_MAC_KEY   0x00000000
#define SCHANNEL_ENC_KEY   0x00000001

//--------------------------------------------------------------------
// dwFlags for the SCHANNEL_ALG structure
// This flag will be set when the SSL cipher suite is exportable 
// outside the United States and Canada. The use of this flag notifies
// the CSP that it must perform the extra export steps when deriving 
// the key.

#define INTERNATIONAL USAGE   0x00000001

void main()
{
//--------------------------------------------------------------------
// Specify the bulk encryption algorithm.

Algorithm.dwUse = SCHANNEL_ENC_KEY;
Algorithm.Algid = CALG_RC4;    // or CALG_RC2, CALG_DES, and so on
Algorithm.cBits = 40;          // or 64, 128, 192, and so on
if (!CryptSetKeyParam(
         hMasterKey, 
         KP_SCHANNEL_ALG, 
         (PBYTE)&Algorithm, 
         0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};

//--------------------------------------------------------------------
// Specify hash algorithm.
Algorithm.dwUse = SCHANNEL_MAC_KEY;
Algorithm.Algid = CALG_MD5;    // or CALG_SHA, and so on
Algorithm.cBits = 128;         // or 160...
if (!CryptSetKeyParam(
          hMasterKey, 
          KP_SCHANNEL_ALG, 
          (PBYTE)&Algorithm, 
          0))
{
    printf("Failed called to CryptSetKeyParam\n");
    exit(1);
};
```



> [!Note]  
> Un motor de protocolo [*Schannel*](../secgloss/s-gly.md) no debe especificar los algoritmos y los tamaños de clave no admitidos por el CSP. Para obtener más información, vea [enumerar los protocolos admitidos](enumerating-supported-protocols.md). Si se especifican los algoritmos no admitidos o los tamaños de clave, la función de CSP debe producir un error y devolver el \_ código de error de datos incorrectos de NTE \_ .

 

 

 
