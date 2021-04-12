---
description: Los blobs opacos, también conocidos como OPAQUEKEYBLOBs, se usan para almacenar las claves de sesión en un formato específico del proveedor, como Schannel.
ms.assetid: a0756c03-0c27-41ff-9b74-8af462e09675
title: Tipo de BLOB opaco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e45cf8899d5cc63fb360a6b5e4177733de3880f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104424036"
---
# <a name="opaque-blob-type"></a>Tipo de BLOB opaco

Los [*blobs opacos*](../secgloss/o-gly.md), también conocidos como OPAQUEKEYBLOBs, se usan para almacenar [*las claves de sesión*](../secgloss/s-gly.md) en un formato específico del proveedor, como [*Schannel*](../secgloss/s-gly.md). Contienen el material de clave base y toda la información de [*Estado*](../secgloss/s-gly.md) actual. Esto incluye información como el [*valor Salt*](../secgloss/s-gly.md), el [*Vector de inicialización*](../secgloss/i-gly.md)y la tabla de claves. El formato de los blobs opacos no se publica. Cada proveedor de CSP determina su propio formato de BLOB.

Dado que una clave se exporta a un BLOB opaco en formato específico de CSP, solo se puede importar en el CSP desde el que se exportó originalmente.

Cuando hay dos procesos implicados, cada [*proceso*](../secgloss/p-gly.md) llama a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) independientemente. Cada proceso obtiene un identificador de un contenedor de claves. Es posible que ambos procesos tengan identificadores al mismo contenedor de claves. Un proceso crea las claves y las exporta a los blobs opacos y, después, pasa los blobs al segundo proceso. El segundo proceso importa las claves del BLOB en el [*contenedor de claves*](../secgloss/k-gly.md).

Si un CSP de hardware no admite la exportación de claves, es posible que el BLOB solo contenga el índice de un registro de claves o algo similar. En este caso, se omite el resto del procedimiento.

``` syntax
<secure process>
cbBlob = sizeof(rgbBlob);
CryptExportKey(
          hKey, 
          0, 
          OPAQUEKEYBLOB, 
          0, 
          rgbBlob, 
          &cbBlob);
hKey = 0;

<BLOB is transferred to other process>

<user process>
CryptImportKey(
            hProv, 
            pbBlob, 
            cbBlob, 
            0, 
            0, 
            &hKey);
```

 

 
