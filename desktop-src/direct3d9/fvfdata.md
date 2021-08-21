---
description: Especifica los datos de malla menos los datos de posición.
ms.assetid: 30a95ca3-84ab-475d-9654-a3853263056b
title: FVFData
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec21cf354ed10e7229f1392dd31bf32bc416c27dff90d5d70858aeefc1b5c68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987995"
---
# <a name="fvfdata"></a>FVFData

Especifica los datos de malla menos los datos de posición.

``` syntax
template FVFData
{
    < B6E70A0E-8EF9-4e83-94AD-ECC8B0C04897 >
    DWORD dwFVF;
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

Donde:

-   dwFVF: un código FVF.
-   nDWords: datos binarios. Número de DWORDS.
-   data \[ nDWords: \] matriz de DWORDS que contienen los datos de cada elemento de vértice.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



