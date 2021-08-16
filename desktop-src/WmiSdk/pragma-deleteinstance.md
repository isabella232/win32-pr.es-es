---
description: Elimina una instancia existente de una clase del repositorio.
ms.assetid: 4389f831-a60e-4198-a55a-79189d10a38a
ms.tgt_platform: multiple
title: pragma deleteinstance
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
ms.openlocfilehash: 29739f1d95cf5c8352c2b7822dbc3da7777f41f69fc5086631e0069c3b832623
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316857"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

El **comando pragma deleteinstance** elimina una instancia existente de una clase del repositorio.

A continuación se describe la sintaxis de este comando:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceId es* un identificador único de la instancia que el compilador MOF elimina del espacio de nombres actual.

*\[ La \]* marca debe ser uno de los argumentos siguientes.



| Marca   | Descripción                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| no superada   | Hace que el compilador MOF se cierre con un mensaje de error si la clase aún no existe en el repositorio. |
| nofail | Hace que el compilador MOF continúe incluso si la clase aún no existe.                                |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




