---
title: Actualizar rutas mediante RtmAddRouteToDest
description: Si el cliente no requiere eficacia al agregar una ruta, debe utilizar el siguiente método de actualización de rutas.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994507"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Actualizar rutas mediante RtmAddRouteToDest

Si el cliente no requiere eficacia al agregar una ruta, debe utilizar el siguiente método de actualización de rutas. Este método es menos eficaz, ya que requiere obtener un identificador de la ruta y pasar la estructura de [**\_ \_ información de ruta RTM**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) hacia y desde el administrador de tabla de enrutamiento. Este método también tarda más tiempo. Dado que [**RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) no manipula directamente la tabla de enrutamiento, el uso de este método se usa para aumentar la eficacia.

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [Agregar y actualizar rutas mediante RtmAddRouteToDest](add-and-update-routes-using-rtmaddroutetodest.md).

 

 




