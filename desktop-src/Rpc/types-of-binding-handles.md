---
title: Tipos de identificadores de enlace
description: Los identificadores de enlace pueden ser automáticos, implícitos o explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a3db77f01bf0228623efe9d3dca5fbeb023d97fbe00e5da4d4ba070f323ba5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011083"
---
# <a name="types-of-binding-handles"></a>Tipos de identificadores de enlace

Los identificadores de enlace pueden ser automáticos, implícitos o explícitos. Difieren en la cantidad de control que tiene la aplicación sobre el proceso de enlace. Como sugiere el nombre, el enlace automático controla el enlace automatizado. Las aplicaciones cliente y servidor no necesitan código para controlar el proceso de enlace. Los identificadores de enlace implícitos permiten a los programas cliente configurar el identificador de enlace antes de que se lleve a cabo el enlace. Una vez que el cliente establece un enlace, la biblioteca en tiempo de ejecución rpc controla el resto. Los identificadores de enlace explícitos mueven un control completo sobre el proceso de enlace al código fuente del cliente y los programas de servidor. Con este control aumenta la complejidad. La aplicación debe llamar a funciones RPC para administrar el enlace. No se realiza automáticamente. Se recomiendan identificadores de enlace explícitos.

En el diagrama siguiente se muestran las diferencias entre los identificadores de enlace automático, implícito y explícito.

![diferencias entre los identificadores de enlace automático, implícito y explícito](images/bhand.png)

Además, cada identificador de enlace es primitivo o personalizado. Cada tipo de identificador de enlace se describe en los temas siguientes:

-   [Identificadores de enlace automático](automatic-binding-handles.md)
-   [Identificadores de enlace implícitos](implicit-binding-handles.md)
-   [Identificadores de enlace explícitos](explicit-binding-handles.md)
-   [Identificadores de enlace primitivos y personalizados](primitive-and-custom-binding-handles.md)

 

 




