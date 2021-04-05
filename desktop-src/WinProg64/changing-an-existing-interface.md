---
title: Cambiar una interfaz existente
description: Siempre que sea posible, implemente una nueva interfaz para la aplicación, en lugar de realizar cambios en una existente.
ms.assetid: 29845cf5-445c-403d-b298-d4e07c3536b7
keywords:
- cambiar interfaces existentes programación de Windows de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a656ee768dcc2e88725d2cff0ddc5604fd771f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104533304"
---
# <a name="changing-an-existing-interface"></a>Cambiar una interfaz existente

Siempre que sea posible, implemente una nueva interfaz para la aplicación, en lugar de realizar cambios en una existente. Si no puede evitar el cambio de una interfaz existente, use los nuevos tipos de datos solo en los nuevos métodos. La introducción de un nuevo tipo de datos o la modificación de un tipo existente es la fuente más común de problemas de incompatibilidad. El modelo de tiempo de ejecución de RPC supone que la aplicación receptora conoce los tipos de datos que recibe, por lo que los datos se colocan en la conexión sin una descripción de datos genéricos. Cuando el destinatario espera un tipo de datos diferente del que el remitente ha colocado en la conexión, el código auxiliar genera una excepción (o se produce un error en la transmisión de otra manera menos estable).

Una interfaz RPC se define mediante su UUID y sus números de versión principal y secundaria. Al cambiar una interfaz existente, debe agregar los nuevos métodos al final de la interfaz y cambiar el número de versión secundaria. Si agrega métodos en cualquier lugar o realiza cualquier otro cambio en la interfaz, también deberá cambiar el número de versión principal.

En realidad, hay ocasiones en las que no se puede cambiar ni siquiera el número de versión secundaria, ya que un nuevo cliente no podrá comunicarse con un servidor antiguo y no podrá actualizar el servidor. El tiempo de ejecución de RPC genera una excepción \_ , \_ PROCNUM \_ de RPC S fuera \_ del \_ intervalo, cuando un cliente llama a un método más allá de los especificados para su interfaz con el servidor. La solución alternativa consiste en dejar sin modificar los números de versión y escribir el código de cliente para controlar esta excepción de forma correcta, por lo que el cliente degrada su rendimiento, por ejemplo, o por cualquier medio que sea adecuado para su aplicación.

Existe una solución similar para un caso especial de cambiar un tipo de datos en un método existente. Si tiene una [**Unión**](/windows/desktop/Midl/union) cuyas ramas son punteros y que no tiene una rama predeterminada para tipos no reconocidos, puede Agregar una nueva bifurcación que use el nuevo tipo de datos. Esto no cambiará el tamaño de la estructura de datos. Cuando el cliente se comunica con un nuevo servidor, puede usar el nuevo tipo de datos. Sin embargo, cuando el cliente se comunica con un servidor anterior, el tiempo de ejecución generará la excepción la \_ \_ etiqueta no válida RPC S \_ . De nuevo, debe escribir el código de cliente para controlar esta excepción de forma adecuada.

Una interfaz DCOM se identifica mediante su GUID. En DCOM, las interfaces se consideran inmutables y solo puede realizar cambios creando una nueva interfaz que herede de la antigua. Estas reglas garantizan que los clientes y los servidores sigan siendo compatibles.

 

 