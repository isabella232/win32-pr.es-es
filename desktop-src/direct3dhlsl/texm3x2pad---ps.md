---
title: texm3x2pad-PS
description: Realiza la multiplicación de la primera fila de una matriz de dos filas. Esta instrucción debe combinarse con texm3x2tex-PS o texm3x2depth-PS. Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904294"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad-PS

Realiza la multiplicación de la primera fila de una matriz de dos filas. Esta instrucción debe combinarse con [texm3x2tex-PS](texm3x2tex---ps.md) o [texm3x2depth-PS](texm3x2depth---ps.md). Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texmpad.

## <a name="syntax"></a>Sintaxis



| tex3x2pad DST, src |
|--------------------|



 

, donde

-   DST es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción no se puede usar por sí sola.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




