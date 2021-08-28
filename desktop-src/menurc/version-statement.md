---
title: Version (instrucción)
description: Define información de versión sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menús de instrucción VERSION y otros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c95f2af63d5c7bdb499d371892d0c2fa6ddb875fda5daf5b19fd0d188a478fa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776665"
---
# <a name="version-statement"></a>Version (instrucción)

Define información de versión sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. El valor *dword* especificado aparece con el recurso en el objeto compilado. Archivo RES. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene ninguna importancia para el sistema.

La **instrucción VERSION** aparece antes del principio del cuerpo de una definición de recursos [**ACCELERATORS,**](accelerators-resource.md) [**DIALOGEX,**](dialogex-resource.md) [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE.**](stringtable-resource.md) El valor especificado solo se aplica a ese recurso.

``` syntax
VERSION dword
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

[**Características**](characteristics-statement.md)
</dt> <dt>

[**Lengua**](language-statement.md)
</dt> <dt>

[**Menú**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




