---
title: Tipos de identificadores de enlace
description: Los identificadores de enlace pueden ser automáticos, implícitos o explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076084"
---
# <a name="types-of-binding-handles"></a>Tipos de identificadores de enlace

Los identificadores de enlace pueden ser automáticos, implícitos o explícitos. Difieren en la cantidad de control que tiene la aplicación sobre el proceso de enlace. Como sugiere el nombre, el enlace automático controla el enlace. Las aplicaciones de cliente y de servidor no necesitan código para controlar el proceso de enlace. Los identificadores de enlace implícitos permiten a los programas cliente configurar el identificador de enlace antes de que tenga lugar el enlace. Una vez que el cliente establece un enlace, la biblioteca en tiempo de ejecución de RPC controla el resto. Los identificadores de enlace explícitos mueven el control completo sobre el proceso de enlace al código fuente del cliente y los programas del servidor. Con este control, se aumenta la complejidad. La aplicación debe llamar a funciones RPC para administrar el enlace. No se produce automáticamente. Se recomiendan los identificadores de enlace explícitos.

En el diagrama siguiente se muestran las diferencias entre los identificadores de enlace automáticos, implícitos y explícitos.

![diferencias entre los identificadores de enlace automático, implícito y explícito](images/bhand.png)

Además, cada identificador de enlace es primitivo o personalizado. En los temas siguientes se describe cada tipo de identificador de enlace:

-   [Identificadores de enlace automáticos](automatic-binding-handles.md)
-   [Identificadores de enlace implícitos](implicit-binding-handles.md)
-   [Identificadores de enlace explícitos](explicit-binding-handles.md)
-   [Identificadores de enlace primitivos y personalizados](primitive-and-custom-binding-handles.md)

 

 




