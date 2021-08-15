---
title: Clases auxiliares vinculadas estáticamente
description: Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo auxiliaryClass o systemExceptionaryClass de la definición classSchema de una clase de objeto en el esquema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Ad de clases auxiliares vinculadas estáticamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce00592052b1b52f82e2758fdfd7241c6bd24233ce6db6c11389165eeaa5e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024723"
---
# <a name="statically-linked-auxiliary-classes"></a>Clases auxiliares vinculadas estáticamente

Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo **auxiliaryClass** o **systemExceptionaryClass** de la definición **classSchema** de una clase de objeto en el esquema. Esto significa que la clase auxiliar forma parte de cada instancia de la clase a la que está asociada.

Una clase auxiliar se puede vincular estáticamente a una clase de objeto cuando se define la clase , es decir, cuando su **objeto classSchema** se agrega al contenedor de esquemas. Esta es la única vez que **se puede usar systemIliaryClass;** después de crear un objeto **classSchema,** no se puede modificar su atributo **systemExceptionaryClass.** Una clase auxiliar que está vinculada estáticamente en este momento puede tener atributos obligatorios (**mustAttribute**) o opcionales (**mayCollection**).

Un usuario con privilegios con los permisos necesarios para extender el esquema puede agregar o quitar clases auxiliares del atributo **systemAttributeiliaryClass** de un objeto **classSchema** existente. Al hacerlo, se agrega o quita la clase auxiliar de cada instancia existente de la clase de objeto. Una clase auxiliar que está vinculada estáticamente en este momento puede tener atributos opcionales, pero no puede tener atributos obligatorios. Esto se debe a que puede haber instancias existentes de la clase de objeto, en cuyo caso, agregar un nuevo atributo obligatorio crearía problemas. Posteriormente, un usuario con privilegios puede quitar una clase auxiliar del atributo **auxiliaryClass** de un **objeto classSchema.**

 

 




