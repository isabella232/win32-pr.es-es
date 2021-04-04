---
title: Marcas de salto siguiente
description: Marcas de salto siguiente
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Siguientes
- Marcas de salto siguiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bd672c9b083e47c3d0a7419d03ab890c1037ce5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076208"
---
# <a name="next-hop-flags"></a>Marcas de salto siguiente

## <a name="next-hop-state-flags"></a>Marcas de estado de próximo salto



| Constante                     | Value | Descripción                              |
|------------------------------|-------|------------------------------------------|
| Estado de NEXTHOP de RTM \_ \_ \_ creado | 0     | Indica que se ha creado el próximo salto. |
| Estado de NEXTHOP de RTM \_ \_ \_ eliminado | 1     | Indica que se eliminó el próximo salto. |



 

## <a name="next-hop-flags"></a>Marcas de salto siguiente



| Constante                    | Value  | Descripción                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| marcas de salto de RTM \_ \_ \_ remotas | 0x0001 | Este próximo salto apunta a un destino remoto que no es accesible directamente. Para obtener la ruta de acceso completa, el cliente debe realizar una búsqueda recursiva. |
| marcas de salto de RTM \_ \_ \_ inactivas   | 0x0002 | Esta marca se reserva para uso futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Próximo salto agregado



| Constante                  | Value | Descripción                 |
|---------------------------|-------|-----------------------------|
| cambio de NEXTHOP de RTM \_ \_ \_ nuevo | 0x01  | Se creó un próximo salto nuevo. |



 

 

 




