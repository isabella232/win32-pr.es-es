---
description: Explica el procedimiento utilizado para almacenar una clave de sesión.
ms.assetid: 9ab7f747-9c69-40b5-af78-163f3ba315bf
title: Almacenar una clave de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3b17de657ddba47dd77f68c1ee7a2adfdf93e7f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170877"
---
# <a name="storing-a-session-key"></a>Almacenar una clave de sesión

> [!Note]  
> En esta sección se da por supuesto que los usuarios poseen un conjunto de [*pares de claves pública y privada.*](../secgloss/p-gly.md) Puede encontrar instrucciones y un ejemplo para crear pares de claves en Ejemplo [de programa C: Creación](example-c-program-creating-a-key-container-and-generating-keys.md)de un contenedor de claves y Generación de claves .

 

**Para almacenar una clave de sesión**

1.  Cree un [*blob de clave*](../secgloss/k-gly.md) simple mediante la función [**CryptExportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) Esto transferirá la clave de sesión del CSP al espacio de memoria de una aplicación. Especifique que se usará una clave pública de intercambio para firmar el blob de clave.
2.  Almacene el blob de clave firmada en el disco. Se supone que todos los discos no son seguros.
3.  Cuando se necesite la clave, lea el BLOB de clave del disco.
4.  Vuelva a importar el blob de clave en el CSP mediante la [**función CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)

Para obtener un [](../secgloss/s-gly.md) ejemplo de cómo crear una clave de sesión y exportar esa clave a un blob de clave [*simple*](../secgloss/s-gly.md) que se puede escribir en un archivo de disco, vea Ejemplo [de programa C:](example-c-program-exporting-a-session-key.md)Exportar una clave de sesión .

Este procedimiento solo proporciona una seguridad mínima. Si la clave de sesión almacenada se usará para cifrar los datos en una fecha posterior, el procedimiento anterior no proporciona la seguridad adecuada.

Para proporcionar mayor seguridad, firme el BLOB de clave con una clave privada de intercambio antes de almacenarla en el disco. Cuando el BLOB de clave se lee más adelante desde el disco, se puede validar su firma para asegurarse de que la clave BLOB está intacta.

Si el BLOB de clave no está firmado, cualquier persona con acceso al disco u otro medio donde se almacena la clave puede crear una nueva clave de sesión.

La nueva clave de sesión se puede [](../secgloss/p-gly.md) cifrar con la clave de intercambio de clave pública del usuario original [*y*](../secgloss/e-gly.md)esta nueva clave se puede sustituir por la original. Si el usuario usó sin saberlo la clave de sesión sustituta para cifrar archivos y mensajes, el usuario que creó la clave de sustitución podría descifrarlos fácilmente.

Las firmas digitales se de abordan con detalle en [Hashes y firmas digitales.](hashes-and-digital-signatures.md)

 

 
