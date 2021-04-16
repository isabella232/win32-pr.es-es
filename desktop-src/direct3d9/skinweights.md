---
description: Se crea una instancia de esta plantilla por cada malla.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536814"
---
# <a name="skinweights"></a>SkinWeights

Se crea una instancia de esta plantilla por cada malla. Dentro de una malla, aparecerá una secuencia de n instancias de esta plantilla, donde n es el número de huesos (fotogramas de archivo X) que influyen en los vértices de la malla. Cada instancia de la plantilla define básicamente la influencia de un hueso determinado en la malla. Hay una lista de índices de vértices y una lista de pesos correspondiente.

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

Donde:

-   El nombre del hueso cuya influencia se está definiendo es transformNodeName y nWeights es el número de vértices afectados por este hueso.
-   Los vértices afectados por este hueso están contenidos en vertexIndices y las ponderaciones de cada uno de los vértices afectados por este hueso están contenidas en pesos.
-   La matriz matrixOffset transforma los vértices de la malla en el espacio del hueso. Cuando se concatena a la transformación del hueso, esto proporciona las coordenadas de espacio universal de la malla según se ve afectada por el hueso. Vea [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



