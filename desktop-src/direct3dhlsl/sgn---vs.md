---
title: sgn- vs
description: Calcula el signo de la entrada.
ms.assetid: b03530d1-c621-483e-bd94-31abafeb2e6e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8573ff7e33a127d7c30af1fe512fbd3da298d0eb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573677"
---
# <a name="sgn---vs"></a>sgn- vs

Calcula el signo de la entrada.

## <a name="syntax"></a>Sintaxis



| sgn dst, src0, src1, src2 |
|---------------------------|



 

, donde

-   dst es el registro de destino.
-   src0 es un registro de origen.
-   src1 es un registro temporal que contiene resultados intermedios. Después de la ejecución, el contenido no está definido.
-   src2 es un registro temporal que contiene resultados intermedios. Después de la ejecución, el contenido no está definido.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Sgn                    |      | x    | x    | x     | x    | x     |



 

Esta instrucción funciona como se muestra a continuación.


```
for each component in src0
{
   if (src0.component < 0) 
       dest.component = -1; 
   else
       if (src0.component == 0) 
           dest.component = 0; 
       else 
           dest.component = 1;
}
```



src1 y src2 deben ser registros [temporales diferentes.](dx9-graphics-reference-asm-vs-registers-temporary.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




