---
title: /WX (modificador)
description: El modificador/WX indica al compilador de MIDL que controle todos los errores en el nivel de advertencia dado como errores.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX (modificador) MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04b502cea5f686de2951f6f21ab92fdbffef779b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904153"
---
# <a name="wx-switch"></a>/WX (modificador)

El modificador **/WX** indica al compilador de MIDL que controle todos los errores en el nivel de advertencia dado como errores.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Opciones de conmutador

Este modificador no tiene parámetros.

## <a name="remarks"></a>Observaciones

Si se especifica el modificador **/WX** y no se especifica el modificador [**/w**](-w.md)*n* , todas las advertencias en el nivel predeterminado, nivel 1, se tratan como errores.

El modificador [**/w**](-w.md)*n* indica al compilador que muestre todas las advertencias en el nivel *n* y **/WX** indica al compilador que controle todas las advertencias como errores. La combinación de estos dos modificadores indica al compilador que controle todas las advertencias en el nivel *n* como errores.

Los errores son diferentes de las advertencias. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

Warning-LEVEL cero (0) indica al compilador de MIDL que debe suprimir la información de advertencia. Cuando se combinan los modificadores **/W0** y **/WX** , el compilador MIDL suprime toda la información de advertencia. En este caso, el modificador **/WX** no tiene ningún efecto.

## <a name="examples"></a>Ejemplos

**MIDL/WX FILENAME. idl**

**MIDL/W3/WX FILENAME. idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis de línea de comandos de MIDL general](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




