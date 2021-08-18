---
title: Estilos de serialización
description: Hay tres estilos que puede usar para manipular los identificadores de serialización.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfaa7cd3198245441a27990d331bcd9f0bd0396b5075d9985b13da58012147d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925391"
---
# <a name="serialization-styles"></a>Estilos de serialización

Hay tres estilos que puede usar para manipular los identificadores de serialización. Estos son:

-   [Serialización de búfer fija](fixed-buffer-serialization.md)
-   [Serialización dinámica de búfer](dynamic-buffer-serialization.md)
-   [Serialización incremental](incremental-serialization.md)

Independientemente del estilo que use, debe crear un identificador de serialización, serializar los datos y, a continuación, liberar el identificador. El estilo se establece cuando el programa crea el identificador y define la forma en que se manipula un búfer. El identificador mantiene el contexto adecuado asociado a cada uno de los tres estilos de serialización.

 

 




