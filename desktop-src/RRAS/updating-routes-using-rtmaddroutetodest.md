---
title: Actualizar rutas mediante RtmAddRouteToDest
description: Si el cliente no requiere eficiencia al agregar una ruta, debe usar el siguiente método de actualización de rutas.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb3212a74637fa4de51f3b05f80f84bace1c0c57ba570e5025adb796da933b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025335"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Actualizar rutas mediante RtmAddRouteToDest

Si el cliente no requiere eficiencia al agregar una ruta, debe usar el siguiente método de actualización de rutas. Este método es menos eficaz, ya que requiere obtener un identificador para la ruta y pasar la estructura [**\_ RTM ROUTE \_ INFO**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) hacia y desde el administrador de tablas de enrutamiento. Este método también tarda más tiempo. Puesto [**que RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) no manipula directamente la tabla de enrutamiento, el uso de este método ofrece eficiencia por simplicidad.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea Agregar y actualizar [rutas mediante RtmAddRouteToDest.](add-and-update-routes-using-rtmaddroutetodest.md)

 

 




