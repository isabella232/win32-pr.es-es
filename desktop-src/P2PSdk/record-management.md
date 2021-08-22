---
description: Para administrar registros, puede trabajar con información almacenada en estructuras RECORD \_ del mismo nivel.
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Administración de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a747ae16e1773fe5944f2e9afdde8377d5e100a9a91316f70bcd1be8db6cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011523"
---
# <a name="record-management"></a>Administración de registros

Para administrar registros, puede trabajar con información almacenada en estructuras [**RECORD \_ del mismo**](/windows/desktop/api/P2P/ns-p2p-peer_record) nivel. Cuando se crean, actualizan o eliminan registros, los cambios realizados en un grafo se replican en todos los nodos. En la tabla siguiente se identifican las reglas para actualizar y actualizar automáticamente los registros.



| Tarea de administración     | Regla                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actualizar un registro   | Mantenga la hora de expiración igual o aumente. No se puede reducir el tiempo de expiración.                                                                                                                      |
| Actualizar un registro | Use la [**marca PEER RECORD FLAG \_ \_ \_ AUTOREFRESH**](/windows/desktop/api/P2P/ns-p2p-peer_record) para actualizar automáticamente un registro. Use esta marca solo cuando el nodo que publica un registro esté en línea. De lo contrario, no use esta marca. |



 

 

 



