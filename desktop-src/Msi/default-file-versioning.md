---
description: En los diagramas de flujo de las secciones siguientes se muestran las reglas de control de versiones de archivo predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo ya instalado en la ubicación de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Control de versiones de archivo predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910978"
---
# <a name="default-file-versioning"></a>Control de versiones de archivo predeterminado

En los diagramas de flujo de las secciones siguientes se muestran las reglas de control de versiones de archivo predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo ya instalado en la ubicación de destino. El control de versiones de archivo predeterminado también se muestra en [reemplazar archivos existentes](replacing-existing-files.md).

Tenga en cuenta que, con Windows Installer, el hash de archivo está disponible para optimizar la copia de archivos. Para obtener más información, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md). La tabla MsiFileHash solo se puede usar con archivos sin versión.

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



