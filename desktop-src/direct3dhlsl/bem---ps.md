---
title: BEM-PS
description: Aplicar una transformación de mapa de entorno de rugosidad falsa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419953"
---
# <a name="bem---ps"></a>BEM-PS

Aplicar una transformación de mapa de entorno de rugosidad falsa.

## <a name="syntax"></a>Sintaxis



| BEM DST. RG, src0, SRC1 |
|------------------------|



 

, donde

-   DST. RG DST es el registro de destino. Se debe usar la máscara de escritura del componente rojo y verde.
-   src0 es un registro de origen.
-   SRC1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| bem                   |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción realiza el cálculo siguiente.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Reglas para usar BEM:

1.  BEM debe aparecer en la primera fase de un sombreador (es decir, antes de un marcador de fase).
2.  BEM consume dos ranuras de Instrucciones aritméticas.
3.  Solo se permite un uso de esta instrucción por sombreador.
4.  El writemask de destino debe ser. RG/.XY.
5.  Esta instrucción no se puede comemisión de forma conjunta.
6.  Aparte de la restricción de que la máscara de escritura de destino sea. RG, los modificadores de los modificadores de instrucción src0, SRC1 y Instruction de origen no están restringidos.

## <a name="instruction-information"></a>Información de instrucciones



|                          |            |
|--------------------------|------------|
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




