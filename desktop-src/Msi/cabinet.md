---
description: El tipo de datos del archivo. cab debe usarse en la columna Cabinet de la tabla de medios.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Archiva
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909041"
---
# <a name="cabinet"></a>Archiva

El tipo de datos del archivo. cab debe usarse en la columna Cabinet de la [tabla de medios](media-table.md).

Si el nombre del archivo. cab va precedido del signo de número, el archivador se almacena como un flujo de datos dentro del paquete. La cadena de caracteres que sigue \# a es un [identificador](identifier.md) de este flujo de datos. Tenga en cuenta que si el archivo. cab se almacena como un flujo de datos, el nombre de un contenedor distingue mayúsculas de minúsculas.

Si el nombre del archivo. cab no está precedido por el signo de número \# , se almacena en un archivo independiente ubicado en la raíz del árbol de origen especificado por la [tabla de directorio](directory-table.md). El archivo. cab debe utilizar la sintaxis de nombre de archivo corto que consta de un nombre de ocho caracteres, un punto y una extensión de tres caracteres. El tipo de datos del archivo. cab no puede usar la \| Sintaxis de longname breve para los nombres de archivo. Si el archivo. cab se almacena como un archivo independiente, el nombre del archivo. cab no distingue mayúsculas de minúsculas.

Para conservar espacio en disco, el instalador quita todos los gabinetes incrustados en el archivo. msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.

Vea [incluir un archivo. cab en una instalación](including-a-cabinet-file-in-an-installation.md).

 

 



