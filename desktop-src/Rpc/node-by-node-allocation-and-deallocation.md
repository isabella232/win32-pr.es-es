---
title: Asignación y desasignación de nodo a nodo
description: La asignación y desasignación de nodos de estructuras de datos mediante el código auxiliar es el método predeterminado de administración de memoria para todos los parámetros tanto en el cliente como en el servidor.
ms.assetid: 04752fd9-438c-4b52-830b-ce136f83b3b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52aea7c2e95615af8549c1f66476e1a105b91abd68dd31089db9cf23d8ec2af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927844"
---
# <a name="node-by-node-allocation-and-deallocation"></a>Asignación y desasignación de nodo a nodo

La asignación y desasignación de nodos de estructuras de datos mediante el código auxiliar es el método predeterminado de administración de memoria para todos los parámetros tanto en el cliente como en el servidor. En el lado cliente, el código auxiliar asigna cada nodo con una llamada independiente a [midl \_ user \_ allocate](/windows/desktop/Midl/midl-user-allocate-1). En el lado servidor, en lugar de llamar a **la asignación de usuario midl, \_ \_** se usa memoria privada siempre que sea posible. Si **se llama a \_ \_ la** asignación de usuario midl, el código auxiliar del servidor llamará al usuario **midl \_ \_ libremente** para liberar los datos. En la mayoría de los casos, el uso de asignación y desasignación de nodo a nodo en lugar de asignar (todos los **\[ \_ nodos) \]** dará como resultado un mayor rendimiento de los códigos auxiliares del lado servidor.

 

 