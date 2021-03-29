---
title: Clases auxiliares vinculadas estáticamente
description: Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo auxiliaryClass o systemAuxiliaryClass de la definición de classSchema de una clase de objeto en el esquema.
ms.assetid: 24765001-7a60-4654-a23a-bf0326b59096
ms.tgt_platform: multiple
keywords:
- Clases auxiliares vinculadas estáticamente AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d1ef6191834687fc2b7741f097f6bfe75b5ef31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773074"
---
# <a name="statically-linked-auxiliary-classes"></a>Clases auxiliares vinculadas estáticamente

Una clase auxiliar vinculada estáticamente es aquella que se incluye en el atributo **auxiliaryClass** o **systemAuxiliaryClass** de la definición de **ClassSchema** de una clase de objeto en el esquema. Esto significa que la clase auxiliar forma parte de cada instancia de la clase a la que está asociada.

Una clase auxiliar puede vincularse estáticamente a una clase de objeto cuando se define la clase, es decir, cuando su objeto **ClassSchema** se agrega al contenedor de esquemas. Esta es la única vez que se puede usar el **systemAuxiliaryClass** ; una vez creado el objeto **ClassSchema** , no se puede modificar su atributo **systemAuxiliaryClass** . Una clase auxiliar vinculada estáticamente en este momento puede tener atributos obligatorios (**mustHave**) y/o opcionales (**mayHave**).

Un usuario con privilegios que tenga los permisos necesarios para extender el esquema puede Agregar o quitar clases auxiliares del atributo **systemAuxiliaryClass** de un objeto **ClassSchema** existente. Al hacerlo, se agrega o se quita la clase auxiliar de cada instancia existente de la clase de objeto. Una clase auxiliar vinculada estáticamente en este momento puede tener atributos opcionales, pero no puede tener atributos obligatorios. Esto se debe a que puede haber instancias existentes de la clase de objeto, en cuyo caso agregar un nuevo atributo obligatorio crearía problemas. Posteriormente, un usuario con privilegios puede quitar una clase auxiliar del atributo **auxiliaryClass** de un objeto **ClassSchema** .

 

 




