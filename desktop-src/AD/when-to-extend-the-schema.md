---
title: Cuándo extender el esquema
description: Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación. Extender el esquema es una operación compleja; Los cambios de esquema se replican en todos los controladores de dominio del bosque empresarial. Tenga en cuenta esto con cuidado.
ms.assetid: 92231f31-d2af-4c3b-981e-e55cc478899d
ms.tgt_platform: multiple
keywords:
- Cuándo extender el ad de esquema
- schema AD , when to extend
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042665069b06804dd648798debca6e0cee5628e115f5f512718ea0a51cc765ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024333"
---
# <a name="when-to-extend-the-schema"></a>Cuándo extender el esquema

Extienda el esquema solo si ninguna clase de objeto existente cumple los requisitos de la aplicación. Extender el esquema es una operación compleja; Los cambios de esquema se replican en todos los controladores de dominio del bosque empresarial. Tenga en cuenta esto con cuidado.

El esquema se puede extender de tres maneras:

-   Derive una nueva subclase de una clase existente: la subclase tiene todos los atributos de la superclase y los atributos que especifique. Derive de una clase existente:
    -   Cuando la clase existente requiere atributos adicionales, pero de lo contrario es aceptable.
    -   Cuando no es necesaria la capacidad de transformar objetos existentes de la clase en una clase nueva. No es posible agregar una subclase a un objeto existente.
    -   Para usar el complemento Administrador de directorios existente para administrar los atributos extendidos de los objetos.
-   Agregue atributos a una clase existente o agregue objetos primarios para la clase. Al agregar varios atributos, realice esta operación de forma estructurada definiendo una clase auxiliar y agregando esa clase auxiliar a la clase existente.
-   Se requiere la modificación de una clase existente cuando una aplicación requiere la capacidad de extender los objetos existentes de la clase. Por ejemplo, para agregar datos específicos de la aplicación al objeto User, extienda la clase User normalmente, ya que debe controlar los usuarios existentes y no solo los usuarios especiales creados por la aplicación.
-   Cree una nueva clase con los atributos necesarios. Cree una nueva clase; es decir, una clase derivada de "Top" cuando ninguna clase existente cumple los requisitos operativos.

Cuando se subclase una clase existente, la subclase no heredará los elementos de interfaz de usuario asociados a la clase original. Por ejemplo, si subclasifica un objeto de usuario, las páginas de propiedades y los elementos de menú asociados al usuario no se heredan. Por este motivo, es preferible extender un objeto existente o crear una clase auxiliar en lugar de crear una subclase.

Tanto si subclasifica una clase existente como si modifica una clase existente, querrá extender herramientas como el complemento Usuarios y equipos de Active Directory para administrar los atributos extendidos de los objetos. Para obtener más información, vea [Extending the Interfaz de usuario for Directory Objects](extending-the-user-interface-for-directory-objects.md).

 

 




