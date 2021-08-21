---
title: Por qué se necesitan objetos proxy
description: Con objetos accesibles, cuando un cliente establece una función de enlace en contexto, el archivo DLL en el que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7038a43bf238d9baebee81e13cd82d904dc1b8a4c9ed7fb0c1576f42cbdfdfb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860995"
---
# <a name="why-proxy-objects-are-needed"></a>Por qué se necesitan objetos proxy

Con objetos accesibles, cuando un cliente establece una función de enlace en contexto [,](in-context-and-out-of-context-hook-functions.md)el archivo DLL en el que se implementa la función de enlace del cliente se carga en el espacio de direcciones del servidor. En este caso, cuando el cliente llama a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) desde dentro de la función de enlace, el puntero de interfaz que se devuelve apunta directamente al código en el espacio de direcciones del servidor. Cuando el cliente llama a una propiedad de interfaz mediante este puntero, la biblioteca del Modelo de objetos componentes (COM) no está implicada en la serialización o la desmarque y no puede detectar si se destruye un objeto. Por lo tanto, el servidor debe detectar esta situación y devolver un código de error al cliente.

 

 




