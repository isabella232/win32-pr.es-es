---
title: Objetos COM e interfaces
description: Objetos COM e interfaces
ms.assetid: a3b78086-0f02-4b3f-a856-46bfcf4457f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8c2b74f2b9741e41e7fe23226041f4c225bd85
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060935"
---
# <a name="com-objects-and-interfaces"></a>Objetos COM e interfaces

COM es una tecnología que permite que los objetos interactúen a través de los límites de proceso y equipo tan fácilmente como dentro de un único proceso. COM permite esto especificando que la única manera de manipular los datos asociados a un objeto es a través de una *interfaz* en el objeto . Cuando este término se usa en esta documentación, hace referencia a una implementación en el código de una interfaz compatible con binarios COM que está asociada a un objeto .

COM usa la interfaz *de palabras* en un sentido diferente de la que se usa normalmente en Visual C++ programación. Una interfaz de C++ hace referencia a todas las funciones que admite una clase y a las que los clientes de un objeto pueden llamar para interactuar con ella. Una interfaz COM hace referencia a un grupo predefinido de funciones relacionadas que implementa una clase COM, pero una interfaz específica no representa necesariamente todas las funciones que admite la clase.

Hacer referencia a un objeto que implementa una interfaz significa que el objeto usa código que implementa cada método de la interfaz y proporciona punteros compatibles con binarios COM *a* esas funciones a la biblioteca COM. A continuación, COM pone esas funciones a disposición de cualquier cliente que solicite un puntero a la interfaz, tanto si el cliente está dentro como fuera del proceso que implementa esas funciones.

Para obtener más información, vea los temas siguientes:

-   [Interfaces e implementaciones de interfaz](interfaces-and-interface-implementations.md)
-   [Interface Pointers and Interfaces](interface-pointers-and-interfaces.md) (Punteros de interfaz e interfaces)
-   [IUnknown y herencia de interfaz](iunknown-and-interface-inheritance.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 




