---
description: Metaarchivos de Enhanced-Format
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Metaarchivos de Enhanced-Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984974"
---
# <a name="enhanced-format-metafiles"></a>Metaarchivos de Enhanced-Format

El *metarchivo con formato mejorado* consta de los siguientes elementos:

-   Un encabezado
-   Una tabla de identificadores para objetos GDI
-   Una paleta privada
-   Matriz de registros de metarchivo

Los metaarchivos mejorados proporcionan una verdadera independencia del dispositivo. Puede pensar en la imagen almacenada en un metarchivo mejorado como una "instantánea" de la pantalla de vídeo tomada en un momento determinado. Esta "instantánea" mantiene sus dimensiones, independientemente de dónde aparezca en una impresora, un trazador, el escritorio o el área cliente de cualquier aplicación.

Puede usar los metaarchivos mejorados para almacenar una imagen creada con las funciones GDI (incluidas las nuevas funciones de trazado y transformación). Dado que el formato de metarchivo mejorado está normalizado, las imágenes que se almacenan en este formato se pueden copiar de una aplicación a otra; y, dado que las imágenes son realmente independientes del dispositivo, se garantiza que mantengan su forma y proporción en cualquier dispositivo de salida.

-   [Registros de metarchivos mejorados](enhanced-metafile-records.md)
-   [Creación mejorada de metarchivos](enhanced-metafile-creation.md)
-   [Operaciones de metarchivo mejoradas](enhanced-metafile-operations.md)

 

 



