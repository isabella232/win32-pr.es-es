---
title: Matrices y punteros
description: La llamada a procedimiento remoto (RPC) está diseñada para ser más transparente para los desarrolladores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Llamada a procedimiento remoto RPC, descrito, matrices y punteros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776872"
---
# <a name="arrays-and-pointers"></a>Matrices y punteros

La llamada a procedimiento remoto (RPC) está diseñada para ser más transparente para los desarrolladores. Para lograr esta transparencia, el código auxiliar del cliente se transmite al servidor tanto el puntero como el objeto de datos al que señala. Si el procedimiento remoto cambia los datos, el servidor debe devolver los datos nuevos al cliente para que el cliente pueda copiar los datos nuevos en los datos originales.

En general, una llamada a procedimiento remoto se comporta igual que una llamada a procedimiento local. Es decir, cuando un puntero es un parámetro, el procedimiento remoto puede tener acceso al objeto de datos al que hace referencia el puntero de la misma manera que un procedimiento local.

Dado que los programas de cliente y servidor se ejecutan en espacios de direcciones diferentes, los programadores deben usar los atributos Lenguaje de definición de interfaz de Microsoft (MIDL) para describir cómo se transmiten los datos de puntero y matriz entre el cliente y el servidor. En esta sección se ofrece información general sobre cómo usar matrices y punteros en aplicaciones distribuidas, en los temas siguientes:

-   [Matrices y RPC](arrays-and-rpc.md)
-   [Punteros y RPC](pointers-and-rpc.md)
-   [Usar matrices, cadenas y punteros](using-arrays-strings-and-pointers.md)

 

 




