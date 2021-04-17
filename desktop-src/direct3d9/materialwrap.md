---
description: Define un conjunto de dos valores booleanos que se usan en la plantilla MeshFaceWraps para definir la topología de textura de una sola persona. Use en lugar de Boolean2d cuando las coordenadas de textura (u, v) abarquen el intervalo de 0 a 2 en lugar de 0 a 1.
ms.assetid: 0d1755fc-66cb-4372-b9d0-fb320c55d6a7
title: MaterialWrap
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6797719919a4f52421751a5cad008aa8a581089a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714690"
---
# <a name="materialwrap"></a>MaterialWrap

Define un conjunto de dos valores booleanos que se usan en la plantilla [**MeshFaceWraps**](meshfacewraps.md) para definir la topología de textura de una sola persona. Use en lugar de [**Boolean2d**](boolean2d.md) cuando las coordenadas de textura (u, v) abarquen el intervalo de 0 a 2 en lugar de 0 a 1.

``` syntax
template MaterialWrap
{
    < 4885ae60-78e8-11cf-8f52-0040333594a3 >
    Boolean u;
    Boolean v;
} 
```

Donde:

-   valor u-booleano. Vea [**Boolean**](boolean.md).
-   valor booleano v. Vea [**Boolean**](boolean.md).

> [!Note]  
> Ya no se usa la plantilla [**MeshFaceWraps**](meshfacewraps.md) .

 

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



