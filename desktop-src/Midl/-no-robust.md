---
title: Modificador /no_robust
description: El modificador /no robust dirige al compilador MIDL a deshabilitar explícitamente la característica de línea de \_ comandos /robust. El modificador de línea de comandos /robust y sus características asociadas es la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.
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
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159731"
---
# <a name="no_robust-switch"></a>/no \_ robust switch

El **modificador /no \_ robust** dirige al compilador MIDL a deshabilitar explícitamente la característica de línea de comandos [**/robust.**](-robust.md) El modificador de línea de comandos **/robust** y sus características asociadas es la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Con MIDL versión 6.0.359 y posteriores, el compilador de MIDL establece [**/robust**](-robust.md) de forma predeterminada. El modificador de línea de comandos **/no \_** sólido debe usarse para deshabilitar la característica **/robust** si los códigos auxiliares generados deben ejecutarse en Microsoft Windows NT, Windows 95/98 o WindowsÂ Me.

## <a name="examples"></a>Ejemplos

**midl /no \_ robust filename.idl**

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> </dl>

 

 




