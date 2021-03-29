---
title: Actualización de las rutas en su lugar mediante RtmUpdateAndUnlockRoute
description: La actualización en contexto suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto, como el que usa la función RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075881"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Actualización de las rutas en su lugar mediante RtmUpdateAndUnlockRoute

La actualización en contexto suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto, como el que usa la función [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) . Este método es más eficaz porque el cliente no necesita obtener un identificador ni pasar la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) hacia y desde el administrador de tablas de enrutamiento. Este método también tarda menos tiempo. Sin embargo, la actualización directa de la tabla de enrutamiento puede ser arriesgada, ya que el administrador de tablas de enrutamiento no funciona como intermediario.

Para ver el código de ejemplo que muestra cómo usar estas funciones, vea [actualizar una ruta en contexto mediante RtmUpdateAndUnlockRoute](update-a-route-in-place-using-rtmupdateandunlockroute.md).

 

 




