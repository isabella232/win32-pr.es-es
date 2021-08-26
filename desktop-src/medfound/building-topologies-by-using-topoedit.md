---
description: Creación de topologías mediante TopoEdit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Creación de topologías mediante TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88e678e0c25cbfe56c2633091820468a6c0313663847870a4de5c912a5edae95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959445"
---
# <a name="building-topologies-by-using-topoedit"></a>Creación de topologías mediante TopoEdit

Una topología debe tener los tres nodos siguientes:

-   Nodo de origen: los flujos de un archivo multimedia, que se usan como origen para la topología.
-   Nodo de transformación: una Media Foundation transformación (MFT). Estos nodos suelen ser codificadores, descodificadores y efectos para la topología.
-   Nodo de salida: receptor de flujo que pasa los datos multimedia, fotogramas de vídeo o secuencias de audio a la sesión multimedia para la reproducción.

Para obtener información sobre la estructura de topología, vea [About Topologies](about-topologies.md).

Para compilar una topología, debe agregar los nodos, conectarlos y resolver la topología para que se pueda reproducir.

Los nodos de topología se muestran como cuadros, con texto que muestra el nombre del nodo. Los cuadros verdes representan los nodos agregados por el usuario. Cuando se resuelve una topología, TopoEdit puede agregar nodos de transformación a la topología automáticamente. Aparecen como cuadros azules en el **panel Topología**.

Las entradas y salidas de topología se representan como cuadrados negros a lo largo del borde del nodo. La *entrada del* nodo se muestra en el  lado izquierdo del nodo y la salida del nodo está en el lado derecho del nodo.

Los nodos de topología se conectan *a* través de una conexión de nodo que aparece como una línea negra que conecta la entrada de nodo de un nodo a la salida del nodo de otro nodo.

En la ilustración siguiente se muestra una topología conectada para un origen de audio.

![ilustración que muestra las conexiones desde el nodo de origen, a dos nodos de transformación y, a continuación, al nodo de salida](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

Esta sección contiene los siguientes temas:



| Tema                                                                                          | Descripción                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [Agregar nodos de origen con TopoEdit](adding-source-nodes-with-topoedit.md)                     | Describe el proceso de agregar nodos de origen a una topología.    |
| [Agregar nodos de transformación con TopoEdit](adding-transform-nodes-with-topoedit.md)               | Describe el proceso de agregar nodos de transformación a una topología. |
| [Agregar nodos de salida con TopoEdit](adding-output-nodes-with-topoedit.md)                     | Describe el proceso de agregar nodos de salida a una topología.    |
| [Conexión y desconexión de nodos de topología](connecting-and-disconnecting-topology-nodes.md) | Describe el proceso de conexión de dos nodos.                 |
| [Resolver una topología con TopoEdit](resolving-a-topology-with-topoedit.md)                   | Describe el proceso de resolución de topología.                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



