---
title: Trabajar con próximo saltos
description: La API RTMv2 permite a los clientes trabajar con la lista de próximo saltos asociados a rutas y destinos.
ms.assetid: ef474091-48fe-48e5-b476-73d77dbcbec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d20a812fd272afafd2cd8eb1d6fb93d97530a2a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073838"
---
# <a name="working-with-next-hops"></a>Trabajar con próximo saltos

La API RTMv2 permite a los clientes trabajar con la lista de próximo saltos asociados a rutas y destinos. Los clientes pueden agregar o actualizar un próximo salto llamando a [**RtmAddNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddnexthop). Los clientes pueden eliminar un próximo salto [**mediante RtmDeleteNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmdeletenexthop). Los clientes pueden buscar próximo saltos llamando [**a RtmFindNextHop**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmfindnexthop).

Los clientes también pueden actualizar el próximo salto directamente. Para ello, el cliente debe bloquear primero el próximo salto con la [**función RtmLockNextHop.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmlocknexthop) A continuación, el cliente puede usar el puntero directo a la estructura DE INFORMACIÓN [**\_ NEXTHOP \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_nexthop_info) DE RTM del administrador de tabla de enrutamiento para realizar las modificaciones necesarias. Por último, el cliente puede desbloquear el próximo salto.

> [!Note]  
> Los campos de dirección de próximo salto e índice de interfaz del próximo salto identifican de forma única el próximo salto y no se deben modificar.

 

 

 




