---
title: CHARACTERISTICS, instrucción
description: Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos.
ms.assetid: 07834b02-a36e-40cc-8907-bff6631842f3
keywords:
- Menús de instrucción CHARACTERISTICS y otros recursos
topic_type:
- apiref
api_name:
- CHARACTERISTICS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de681785fa2ec815b1edbdda913dd8032f8feb8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359725"
---
# <a name="characteristics-statement"></a>CHARACTERISTICS, instrucción

Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos. El valor **DWORD** especificado aparece con el recurso en el archivo .res compilado. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene ninguna importancia para el sistema.

La **instrucción CHARACTERISTICS** aparece antes del principio del cuerpo de una definición de recurso [**ACCELERATORS**](accelerators-resource.md), [**DIALOG,**](dialog-resource.md) [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE.**](stringtable-resource.md) El valor especificado solo se aplica a ese recurso.

``` syntax
CHARACTERISTICS dword
```

<dl> <dt>

<span id="dword"></span><span id="DWORD"></span>*Dword*
</dt> <dd>

Valor **DWORD** definido por el usuario.

</dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**DIÁLOGO**](dialog-resource.md)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**MENÚ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




