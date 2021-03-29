---
title: Restricciones en la extensión de esquema
description: Con el fin de reducir la posibilidad de que los cambios de esquema en una aplicación interrumpan otras aplicaciones y mantengan la coherencia del esquema, Active Directory Domain Services aplicar restricciones en el tipo de cambios de esquema que puede realizar una aplicación o un usuario.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c97ab3d9f6406a89b24c772e7df8254095f1286
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773104"
---
# <a name="restrictions-on-schema-extension"></a>Restricciones en la extensión de esquema

Con el fin de reducir la posibilidad de que los cambios de esquema en una aplicación interrumpan otras aplicaciones y mantengan la coherencia del esquema, Active Directory Domain Services aplicar restricciones en el tipo de cambios de esquema que puede realizar una aplicación o un usuario.

Las restricciones solo se imponen en la modificación de objetos de esquema existentes. El esquema se clasifica en dos categorías. Los objetos de esquema que se incluyen con Windows 2000 en el esquema base pertenecen a la categoría 1. Los objetos de esquema agregados posteriormente por otras aplicaciones o usuarios a través de la extensión de esquema dinámico pertenecen a la categoría 2. La categoría de un objeto de esquema se puede determinar mediante el bit 0x10 establecido en el atributo **systemFlags** en el objeto **ClassSchema** . Este bit solo se establece en objetos de categoría 1 y no se puede modificar ni se puede establecer en ningún objeto de categoría 2.

El atributo **systemFlags** lo usa internamente Active Directory Domain Services para identificar características especiales de los objetos de "infraestructura" del esquema base. Además de identificar objetos de categoría 1, **systemFlags** controla si un objeto se puede quitar, eliminar o cambiar de nombre. Estas operaciones se impiden para los objetos de los que Windows 2000 depende para ejecutarse.

En cualquier objeto de esquema, categoría 1 o 2, Active Directory Domain Services imponen las restricciones siguientes:

-   No se puede Agregar un nuevo **mustContain** a una clase (directamente o a través de la herencia agregando una clase auxiliar).
-   No se puede eliminar ningún **mustContain** de la clase (directamente o a través de la herencia).

Además, se imponen las siguientes restricciones adicionales en los objetos de esquema de categoría 1:

-   No se pueden cambiar los siguientes atributos de un atributo de categoría 1:

    -   **rangeLower** y **rangeUpper** (intervalo de valores).
    -   **attributeSecurityGuid** (determina a qué conjunto de propiedades pertenece el atributo, si existe).

-   No se puede cambiar el **defaultObjectCategory** de una clase de categoría 1.
-   No se puede cambiar el **objectCategory** de ninguna instancia de una clase de categoría 1.
-   No se puede convertir una clase o atributo de categoría 1 en inactivo.
-   No se puede cambiar el **lDAPDisplayName** de una clase o atributo de categoría 1.
-   No se puede cambiar el nombre de una clase o atributo de categoría 1.

 

 




