---
title: 'fase: PS'
description: La instrucción de fase marca la transición entre la fase 1 y la fase 2. Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si se tratase de un sombreador de fase 2.
ms.assetid: e0e89425-dc8e-489f-a0d1-3eefbfd09178
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e9a16b01e186de5645ffe65e003ebbe6defca2d5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077121"
---
# <a name="phase---ps"></a>fase: PS

La instrucción de fase marca la transición entre la fase 1 y la fase 2. Si no hay ninguna instrucción de fase, todo el sombreador se ejecuta como si se tratase de un sombreador de fase 2.

Esta instrucción solo se aplica a la versión \_ 4.

## <a name="syntax"></a>Sintaxis


```
phase
```



## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| phase                 |      |      |      | x    |      |      |       |      |       |



 

Las instrucciones del sombreador que se producen antes de la instrucción de la fase son instrucciones de la fase 1. Todas las demás instrucciones son instrucciones de la fase 2. Si hay dos fases para las instrucciones, se aumenta el número máximo de instrucciones por sombreador.

El efecto secundario desafortunado de la transición de fase es que el componente alfa de los [registros temporales](dx9-graphics-reference-asm-ps-registers-ps-1-x.md) no se mantiene en la transición. En otras palabras, el componente alfa se debe reinicializar después de la instrucción de fase.

## <a name="example"></a>Ejemplo

En este ejemplo se muestra cómo agrupar instrucciones como instrucciones de fase 1 o fase 2 en un sombreador.

La instrucción de fase también se denomina normalmente el marcador de fase porque marca la transición entre las instrucciones de las fases 1 y 2. En un \_ sombreador de 4 píxeles de la versión 1, si el marcador de fase no está presente, el sombreador se ejecuta como si se estuviera ejecutando en la fase 2. Esto es importante porque existen diferencias entre las instrucciones de las fases 1 y 2 y se registra la disponibilidad. Las diferencias se indican en la sección de referencia.


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

 

 




