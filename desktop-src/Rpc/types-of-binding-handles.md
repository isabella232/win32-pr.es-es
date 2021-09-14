---
title: Tipos de identificadores de enlace
description: Los identificadores de enlace pueden ser automáticos, implícitos o explícitos.
ms.assetid: 7f026199-6045-4f60-9002-543636cf6275
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60a09b858dfc677d06cf5885dc7a5f7a6ba599eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071391"
---
# <a name="types-of-binding-handles"></a>Tipos de identificadores de enlace

Los identificadores de enlace pueden ser automáticos, implícitos o explícitos. Difieren en la cantidad de control que tiene la aplicación sobre el proceso de enlace. Como sugiere el nombre, el enlace automático controla el enlace automatizado. Las aplicaciones cliente y servidor no necesitan código para controlar el proceso de enlace. Los identificadores de enlace implícitos permiten a los programas cliente configurar el identificador de enlace antes de que se lleve a cabo el enlace. Una vez que el cliente establece un enlace, la biblioteca rpc en tiempo de ejecución controla el resto. Los identificadores de enlace explícitos mueven un control completo sobre el proceso de enlace al código fuente del cliente y los programas del servidor. Con este control aumenta la complejidad. La aplicación debe llamar a funciones RPC para administrar el enlace. No se realiza automáticamente. Se recomiendan identificadores de enlace explícitos.

En el diagrama siguiente se muestran las diferencias entre los identificadores de enlace automático, implícito y explícito.

![diferencias entre identificadores de enlace automáticos, implícitos y explícitos](images/bhand.png)

Además, todos los identificadores de enlace son primitivos o personalizados. Cada tipo de identificador de enlace se describe en los temas siguientes:

-   [Identificadores de enlace automáticos](automatic-binding-handles.md)
-   [Identificadores de enlace implícitos](implicit-binding-handles.md)
-   [Identificadores de enlace explícitos](explicit-binding-handles.md)
-   [Identificadores de enlace primitivos y personalizados](primitive-and-custom-binding-handles.md)

 

 




