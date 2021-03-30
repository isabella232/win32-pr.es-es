---
description: El calificador de clave indica si la propiedad forma parte del identificador de espacio de nombres.
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
ms.openlocfilehash: affc9f4be594723700a65c9c92f8ae37ffead265
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816123"
---
# <a name="key-qualifier"></a>Calificador de clave

El calificador de **clave** indica si la propiedad forma parte del identificador de espacio de nombres. Si hay más de una propiedad que tiene el calificador de **clave** , todas estas propiedades forman colectivamente la clave (una clave compuesta). Cuando se toman juntas, las propiedades clave deben proporcionar una referencia única para cada instancia de clase. Si este calificador se coloca en una propiedad, solo se permite el valor **true** .

Puede usar cualquier tipo de propiedad, excepto los siguientes:

-   Matrices
-   Números reales y de punto flotante
-   Objetos insertados
-   Caracteres inferiores a ASCII 32 (es decir, caracteres de espacio en blanco)
-   Las cadenas de caracteres de tipo **char16** o cadenas de caracteres que se definen como claves deben contener valores mayores que U + 0020. Esto se debe a que WMI usa valores de clave en las rutas de acceso de objeto y no se pueden usar caracteres no imprimibles en una ruta de acceso de objeto.

Cuando una clase primaria especifica una clave, todas las clases derivadas de la clase primaria heredan esa clave. Las clases derivadas no pueden modificar la clave heredada ni definir ninguna propiedad de clave nueva. Sin embargo, al derivar una subclase de una clase abstracta sin una clave, puede introducir una clave en la subclase.

Todas las clases que definen más de una instancia de deben especificar una clave. Dado que las clases abstractas no definen ninguna instancia, no necesitan especificar claves. Dado que las clases singleton definen solo una instancia, no pueden especificar claves.

Las claves se escriben una vez en la creación de instancias de objeto y no se deben modificar posteriormente. No tiene sentido aplicar un valor predeterminado a una propiedad con clave calificada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

 




