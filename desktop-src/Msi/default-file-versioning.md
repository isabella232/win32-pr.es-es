---
description: Los diagramas de flujo de las secciones siguientes muestran las reglas de control de versiones de archivos predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Control de versiones de archivo predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c239cd7989308e79dbb0ee621241560ac33a7a049c83c0a44d2cb1c3c32f5fb0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039995"
---
# <a name="default-file-versioning"></a>Control de versiones de archivo predeterminado

Los diagramas de flujo de las secciones siguientes muestran las reglas de control de versiones de archivos predeterminadas que se usan cuando el archivo de clave de un componente que se está instalando tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino. El control de versiones de archivos predeterminado también se muestra [en Reemplazo de archivos existentes.](replacing-existing-files.md)

Tenga en cuenta que Windows instalador, el hash de archivos está disponible para optimizar la copia de archivos. Para obtener más información, [**vea MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) y la [tabla MsiFileHash](msifilehash-table.md). La tabla MsiFileHash solo se puede usar con archivos sin versión.

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



