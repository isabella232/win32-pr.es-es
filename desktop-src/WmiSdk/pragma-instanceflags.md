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
ms.openlocfilehash: 107325b329fcc51f474dd3ac9ea3a16e8882ff55114012d87a303ac73647bb37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817991"
---
# <a name="pragma-instanceflags"></a>pragma instanceflags

El **comando pragma instanceflags** preprocessor controla la forma en que se crean o actualizan las instancias en función de las marcas especificadas.

A continuación se describe la sintaxis:


```mof
#pragma instanceflags ([Flag])
```



*\[ La \]* marca debe ser uno de los argumentos siguientes.



| Marca       | Descripción                                                                                                |
|------------|------------------------------------------------------------------------------------------------------------|
| createonly | Impide que el compilador cambie las instancias existentes en el archivo MOF.                                |
| updateonly | Impide que el compilador cree nuevas instancias si no existe una instancia especificada en el archivo MOF. |



 

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo usar este comando.


```mof
#pragma instanceflags("createonly")
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Comandos de preprocesador](preprocessor-commands.md)
</dt> </dl>

 

 




