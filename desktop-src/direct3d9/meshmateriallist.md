---
description: Se usa en un objeto Mesh para especificar qué material se aplica a qué caras. El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican el material que se va a aplicar.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714667"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Se usa en un objeto Mesh para especificar qué material se aplica a qué caras. El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican el material que se va a aplicar.

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

Donde:

-   nMaterials: un valor DWORD. El número de materiales.
-   nFaceIndexes: un valor DWORD. Número de índices.
-   faceIndexes \[ nFaceIndexes \] : una matriz de DWORD que contiene los índices de caras.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



