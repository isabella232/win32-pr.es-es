---
title: modificador/syntax_check
description: El \_ modificador de comprobación/Syntax indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.
ms.assetid: 8d9139d3-6018-48a7-bea5-0c843b6273d3
keywords:
- /syntax_check modificador MIDL
topic_type:
- apiref
api_name:
- /syntax_check
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b064a096b5064e6996ea4288c9ae9d4a798c2e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784013"
---
# <a name="syntax_check-switch"></a>\_modificador de comprobación de/Syntax

El modificador de **\_ comprobación/Syntax** indica que el compilador solo comprueba la sintaxis y no genera archivos de salida.

``` syntax
midl /syntax_check
midl /Zs
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Este modificador invalida todos los demás modificadores que especifican información acerca de los archivos de salida.

También puede especificar el modo de comprobación de sintaxis con la opción del compilador de MIDL [**/ZS**](-zs.md).

## <a name="examples"></a>Ejemplos

**MIDL/ZS nombrearchivo. idl**

**/Syntax de MIDL \_ : Compruebe FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ZS**](-zs.md)
</dt> </dl>

 

 




