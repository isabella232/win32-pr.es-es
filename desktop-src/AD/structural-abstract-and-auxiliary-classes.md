---
title: Clases estructurales, abstractas y auxiliares
description: El atributo objectClassCategory de un objeto classSchema puede tener un valor, como se muestra en la tabla siguiente, que indica si la clase es estructural, abstracta o auxiliar.
ms.assetid: 5af740cb-b292-4d80-abe5-3e3d194758f3
ms.tgt_platform: multiple
keywords:
- Clases estructurales, abstractas y auxiliares de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 393c08f5c26690d5b08b76dfea8ab4ff2833c94851a10ddcea2a69209279fbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024713"
---
# <a name="structural-abstract-and-auxiliary-classes"></a>Clases estructurales, abstractas y auxiliares

El **atributo objectClassCategory** de un objeto **classSchema** puede tener un valor, como se muestra en la tabla siguiente, que indica si la clase es estructural, abstracta o auxiliar.



| Value | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Clase estructural, que es el único tipo de clase que puede tener instancias en Active Directory Domain Services. Una clase estructural puede ser una subclase de una clase abstracta o estructural. Una clase estructural puede incluir cualquier número de clases auxiliares en su definición.                                                                                                                                                                                                                                           |
| 2     | Una clase abstracta, que es una plantilla que se usa para derivar nuevas clases abstractas, auxiliares y estructurales. Una clase abstracta solo puede ser una subclase de una clase abstracta. No se pueden crear instancias de clases abstractas en Active Directory Domain Services. Una clase abstracta puede incluir cualquier número de clases auxiliares en su definición.                                                                                                                                                                                   |
| 3     | Una clase auxiliar, que se puede incluir en la definición de una clase estructural, abstracta o auxiliar, en cuyo caso, los valores **mustContain**, **systemMustContain**, **mayContain** y **systemMayContain** de la clase auxiliar se agregan a los de la clase . Una clase auxiliar puede ser una subclase de una clase abstracta o auxiliar. No se pueden crear instancias de clases auxiliares en Active Directory Domain Services. Una clase auxiliar puede incluir cualquier número de clases auxiliares en su definición. |



 

No confunda **objectClassCategory** con una categoría [de objeto](object-class-and-object-category.md).

 

 




