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
ms.openlocfilehash: 10d4c735f1e59533b57ae1814cfb8e36b2c1ad76
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082279"
---
# <a name="pragma-deleteinstance"></a>pragma deleteinstance

El comando **pragma deleteinstance** elimina una instancia existente de una clase del repositorio.

A continuación se describe la sintaxis de este comando:


```mof
#pragma deleteinstance("InstanceId", [Flag])
```



*InstanceID* es un identificador único de la instancia que el compilador MOF elimina del espacio de nombres actual.

La *\[ marca \]* debe ser uno de los argumentos siguientes.



| Marca   | Descripción                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| no superada   | Hace que el compilador MOF salga de un mensaje de error si la clase aún no existe en el repositorio. |
| nofail | Hace que el compilador MOF continúe aunque la clase no exista todavía.                                |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando.


```mof
#pragma deleteinstance(
    "MSFT_RisingFallingTemplate.id='TestRisingFallingCorrId'",
    nofail)
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

 

 




