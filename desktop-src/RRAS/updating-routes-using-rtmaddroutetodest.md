---
title: Actualización de rutas mediante RtmAddRouteToDest
description: Si el cliente no requiere eficiencia al agregar una ruta, debe usar el siguiente método de actualización de rutas.
ms.assetid: bfa914ea-5d54-4ce9-a97c-903c497d135b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c7972b2d5ec0996cafc1dd32a8a4056a6aeb0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361977"
---
# <a name="updating-routes-using-rtmaddroutetodest"></a>Actualización de rutas mediante RtmAddRouteToDest

Si el cliente no requiere eficiencia al agregar una ruta, debe usar el siguiente método de actualización de rutas. Este método es menos eficaz, ya que requiere obtener un identificador a la ruta y pasar la estructura [**\_ DE INFORMACIÓN \_**](/windows/desktop/api/Rtmv2/ns-rtmv2-rtm_route_info) DE RUTA DE RTM hacia y desde el administrador de tablas de enrutamiento. Este método también tarda más tiempo. Puesto [**que RtmAddRouteToDest**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmaddroutetodest) no manipula la tabla de enrutamiento directamente, el uso de este método permite cambiar la eficacia por simplicidad.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea Agregar y actualizar [rutas mediante RtmAddRouteToDest.](add-and-update-routes-using-rtmaddroutetodest.md)

 

 




