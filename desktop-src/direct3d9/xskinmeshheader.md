---
description: Solo se crea una instancia de esta plantilla por malla en mallas que contienen información de desenlazado exportada. El propósito de esta plantilla es proporcionar información sobre la naturaleza de la información de desenlazado que se exportó.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c86127e46809cd1415b191a769b25e09535405e6500e511df6248e6174888d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118796859"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Solo se crea una instancia de esta plantilla por malla en mallas que contienen información de desenlazado exportada. El propósito de esta plantilla es proporcionar información sobre la naturaleza de la información de desenlazado que se exportó.

``` syntax
template XSkinMeshHeader 
{ 
    < 3CF169CE-FF7C-44ab-93C0-F78F62D172E2 >  
    WORD nMaxSkinWeightsPerVertex; 
    WORD nMaxSkinWeightsPerFace; 
    WORD nBones; 
}
```

Donde:

-   nMaxSkinWeightsPerVertex: número máximo de transformaciones que afectan a un vértice de la malla.
-   nMaxSkinWeightsPerFace: número máximo de transformaciones únicas que afectan a los tres vértices de cualquier cara.
-   nMuts: número de ramas que afectan a los vértices de esta malla.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



