---
title: rep - ps
description: 'Iniciar un representante... endrep: bloque ps.'
ms.assetid: vs|directx_sdk|~\rep___ps.htm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ec879ad172b5cfc615a67797dd91c1461d844444326df6485b120179f6ecb74e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853875"
---
# <a name="rep---ps"></a>rep - ps

Iniciar un representante... [endrep: bloque ps.](endrep---ps.md)

## <a name="syntax"></a>Syntax



| rep i\# |
|---------|



 

donde i \# es un registro entero que especifica el recuento de repeticiones en el componente .x. Vea [Registro de enteros constantes.](dx9-graphics-reference-asm-ps-registers-constant-integer.md)

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Representante                   |      |      |      |      |      | x    | x     | x    | x     |



 

-   i \# .x especifica el recuento de iteraciones. El intervalo legal es \[ 0, 255 \] . Tenga en cuenta que esta instrucción no incrementa ni disminuye el valor de i \# .x.
-   El bloque repeat no usa i \# .yzw.
-   Los bloques de repetición pueden estar anidados. Vea [Flow control de datos](dx9-graphics-reference-asm-ps-instructions-flow-control.md).
-   Los bloques de repetición pueden estar completamente dentro de un bloque if \* o rodeando por completo. No se permite ningún estrango.
-   El uso de la misma i para instrucciones de representantes diferentes o anidadas es \# perfecto: cada bucle iterará en función del recuento especificado.

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

 

 




