---
description: Define un conjunto de dos valores booleanos usados en la plantilla MeshFaceWraps para definir la topología de textura de una cara individual. Use en lugar de Boolean2d cuando las coordenadas de textura (u, v) abarcan el intervalo de 0 a 2 en lugar de 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 656c5f7d4eaad52a75cffca0189a1e6fa36e3e89714d8ee0225a3aeec21c8e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798926"
---
# <a name="materialwrap"></a>MaterialWrap

Define un conjunto de dos valores booleanos usados en la plantilla [**MeshFaceWraps**](meshfacewraps.md) para definir la topología de textura de una cara individual. Use en lugar de [**Boolean2d**](boolean2d.md) cuando las coordenadas de textura (u, v) abarcan el intervalo de 0 a 2 en lugar de 0 a 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Donde:

-   u: valor booleano. Vea [**Boolean**](boolean.md).
-   v: valor booleano. Vea [**Boolean**](boolean.md).

> [!Note]  
> Ya no se usa la plantilla [**MeshFaceWraps.**](meshfacewraps.md)

 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



