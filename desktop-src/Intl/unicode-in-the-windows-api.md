---
description: 'Windows Las funciones de API que manipulan caracteres se implementan generalmente en uno de estos tres formatos:'
ms.assetid: e7698f0b-dbcb-4cd0-9cb5-23a26edb966a
title: Unicode en la API de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c36e1e292eddd786d4c4bf336f980486f66870deb809587f9c51334f269ce9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764815"
---
# <a name="unicode-in-the-windows-api"></a>Unicode en la API de Windows

Windows Las funciones de API que manipulan caracteres se implementan generalmente en uno de estos tres formatos:

-   Una versión genérica que se puede compilar para páginas de códigos Windows o Unicode
-   Una [Windows de página de códigos](code-pages.md) con la letra "A" usada para indicar "ANSI"
-   Una [versión Unicode](unicode.md) con la letra "W" usada para indicar "wide"

Algunas funciones más recientes solo admiten versiones Unicode. Para obtener más información, vea [Convenciones para prototipos de función](conventions-for-function-prototypes.md).

En los temas siguientes se tratan los tipos de datos Unicode y cómo se usan en funciones y mensajes. el uso de recursos, nombres de archivo y argumentos de línea de comandos; y métodos de traducción entre distintos tipos de cadenas.

-   [Traducción automática de mensajes](automatic-message-translation.md)
-   [Juegos de caracteres usados en nombres de archivo](character-sets-used-in-file-names.md)
-   [Argumentos de la línea de comandos](command-line-arguments.md)
-   [Convenciones para Prototipos de función](conventions-for-function-prototypes.md)
-   [Funciones estándar de C](standard-c-functions.md)
-   [Diferencias de función de cadena](string-function-differences.md)
-   [Traducción entre tipos de cadena](translation-between-string-types.md)
-   [Tipos de datos de Windows para cadenas](windows-data-types-for-strings.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Unicode y juegos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



