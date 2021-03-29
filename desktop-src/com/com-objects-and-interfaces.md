---
title: Objetos e interfaces COM
description: Objetos e interfaces COM
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773321"
---
# <a name="com-objects-and-interfaces"></a>Objetos e interfaces COM

COM es una tecnología que permite a los objetos interactuar a través de los límites de equipos y procesos tan fácilmente como dentro de un único proceso. COM lo habilita especificando que la única manera de manipular los datos asociados a un objeto es a través de una *interfaz* en el objeto. Cuando este término se usa en esta documentación, hace referencia a una implementación en el código de una interfaz compatible con binario COM que está asociada a un objeto.

COM utiliza la *interfaz* de Word en un sentido diferente del que se usa normalmente en la programación de Visual C++. Una interfaz de C++ hace referencia a todas las funciones que admite una clase y a la que los clientes de un objeto pueden llamar para interactuar con ella. Una interfaz COM hace referencia a un grupo predefinido de funciones relacionadas que implementa una clase COM, pero una interfaz concreta no representa necesariamente todas las funciones que admite la clase.

La referencia a un objeto que *implementa* una interfaz significa que el objeto utiliza código que implementa cada método de la interfaz y proporciona punteros com compatibles con binario a esas funciones a la biblioteca com. COM hace que estas funciones estén disponibles para cualquier cliente que solicite un puntero a la interfaz, tanto si el cliente está dentro o fuera del proceso que implementa esas funciones.

Para obtener más información, vea los temas siguientes:

-   [Interfaces e implementaciones de interfaz](interfaces-and-interface-implementations.md)
-   [Interface Pointers and Interfaces](interface-pointers-and-interfaces.md) (Punteros de interfaz e interfaces)
-   [IUnknown y herencia de interfaz](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




