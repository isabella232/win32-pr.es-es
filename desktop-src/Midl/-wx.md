---
title: Modificador /WX
description: El modificador /WX indica al compilador MIDL que controle todos los errores en el nivel de advertencia dado como errores.
ms.assetid: 1dd9791c-0488-4ca3-8a29-082ae03c3cd4
keywords:
- /WX switch MIDL
topic_type:
- apiref
api_name:
- /WX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5255b7256b82889f50b6bcffbc323e405f31d1423bb51a5b35b716dca170a25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913625"
---
# <a name="wx-switch"></a>Modificador /WX

El **modificador /WX** indica al compilador MIDL que controle todos los errores en el nivel de advertencia dado como errores.

``` syntax
midl /WX
```

## <a name="switch-options"></a>Cambiar opciones

Este modificador no tiene parámetros.

## <a name="remarks"></a>Comentarios

Si se especifica el modificador **/WX** y no se especifica el modificador [**/W**](-w.md)*n,* todas las advertencias en el nivel predeterminado, nivel 1, se tratan como errores.

El [**modificador /W**](-w.md)*n* dirige al compilador para que muestre todas las advertencias en el nivel *n* y **/WX** dirige al compilador para que controle todas las advertencias como errores. La combinación de estos dos modificadores dirige al compilador a controlar todas las advertencias en el nivel *n* como errores.

Los errores son diferentes de las advertencias. Los errores hacen que el compilador MIDL detenga el procesamiento del archivo IDL. Las advertencias hacen que el compilador de MIDL emita un mensaje informativo y continúe procesando el archivo IDL.

El nivel de advertencia cero (0) dirige al compilador MIDL a suprimir la información de advertencia. Cuando se **combinan los modificadores /W0** y **/WX,** el compilador midl suprime toda la información de advertencia. En este caso, el **modificador /WX** no tiene ningún efecto.

## <a name="examples"></a>Ejemplos

**midl /WX filename.idl**

**midl /W3 /WX filename.idl**

## <a name="see-also"></a>Vea también

<dl> <dt>

[Sintaxis general de la línea de comandos de MIDL](general-midl-command-line-syntax.md)
</dt> <dt>

[**/W**](-w.md)
</dt> </dl>

 

 




