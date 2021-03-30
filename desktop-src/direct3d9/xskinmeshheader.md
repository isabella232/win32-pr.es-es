---
description: Se crea una instancia de esta plantilla por cada malla solo en mallas que contienen información de la piel exportada. La finalidad de esta plantilla es proporcionar información sobre la naturaleza de la información de la piel que se exportó.
ms.assetid: 95a4fa45-63d1-4931-9c91-b26807d2b043
title: XSkinMeshHeader
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306f8c183086846fca020040af00b9ccef2665cc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423052"
---
# <a name="xskinmeshheader"></a>XSkinMeshHeader

Se crea una instancia de esta plantilla por cada malla solo en mallas que contienen información de la piel exportada. La finalidad de esta plantilla es proporcionar información sobre la naturaleza de la información de la piel que se exportó.

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

-   nMaxSkinWeightsPerVertex: número máximo de transformaciones que afectan a un vértice en la malla.
-   nMaxSkinWeightsPerFace: número máximo de transformaciones únicas que afectan a los tres vértices de cualquier aspecto.
-   nBones: número de huesos que afectan a los vértices de esta malla.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



