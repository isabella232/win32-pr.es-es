---
description: Se usa en un objeto de malla para especificar qué material se aplica a qué caras. El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican qué material se va a aplicar.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: MeshMaterialList
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ef1d200e5f6a6913f996c186e121a8390de01e8f3347b6dcbaeac8eeefa708
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798791"
---
# <a name="meshmateriallist"></a>MeshMaterialList

Se usa en un objeto de malla para especificar qué material se aplica a qué caras. El miembro nMaterials especifica cuántos materiales están presentes y los materiales especifican qué material se va a aplicar.

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

-   nMateriales: DWORD. Número de materiales.
-   nFaceIndexes: DWORD. Número de índices.
-   faceIndexes \[ nFaceIndexes: \] matriz de DWORD que contiene los índices faciales.

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



