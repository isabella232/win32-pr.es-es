---
title: Interfaz (RRAS)
description: Una interfaz es una conexión lógica a una red. Cada interfaz se identifica mediante un índice único. Los protocolos de enrutamiento de multidifusión (como MOSPF) abordan todos los tipos de interfaces de forma similar.
ms.assetid: 761a033c-b95e-46f0-948b-d0a60337390f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd1e3988eac75bd465bf9a9b890f360f850a0d7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103995830"
---
# <a name="interface-rras"></a>Interfaz (RRAS)

Una interfaz es una conexión lógica a una red. Cada interfaz se identifica mediante un índice único. Los protocolos de enrutamiento de multidifusión (como MOSPF) abordan todos los tipos de interfaces de forma similar.

En el caso de una interfaz LAN, la interfaz corresponde a un dispositivo físico real del equipo (el adaptador de LAN). En el caso de una interfaz WAN, la interfaz se asigna a un puerto cuando se establece una conexión. Las interfaces WAN pueden basarse en túneles y el puerto puede ser un puerto de red privada virtual (VPN).

Los sistemas operativos Windows 2000 y versiones posteriores admiten una interfaz "Point-to-multipunto". Este tipo de interfaz se puede ver como una colección de vínculos de punto a punto que comparten un único punto de finalización.

Para identificar de forma única un vínculo exacto en una interfaz de punto a multipunto, la API MGM usa la dirección del próximo salto del identificador de interfaz. Para admitir esta identificación, la API MGM usa un identificador de interfaz extendida, que incluye una dirección del [próximo salto](next-hop.md) .

 

 




