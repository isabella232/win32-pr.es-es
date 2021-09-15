---
title: Version (instrucción)
description: Define la información de versión sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.
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
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468544"
---
# <a name="version-statement"></a>Version (instrucción)

Define la información de versión sobre un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. El valor *dword* especificado aparece con el recurso en el compilado. Archivo RES. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene ninguna importancia para el sistema.

La **instrucción VERSION** aparece antes del principio del cuerpo de una definición de recursos [**ACCELERATORS**](accelerators-resource.md), [**DIALOGEX,**](dialogex-resource.md) [**MENU,**](menu-resource.md) [**RCDATA**](rcdata-resource.md)o [**STRINGTABLE.**](stringtable-resource.md) El valor especificado solo se aplica a ese recurso.

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

[**ACELERADORES**](accelerators-resource.md)
</dt> <dt>

[**CARACTERÍSTICAS**](characteristics-statement.md)
</dt> <dt>

[**LENGUA**](language-statement.md)
</dt> <dt>

[**MENÚ**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




