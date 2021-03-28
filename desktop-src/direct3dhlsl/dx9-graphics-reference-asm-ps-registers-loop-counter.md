---
title: Registro de contadores de bucle (referencia de PS de HLSL)
description: El único registro de este banco es el registro del contador de bucle actual (aL).
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 47582552b7e32ede7cd83637cbc3900494dfd611
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "103785075"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro de contadores de bucle (referencia de PS de HLSL)

El único registro de este banco es el registro del contador de bucle actual (aL). Se incrementa automáticamente en cada ejecución del bloque [Loop-PS](loop---ps.md) / [ENDLOOP-PS](endloop---ps.md) . Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido para usarlo fuera del bucle.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de contador de bucle |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registra](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




