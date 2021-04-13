---
title: Estilos de serialización
description: Hay tres estilos que puede usar para manipular los identificadores de serialización.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418909"
---
# <a name="serialization-styles"></a>Estilos de serialización

Hay tres estilos que puede usar para manipular los identificadores de serialización. Dichos componentes son:

-   [Serialización de búfer fijo](fixed-buffer-serialization.md)
-   [Serialización de búfer dinámico](dynamic-buffer-serialization.md)
-   [Serialización incremental](incremental-serialization.md)

Independientemente del estilo que use, debe crear un identificador de serialización, serializar los datos y, a continuación, liberar el identificador. El estilo se establece cuando el programa crea el identificador y define el modo en que se manipula un búfer. El identificador mantiene el contexto adecuado asociado a cada uno de los tres estilos de serialización.

 

 




