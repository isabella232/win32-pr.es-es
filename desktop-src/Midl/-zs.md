---
title: Modificador/ZS
description: El modificador/ZS indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.
ms.assetid: 5ff44607-12c3-4a2d-8a7f-2056504990e2
keywords:
- /ZS modificador MIDL
topic_type:
- apiref
api_name:
- /Zs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 469802434d54319aa55c1e409ccb8d64e942836f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103783700"
---
# <a name="zs-switch"></a>Modificador/ZS

El modificador **/ZS** indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.

``` syntax
midl /Zs
midl /syntax_check
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este modificador invalida todos los demás modificadores que especifican información acerca de los archivos de salida.

También puede especificar el modo de comprobación de sintaxis con el modificador de compilador de MIDL [**/Syntax \_ check**](-syntax-check.md).

## <a name="examples"></a>Ejemplos

**MIDL/ZS nombrearchivo. idl**

**/Syntax de MIDL \_ : Compruebe FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**comprobación de/Syntax \_**](-syntax-check.md)
</dt> </dl>

 

 




