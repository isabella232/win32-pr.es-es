---
title: Asignación y desasignación de nodo por nodo
description: La asignación y desasignación de estructuras de datos de nodo por nodo es el método predeterminado de administración de memoria para todos los parámetros tanto en el cliente como en el servidor.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6cc6b3ff61d4db3ba716664a2ff854e94cb28fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104487982"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Asignación y desasignación de nodo por nodo

La asignación y desasignación de estructuras de datos de nodo por nodo es el método predeterminado de administración de memoria para todos los parámetros tanto en el cliente como en el servidor. En el lado del cliente, el código auxiliar asigna cada nodo con una llamada independiente a [la \_ \_ asignación de usuarios de MIDL](/windows/desktop/Midl/midl-user-allocate-1). En el lado del servidor, en lugar de llamar a la **\_ \_ asignación de usuarios de MIDL**, se usa la memoria privada siempre que sea posible. Si se llama a la **\_ \_ asignación de usuarios de MIDL** , el código auxiliar del servidor llamará **\_ \_ gratuitamente al usuario de MIDL** para liberar los datos. En la mayoría de los casos, el uso de la asignación y desasignación de nodo por nodo en lugar de usar **\[ asignar (todos los \_ nodos) \]** dará como resultado un mayor rendimiento del código auxiliar del lado servidor.

 

 