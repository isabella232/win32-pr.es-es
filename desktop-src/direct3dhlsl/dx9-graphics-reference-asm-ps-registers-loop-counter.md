---
title: Registro de contador de bucles (referencia de HLSL PS)
description: Obtenga información sobre el registro del contador de bucles para sombreadores de píxeles. El único registro de este banco es el registro del contador de bucles (aL) actual.
ms.assetid: 36999873-a251-4939-aac0-faa7f910bc33
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a2f7f42c83308fa72ceae2875c35c600dfd7db
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405518"
---
# <a name="loop-counter-register-hlsl-ps-reference"></a>Registro de contador de bucles (referencia de HLSL PS)

El único registro de este banco es el registro del contador de bucles (aL) actual. Se incrementa automáticamente en cada ejecución del [bucle - ps](loop---ps.md) / [endloop - ps](endloop---ps.md) block. Por lo tanto, se puede usar en el bloque para el direccionamiento relativo si es necesario y no es válido usarlo fuera del bucle.



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de contador de bucles |      |      |      |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registros](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




