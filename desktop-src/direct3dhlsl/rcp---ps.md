---
title: RCP-PS
description: Calcula el recíproco del escalar del origen. | RCP-PS
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2df8ad2d673d96dced84630b1a641c7e4f27ceb2
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986526"
---
# <a name="rcp---ps"></a>RCP-PS

Calcula el recíproco del escalar del origen.

## <a name="syntax"></a>Sintaxis



| RCP DST, src |
|--------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicate swizzle, es decir, se debe especificar exactamente uno de los componentes. x,. y,. z,. w swizzle (o. r,. g,. b,. a equivalentes).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

La salida debe ser exactamente 1,0 si la entrada es exactamente 1,0. Un origen de 0,0 produce infinito.

El resultado escalar se replica en todos los canales de la máscara de escritura de destino.

La precisión debe ser al menos de 1,0/(2 ² ²) error absoluto en el intervalo (1,0, 2,0) porque las implementaciones comunes separan la mantisa y el exponente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




