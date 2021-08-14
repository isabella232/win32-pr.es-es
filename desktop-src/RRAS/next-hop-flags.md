---
title: Marcas de próximo salto
description: Marcas de próximo salto
ms.assetid: e4c7e9ea-21f5-491a-b005-1ef1a457cb80
keywords:
- Siguientes
- Marcas de próximo salto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45dbad78f5f10d7a9d7bf42f694f7e2fb3109c03b92dccdb5f31697f5cf8988c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790399"
---
# <a name="next-hop-flags"></a>Marcas de próximo salto

## <a name="next-hop-state-flags"></a>Marcas de estado de próximo salto



| Constante                     | Valor | Descripción                              |
|------------------------------|-------|------------------------------------------|
| ESTADO \_ NEXTHOP DE RTM \_ \_ CREADO | 0     | Indica que se creó el próximo salto. |
| ESTADO \_ NEXTHOP DE RTM \_ \_ ELIMINADO | 1     | Indica que se eliminó el próximo salto. |



 

## <a name="next-hop-flags"></a>Marcas de próximo salto



| Constante                    | Valor  | Descripción                                                                                                                                           |
|-----------------------------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| MARCAS \_ NEXTHOP DE RTM \_ REMOTAS \_ | 0x0001 | Este próximo salto apunta a un destino remoto al que no se puede acceder directamente. Para obtener la ruta de acceso completa, el cliente debe realizar una búsqueda recursiva. |
| MARCAS \_ NEXTHOP DE RTM \_ HACIA \_ ABAJO   | 0x0002 | Esta marca está reservada para su uso futuro.                                                                                                                 |



 

## <a name="next-hop-added"></a>Próximo salto agregado



| Constante                  | Valor | Descripción                 |
|---------------------------|-------|-----------------------------|
| RTM \_ NEXTHOP \_ CHANGE \_ NEW | 0x01  | Se creó un nuevo próximo salto. |



 

 

 




