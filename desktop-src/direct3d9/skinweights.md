---
description: Se crea una instancia de esta plantilla por malla.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: SkinWeights
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bb76b1c0860e64f2e1e8b42cb7ed4d2af984cc043425b97e03cf997714d0e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627915"
---
# <a name="skinweights"></a>SkinWeights

Se crea una instancia de esta plantilla por malla. Dentro de una malla, aparecerá una secuencia de n instancias de esta plantilla, donde n es el número de ramas (X marcos de archivo) que influyen en los vértices de la malla. Cada instancia de la plantilla define básicamente la influencia de un póreo determinado en la malla. Hay una lista de índices de vértices y una lista correspondiente de pesos.

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

-   El nombre del pórtico cuya influencia se está definindo es transformNodeName y nWeights es el número de vértices afectados por este pórtico.
-   Los vértices influenciados por este pórtico están contenidos en vérticesIndices, y los pesos de cada uno de los vértices influenciados por este pórtico están contenidos en pesos.
-   La matriz matrixOffset transforma los vértices de malla en el espacio del pórtico. Cuando se concatena a la transformación del tejido, proporciona las coordenadas del espacio mundial de la malla afectadas por el póreo. Vea [**Matrix4x4**](matrix4x4.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



