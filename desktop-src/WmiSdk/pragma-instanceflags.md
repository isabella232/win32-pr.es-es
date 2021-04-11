---
description: Controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.
ms.assetid: 9932edf2-2e5f-4c5e-9889-f2be4af11bf2
ms.tgt_platform: multiple
title: pragma instanceflags
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
ms.openlocfilehash: acc05e201fcf153ab2156d4a360ce36b4539cd57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279120"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

El comando de preprocesador **pragma instanceflags** controla la manera en que se crean o actualizan las instancias en función de las marcas especificadas.

A continuación se describe la sintaxis:


```mof
#pragma instanceflags ([Flag])
```



La *\[ marca \]* debe ser uno de los argumentos siguientes.



| Marca       | Descripción                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| createonly | Impide que el compilador cambie cualquier instancia existente en el archivo MOF.                                |
| updateonly | Impide que el compilador cree nuevas instancias si no existe una instancia especificada en el archivo MOF. |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando.


```mof
#pragma instanceflags("createonly")
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

 

 




