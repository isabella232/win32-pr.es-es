---
description: Se usa con el proveedor de estándar de firma digital (DSS) para exportar claves desde el proveedor de servicios de cifrado (CSP) e importarlas en él.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Blobs de clave del proveedor de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001052"
---
# <a name="dss-provider-key-blobs"></a>Blobs de clave del proveedor de DSS

Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de [*estándar de firma digital*](../secgloss/d-gly.md) (DSS) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.

-   [Blobs de clave pública](#public-key-blobs)
-   [Blobs de clave privada](#private-key-blobs)

## <a name="public-key-blobs"></a>Blobs de clave pública

Una [*clave pública*](../secgloss/p-gly.md) de DSS se exporta e importa como un BLOB, una secuencia de bytes estructurada de la manera siguiente.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

En la tabla siguiente se describen estos componentes. Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descripción                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Estructura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . El miembro **mágico** debe tener un valor de 0x31535344. Este número hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DSS1. |
| e              | Secuencia de **bytes** . El generador, g. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.                                                                      |
| p              | Secuencia de **bytes** . El módulo primo, p. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                                 |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                                |
| q              | Secuencia de **bytes** . La longitud Prime, q, 20 bytes. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                     |
| seedstruct     | Estructura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valores de inicialización y contador para comprobar los primos.                                                                                                                                |
| y              | Secuencia de **bytes** . La clave pública, y. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.                                                                         |



 

> [!Note]  
> No se cifran los [*blobs de clave pública*](../secgloss/p-gly.md) . Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .

 

## <a name="private-key-blobs"></a>Blobs de clave privada

Una [*clave privada*](../secgloss/p-gly.md) de DSS se exporta e importa como una secuencia de bytes estructurada como se indica a continuación.

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

En la tabla siguiente se describe cada componente. Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .



| Campo          | Descripción                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | Estructura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) . El miembro **mágico** debe establecerse en 0x32535344. Este número hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DSS2. |
| e              | Secuencia de **bytes** . El generador, g. Debe tener la misma longitud que p. Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.                                                                |
| publickeystruc | Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .                                                                                                                                                          |
| p              | Secuencia de **bytes** . El módulo primo, p. El bit más significativo del byte más significativo debe establecerse en uno.                                                                                           |
| q              | Secuencia de **bytes** . El primo, q. q tiene una longitud de 20 bytes. El bit más significativo del byte más significativo debe establecerse en uno.                                                                          |
| seedstruct     | Estructura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) . Valores de inicialización y contador para comprobar los primos.                                                                                                                          |
| x              | Secuencia de **bytes** . El exponente secreto, x. Siempre debe tener una longitud de 20 bytes. Si x tiene menos de 20 bytes de longitud, debe rellenarse con 0x00.                                                     |



 

Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave. El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión. Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.

> [!Note]  
> Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada. La aplicación debe administrar y almacenar esta información. Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.

 

> [!Caution]  
> Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.

 

 

 
