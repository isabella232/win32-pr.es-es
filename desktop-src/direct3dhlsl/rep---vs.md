---
title: rep- vs
description: Iniciar un representante... endrep block.
ms.assetid: vs|directx_sdk|~\rep___vs.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6e800f2ef313cd5c9a4fc90d7205502db5532ae24f51ec0f1255d05cc9a589bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853795"
---
# <a name="rep---vs"></a>rep- vs

Iniciar un representante... [endrep](endrep---vs.md) block.

## <a name="syntax"></a>Syntax



| rep i\# |
|---------|



 

donde i \# es un registro entero que especifica el recuento de repeticiones en el componente .x. Vea [Registro de enteros constantes.](dx9-graphics-reference-asm-vs-registers-constant-integer.md)

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Representante                    |      | x    | x    | x     | x    | x     |



 

-   i \# .x especifica el recuento de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .x.
-   El bloque repeat no usa i \# .yzw.
-   Los bloques de repetición pueden estar anidados. Vea [Flow límites de anidamiento de controles .](dx9-graphics-reference-asm-vs-instructions-flow-control.md)
-   Los bloques de repetición pueden estar completamente dentro de un bloque if \* o rodearse completamente. No se permite ningún estrango.
-   El uso de la misma i para instrucciones de representantes diferentes o anidadas es bueno: cada \# bucle iterará en función del recuento especificado.

## <a name="example"></a>Ejemplo


```
rep i2
    add r0, r0, c0
endrep  
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




