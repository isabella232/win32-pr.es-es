---
description: Crear topologías
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Crear topologías
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423563"
---
# <a name="creating-topologies"></a>Crear topologías

En esta sección se describen algunos de los procedimientos generales para crear una topología.

Los pasos generales para crear una topología son los siguientes:

1.  Cree un nuevo objeto Topology llamando a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology). Esta función devuelve un puntero a la interfaz [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topología.

2.  Inicialmente, la topología no contiene ningún nodo. Para crear nodos para la topología, llame a [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode). Esta función devuelve un puntero a la interfaz [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) del nodo. Debe especificar el tipo de nodo al crear el nodo:

    -   Nodo de origen.

    -   Nodo de transformación.

    -   Nodo de salida.

    -   Nodo tee.

3.  Inicialice cada nodo. El proceso de inicialización depende del tipo de nodo, tal y como se describe en los temas siguientes.

4.  Agregue cada nodo a la topología mediante una llamada a [**IMFTopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).

5.  Conecte los nodos. Para conectar un nodo, llame a [**IMFTopologyNode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) en el nodo de nivel superior y pase un puntero al nodo de nivel inferior.

En los temas siguientes se proporcionan los pasos específicos para cada tipo de nodo.



| Tema                                                    | Descripción                     |
|----------------------------------------------------------|---------------------------------|
| [Crear nodos de origen](creating-source-nodes.md)       | Cómo crear un nodo de origen.    |
| [Crear nodos de transformación](creating-transform-nodes.md) | Cómo crear un nodo de transformación. |
| [Crear nodos de salida](creating-output-nodes.md)       | Cómo crear un nodo de salida.   |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Topologías](topologies.md)
</dt> </dl>

 

 



