---
title: CHARACTERISTICS (Instrucción)
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
ms.openlocfilehash: d9910a86263d14dd928fb01347dfea4fd6c796c23b4e5d42d69cdba4bc40e14c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034322"
---
# <a name="characteristics-statement"></a>CHARACTERISTICS (Instrucción)

Define información sobre un recurso que pueden usar las herramientas que leen y escriben archivos de definición de recursos. El valor **DWORD** especificado aparece con el recurso en el archivo .res compilado. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene ninguna importancia para el sistema.

La **instrucción CHARACTERISTICS** aparece antes del principio del cuerpo de una definición de recursos [**ACCELERATORS**](accelerators-resource.md), [**DIALOG,**](dialog-resource.md) [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md) [**o STRINGTABLE.**](stringtable-resource.md) El valor especificado solo se aplica a ese recurso.

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

[**Aceleradores**](accelerators-resource.md)
</dt> <dt>

[**Diálogo**](dialog-resource.md)
</dt> <dt>

[**Lengua**](language-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




