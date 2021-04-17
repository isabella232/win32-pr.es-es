---
description: Para administrar registros, puede trabajar con información que se almacena en estructuras de registro del mismo nivel \_ .
ms.assetid: d38ea2d3-5cfb-4c4a-a63f-b274aa0dfe71
title: Administración de registros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c762689263e4a012bbdfad726b13e3ee8c79397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667927"
---
# <a name="record-management"></a>Administración de registros

Para administrar registros, puede trabajar con información que se almacena en estructuras [**de \_ registro del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) . Cuando se crean, actualizan o eliminan registros, los cambios realizados en un gráfico se replican en todos los nodos. En la tabla siguiente se identifican las reglas para actualizar y actualizar automáticamente los registros.



| Tarea de administración     | Regla                                                                                                                                                                                                            |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actualizar un registro   | Mantenga la hora de expiración igual o auméntelo. No se puede reducir la hora de expiración.                                                                                                                      |
| Actualizar un registro | Use la marca de actualización automática de la [**\_ marca de registro \_ \_ del mismo nivel**](/windows/desktop/api/P2P/ns-p2p-peer_record) para actualizar un registro automáticamente. Use esta marca solo cuando el nodo que está publicando un registro está en línea. De lo contrario, no utilice esta marca. |



 

 

 



