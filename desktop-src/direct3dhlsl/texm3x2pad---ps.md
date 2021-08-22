---
title: texm3x2pad - ps
description: Realiza la multiplicación de la primera fila de una matriz de dos filas multiplicada. Esta instrucción debe combinarse con texm3x2tex - ps o texm3x2depth - ps. Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texasmpad.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 55943d2a62f49e6bdb45d893385f0824898d665ee4a4065c4f8c8ed75c2f8249
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485445"
---
# <a name="texm3x2pad---ps"></a>texm3x2pad - ps

Realiza la multiplicación de la primera fila de una matriz de dos filas multiplicada. Esta instrucción debe combinarse con [texm3x2tex - ps](texm3x2tex---ps.md) o [texm3x2depth - ps](texm3x2depth---ps.md). Consulte cualquiera de estas instrucciones para obtener más información sobre el uso de texasmpad.

## <a name="syntax"></a>Syntax



| tex3x2pad dst, src |
|--------------------|



 

where

-   dst es el registro de destino.
-   src es un registro de origen.

## <a name="remarks"></a>Comentarios



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2pad            | x    | x    | x    |      |      |      |       |      |       |



 

Esta instrucción no se puede usar por sí misma.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




