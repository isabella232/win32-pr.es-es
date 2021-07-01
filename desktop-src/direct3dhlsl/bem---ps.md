---
title: bem - ps
description: Aplicar una transformación de mapa de entorno de protuberancia falsa.
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129934"
---
# <a name="bem---ps"></a>bem - ps

Aplicar una transformación de mapa de entorno de protuberancia falsa.

## <a name="syntax"></a>Sintaxis



| bem dst.rg, src0, src1 |
|------------------------|



 

where

-   dst.rg dst es el registro de destino. Se debe usar la máscara de escritura del componente rojo y verde.
-   src0 es un registro de origen.
-   src1 es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Bem                   |      |      |      | x    |      |      |       |      |       |



 

Esta instrucción realiza el cálculo siguiente.


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



Reglas para usar bem:

1.  bem debe aparecer en la primera fase de un sombreador (es decir, antes de un marcador de fase).
2.  bem consume dos ranuras de instrucciones aritméticas.
3.  Solo se permite un uso de esta instrucción por sombreador.
4.  La máscara de escritura de destino debe ser .rg /.xy.
5.  Esta instrucción no se puede emitir de forma coe emitida.
6.  Aparte de la restricción de que la máscara de escritura de destino sea .rg, los modificadores de origen src0, src1 y modificadores de instrucción no están entrenados.

## <a name="instruction-information"></a>Información de instrucciones



| Requisito                         | Valor           |
|--------------------------|------------|
| Sistema operativo mínimo | Windows 98 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




