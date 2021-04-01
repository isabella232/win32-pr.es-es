---
description: Elimina una clase existente y sus instancias del repositorio.
ms.assetid: 6f96d14a-16ab-4e83-a75f-5dbf162d1692
ms.tgt_platform: multiple
title: pragma deleteclass
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
ms.openlocfilehash: 0d3b5b1fa209be7fd472a87aec25a5e590d93c5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913209"
---
# <a name="pragma-deleteclass"></a>pragma deleteclass

El comando de preprocesador **pragma deleteclass** elimina una clase existente y sus instancias del repositorio.

A continuación se describe la sintaxis:


```mof
#pragma deleteclass("ClassName", [Flag])
```



*ClassName* es el nombre de la clase que el compilador MOF elimina del espacio de nombres actual.

La *\[ marca \]* debe ser uno de los argumentos siguientes.



| Marca   | Descripción                                                                                                  |
|--------|--------------------------------------------------------------------------------------------------------------|
| no superada   | Hace que el compilador MOF salga de un mensaje de error si la clase aún no existe en el repositorio. |
| nofail | Hace que el compilador MOF continúe aunque la clase no exista todavía.                                |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando.


```mof
#pragma deleteclass("MyClass1",FAIL)
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

 

 




