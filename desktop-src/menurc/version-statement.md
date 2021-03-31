---
title: VERSION (instrucción)
description: Define la información de versión de un recurso que pueden usar las herramientas que leen y escriben archivos de recursos.
ms.assetid: 3a33cff3-b8b3-43f4-b43a-ff1d1728cdc1
keywords:
- Menús de instrucciones de versión y otros recursos
topic_type:
- apiref
api_name:
- VERSION
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 302ffcee38b287afff2697b9c5a5241fa406b55c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784048"
---
# <a name="version-statement"></a>VERSION (instrucción)

Define la información de versión de un recurso que pueden usar las herramientas que leen y escriben archivos de recursos. El valor *DWORD* especificado aparece con el recurso en el compilado. Archivo RES. Sin embargo, el valor no se almacena en el archivo ejecutable y no tiene importancia para el sistema.

La instrucción de la **versión** aparece antes del principio del cuerpo de una definición de recursos [**Accelerators**](accelerators-resource.md), [**DIALOGEX**](dialogex-resource.md), [**Menu**](menu-resource.md), [**RCDATA**](rcdata-resource.md)o [**stringtable**](stringtable-resource.md) . El valor especificado se aplica solo a ese recurso.

``` syntax
VERSION dword
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

[**SUS**](characteristics-statement.md)
</dt> <dt>

[**MÓDULO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**STRINGTABLE**](stringtable-resource.md)
</dt> </dl>

 

 




