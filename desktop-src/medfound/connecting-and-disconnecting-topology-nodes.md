---
description: Conexión y desconexión de nodos de topología
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Conexión y desconexión de nodos de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705419"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Conexión y desconexión de nodos de topología

Para que una topología sea funcional, el nodo de origen y el nodo de salida deben estar conectados. Para conectar dos nodos de topología, arrastre la salida de nodo de un nodo a la entrada de nodo del otro nodo. TopoEdit muestra la conexión de nodo como una línea negra. Esto es equivalente a la conexión de nodos de topología mediante una llamada al método [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) .

La topología solo se puede resolver si la conexión de nodo es válida; es decir, si los tipos de medios de los dos nodos son compatibles. Para obtener información sobre la resolución de topologías, consulte [resolución de una topología con TopoEdit](resolving-a-topology-with-topoedit.md).

Si intenta establecer una conexión desde un nodo que ya está conectado, la nueva conexión de nodo reemplaza a la antigua conexión de nodo.

Para eliminar una conexión, seleccione la conexión de nodo y presione la tecla SUPRIMIr o seleccione **eliminar** en el menú de **topología** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



