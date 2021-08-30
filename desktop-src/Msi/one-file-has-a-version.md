---
description: Si solo uno de los archivos tiene un número de versión, el instalador de Windows usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente.
ms.assetid: 1eda5521-6e23-49b8-9870-f5370def487e
title: Un archivo tiene una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e0dd1fd27dc5a0438e1cf5b6bbd787348d0971a378344536096ce7b99008fc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129245"
---
# <a name="one-file-has-a-version"></a>Un archivo tiene una versión

Si el archivo de clave de un componente que se está instalando (copy-A) tiene el mismo nombre que un archivo ya instalado en la ubicación de destino (copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.

Si solo uno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que en este diagrama se muestran las reglas de [control](file-versioning-rules.md)de versiones de archivos predeterminadas, que se pueden invalidar estableciendo la [**propiedad REINSTALLMODE.**](reinstallmode.md) El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

![reglas de control de versiones de archivos predeterminadas cuando solo un archivo tiene un número de versión](images/waiflow3.png)

Vea los ejemplos de control de versiones de archivos predeterminados en [Reemplazo de archivos existentes.](replacing-existing-files.md)

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)

 

 



