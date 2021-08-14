---
title: rcp - ps
description: Calcula el recíproco del escalar de origen. | rcp - ps
ms.assetid: d8dfc2b3-4404-47ec-aeaf-1adb7e7a342e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fba443d4a2e05794f8c1965e46a61c65edae50b95845f0f80faa0c0ab6c6bf71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510960"
---
# <a name="rcp---ps"></a>rcp - ps

Calcula el recíproco del escalar de origen.

## <a name="syntax"></a>Syntax



| rcp dst, src |
|--------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen. El registro de origen requiere el uso explícito de replicar swzzle, es decir, exactamente uno de los componentes .x, .y, .z, .w swzzle (o los componentes .r, .g, .b, .a equivalentes).

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| rcp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

La salida debe ser exactamente 1.0 si la entrada es exactamente 1.0. Una fuente de 0,0 produce infinito.

El resultado escalar se replica en todos los canales de la máscara de escritura de destino.

La precisión debe ser de al menos un error absoluto de 1,0/(2):2): en el intervalo (1.0, 2.0), ya que las implementaciones comunes separarán la mantisa y el exponente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




