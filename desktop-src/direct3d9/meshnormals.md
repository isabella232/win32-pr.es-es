---
description: Define las normales de una malla.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: MeshNormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02a261dd8dbd46cf26116657b983eca4f693603869a80bf2fb110c0f165221ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846465"
---
# <a name="meshnormals"></a>MeshNormals

Define las normales de una malla. La primera matriz de vectores son los propios vectores normales y la segunda matriz es una matriz de índices que especifica qué normales se deben aplicar a una cara determinada. El valor del miembro nFaceNormals debe ser igual al número de caras de una malla.

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
-   array Vector normals \[ nNormals: \] matriz de normales. Vea [**Vector**](vector.md).
-   nFaceNormals: número de normales faciales.
-   array MeshFace faceNormals \[ nFaceNormals: \] matriz de normales de cara de malla. Vea [**MeshFace**](meshface.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Templates](dx9-graphics-reference-x-file-format-templates.md) (Plantillas [C++])
</dt> </dl>

 

 



