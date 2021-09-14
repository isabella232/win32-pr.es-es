---
title: Memory-Management modelos
description: Memory-Management modelos
ms.assetid: 1690901b-2a1e-455b-a440-2674f5e5dfa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8114f11755829be9d5f7b17b751e075701ac0aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244466"
---
# <a name="memory-management-models"></a>Memory-Management modelos

Como desarrollador, tiene varias opciones para asignar y liberar memoria. Considere una estructura de datos compleja que consta de nodos conectados con punteros, como una lista vinculada o un árbol. Puede aplicar atributos que seleccionen uno de los siguientes modelos:

-   [Asignación y desasignación de](node-by-node-allocation-and-deallocation.md)nodo a nodo.
-   [Un único búfer lineal asignado por el código auxiliar para todo el árbol](stub-allocated-buffers.md).
-   [Administración de memoria de código auxiliar del servidor](server-stub-memory-management.md)
-   [Un único búfer lineal asignado por la aplicación cliente para todo el árbol](application-allocated-buffer.md).
-   [Almacenamiento persistente en el servidor](persistent-storage-on-the-server.md).

 

 




