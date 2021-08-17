---
title: 'fase: ps'
description: La instrucción de fase marca la transición entre la fase 1 y la fase 2. Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si fuera un sombreador de fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aac29792274a36ad4bb7266ffa02d0ea5d2bb1b6cec8efe2db213e9b0dd4890b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118088698"
---
# <a name="phase---ps"></a>fase: ps

La instrucción de fase marca la transición entre la fase 1 y la fase 2. Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si fuera un sombreador de fase 2.

Esta instrucción solo se aplica a la versión \_ 1 4.

## <a name="syntax"></a>Sintaxis


```
phase
```



## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| phase                 |      |      |      | x    |      |      |       |      |       |



 

Las instrucciones del sombreador que se producen antes de la instrucción de fase son instrucciones de la fase 1. Todas las demás instrucciones son instrucciones de la fase 2. Al tener dos fases para las instrucciones, se aumenta el número máximo de instrucciones por sombreador.

El efecto secundario de la transición de fase [](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) es que el componente alfa de los registros temporales no persiste durante la transición. En otras palabras, el componente alfa debe reinicializarse después de la instrucción de fase.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo agrupar instrucciones como instrucciones de fase 1 o fase 2 dentro de un sombreador.

La instrucción de fase también se denomina normalmente marcador de fase porque marca la transición entre las instrucciones de fase 1 y 2. En un sombreador de 4 píxeles de la versión 1, si el marcador de fase no está presente, el sombreador se ejecuta como si se \_ ejecutase en la fase 2. Esto es importante porque hay diferencias entre las instrucciones de las fases 1 y 2 y registrar la disponibilidad. Las diferencias se observan en toda la sección de referencia.


```
ps_1_4
  // Add phase 1 instructions here

phase
  // Add phase 2 instructions here
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




