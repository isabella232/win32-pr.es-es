---
description: Conexión y desconexión de nodos de topología
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Conexión y desconexión de nodos de topología
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359744"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a>Conexión y desconexión de nodos de topología

Para que una topología sea funcional, el nodo de origen y el nodo de salida deben estar conectados. Para conectar dos nodos de topología, arrastre la salida del nodo de un nodo a la entrada de nodo del otro nodo. TopoEdit muestra la conexión del nodo como una línea negra. Esto equivale a conectar nodos de topología mediante una llamada al [**método IMFTopologyNode::ConnectOutput.**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput)

La topología solo se puede resolver si la conexión del nodo es válida; es decir, si los tipos de medios de los dos nodos son compatibles. Para obtener información sobre cómo resolver topologías, vea [Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md).

Si intenta realizar una conexión desde un nodo que ya está conectado, la nueva conexión de nodo reemplaza a la antigua.

Para eliminar una conexión, seleccione la conexión de nodo y presione la tecla DELETE o **seleccione Eliminar en** el menú **Topología.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Creación de topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



