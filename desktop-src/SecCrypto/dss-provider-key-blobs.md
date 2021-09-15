---
description: Se usa con el proveedor de Digital Signature Standard (DSS) para exportar claves del proveedor de servicios criptográficos (CSP) e importar claves en él.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Blobs de claves del proveedor de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476476"
---
# <a name="dss-provider-key-blobs"></a>Blobs de claves del proveedor de DSS

[*Los blobs se*](../secgloss/b-gly.md) usan con el proveedor [*de Digital Signature Standard*](../secgloss/d-gly.md) (DSS) para exportar claves desde el proveedor de servicios criptográficos (CSP) e importar claves en él. [](../secgloss/c-gly.md)

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Una clave pública [*DSS*](../secgloss/p-gly.md) se exporta e importa como BLOB, una secuencia de bytes estructurados de la manera siguiente.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

En la tabla siguiente se describen estos componentes. Todos los valores están en [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descripción                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Estructura [**DSSPUBKEY.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) El **miembro** mágico debe tener un valor de 0x31535344. Este número hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de DSS1. |
| e              | Secuencia **BYTE.** Generador, g. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe agregarse con 0x00 bytes.                                                                      |
| p              | Secuencia **BYTE.** Módulo primo, p. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                                 |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                                |
| q              | Secuencia **BYTE.** Prime, q, 20 bytes de longitud. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                     |
| seedstruct     | Estructura [**DSSSEED.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Valores de valor de valor de valor de valor y contador para comprobar los valores primos.                                                                                                                                |
| y              | Secuencia **BYTE.** La clave pública, y. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe agregarse con 0x00 bytes.                                                                         |



 

> [!Note]  
> [*Los blobs de clave pública*](../secgloss/p-gly.md) no están cifrados. Contienen claves públicas en [*formato de texto*](../secgloss/p-gly.md) no cifrado.

 

## <a name="private-key-blobs"></a>Blobs de clave privada

Una clave privada [*de*](../secgloss/p-gly.md) DSS se exporta e importa como una secuencia de bytes estructurados como se muestra a continuación.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

En la tabla siguiente se describe cada componente. Todos los valores están en [*formato little-endian.*](../secgloss/l-gly.md)



| Campo          | Descripción                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Estructura [**DSSPUBKEY.**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) El **miembro** mágico debe establecerse en 0x32535344. Este número hexadecimal es la [*codificación ASCII*](../secgloss/a-gly.md) de DSS2. |
| e              | Secuencia **BYTE.** Generador, g. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe agregarse con 0x00 bytes.                                                                |
| publickeystruc | Estructura [**PUBLICKEYSTRUC.**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)                                                                                                                                                          |
| p              | Secuencia **BYTE.** Módulo primo, p. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                           |
| q              | Secuencia **BYTE.** El valor primo, q. q tiene una longitud de 20 bytes. El bit más significativo del byte más significativo debe establecerse en uno.                                                                          |
| seedstruct     | Estructura [**DSSSEED.**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) Valores de valor de valor de valor de valor y contador para comprobar los valores primos.                                                                                                                          |
| x              | Secuencia **BYTE.** Exponente secreto, x. Siempre debe tener una longitud de 20 bytes. Si x tiene una longitud inferior a 20 bytes, se debe agregar con 0x00.                                                     |



 

Al llamar [**a CryptExportKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)el desarrollador puede elegir si cifrar la clave. **PrivateKEYBLOB se** cifra si el *parámetro hExpKey* contiene un identificador válido para una clave de sesión. Todo menos la [**parte PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrada.

> [!Note]  
> El algoritmo de cifrado y los parámetros de clave de cifrado no se almacenan junto con el blob de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar claves privadas sin cifrado porque, a continuación, son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

 

 
