---
description: El tipo de datos Cabinet debe usarse en la columna Cabinet de la tabla Media.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Gabinete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814473ef4d21d5445b5b5319278a5e25a7f5540
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158950"
---
# <a name="cabinet"></a>Gabinete

El tipo de datos Cabinet debe usarse en la columna Cabinet de la [tabla Media](media-table.md).

Si el nombre del gabinete va precedido del signo de número, el gabinete se almacena como un flujo de datos dentro del paquete. La cadena de caracteres que sigue a \# es un [identificador](identifier.md) para este flujo de datos. Tenga en cuenta que si el archivador se almacena como un flujo de datos, el nombre de un gabinete distingue mayúsculas de minúsculas.

Si el nombre del gabinete no va precedido del signo de número , el archivador se almacena en un archivo independiente ubicado en la raíz del árbol de origen especificado por la tabla \# [de directorios](directory-table.md). El archivo archivador debe usar la sintaxis de nombre de archivo corto que consta de un nombre de ocho caracteres, un punto y una extensión de tres caracteres. El tipo de datos Cabinet no puede usar la sintaxis \| longname corta para los nombres de archivo. Si el archivo de archivador se almacena como un archivo independiente, el nombre del archivo de archivador no distingue mayúsculas de minúsculas.

Para ahorrar espacio en disco, el instalador quita los gabinetes insertados en el archivo .msi antes de almacenar en caché el paquete de instalación en el equipo del usuario.

Vea [Incluir un archivo de archivador en una instalación](including-a-cabinet-file-in-an-installation.md)de .

 

 



