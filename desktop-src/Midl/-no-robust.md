---
title: modificador/no_robust
description: El \_ conmutador/no robusto indica al compilador de MIDL que debe deshabilitar explícitamente la característica de línea de comandos de/ROBUST. El modificador de la línea de comandos de/ROBUST y sus características asociadas son la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust modificador MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784307"
---
# <a name="no_robust-switch"></a>\_cambio sólido de/no

El conmutador **/no \_ robusto** indica al compilador de MIDL que debe deshabilitar explícitamente la característica de línea de comandos de [**/Robust**](-robust.md) . El modificador de la línea de comandos de **/Robust** y sus características asociadas son la configuración predeterminada del compilador para MIDL versión 6.0.359 y versiones posteriores.

``` syntax
midl /no_robust
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Con la versión 6.0.359 de MIDL y versiones posteriores, el compilador MIDL establece [**/Robust**](-robust.md) de forma predeterminada. El modificador de línea de comandos de **/no \_ Robust** se debe usar para deshabilitar la característica de **/Robust** si los códigos auxiliares generados deben ejecutarse en Microsoft Windows NT, Windows 95/98 o Windows me.

## <a name="examples"></a>Ejemplos

**MIDL/no \_ Robust FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Robust**](-robust.md)
</dt> </dl>

 

 




