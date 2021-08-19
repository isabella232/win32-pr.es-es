---
title: Modificador /no_robust
description: El modificador /no robust dirige al compilador MIDL a deshabilitar \_ explícitamente la característica de línea de comandos /robust. El modificador de línea de comandos /robust y sus características asociadas es la configuración predeterminada del compilador para MIDL versión 6.0.359 y posteriores.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust switch MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a1078a3eec25d6b6fdf44268ae915c20e7a2a9cf0c07a29730461bd544a7a0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808860"
---
# <a name="no_robust-switch"></a>/no \_ robust switch

El **modificador /no \_ robust** dirige al compilador MIDL a deshabilitar explícitamente la característica de línea de comandos [**/robust.**](-robust.md) El modificador de línea de comandos **/robust** y sus características asociadas es la configuración predeterminada del compilador para MIDL versión 6.0.359 y posteriores.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Opciones de cambio

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Con midl versión 6.0.359 y posteriores, el compilador midl establece [**/robust**](-robust.md) de forma predeterminada. El modificador de línea de comandos **/no \_ robust** debe usarse para deshabilitar la característica **/robust** si los códigos auxiliares generados deben ejecutarse en Microsoft Windows NT, Windows 95/98 o WindowsÂ Me.

## <a name="examples"></a>Ejemplos

**midl /no \_ robust filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




