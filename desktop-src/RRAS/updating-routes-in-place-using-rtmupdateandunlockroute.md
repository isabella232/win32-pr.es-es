---
title: Actualización de rutas en su lugar mediante RtmUpdateAndUnlockRoute
description: La actualización en su lugar suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto como el utilizado por la función RtmAddRouteToDest.
ms.assetid: d4b0b14e-957a-43d5-bacc-8eee4512e2ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d76d2af5d60172b890eefa1041a08d47a5221b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361978"
---
# <a name="updating-routes-in-place-using-rtmupdateandunlockroute"></a>Actualización de rutas en su lugar mediante RtmUpdateAndUnlockRoute

La actualización en su lugar suele ser más eficaz que actualizar la tabla de enrutamiento con un método indirecto como el utilizado por la [**función RtmAddRouteToDest.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) Este método es más eficaz porque el cliente no es necesario para obtener un identificador, ni para pasar la estructura [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) al administrador de tablas de enrutamiento y desde él. Este método también tarda menos tiempo. Sin embargo, la actualización directa de la tabla de enrutamiento puede ser arriesgada, ya que el administrador de tablas de enrutamiento no funciona como intermediario.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea Actualizar una ruta en su lugar [mediante RtmUpdateAndUnlockRoute.](update-a-route-in-place-using-rtmupdateandunlockroute.md)

 

 




