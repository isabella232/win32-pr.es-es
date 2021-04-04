---
title: Instrucción CHARACTERISTICS
description: Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menús de instrucciones de características y otros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076728"
---
# <a name="characteristics-statement"></a>Instrucción CHARACTERISTICS

Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos. El valor **DWORD** especificado aparece con el recurso en el archivo. res compilado. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene importancia para el sistema.

La instrucción **Characteristics** aparece antes del principio del cuerpo de un [**acelerador**](accelerators-resource.md), [**cuadro de diálogo**](dialog-resource.md), [**menú**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o definición de recursos [**stringtable**](stringtable-resource.md) . El valor especificado se aplica solo a ese recurso.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*DWORD*
</dt> <dd>

Valor **DWORD** definido por el usuario.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




