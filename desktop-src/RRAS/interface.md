---
title: Interfaz (RRAS)
description: Una interfaz es una conexión lógica a una red. Cada interfaz se identifica mediante un índice único. Los protocolos de enrutamiento de multidifusión (como MOSPF) tratan de forma similar a todos los tipos de interfaces.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1347f1a8d9afd049dd8283e7199c6da7d8a9dce6990a1e7ea674943f32811f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030165"
---
# <a name="interface-rras"></a>Interfaz (RRAS)

Una interfaz es una conexión lógica a una red. Cada interfaz se identifica mediante un índice único. Los protocolos de enrutamiento de multidifusión (como MOSPF) tratan de forma similar a todos los tipos de interfaces.

En el caso de una interfaz LAN, la interfaz corresponde a un dispositivo físico real en el equipo (el adaptador de LAN). En el caso de una interfaz WAN, la interfaz se asigna a un puerto cuando se establece una conexión. Las interfaces WAN se pueden basar en túneles y el puerto podría ser un puerto de red privada virtual (VPN).

Windows sistemas operativos 2000 y versiones posteriores admiten una interfaz de punto a punto múltiple. Este tipo de interfaz se puede ver como una colección de vínculos de punto a punto que comparten un único punto de terminación.

Para identificar de forma única un vínculo exacto en una interfaz de punto a multipunto, la API de MGM usa la dirección del próximo salto del identificador de interfaz. Para admitir esta identificación, la API de MGM usa un identificador de interfaz extendido, que incluye una [dirección de próximo](next-hop.md) salto.

 

 




