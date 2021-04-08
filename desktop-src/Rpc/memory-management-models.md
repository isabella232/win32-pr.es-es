---
title: Modelos de Memory-Management
description: Modelos de Memory-Management
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994611"
---
# <a name="memory-management-models"></a>Modelos de Memory-Management

Como desarrollador, tiene varias opciones para la asignación y liberación de la memoria. Considere una estructura de datos compleja que consta de nodos conectados con punteros, como una lista vinculada o un árbol. Puede aplicar atributos que seleccionen uno de los siguientes modelos:

-   [Asignación y desasignación de nodo por nodo](node-by-node-allocation-and-deallocation.md).
-   [Un búfer lineal único asignado por el código auxiliar para todo el árbol](stub-allocated-buffers.md).
-   [Administración de memoria de código auxiliar de servidor](server-stub-memory-management.md)
-   [Un búfer lineal único asignado por la aplicación cliente para todo el árbol](application-allocated-buffer.md).
-   [Almacenamiento persistente en el servidor](persistent-storage-on-the-server.md).

 

 




