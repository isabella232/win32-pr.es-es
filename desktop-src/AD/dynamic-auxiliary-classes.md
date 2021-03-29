---
title: Clases auxiliares dinámicas
description: De forma similar a las clases de objeto estructural y abstracto, las clases auxiliares se definen mediante un objeto classSchema en el esquema de Active Directory.
ms.assetid: bd5f6aed-c79a-4c03-ad03-a4ae00f0b888
ms.tgt_platform: multiple
keywords:
- Clases auxiliares dinámicas AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8c13fc8231b5232b82a61b9409f1736e5bd9249
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487451"
---
# <a name="dynamic-auxiliary-classes"></a>Clases auxiliares dinámicas

De forma similar a las clases de objeto estructural y abstracto, las clases auxiliares se definen mediante un objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) en el esquema de Active Directory. Para obtener más información, vea [clases estructurales, abstractas y auxiliares](structural-abstract-and-auxiliary-classes.md). Esta definición de esquema especifica varias características de la clase, incluidos los atributos asociados a la clase.

A diferencia de las clases estructurales, no se puede crear una instancia de una clase auxiliar como se haría con una clase estructural. En su lugar, se usa una clase auxiliar para extender la lista de atributos que está asociada a otra clase de objeto estructural, abstract u auxiliar.

En la versión inicial de Windows 2000, Active Directory Domain Services proporcionaban compatibilidad con la vinculación estática de clases auxiliares con la definición de [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) de otra clase de objeto. Cuando se utiliza una clase auxiliar de esta manera, cada instancia de la clase de objeto admite los atributos de la clase auxiliar.

**Windows 2000 Server y versiones anteriores:** Active Directory Domain Services no proporciona compatibilidad con la vinculación dinámica de clases auxiliares a objetos individuales, y no solo a clases completas de objetos. Además, las clases auxiliares que se han adjuntado a una instancia de objeto no se pueden quitar de la instancia posteriormente.

**Windows Server 2003:** Se admiten las clases auxiliares dinámicas cuando todos los controladores de dominio del bosque ejecutan Windows Server 2003 y el modo funcional del bosque es Windows Server 2003.

Para obtener más información acerca de las clases auxiliares, consulte:

-   [Clases auxiliares vinculadas dinámicamente](dynamically-linked-auxiliary-classes.md)
-   [Clases auxiliares vinculadas estáticamente](statically-linked-auxiliary-classes.md)
-   [Determinar las clases asociadas a una instancia de objeto](determining-the-classes-associated-with-an-object-instance.md)
-   [Agregar una clase auxiliar a una instancia de objeto](adding-an-auxiliary-class-to-an-object-instance.md)

Para obtener más información acerca de los niveles funcionales del bosque, vea el tema sobre cómo Active Directory elevar los niveles funcionales de dominio y bosque en la base de conocimiento de ayuda y soporte técnico en [https://support/microsoft.com/kb/322692\#4](https://support.microsoft.com/kb/322692) .

 

 