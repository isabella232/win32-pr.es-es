---
title: Objetos COM e interfaces
description: Objetos COM e interfaces
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a663b5d6e5966422927e37f1501924bf8ec8921210c9d38765153dc0d80fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119501555"
---
# <a name="com-objects-and-interfaces"></a>Objetos COM e interfaces

COM es una tecnología que permite que los objetos interactúen a través de los límites del proceso y del equipo tan fácilmente como dentro de un único proceso. COM permite esto especificando que la única manera de manipular los datos asociados a un objeto es a través de una *interfaz* en el objeto . Cuando este término se usa en esta documentación, hace referencia a una implementación en código de una interfaz compatible con binarios COM que está asociada a un objeto .

COM usa la palabra *interface en* un sentido diferente del que se usa normalmente en Visual C++ programación. Una interfaz de C++ hace referencia a todas las funciones que admite una clase y a las que los clientes de un objeto pueden llamar para interactuar con ella. Una interfaz COM hace referencia a un grupo predefinido de funciones relacionadas que implementa una clase COM, pero una interfaz específica no representa necesariamente todas las funciones que admite la clase.

Hacer referencia  a un objeto que implementa una interfaz significa que el objeto usa código que implementa cada método de la interfaz y proporciona punteros compatibles con binarios COM a esas funciones a la biblioteca COM. A continuación, COM pone esas funciones a disposición de cualquier cliente que solicite un puntero a la interfaz, tanto si el cliente está dentro como fuera del proceso que implementa esas funciones.

Para obtener más información, vea los temas siguientes:

-   [Interfaces e implementaciones de interfaz](interfaces-and-interface-implementations.md)
-   [Interface Pointers and Interfaces](interface-pointers-and-interfaces.md) (Punteros de interfaz e interfaces)
-   [Herencia de IUnknown e interfaz](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




