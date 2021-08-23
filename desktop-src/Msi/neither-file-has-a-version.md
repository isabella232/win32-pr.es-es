---
description: Si ninguno de los archivos tiene un número de versión, el instalador de Windows usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente.
ms.assetid: 82cb0d96-f49f-408e-a8c6-a0d1ee9af8c7
title: Ninguno de los archivos tiene una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68a6d74a26a810f2ddb33e1c13b2ed7b372a75d5b262a8b6d8d7ecaca1c99f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065944"
---
# <a name="neither-file-has-a-version"></a>Ninguno de los archivos tiene una versión

Si el archivo de clave de un componente que se está instalando (copy-A) tiene el mismo nombre que un archivo ya instalado en la ubicación de destino (copy-B), el instalador compara el número de versión, la fecha y el idioma de los dos archivos.

Si ninguno de los archivos tiene un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que en este diagrama se muestran las reglas de [control](file-versioning-rules.md)de versiones de archivo predeterminadas, que se pueden invalidar estableciendo la [**propiedad REINSTALLMODE.**](reinstallmode.md) El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

![reglas de control de versiones de archivos predeterminadas cuando ninguno de los archivos tiene un número de versión](images/waiflow2.png)

Vea los ejemplos de control de versiones de archivos predeterminados en [Reemplazo de archivos existentes.](replacing-existing-files.md)

-   [Ambos archivos tienen una versión](both-files-have-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



