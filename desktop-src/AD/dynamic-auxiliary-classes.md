---
title: Clases auxiliares dinámicas
description: De forma similar a las clases de objetos estructurales y abstractos, las clases auxiliares se definen mediante un objeto classSchema en el Active Directory esquema.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Clases auxiliares dinámicas de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45ce88f525b5d72a271aab1746a0ce0d0b308cb7022c4702433b82038c101435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429905"
---
# <a name="dynamic-auxiliary-classes"></a>Clases auxiliares dinámicas

De forma similar a las clases de objetos estructurales y abstractos, las clases auxiliares se definen mediante un [**objeto classSchema**](/windows/desktop/ADSchema/c-classschema) en el Active Directory esquema. Para obtener más información, [vea Clases estructurales, abstractas y auxiliares.](structural-abstract-and-auxiliary-classes.md) Esta definición de esquema especifica varias características de la clase, incluidos los atributos asociados a la clase .

A diferencia de las clases estructurales, no se puede crear una instancia de una clase auxiliar como se puede hacer con una clase estructural. En su lugar, se usa una clase auxiliar para ampliar la lista de atributos asociados a otra clase de objeto estructural, abstracta o auxiliar.

En la versión inicial de Windows 2000, Active Directory Domain Services proporcionaba compatibilidad para vincular estáticamente clases auxiliares a la definición [**classSchema**](/windows/desktop/ADSchema/c-classschema) de otra clase de objeto. Cuando se usa una clase auxiliar de esta manera, cada instancia de la clase de objeto admite los atributos de la clase auxiliar.

**Windows 2000 Server y versiones anteriores:** Active Directory Domain Services no proporciona compatibilidad para vincular dinámicamente clases auxiliares a objetos individuales, y no solo a clases enteras de objetos. Además, las clases auxiliares que se han asociado a una instancia de objeto no se pueden quitar posteriormente de la instancia de .

**Windows Server 2003:** Las clases auxiliares dinámicas se admiten cuando todos los controladores de dominio del bosque ejecutan Windows Server 2003 y el modo funcional del bosque Windows Server 2003.

Para obtener más información sobre las clases auxiliares, vea:

-   [Clases auxiliares vinculadas dinámicamente](dynamically-linked-auxiliary-classes.md)
-   [Clases auxiliares vinculadas estáticamente](statically-linked-auxiliary-classes.md)
-   [Determinar las clases asociadas a una instancia de objeto](determining-the-classes-associated-with-an-object-instance.md)
-   [Agregar una clase auxiliar a una instancia de objeto](adding-an-auxiliary-class-to-an-object-instance.md)

Para obtener más información sobre los niveles funcionales de bosque, vea "Cómo generar niveles funcionales de Active Directory dominio y bosque" en la página ayuda y soporte técnico Knowledge Base en [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 