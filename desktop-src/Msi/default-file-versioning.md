---
description: Los diagramas de flujo de las secciones siguientes muestran las reglas de control de versiones de archivos predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Control de versiones de archivo predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158616"
---
# <a name="default-file-versioning"></a>Control de versiones de archivo predeterminado

Los diagramas de flujo de las secciones siguientes muestran las reglas de control de versiones de archivos predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino. El control de versiones de archivos predeterminado también se ilustra [en Reemplazar archivos existentes.](replacing-existing-files.md)

Tenga en cuenta que Windows instalador de archivos, el hash de archivos está disponible para optimizar la copia de archivos. Para obtener más información, [**vea MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md). La tabla MsiFileHash solo se puede usar con archivos sin versión.

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



