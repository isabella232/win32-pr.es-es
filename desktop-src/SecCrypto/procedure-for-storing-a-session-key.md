---
description: Explica el procedimiento utilizado para almacenar una clave de sesión.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Almacenar una clave de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687592"
---
# <a name="storing-a-session-key"></a>Almacenar una clave de sesión

> [!Note]  
> En esta sección se da por supuesto que los usuarios disponen de un conjunto de [*pares de claves pública y privada*](../secgloss/p-gly.md). Puede encontrar instrucciones y un ejemplo para crear pares de claves en [el programa C de ejemplo: crear un contenedor de claves y generar claves](example-c-program-creating-a-key-container-and-generating-keys.md).

 

**Para almacenar una clave de sesión**

1.  Cree un [*BLOB de clave*](../secgloss/k-gly.md) simple mediante la función [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) . Esto transferirá la clave de sesión del CSP al espacio de memoria de la aplicación. Especifique que se use una clave pública de Exchange para firmar el BLOB de clave.
2.  Almacene el BLOB de clave firmado en el disco. Se supone que todos los discos no son seguros.
3.  Cuando se necesite la clave, lea el BLOB de la clave desde el disco.
4.  Vuelva a importar el BLOB de la clave en el CSP mediante la función [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) .

Para obtener un ejemplo de cómo crear una [*clave de sesión*](../secgloss/s-gly.md) y exportar esa clave a un [*BLOB de clave simple*](../secgloss/s-gly.md) que se puede escribir en un archivo de disco, vea el [ejemplo C programa: exportar una clave de sesión](example-c-program-exporting-a-session-key.md).

Este procedimiento solo proporciona una seguridad mínima. Si la clave de sesión almacenada se va a usar para cifrar los datos en una fecha posterior, el procedimiento anterior no proporciona la seguridad adecuada.

Para proporcionar mayor seguridad, firme el BLOB de clave con una clave privada de Exchange antes de que se almacene en el disco. Cuando el BLOB de clave se lee después del disco, se puede validar su firma para asegurarse de que el BLOB de clave está intacto.

Si el BLOB de clave no está firmado, cualquier usuario con acceso al disco u otro medio donde se almacena la clave puede crear una nueva clave de sesión.

La nueva clave de sesión puede cifrarse con la [*clave de intercambio*](../secgloss/e-gly.md)de [*claves públicas*](../secgloss/p-gly.md) del usuario original, y esta nueva clave se puede sustituir por la original. Si el usuario usaba sin saberlo la clave de sesión sustituida para cifrar archivos y mensajes, el individuo que creó la clave sustitutivo podría descifrarlos fácilmente.

Las firmas digitales se describen en detalle en [hashes y firmas digitales](hashes-and-digital-signatures.md).

 

 
