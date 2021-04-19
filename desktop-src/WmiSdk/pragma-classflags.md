---
description: Controla la forma en que WMI crea o actualiza las clases según las marcas especificadas.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696670"
---
# <a name="pragma-classflags"></a>pragma classflags

El comando de preprocesador **pragma classflags** controla la manera en que WMI crea o actualiza las clases según las marcas especificadas.

A continuación se describe la sintaxis de este comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



La *\[ marca \]* debe ser uno o varios de los siguientes argumentos. Puede combinar las marcas que no se contradicen entre sí.



| Marca        | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Indica al compilador que no realice ningún cambio en las clases existentes y finaliza una compilación si ya existe una clase especificada en el archivo MOF en WMI.                                                                                                                                                                                                        |
| Forza | Fuerza la actualización de las clases cuando existen clases secundarias en conflicto. Por ejemplo, si define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador, el uso de esta marca hace que el compilador resuelva este conflicto eliminando el calificador en conflicto de la clase secundaria. Si la clase secundaria tiene instancias, se produce un error en la actualización. |
| safeupdate  | Permite al compilador actualizar clases incluso si existen clases secundarias, si el cambio no provoca conflictos con las clases secundarias. Por ejemplo, esta marca permite agregar una nueva propiedad a una clase base sin tener que agregar también la propiedad a cualquier clase secundaria existente previamente. Si las clases secundarias tienen instancias, se produce un error en la actualización.                           |
| updateonly  | Indica al compilador que no cree ninguna clase nueva y hace que el compilador finalice la compilación si no existe una clase especificada en el archivo MOF.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando con las marcas updateonly y ForceUpdate.


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




