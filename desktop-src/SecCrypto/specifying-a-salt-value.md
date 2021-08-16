---
description: Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del valor salt que se va a usar. El proveedor base establece un valor salt mediante el valor del \_ parámetro KP SALT. El proveedor base siempre establece once bytes de valor salt.
ms.assetid: ea56d064-b725-431f-b951-66167624e14b
title: Especificar un valor salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d80ca64bc69cbcf0ed98d72b5b061616fc3cf641f3970d1533b094ef5687f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897950"
---
# <a name="specifying-a-salt-value"></a>Especificar un valor salt

Tanto el proveedor base como el proveedor extendido pueden especificar el valor y la longitud del [*valor salt*](../secgloss/s-gly.md) que se va a usar. El proveedor base establece un valor salt mediante el valor del \_ parámetro KP SALT. El proveedor base siempre establece once bytes de valor salt.

El proveedor mejorado establece el valor salt llamando a [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) con el valor del parámetro KP SALT EX especificado y con el parámetro pbData que apunta a una estructura \_ \_ [**CRYPT \_ INTEGER \_ BLOB**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))  que contiene el valor salt.

> [!Note]  
> La longitud total de una clave [*simétrica*](../secgloss/s-gly.md) del proveedor mejorado y su valor de sal no puede ser superior a 128 bits.

 

KP \_ SALT se sigue proporcionando para la compatibilidad con versiones anteriores con el proveedor base. Las aplicaciones más recientes deben usar el valor \_ del parámetro KP SALT \_ EX.

En el ejemplo siguiente se establece un valor sal.


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



 

 
