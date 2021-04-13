---
description: El tipo de datos FILENAME es una cadena de texto que contiene un nombre de archivo o una carpeta.
ms.assetid: af59e1b8-0699-4031-895f-415752611e21
title: Nombre de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fc049fa0808efc180afbd715e311a124bfdada9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544278"
---
# <a name="filename"></a>Nombre de archivo

El tipo de datos FILENAME es una cadena de texto que contiene un nombre de archivo o una carpeta. De forma predeterminada, se supone que el nombre de archivo usa la sintaxis de nombre de archivo corto; es decir, el nombre de ocho caracteres, el punto (.) y la extensión de 3 caracteres. Siempre se debe proporcionar un nombre corto de archivo porque se puede establecer la propiedad [**SHORTFILENAMES**](shortfilenames.md) o el volumen de destino de la instalación solo puede admitir nombres de archivo cortos.

Para incluir un nombre de archivo largo con el nombre de archivo corto, sepárelo del nombre de archivo corto con una barra vertical ( \| ).

Por ejemplo, las dos cadenas siguientes son válidas:

-   status.txt
-   Project ~1.txt\| Status.txt de proyecto

Los nombres de archivo cortos y largos no deben contener los caracteres siguientes:

-   barra diagonal (/) o ( \\ )
-   signo de interrogación (?)
-   barra vertical ( \| )
-   corchete angular de cierre (>)
-   corchete angular de apertura (<)
-   dos puntos (:)
-   asterisco ( \* )
-   comillas dobles (")

Además, los nombres de archivo cortos no deben contener los caracteres siguientes:

-   signo más (+)
-   coma (,)
-   punto y coma (;)
-   signo igual (=)
-   corchete de apertura ( \[ )
-   corchete de cierre ( \] )

No se permite ningún espacio delante del \| separador de barra vertical () para la sintaxis de nombre de archivo corto/nombre de archivo largo. Los nombres de archivo cortos no pueden incluir un espacio, aunque puede ser un nombre de archivo largo. Solo puede existir un espacio después del separador si el nombre de archivo largo del nombre de archivo comienza con el espacio. No se permite la sintaxis de ruta de acceso completa.

> [!Note]  
> El formato de la columna FileName de la tabla [MsiEmbeddedUI](msiembeddedui-table.md) es similar al tipo de datos Format FILENAME, excepto \| en que no está disponible el separador de barra vertical () para la sintaxis de nombre de archivo corto/nombre de archivo largo.

 

 

 



