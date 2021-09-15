---
title: Administración de identificadores
description: El administrador de tablas de enrutamiento mantiene un recuento de referencias para toda la información que mantiene.
ms.assetid: bcd02881-b021-414f-8a40-14baac5baac7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f24653dd98db9b0427e5a3bee3f2f6613a68ce41
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473623"
---
# <a name="managing-handles"></a>Administración de identificadores

El administrador de tablas de enrutamiento mantiene un recuento de referencias para toda la información que mantiene. Esto evita que el administrador de tablas de enrutamiento devuelva a un cliente los identificadores a la memoria que se han liberado. Cada vez que se devuelve un identificador al autor de la llamada, ya sea como identificador explícito o como parte de una estructura de información, como [**RTM \_ DEST \_ INFO,**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_dest_info)se incrementa el recuento de referencias para el objeto que corresponde al identificador. Cuando se libera el identificador o la estructura de información, se disminuye el recuento de referencias adecuado. Cuando el recuento de referencias se convierte en cero, el objeto se libera.

Las [**funciones RtmGetDestInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetdestinfo) [**RtmGetEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetentityinfo) [**RtmGetRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetrouteinfo) y [**RtmGetNextHopInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetnexthopinfo) devuelven estructuras de información. Estas funciones corresponden a las funciones [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) y [**RtmRelaseNextHopInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo) respectivamente.

> [!Note]  
> La [**función RtmReleaseChangedDests**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasechangeddests) debe usarse para liberar identificadores devueltos por una llamada a [**RtmGetChangedDests.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmgetchangeddests) No use [**RtmReleaseDests para**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedests) las estructuras de destino modificadas.

 

Si un cliente debe mantener un identificador específico en una estructura de información mientras libera el resto, el cliente puede llamar a [**RtmReferenceHandles**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreferencehandles) con ese identificador antes de liberar la estructura de información. Después, el identificador se puede liberar mediante una llamada a las funciones [**RtmReleaseDestInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasedestinfo), [**RtmReleaseEntityInfo,**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaseentityinfo) [**RtmReleaseRouteInfo**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleaserouteinfo) y [**RtmRelaseNextHopInfo.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmreleasenexthopinfo)

 

 




