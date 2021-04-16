---
description: Las siguientes funciones se encuentran entre las funciones de CryptoAPI que se pueden extender.
ms.assetid: eb4c1352-1432-4f45-a309-fa17b694a35e
title: Crear la nueva funcionalidad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d660c14e99247c7d17f57100858b104d1cbcc9ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541006"
---
# <a name="creating-the-new-functionality"></a>Crear la nueva funcionalidad

Las siguientes funciones se encuentran entre las funciones de CryptoAPI que se pueden extender.



| Función CryptoAPI                                   | Definición de nombre de función OID                         | Cadena de nombre de función OID  |
|------------------------------------------------------|--------------------------------------------------|---------------------------|
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)       | CRYPT \_ OID \_ encode \_ Object \_ FUNC<br/>     | "CryptDllEncodeObject"    |
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)       | CRYPT \_ OID \_ descodificar \_ objeto \_ FUNC<br/>     | "CryptDllDecodeObject"    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)               | CIFRAdo de \_ almacenamiento abierto de OID de CRYPT \_ \_ \_ \_ FUNC<br/>  | "CertDllOpenStoreProv"    |
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)     | CIFRAr \_ OID \_ comprobar \_ CTL \_ uso \_ FUNC<br/> | "CertDllVerifyCTLUsage"   |
| [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation) | CIFRAr \_ OID \_ comprobar la \_ revocación \_ funci<br/> | "CertDllVerifyRevocation" |



 

En el uso normal con un OID y un tipo de codificación existentes, se utiliza el código de la función CryptoAPI. Si se llama a una de estas funciones con un OID y un tipo de codificación que el código de la función CryptoAPI no estaba diseñado para controlar, se debe crear una nueva función que contenga la nueva funcionalidad en un archivo DLL. Ese archivo DLL debe estar registrado en el registro o instalado en la memoria.

Cuando se llama a una de las funciones enumeradas con el OID y el tipo de codificación recién designados, se usa el código del nuevo archivo DLL en lugar del código proporcionado como parte de la función CryptoAPI.

El nombre de la función recién desarrollada puede ser el nombre que aparece en "cadena de nombre de función OID" en la tabla anterior o se puede proporcionar un nombre diferente cuando se registra el nuevo código de función.

La nueva función debe usar un prototipo adecuado. En todos los casos excepto [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore), este prototipo es el mismo que el de la función CryptoAPI que llama a la nueva función. En el caso de **CertOpenStore** , el prototipo es como se indica a continuación.


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
> Si los prototipos no coinciden, la pila del sistema estará dañada.

 

Además de proporcionar el código para la nueva función en un archivo DLL, la extensión de la funcionalidad de [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject) o [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject) requiere una definición de tipo para la nueva estructura de datos de C que se va a colocar en un archivo de encabezado incluido al compilar el programa del usuario.

 

 




