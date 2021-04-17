---
description: 'Las funciones de la API de Windows que manipulan caracteres suelen implementarse en uno de los tres formatos siguientes:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode en la API de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5686a7f65edefb11458374b7f72262448becd6d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687933"
---
# <a name="unicode-in-the-windows-api"></a>Unicode en la API de Windows

Las funciones de la API de Windows que manipulan caracteres suelen implementarse en uno de los tres formatos siguientes:

-   Una versión genérica que se puede compilar para páginas de códigos de Windows o Unicode
-   Una versión de [Página de códigos de Windows](code-pages.md) con la letra "a" que se usa para indicar "ANSI"
-   Una versión [Unicode](unicode.md) con la letra "W" utilizada para indicar "Wide"

Algunas funciones más recientes solo admiten versiones Unicode. Para obtener más información, vea [convenciones de los prototipos de función](conventions-for-function-prototypes.md).

En los temas siguientes se describen los tipos de datos Unicode y cómo se usan en funciones y mensajes; el uso de recursos, nombres de archivo y argumentos de la línea de comandos; y métodos de traducción entre distintos tipos de cadenas.

-   [Traducción automática de mensajes](automatic-message-translation.md)
-   [Juegos de caracteres usados en nombres de archivo](character-sets-used-in-file-names.md)
-   [Argumentos de la línea de comandos](command-line-arguments.md)
-   [Convenciones para Prototipos de función](conventions-for-function-prototypes.md)
-   [Funciones estándar de C](standard-c-functions.md)
-   [Diferencias de las funciones de cadena](string-function-differences.md)
-   [Conversión entre tipos de cadena](translation-between-string-types.md)
-   [Tipos de datos de Windows para cadenas](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los juegos de caracteres y Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



