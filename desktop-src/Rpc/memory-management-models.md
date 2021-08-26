---
title: Memory-Management modelos
description: Memory-Management modelos
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a985158f54bf09d149e04c7eebc5853417e39191ca0bb854cb7d1ba5de1e5d86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019985"
---
# <a name="memory-management-models"></a>Memory-Management modelos

Como desarrollador, tiene varias opciones para asignar y liberar memoria. Considere una estructura de datos compleja que consta de nodos conectados con punteros, como una lista vinculada o un árbol. Puede aplicar atributos que seleccionen uno de los siguientes modelos:

-   [Asignación y desasignación de](node-by-node-allocation-and-deallocation.md)nodo a nodo.
-   [Un único búfer lineal asignado por el código auxiliar para todo el árbol](stub-allocated-buffers.md).
-   [Administración de memoria de código auxiliar del servidor](server-stub-memory-management.md)
-   [Un único búfer lineal asignado por la aplicación cliente para todo el árbol](application-allocated-buffer.md).
-   [Almacenamiento persistente en el servidor](persistent-storage-on-the-server.md).

 

 




