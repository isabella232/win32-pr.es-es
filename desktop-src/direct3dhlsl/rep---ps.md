---
title: REP-PS
description: 'Iniciar un representante... endrep: bloque PS.'
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6873a6aee9e31b1f28ba2755b1869cddb177306
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784924"
---
# <a name="rep---ps"></a>REP-PS

Iniciar un representante... [endrep: bloque PS](endrep---ps.md) .

## <a name="syntax"></a>Sintaxis



| REP i\# |
|---------|



 

donde i \# es un registro entero que especifica el número de repeticiones en el componente. x. Vea [registro de entero constante](dx9-graphics-reference-asm-ps-registers-constant-integer.md).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Selecc                   |      |      |      |      |      | x    | x     | x    | x     |



 

-   i \# . x especifica el número de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni reduce el valor de i \# . x.
-   i \# . YZW no se usa en el bloque REPEAT.
-   Los bloques de repetición pueden estar anidados. Vea [limitaciones del control de flujo](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Los bloques de repetición pueden estar completamente dentro \* de un bloque if o por completo. No se permite la necesidad de estar en el mismo.
-   El uso de la misma \# instrucción i para instrucciones de representación diferentes o anidadas es correcto: cada bucle se iterará en función del recuento especificado.

## <a name="example"></a>Ejemplo


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




