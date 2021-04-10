---
description: Compilar topologías mediante TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Compilar topologías mediante TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153687"
---
# <a name="building-topologies-by-using-topoedit"></a>Compilar topologías mediante TopoEdit

Una topología debe tener los tres nodos siguientes:

-   Nodo de origen: el flujo de un archivo multimedia, que se usa como origen de la topología.
-   Nodo de transformación: transformación de Media Foundation (MFT). Normalmente, estos nodos son codificadores, descodificadores y efectos de la topología.
-   Nodo de salida: receptor de la secuencia que pasa los datos multimedia, los fotogramas de vídeo o las secuencias de audio a la sesión multimedia para la reproducción.

Para obtener información acerca de la estructura de la topología, consulte [acerca de las topologías](about-topologies.md).

Para compilar una topología, debe agregar los nodos, conectar los nodos y resolver la topología para que pueda reproducirse.

Los nodos de topología se muestran como cuadros, donde el texto muestra el nombre del nodo. Los cuadros verdes representan los nodos agregados por el usuario. Cuando se resuelve una topología, TopoEdit puede agregar nodos de transformación a la topología automáticamente. Aparecen como cuadros azules en el **Panel de topología**.

Las entradas y salidas de la topología se representan en forma de cuadrados negros a lo largo del borde del nodo. La *entrada de nodo* se muestra en el lado izquierdo del nodo y la *salida del nodo* está en el lado derecho del nodo.

Los nodos de topología se conectan a través de una *conexión de nodo* que aparece como una línea negra que conecta la entrada de nodo de un nodo con la salida de nodo de otro nodo.

En la ilustración siguiente se muestra una topología conectada para un origen de audio.

![Ilustración que muestra las conexiones del nodo de origen a dos nodos de transformación y, a continuación, al nodo de salida](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Esta sección contiene los siguientes temas:



| Tema                                                                                          | Descripción                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Agregar nodos de origen con TopoEdit](adding-source-nodes-with-topoedit.md)                     | Describe el proceso de agregar nodos de origen a una topología.    |
| [Agregar nodos de transformación con TopoEdit](adding-transform-nodes-with-topoedit.md)               | Describe el proceso de agregar nodos de transformación a una topología. |
| [Agregar nodos de salida con TopoEdit](adding-output-nodes-with-topoedit.md)                     | Describe el proceso de agregar nodos de salida a una topología.    |
| [Conexión y desconexión de nodos de topología](connecting-and-disconnecting-topology-nodes.md) | Describe el proceso de conexión de dos nodos.                 |
| [Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md)                   | Describe el proceso de resolución de la topología.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



