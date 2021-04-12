---
description: Los caracteres definidos por el usuario final (EUDC) en los juegos de caracteres de doble byte (DBCS) y los caracteres de área de uso privado (PUA) de Unicode son caracteres personalizados.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caracteres de área de uso privado y definidos por el usuario final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361227"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caracteres de área de uso privado y definidos por el usuario final

Los caracteres definidos por el usuario final (EUDC) en los [juegos de caracteres de doble byte](double-byte-character-sets.md) (DBCS) y los caracteres de área de uso privado (PUA) de [Unicode](unicode.md) son caracteres personalizados. Pueden definirse e implementarse a través de un usuario final o de otra entidad, como un fabricante de equipo, un grupo de usuarios, un organismo gubernamental o una empresa de diseño de fuentes. Su uso permite a los usuarios formar nombres y otras palabras mediante caracteres que no están disponibles en las fuentes de pantalla y impresora estándar.

Los caracteres EUDC y PUA se pueden asignar de forma diferente o no asignarse en absoluto en equipos diferentes. Algunas páginas de códigos tienen extensiones que reutilizan el intervalo de EUDC y estas extensiones pueden entrar en conflicto entre sí. En otros casos, un fabricante podría proporcionar un conjunto personalizado de caracteres en uno de estos intervalos. Además, los grupos de usuarios pueden intentar proporcionar caracteres adicionales en PUA. Diferentes combinaciones de estos casos pueden causar conflictos. Al crear aplicaciones que se basan en caracteres EUDC o PUA, debe tener en cuenta las interpretaciones conflictivas de un punto de código individual.

En los temas siguientes se describen las fuentes que admiten EUDCs y el acceso y la administración de estos caracteres:

-   [Juegos de caracteres y fuentes](character-sets-and-fonts.md)
-   [Entradas del registro de EUDC](eudc-registry-entries.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los juegos de caracteres y Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



