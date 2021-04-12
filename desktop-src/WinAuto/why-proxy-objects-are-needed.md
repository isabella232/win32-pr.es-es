---
title: Por qué se necesitan objetos proxy
description: Con objetos accesibles, cuando un cliente establece una función de enlace en contexto, la DLL en la que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357082"
---
# <a name="why-proxy-objects-are-needed"></a>Por qué se necesitan objetos proxy

Con objetos accesibles, cuando un cliente establece una [función de enlace en contexto](in-context-and-out-of-context-hook-functions.md), la dll en la que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor. En este caso, cuando el cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) desde dentro de la función de enlace, el puntero de interfaz que se devuelve apunta directamente al código en el espacio de direcciones del servidor. Cuando el cliente llama a una propiedad de interfaz mediante este puntero, la biblioteca del modelo de objetos componentes (COM) no está implicada en la serialización o la desserialización, y no puede detectar si se destruye un objeto. Por lo tanto, el servidor debe detectar esta situación y devolver un código de error al cliente.

 

 




