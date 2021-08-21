---
title: Actualización de rutas en su lugar mediante RtmUpdateAndUnlockRoute
description: La actualización en su lugar suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto como el utilizado por la función RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfcfdc7abd355cd70bb1295af6ce8b4fb4749dfed6c55af4d1fd06ca8257170
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073705"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Actualización de rutas en su lugar mediante RtmUpdateAndUnlockRoute

La actualización en su lugar suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto como el utilizado por la [**función RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) Este método es más eficaz porque el cliente no es necesario para obtener un identificador, ni para pasar la estructura [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) al administrador de tablas de enrutamiento y desde él. Este método también tarda menos tiempo. Sin embargo, la actualización directa de la tabla de enrutamiento puede ser arriesgada, ya que el administrador de tablas de enrutamiento no funciona como intermediario.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea Actualizar una ruta en su lugar [mediante RtmUpdateAndUnlockRoute.](update-a-route-in-place-using-rtmupdateandunlockroute.md)

 

 




