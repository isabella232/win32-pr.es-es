---
description: Define las normales para una malla.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274735"
---
# <a name="meshnormals"></a>MeshNormals

Define las normales para una malla. La primera matriz de vectores son los vectores normales y la segunda matriz es una matriz de índices que especifican qué normales se deben aplicar a una cara determinada. El valor del miembro nFaceNormals debe ser igual al número de caras de una malla.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Donde:

-   nNormals: número de normales.
-   Vector de matriz normaliza \[ nNormals \] : matriz de normales. Consulte [**Vector**](vector.md).
-   nFaceNormals: número de normales de caras.
-   array MeshFace faceNormals \[ nFaceNormals \] : matriz de normales de cara de malla. Vea [**MeshFace**](meshface.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



