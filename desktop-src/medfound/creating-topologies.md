---
description: Creación de topologías
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Creación de topologías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573436"
---
# <a name="creating-topologies"></a>Creación de topologías

En esta sección se describen algunos de los procedimientos generales para crear una topología.

Los pasos generales para crear una topología son los siguientes:

1.  Cree un nuevo objeto de topología mediante una [**llamada a MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Esta función devuelve un puntero a la interfaz [**DETOPOLOGY de la**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) topología.

2.  Inicialmente, la topología no contiene ningún nodo. Para crear nodos para la topología, llame [**a MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Esta función devuelve un puntero a la interfaz [**DETOPOLOGYNode del**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) nodo. Debe especificar el tipo de nodo al crear el nodo:

    -   Nodo de origen.

    -   Nodo de transformación.

    -   Nodo de salida.

    -   Nodo de tee.

3.  Inicialice cada nodo. El proceso de inicialización depende del tipo de nodo, como se describe en los temas siguientes.

4.  Agregue cada nodo a la topología mediante una llamada [**a IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Conectar los nodos. Para conectar un nodo, llame a [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) en el nodo ascendente y pase un puntero al nodo de bajada.

En los temas siguientes se proporcionan los pasos específicos para cada tipo de nodo.



| Tema                                                    | Descripción                     |
|----------------------------------------------------------|---------------------------------|
| [Creación de nodos de origen](creating-source-nodes.md)       | Cómo crear un nodo de origen.    |
| [Creación de nodos de transformación](creating-transform-nodes.md) | Cómo crear un nodo de transformación. |
| [Creación de nodos de salida](creating-output-nodes.md)       | Cómo crear un nodo de salida.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



