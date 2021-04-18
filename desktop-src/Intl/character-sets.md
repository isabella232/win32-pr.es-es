---
description: Un &\# 0034; juego de caracteres&\# 0034; es una asignación de caracteres a sus valores de código de identificación.
ms.assetid: 0a055c02-c5ed-4790-83e4-183bc3cc6b51
title: Juegos de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8e62a0afbe9e5b2b3ab596a8129db833477e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686722"
---
# <a name="character-sets"></a>Juegos de caracteres

Un "juego de caracteres" es una asignación de caracteres a sus valores de código de identificación. El juego de caracteres que se usa con más frecuencia en los equipos de hoy en día es [Unicode](unicode.md), un estándar global para la codificación de caracteres. Internamente, las aplicaciones de Windows utilizan la implementación UTF-16 de Unicode. En UTF-16, la mayoría de los caracteres se identifican mediante códigos de dos bytes. Los caracteres complementarios usados con menos frecuencia se representan mediante un par suplente, que es un par de códigos de dos bytes. Para obtener más información, vea [suplentes y caracteres adicionales](surrogates-and-supplementary-characters.md).

Algunas aplicaciones de Windows deben funcionar con los juegos de caracteres más antiguos que son nativos de Windows Me/98/95. [Las páginas de códigos de Windows](code-pages.md) permiten que la aplicación funcione con estos juegos de caracteres. Estos juegos de caracteres se pueden dividir en:

-   [Juegos de caracteres de un solo byte](single-byte-character-sets.md) (SBCS). En un SBCS, cada carácter se identifica con un valor de ancho de un byte.
-   Juegos de caracteres multibyte, en particular, los [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS). Los juegos de caracteres multibyte proporcionan un medio para representar el gran número de caracteres en muchos idiomas asiáticos.

Para obtener más información, vea los temas siguientes:

-   [Páginas de códigos](code-pages.md)
-   [Juegos de caracteres de doble byte](double-byte-character-sets.md)
-   [Juegos de caracteres de un solo byte](single-byte-character-sets.md)
-   [Suplentes y caracteres suplementarios](surrogates-and-supplementary-characters.md)
-   [Unicode](unicode.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los juegos de caracteres y Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



