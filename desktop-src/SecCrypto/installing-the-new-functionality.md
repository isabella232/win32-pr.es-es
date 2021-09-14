---
description: La instalación de nuevas funcionalidades en la memoria puede mejorar el rendimiento. Las funciones cryptoAPI buscan en la memoria la funcionalidad antes de buscar el archivo DLL en el Registro. El archivo DLL debe cargarse antes de instalar la funcionalidad.
ms.assetid: f6e5fc6a-a186-4648-af63-0555307f53d8
title: Instalación de la nueva funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7147a1a70ffe57f4948d7db94aab0184d29e5dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170990"
---
# <a name="installing-the-new-functionality"></a>Instalación de la nueva funcionalidad

La instalación de nuevas funcionalidades en la memoria puede mejorar el rendimiento. [*Las funciones cryptoAPI*](../secgloss/c-gly.md) buscan en la memoria la funcionalidad antes de buscar el archivo DLL en el Registro. El archivo DLL debe cargarse antes de instalar la funcionalidad.

[**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress) instala la dirección de la nueva funcionalidad. Debe colocarse en la **función DllMain** del archivo DLL.

Si *hModule* se pasa a [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress), una vez instalado, el archivo DLL no se descarga hasta que Crypt32.dll descarga.

En el ejemplo siguiente se llama a la función [**CryptInstallOIDFunctionAddress.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)


```C++
#include <windows.h>
#include <stdio.h>

#define X509_ENCODE_FUNC_COUNT (sizeof(X509EncodeFuncTable) / \
                                sizeof(X509EncodeFuncTable[0]))

static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD dwCertEncodingType,
        IN LPCSTR lpszStructType,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded
);

static const CRYPT_OID_FUNC_ENTRY X509EncodeFuncTable[] = {
    X509_ENHANCED_KEY_USAGE, OssX509CtlUsageEncode,
};

BOOL WINAPI DllMain(
    HMODULE hModule,
    ULONG  ulReason,
    LPVOID lpReserved)
{
    switch (ulReason)
    {
        case DLL_PROCESS_ATTACH:
            if (!CryptInstallOIDFunctionAddress(
                  hModule,
                  X509_ASN_ENCODING,
                  CRYPT_OID_ENCODE_OBJECT_FUNC,
                  X509_ENCODE_FUNC_COUNT,
                  X509EncodeFuncTable,
                  0))
            {
                printf("Install OID function address failed."); 
                return FALSE;
            }
            break;
         default:
            break;
    }
    return TRUE;
}

//-------------------------------------------------------------------
//  CTL Usage (Enhanced Key Usage) Encode (OSS X509)
//-------------------------------------------------------------------
static BOOL WINAPI OssX509CtlUsageEncode(
        IN DWORD /*dwCertEncodingType*/,
        IN LPCSTR /*lpszStructType*/,
        IN PCTL_USAGE pInfo,
        OUT BYTE *pbEncoded,
        IN OUT DWORD *pcbEncoded)
{
    //Encoding logic goes here.
}
```



 

 
