---
description: Si solo uno de los archivos tiene un número de versión, el Windows Installer usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Un archivo tiene una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417060119f8b13b1545161faa80552c79e8ca9aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155129"
---
# <a name="one-file-has-a-version"></a>Un archivo tiene una versión

Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.

Si solo uno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) . El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".

![reglas predeterminadas de control de versiones de archivo cuando solo un archivo tiene un número de versión](images/waiflow3.png)

Vea los ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)

 

 



