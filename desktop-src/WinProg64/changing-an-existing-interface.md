---
title: Cambiar una interfaz existente
description: Siempre que sea posible, implemente una nueva interfaz para la aplicación, en lugar de realizar cambios en una existente.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- cambiar las interfaces existentes de 64 bits Windows programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782587471de5616750501552445599a94571ff2275d080347937c595e2cd7668
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899075"
---
# <a name="changing-an-existing-interface"></a>Cambiar una interfaz existente

Siempre que sea posible, implemente una nueva interfaz para la aplicación, en lugar de realizar cambios en una existente. Si no puede evitar cambiar una interfaz existente, use nuevos tipos de datos solo en métodos nuevos. La introducción de un nuevo tipo de datos o la modificación de un tipo existente es el origen más común de problemas de incompatibilidad. El modelo en tiempo de ejecución de RPC supone que la aplicación receptora conoce los tipos de datos que recibe, por lo que los datos se ponen en la conexión sin una descripción de datos genérica. Cuando el destinatario espera un tipo de datos diferente al que el remitente ha puesto en la conexión, el código auxiliar genera una excepción (o se produce un error de transmisión de alguna otra manera menos correcta).

Una interfaz RPC se define mediante su UUID y sus números de versión principal y secundaria. Al cambiar una interfaz existente, debe agregar los nuevos métodos al final de la interfaz y cambiar el número de versión secundaria. Si agrega métodos en cualquier otro lugar o realiza cualquier otro cambio en la interfaz, también tendrá que cambiar el número de versión principal.

En realidad, hay ocasiones en las que no se puede cambiar incluso el número de versión secundaria, porque un nuevo cliente no podrá comunicarse con un servidor antiguo y no se puede actualizar el servidor. El tiempo de ejecución de RPC genera una excepción, RPC S PROCNUM OUT OF RANGE, cuando un cliente llama a un método más allá de los especificados para su interfaz \_ \_ con el \_ \_ \_ servidor. La solución alternativa consiste en dejar los números de versión sin cambios y escribir el código de cliente para controlar esta excepción correctamente, mediante la degradación del rendimiento del cliente, por ejemplo, o por los medios adecuados para la aplicación.

Hay una solución alternativa similar para un caso especial de cambio de un tipo de datos en un método existente. Si tiene [](/windows/desktop/Midl/union) una unión cuyas ramas son punteros y que no tiene una rama predeterminada para tipos no reconocidos, puede agregar una nueva rama que use el nuevo tipo de datos. Esto no cambiará el tamaño de la estructura de datos. Cuando el cliente se pone en conversación con un nuevo servidor, puede usar el nuevo tipo de datos. Sin embargo, cuando el cliente se hable con un servidor antiguo, el tiempo de ejecución producirá la excepción RPC \_ S \_ INVALID \_ TAG. De nuevo, tendrá que escribir el código de cliente para controlar esta excepción correctamente.

Una interfaz DCOM se identifica mediante su GUID. En DCOM, las interfaces se consideran inmutables y solo se pueden realizar cambios mediante la creación de una nueva interfaz que herede de la anterior. Estas reglas garantizan que los clientes y servidores sigan siendo compatibles.

 

 