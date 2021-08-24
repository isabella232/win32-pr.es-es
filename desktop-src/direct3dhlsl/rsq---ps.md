---
title: rsq - ps
description: Calcula la raíz cuadrada mutua (solo positiva) del escalar de origen. | rsq - ps
ms.assetid: deb1bd12-6347-4b1e-b21b-f3ef48da4c13
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 48a36715113678e199b3da22be9cdf118f385c15397a16ddd39bdd83622f76f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788705"
---
# <a name="rsq---ps"></a>rsq - ps

Calcula la raíz cuadrada mutua (solo positiva) del escalar de origen.

## <a name="syntax"></a>Syntax



| rsq dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Lrq                   |      |      |      |      | x    | x    | x     | x    | x     |



 

El valor absoluto se toma antes del procesamiento.

La precisión debe ser de al menos un error absoluto de 1,0/(2ntes): en el intervalo (1.0, 4.0), ya que las implementaciones comunes separarán la mantisa y el exponente.

La salida debe ser exactamente 1.0 si la entrada es exactamente 1.0. Una fuente de 0,0 produce infinito.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




