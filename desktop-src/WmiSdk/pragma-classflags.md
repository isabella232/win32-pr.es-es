---
description: Controla la forma en que WMI crea o actualiza clases en función de las marcas especificadas.
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
ms.openlocfilehash: 6fd2b8ec75bd0521ce31af1ee7ce9dba2d9498890f9b5ddc768463f733322cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996325"
---
# <a name="pragma-classflags"></a>pragma classflags

El **comando pragma classflags** preprocessor controla la forma en que WMI crea o actualiza clases en función de las marcas especificadas.

A continuación se describe la sintaxis de este comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



*\[ La \]* marca debe ser uno o varios de los argumentos siguientes. Puede combinar cualquier marca que no se contradiga entre sí.



| Marca        | Descripción                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Indica al compilador que no realiza ningún cambio en las clases existentes y finaliza una compilación si ya existe una clase especificada en el archivo MOF en WMI.                                                                                                                                                                                                        |
| forceupdate | Fuerza las actualizaciones de clases cuando existen clases secundarias en conflicto. Por ejemplo, si define un calificador de clase en una clase secundaria y la clase base intenta agregar el mismo calificador, el uso de esta marca hace que el compilador resuelva este conflicto eliminando el calificador en conflicto de la clase secundaria. Si la clase secundaria tiene instancias, se produce un error en la actualización. |
| safeupdate  | Permite al compilador actualizar clases incluso si existen clases secundarias, si el cambio no provoca conflictos con las clases secundarias. Por ejemplo, esta marca permite agregar una nueva propiedad a una clase base sin tener que agregar también la propiedad a ninguna clase secundaria existente. Si las clases secundarias tienen instancias, se produce un error en la actualización.                           |
| updateonly  | Indica al compilador que no cree clases nuevas y hace que finalice la compilación si no existe una clase especificada en el archivo MOF.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando con las marcas updateonly y forceupdate.


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

 

 




