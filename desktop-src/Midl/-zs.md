---
title: Modificador /Zs
description: El modificador /Zs indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /Zs switch MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f92bd2321567bbc565d3198fe5ebf5c98a3d8df440ea967409830c8e73488609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014023"
---
# <a name="zs-switch"></a>Modificador /Zs

El **modificador /Zs** indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Este modificador invalida todos los demás modificadores que especifican información sobre los archivos de salida.

También puede especificar el modo de comprobación de sintaxis con el modificador del compilador MIDL [**/syntax \_ check**](-syntax-check.md).

## <a name="examples"></a>Ejemplos

**midl /Zs filename.idl**

**midl /syntax \_ check filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/syntax \_ check**](-syntax-check.md)
</dt> </dl>

 

 




