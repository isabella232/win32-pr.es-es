---
title: Introducción a la administración de memoria RPC
description: Introducción a la administración de memoria de la llamada a procedimiento remoto (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359283"
---
# <a name="introduction-to-rpc-memory-management"></a>Introducción a la administración de memoria RPC

En el contexto de RPC, la administración de memoria implica:

-   Asignar y desasignar la memoria necesaria para simular un solo espacio de direcciones conceptual entre el cliente y el servidor en los diferentes espacios de direcciones de los subprocesos del cliente y del servidor.
-   Determinar qué componente de software es responsable de administrar la memoria, la aplicación o el código auxiliar generado por MIDL.
-   Seleccionar atributos MIDL que afectan a la administración de memoria: atributos direccionales, atributos de puntero, atributos de matriz y atributos ACF \[ [ \_ recuento de bytes](/windows/desktop/Midl/byte-count) \] , \[ [asignación](/windows/desktop/Midl/allocate) \] y \[ [habilitar \_ asignación](/windows/desktop/Midl/enable-allocate) \] .

Cuando un programa llama a una función o un procedimiento en su espacio de direcciones, la administración de la memoria es más sencilla que en una aplicación distribuida. En el siguiente diagrama se muestra un árbol binario. Para pasar esta estructura de datos a un procedimiento en su espacio de direcciones, un programa simplemente pasa un puntero a la raíz del árbol.

![un árbol binario, con punteros para estructurar los datos alojados en la raíz del árbol.](images/bintree.png)

Las aplicaciones RPC cliente/servidor comparten datos entre dos espacios de memoria distintos. Estos espacios de memoria pueden estar o no en el mismo equipo. En cualquier caso, el cliente y el servidor no tienen acceso directo al espacio de memoria de los demás. RPC depende de la capacidad de simular el espacio de direcciones del programa cliente en el espacio de direcciones del programa de servidor. También debe devolver datos, incluidos los datos nuevos y modificados, del servidor a la memoria del cliente.

En casos como el árbol binario representado en el diagrama anterior, no basta con pasar un puntero al nodo raíz a un procedimiento remoto. El programa o el código auxiliar debe pasar el árbol completo al espacio de direcciones del servidor para que el procedimiento remoto opere en él.

 

 