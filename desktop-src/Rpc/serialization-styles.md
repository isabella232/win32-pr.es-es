---
title: Estilos de serialización
description: Hay tres estilos que puede usar para manipular identificadores de serialización.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473536"
---
# <a name="serialization-styles"></a>Estilos de serialización

Hay tres estilos que puede usar para manipular identificadores de serialización. Dichos componentes son:

-   [Serialización de búfer fija](fixed-buffer-serialization.md)
-   [Serialización de búfer dinámico](dynamic-buffer-serialization.md)
-   [Serialización incremental](incremental-serialization.md)

Independientemente del estilo que use, debe crear un identificador de serialización, serializar los datos y, a continuación, liberar el identificador. El estilo se establece cuando el programa crea el identificador y define la forma en que se manipula un búfer. El identificador mantiene el contexto adecuado asociado a cada uno de los tres estilos de serialización.

 

 




