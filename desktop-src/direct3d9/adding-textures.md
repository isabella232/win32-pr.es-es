---
description: Para agregar texturas, use la naturaleza jerárquica del formato de archivo y agregue un objeto de datos TextureFilename opcional a los objetos de datos Material.
ms.assetid: 741f4c05-49f8-4c76-be5c-ce5b496124bb
title: Agregar texturas (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c2b60ea80702ffc339fe753dec3ad9b72170b03bc8f23598e545e17bc71209d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045243"
---
# <a name="adding-textures-direct3d-9"></a>Agregar texturas (Direct3D 9)

Para agregar texturas, use la naturaleza jerárquica del formato de archivo y agregue un objeto de datos [**TextureFilename**](texturefilename.md) opcional a los objetos de datos [**Material.**](material.md) Los **objetos Material** ahora se leen de la siguiente manera:


```
Material RedMaterial {
1.000000;0.000000;0.000000;1.000000;;    // R = 1.0, G = 0.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "tex1.ppm"; }
}

Material GreenMaterial {
0.000000;1.000000;0.000000;1.000000;;     // R = 0.0, G = 1.0, B = 0.0
0.000000;
0.000000;0.000000;0.000000;;
0.000000;0.000000;0.000000;;
TextureFilename { "win95.ppm"; }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Archivos X (heredados)](x-files--legacy-.md)
</dt> </dl>

 

 



