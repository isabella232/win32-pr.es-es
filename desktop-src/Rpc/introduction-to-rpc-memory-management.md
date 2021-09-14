---
title: Introducción a la administración de memoria RPC
description: Introducción a la administración de memoria de llamadas a procedimientos remotos (RPC).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94ac4b6aecb2fd78448ebe31c72587fafb8f6fde
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244574"
---
# <a name="introduction-to-rpc-memory-management"></a>Introducción a la administración de memoria RPC

En el contexto de RPC, la administración de memoria implica:

-   Asignar y desasignar la memoria necesaria para simular un único espacio de direcciones conceptuales entre el cliente y el servidor en los distintos espacios de direcciones de los subprocesos del cliente y del servidor.
-   Determinar qué componente de software es responsable de administrar la memoria: la aplicación o el código auxiliar generado por MIDL.
-   Seleccionar atributos MIDL que afectan a la administración de memoria: atributos direccionales, atributos de puntero, atributos de matriz y el recuento de bytes de atributos de ACF, asignar \[ [ \_ ](/windows/desktop/Midl/byte-count) \] y habilitar \[ [](/windows/desktop/Midl/allocate) \] \[ [ \_ asignar](/windows/desktop/Midl/enable-allocate) \] .

Cuando un programa llama a una función o procedimiento en su espacio de direcciones, la administración de memoria es más sencilla que en una aplicación distribuida. Para ilustrar esto, en el diagrama siguiente se muestra un árbol binario. Para pasar esta estructura de datos a un procedimiento en su espacio de direcciones, un programa simplemente pasa un puntero a la raíz del árbol.

![un árbol binario, con punteros a datos de estructura ubicados en la raíz del árbol](images/bintree.png)

Las aplicaciones RPC de cliente/servidor comparten datos entre dos espacios de memoria diferentes. Estos espacios de memoria pueden estar o no en el mismo equipo. En cualquier caso, el cliente y el servidor no tienen acceso directo al espacio de memoria del otro. RPC depende de la capacidad de simular el espacio de direcciones del programa cliente en el espacio de direcciones del programa de servidor. También debe devolver datos, incluidos los datos nuevos y modificados, del servidor a la memoria del cliente.

En casos como el árbol binario representado en el diagrama anterior, no es suficiente pasar un puntero al nodo raíz a un procedimiento remoto. El programa o los códigos auxiliares deben pasar todo el árbol al espacio de direcciones del servidor para que el procedimiento remoto funcione en él.

 

 