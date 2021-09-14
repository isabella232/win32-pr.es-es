---
description: Las siguientes funciones se encuentran entre las funciones cryptoAPI que se pueden extender.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Creación de la nueva funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173281"
---
# <a name="creating-the-new-functionality"></a>Creación de la nueva funcionalidad

Las siguientes funciones se encuentran entre las funciones cryptoAPI que se pueden extender.



| Función CryptoAPI                                   | Definición del nombre de la función OID                         | Cadena de nombre de función OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | CRYPT \_ OID \_ ENCODE \_ OBJECT \_ FUNC<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ DECODE \_ OBJECT \_ FUNC<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CRYPT \_ OID \_ OPEN \_ STORE \_ PROV \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CRYPT \_ OID \_ VERIFY \_ CTL \_ USAGE \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CRYPT \_ OID \_ VERIFY \_ REVOCATION \_ FUNC<br/> | "CertDllVerifyRevocation" |



 

En uso normal con un OID y un tipo de codificación existentes, se usa el código de la función CryptoAPI. Si se llama a una de estas funciones con un OID y un tipo de codificación que el código de la función CryptoAPI no se ha diseñado para controlar, se debe crear una nueva función, que contiene la nueva funcionalidad, en un archivo DLL. Ese archivo DLL debe estar registrado en el registro o instalado en memoria.

Cuando se llama a una de las funciones enumeradas con el OID recién designado y el tipo de codificación, se usa el código del nuevo archivo DLL en lugar del código proporcionado como parte de la función CryptoAPI.

El nombre de la función recién desarrollada puede ser el nombre que aparece en "OID function name string" (Cadena de nombre de función OID) en la tabla anterior o se puede proporcionar un nombre diferente cuando se registra el nuevo código de función.

La nueva función debe usar un prototipo adecuado. En todos los casos, excepto [**CertOpenStore,**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)este prototipo es el mismo que la función CryptoAPI que llama a la nueva función. En el caso de **CertOpenStore,** el prototipo es el siguiente.


```C++
#include <windows.h>

BOOL WINAPI CertDllOpenStoreProv(
  IN LPCSTR lpszStoreProvider,
  IN DWORD dwEncodingType,
  IN HCRYPTPROV hCryptProv,
  IN DWORD dwFlags,
  IN const void *pvPara,
  IN HCERTSTORE hCertStore,
  IN OUT PCERT_STORE_PROV_INFO pStoreProvInfo
);
```



> [!Note]  
> Si los prototipos no coinciden, la pila del sistema se dañará.

 

Además de proporcionar el código para la nueva función en un archivo DLL, la extensión de la funcionalidad de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requiere una definición de tipo para que la nueva estructura de datos de C se coloque en un archivo de encabezado incluido cuando se compile el programa del usuario.

 

 




