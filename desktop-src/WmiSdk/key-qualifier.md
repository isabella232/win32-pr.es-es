---
description: El calificador Key indica si la propiedad forma parte del identificador del espacio de nombres.
ms.assetid: 838d295f-e812-4e46-99a4-d2714a0ae8dc
ms.tgt_platform: multiple
title: Calificador de clave
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Key
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9ae5525aa85ab744e7e6824bb6079511a3611643d53594503e70c8e587f363cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118555905"
---
# <a name="key-qualifier"></a>Calificador de clave

El **calificador** Key indica si la propiedad forma parte del identificador del espacio de nombres. Si más de una propiedad tiene el **calificador Key,** todas estas propiedades forman colectivamente la clave (una clave compuesta). Cuando se toman juntas, las propiedades de clave deben proporcionar una referencia única para cada instancia de clase. Si este calificador se coloca en una propiedad, solo se permite el valor **TRUE.**

Puede usar cualquier tipo de propiedad, excepto lo siguiente:

-   Matrices
-   Números reales y de punto flotante
-   Objetos insertados
-   Caracteres inferiores a ASCII 32 (es decir, caracteres de espacio en blanco)
-   Las cadenas de caracteres de **tipo char16** o cadenas de caracteres que se definen como claves deben contener valores mayores que U+0020. Esto se debe a que WMI usa valores clave en rutas de acceso de objeto y no se pueden usar caracteres que no se imprimen en una ruta de acceso de objeto.

Cuando una clase primaria especifica una clave, todas las clases derivadas de la clase primaria heredan esa clave. Las clases derivadas no pueden modificar la clave heredada ni definir ninguna nueva propiedad de clave. Sin embargo, al derivar una subclase de una clase abstracta sin una clave, puede introducir una clave en la subclase.

Todas las clases que definen más de una instancia deben especificar una clave. Dado que las clases abstractas no definen ninguna instancia, no necesitan especificar claves. Dado que las clases singleton definen una sola instancia, no pueden especificar claves.

Las claves se escriben una vez en la creación de instancias del objeto y no se deben modificar más adelante. No tiene sentido aplicar un valor predeterminado a una propiedad calificada por clave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

 




