---
description: Si ambos archivos tienen un número de versión, el instalador de Windows usa la lógica ilustrada en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Ambos archivos tienen una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1338a93b4a45094a9a5951c3c59def15affde96dbbe74f3b134ba9dd7532092
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118380857"
---
# <a name="both-files-have-a-version"></a>Ambos archivos tienen una versión

Si el archivo de clave de un componente que se está instalando (copy-A) tiene el mismo nombre que un archivo ya instalado en la ubicación de destino (copy-B), el instalador compara el número de versión y el idioma de los dos archivos.

Si ambos archivos tienen un número de versión, el instalador usa la lógica ilustrada en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenecen al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que en este diagrama se muestran las reglas de [control](file-versioning-rules.md)de versiones de archivo predeterminadas, que se pueden invalidar estableciendo la [**propiedad REINSTALLMODE.**](reinstallmode.md) El valor predeterminado de la **propiedad REINSTALLMODE** es "omus".

![reglas de control de versiones de archivos predeterminadas cuando ambos archivos tienen el mismo nombre o número de versión](images/waiflow1.png)

El diagrama anterior también se puede usar con archivos sin ningún idioma especificado. Si copy-A tiene un idioma especificado y copy-B no tiene ningún idioma especificado, copy-B se reemplaza por copy-A. Si copy-A y copy-B no tienen ningún idioma especificado, copy-B no se reemplaza.

Vea ejemplos de control de versiones de archivos predeterminados [en Reemplazo de archivos existentes.](replacing-existing-files.md)

-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



