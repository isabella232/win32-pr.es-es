---
description: El hash de archivos está disponible con Windows instalador. Para obtener más información, vea MsiGetFileHash y la tabla MsiFileHash. La tabla MsiFileHash solo se puede usar con archivos sin versión.
ms.assetid: 608859ac-6640-4c28-b4f0-34ab36d804d7
title: Ninguno de los archivos tiene una versión con comprobación de hash de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb874cdc29c56f34be2d4ec8604c2436892744e44581258ec237f515600f9024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869205"
---
# <a name="neither-file-has-a-version-with-file-hash-check"></a>Ninguno de los archivos tiene una versión con comprobación de hash de archivo

El hash de archivos está disponible con Windows instalador. Para obtener más información, [**vea MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md). La tabla MsiFileHash solo se puede usar con archivos sin versión.

Si el archivo de clave de un componente que se está instalando (copy-A) tiene el mismo nombre que un archivo ya instalado en la ubicación de destino (copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.

Si ninguno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que en este diagrama se muestran las reglas de [control](file-versioning-rules.md)de versiones de archivos predeterminadas, que se pueden invalidar estableciendo la [**propiedad REINSTALLMODE.**](reinstallmode.md) El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

![reglas de control de versiones de archivos predeterminadas cuando se reemplazan por la configuración de la propiedad reinstallmode](images/waiflow2b.png)

Vea los ejemplos de control de versiones de archivos predeterminados en [Reemplazo de archivos existentes.](replacing-existing-files.md)

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



