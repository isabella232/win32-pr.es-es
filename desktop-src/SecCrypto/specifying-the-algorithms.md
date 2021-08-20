---
description: Después de crear o importar una clave maestra, TANTO RSA/Schannel como Diffie-Hellman/Schannel informan al CSP del tipo de claves de cifrado masivo y claves MAC que se derivarán de la clave maestra.
ms.assetid: d0976a7e-3c8e-4bbe-80e1-568a27ab81c6
title: Especificar los algoritmos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b45bf68025b7233b5347e320eab348a3fe3528b76ceec3ec047ef634710d90e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117972646"
---
# <a name="specifying-the-algorithms"></a>Especificar los algoritmos

Después [](../secgloss/m-gly.md) de crear o importar una clave maestra, [*RSA*](../secgloss/r-gly.md)/Schannel y [*Diffie-Hellman*](../secgloss/d-gly.md)/Schannel informan al [*CSP*](../secgloss/c-gly.md) del tipo de claves de cifrado masivo y claves [*MAC*](../secgloss/m-gly.md) que se derivarán de la clave maestra. [](../secgloss/b-gly.md) En el ejemplo siguiente se especifican estos algoritmos. Se usa el mismo código para el cliente y el servidor.


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
> Un [*motor de protocolo de Schannel*](../secgloss/s-gly.md) no debe especificar algoritmos y tamaños de clave no admitidos por el CSP. Para obtener más información, [vea Enumerating Supported Protocols](enumerating-supported-protocols.md). Si se especifican algoritmos o tamaños de clave no admitidos, la función CSP debe producir un error y devolver el código de \_ error NTE BAD \_ DATA.

 

 

 
