---
description: Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del valor de sal que se va a utilizar. El proveedor base establece un valor Salt mediante el \_ valor del parámetro sal de KP. El proveedor base siempre establece once bytes de valor Salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Especificar un valor Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9fc8aeea66c536db1c24d7ef3cf4fb9a05b543f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669884"
---
# <a name="specifying-a-salt-value"></a>Especificar un valor Salt

Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del [*valor de sal*](../secgloss/s-gly.md) que se va a utilizar. El proveedor base establece un valor Salt mediante el \_ valor del parámetro sal de KP. El proveedor base siempre establece once bytes de valor Salt.

El proveedor mejorado establece el valor Salt llamando a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con el \_ valor de parámetro PK sal \_ ex especificado y con el parámetro *pbData* que apunta a una estructura de [**\_ \_ BLOB de tipo entero de cifrado**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)) que contiene el valor Salt.

> [!Note]  
> La longitud total de una [*clave simétrica*](../secgloss/s-gly.md) de proveedor mejorada y su valor Salt no puede ser superior a 128 bits.

 

\_Se sigue proporcionando sal de KP para la compatibilidad con versiones anteriores con el proveedor base. Las aplicaciones más recientes deben usar el \_ valor del parámetro PK sal \_ ex.

En el ejemplo siguiente se establece un valor Salt.


```C++
// Specify 4 bytes of salt.
BYTE rgbSalt[] = {0x01, 0x02, 0x03, 0x04};
CRYPT_DATA_BLOB sSaltData;
sSaltData.pbData = rgbSalt;
sSaltData.cbData = sizeof(rgbSalt);

// Set the 4 bytes of salt required.
// hKey is an HCRYPTPROV handle previously
// assigned, such as by CryptImportKey.
if (CryptSetKeyParam(
        hKey,    
        KP_SALT_EX,    
        (BYTE*)&sSaltData,    
        0))
{
     printf("The salt value is set.\n");
}
else
{
     printf("Setting the salt value failed.\n");
}
```



 

 
