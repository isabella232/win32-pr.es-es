---
description: Si ambos archivos tienen un número de versión, el Windows Installer usa la lógica que se ilustra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente.
ms.assetid: c4c8a23b-e1c2-4c96-b708-7cbcbcab4cd4
title: Ambos archivos tienen una versión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb52c7333e5455d40475c9f845643535b271d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909046"
---
# <a name="both-files-have-a-version"></a>Ambos archivos tienen una versión

Si el archivo de clave de un componente que se está instalando (Copy-A) tiene el mismo nombre que un archivo que ya está instalado en la ubicación de destino (Copy-B), el instalador compara el número de versión y el idioma de los dos archivos.

Si ambos archivos tienen un número de versión, el instalador usa la lógica que se muestra en el siguiente diagrama de flujo para determinar si se deben reemplazar todos los archivos instalados que pertenezcan al componente. Dado que el instalador solo instala componentes completos, si se reemplaza el archivo de clave instalado, se reemplazan todos los archivos del componente.

Tenga en cuenta que este diagrama muestra las [reglas](file-versioning-rules.md)predeterminadas de control de versiones de archivo, que se pueden invalidar estableciendo la propiedad [**REINSTALLMODE**](reinstallmode.md) . El valor predeterminado de la propiedad **REINSTALLMODE** es "OMUs".

![reglas predeterminadas de control de versiones de archivo cuando ambos archivos tienen el mismo nombre o número de versión](images/waiflow1.png)

El diagrama anterior también se puede usar con archivos sin idioma especificado. Si Copy-A tiene un idioma especificado y Copy-B no tiene ningún idioma especificado, Copy-B se reemplaza por Copy-A. Si no se especifica ningún idioma para Copy-A y Copy-B, no se reemplazará Copy-B.

Vea ejemplos de control de versiones de archivo predeterminados en [reemplazar archivos existentes](replacing-existing-files.md).

-   [Ninguno de los archivos tiene una versión](neither-file-has-a-version.md)
-   [Ninguno de los archivos tiene una versión con comprobación de hash de archivo](neither-file-has-a-version-with-file-hash-check.md)
-   [Un archivo tiene una versión](one-file-has-a-version.md)

 

 



