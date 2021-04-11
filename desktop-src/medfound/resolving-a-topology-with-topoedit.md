---
description: Resolver una topología con TopoEdit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Resolver una topología con TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275819"
---
# <a name="resolving-a-topology-with-topoedit"></a>Resolver una topología con TopoEdit

Hay dos tipos de topologías:

-   Topología parcial. El nodo de origen se conecta directamente al nodo de salida. En algunos casos, una topología parcial puede tener algunos nodos de transformación intermedios, como efectos, pero no todos. Los nodos de transformación que se omiten suelen ser descodificadores o conversión de formato MFTs, como convertidores de colores y remuestreadores de audio.

-   Topología completa. El nodo de origen se conecta al nodo de salida a través de un nodo de transformación. Este tipo de topología debe tener todos los nodos para procesar los datos.

TopoEdit solo puede reproducir topologías completas. TopoEdit usa el objeto cargador de topología, proporcionado por Media Foundation, para convertir una topología parcial en una topología completa mediante la inserción de las transformaciones necesarias. El proceso de creación de una topología completa se denomina resolver una topología.

Para obtener información sobre los tipos de topología, consulte la sección topologías parciales en acerca de las [topologías](about-topologies.md).

Antes de resolver una topología, asegúrese de que:

-   La topología contiene un nodo de origen y un nodo de salida.

-   Los nodos de origen y de salida están conectados mediante una conexión de nodo válida. Durante la resolución de la topología, el cargador de topología comprueba la compatibilidad del tipo de medio de los nodos. Si existe una conexión de nodo no válida, se produce un error en el proceso y se muestra un mensaje de error.

Para resolver una topología, en el menú **topología** , haga clic en **resolver topología**.

La barra de herramientas indica el estado de la topología: **\[ resuelto \]** o **\[ no resuelto \]**.

Si TopoEdit resuelve una topología correctamente, el estado de la **topología** se establece en **\[ resolved \]** y se habilitan los controles de reproducción.

Cada vez que realiza cambios en la topología, el **Estado** de la topología se establece en **\[ no \] resuelto** , lo que indica que se debe volver a resolver.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Compilar topologías mediante TopoEdit](building-topologies-by-using-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



