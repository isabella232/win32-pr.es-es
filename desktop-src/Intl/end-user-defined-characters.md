---
description: Los caracteres definidos por el usuario final (EUDC) en los juegos de caracteres de doble byte (DBCS) y los caracteres de área de uso privado (PUA) en Unicode son caracteres personalizados.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caracteres de área de uso privado y definido por el usuario final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19152ff8564cae4ccccc154a6c9d349f0fc6cd8791fcccb1973b553bc681cc5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898765"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caracteres de área de uso privado y definido por el usuario final

Los caracteres definidos por el usuario [](double-byte-character-sets.md) final (EUDC) en los juegos de caracteres de doble byte (DBCS) y los caracteres de área de uso privado (PUA) en [Unicode](unicode.md) son caracteres personalizados. Pueden definirse e implementarse por un usuario final o por otra parte, como un fabricante de equipos, un grupo de usuarios, un organismo gubernamental o una empresa de diseño de fuentes. Su uso permite a los usuarios formar nombres y otras palabras mediante caracteres que no están disponibles en las fuentes estándar de pantalla e impresora.

Los caracteres EUDC y PUA se pueden asignar de forma diferente, o no asignarse, en equipos diferentes. Algunas páginas de códigos tienen extensiones que reutilizan el intervalo eudc y estas extensiones pueden estar en conflicto entre sí. En otros casos, un fabricante podría proporcionar un conjunto personalizado de caracteres en uno de estos intervalos. Además, los grupos de usuarios pueden intentar proporcionar caracteres adicionales en la PUA. Diferentes combinaciones de estos casos pueden provocar conflictos. Al crear aplicaciones que se basan en caracteres EUDC o PUA, debe tener en cuenta las interpretaciones en conflicto de un punto de código individual.

En los temas siguientes se tratan las fuentes que admiten los EUDC, así como el acceso y la administración de estos caracteres:

-   [Juegos de caracteres y fuentes](character-sets-and-fonts.md)
-   [Entradas del Registro eudc](eudc-registry-entries.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Unicode y juegos de caracteres](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



