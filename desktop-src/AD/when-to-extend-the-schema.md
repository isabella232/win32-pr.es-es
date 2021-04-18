---
title: Cuándo extender el esquema
description: Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación. La extensión del esquema es una operación compleja; los cambios de esquema se replican en todos los controladores de dominio del bosque de la empresa. Tenga en cuenta esto con cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Cuándo extender el esquema AD
- esquema AD, Cuándo se debe extender
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c182b346fd1e31bc549325260d9b57d75bbb63
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656211"
---
# <a name="when-to-extend-the-schema"></a>Cuándo extender el esquema

Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación. La extensión del esquema es una operación compleja; los cambios de esquema se replican en todos los controladores de dominio del bosque de la empresa. Tenga en cuenta esto con cuidado.

El esquema puede extenderse de tres maneras:

-   Derivar una nueva subclase de una clase existente: la subclase tiene todos los atributos de la superclase y cualquier atributo que especifique. Derivar de una clase existente:
    -   Cuando la clase existente requiere atributos adicionales, pero de lo contrario es aceptable.
    -   Cuando la capacidad de transformar objetos existentes de la clase en una nueva clase no es necesaria. No es posible agregar una subclase a un objeto existente.
    -   Usar el complemento Administrador de directorios existente para administrar los atributos extendidos de los objetos.
-   Agregue atributos a una clase existente y/o agregue objetos primarios para la clase. Al agregar varios atributos, realice esta operación de una manera estructurada definiendo una clase auxiliar y agregando esa clase auxiliar a la clase existente.
-   La modificación de una clase existente es necesaria cuando una aplicación requiere la capacidad de extender objetos existentes de la clase. Por ejemplo, para agregar datos específicos de la aplicación al objeto de usuario, extienda normalmente el usuario de clase, ya que debe administrar los usuarios existentes y no solo los usuarios especiales creados por la aplicación.
-   Cree una nueva clase con los atributos necesarios. Cree una nueva clase; es decir, una clase derivada de "Top" cuando ninguna clase existente cumple los requisitos operativos.

Cuando se crea una subclase de una clase existente, la subclase no heredará los elementos de interfaz de usuario asociados a la clase original. Por ejemplo, si se subclase de un objeto de usuario, las páginas de propiedades y los elementos de menú asociados al usuario no se heredan. Por esta razón, es preferible extender un objeto existente o crear una clase auxiliar en lugar de crear una subclase.

Tanto si crea subclases de una clase existente como si modifica una clase existente, querrá extender herramientas como el complemento usuarios y equipos de Active Directory para administrar los atributos extendidos de los objetos. Para obtener más información, consulte [extensión de la interfaz de usuario para objetos de directorio](extending-the-user-interface-for-directory-objects.md).

 

 




