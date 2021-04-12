---
description: Un primitivo 3D es una colección de vértices que forman una única entidad 3D. El primitivo más sencillo es una colección de puntos en un sistema de coordenadas 3D, que se denomina lista de puntos.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitivas (gráficos de Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104151973"
---
# <a name="primitives-direct3d-9-graphics"></a>Primitivas (gráficos de Direct3D 9)

Un primitivo 3D es una colección de vértices que forman una única entidad 3D. El primitivo más sencillo es una colección de puntos en un sistema de coordenadas 3D, que se denomina lista de puntos.

A menudo, las primitivas 3D son polígonos. Un polígono es una ilustración en 3D cerrada delimitada por al menos tres vértices. El polígono más sencillo es un triángulo. Microsoft Direct3D usa triángulos para componer la mayoría de sus polígonos, ya que se garantiza que los tres vértices de un triángulo son coplanares. La representación de vértices no planos es ineficaz. Puede combinar triángulos para formar polígonos y mallas grandes y complejos.

En la ilustración siguiente se muestra un cubo. Dos triángulos forman cada una de las caras del cubo. El conjunto completo de triángulos forma un primitivo cúbico. Puede aplicar texturas y materiales a las superficies de primitivas para que parezcan una única forma sólida. Para obtener más información, vea [materiales (Direct3D 9)](materials.md) y [texturas de Direct3D (Direct3D 9)](direct3d-textures.md).

![Ilustración de un cubo con dos triángulos en cada superficie](images/cube3d.png)

También puede utilizar triángulos para crear primitivas cuyas superficies parezcan curvas suaves. En la ilustración siguiente se muestra cómo se puede simular una esfera con triángulos. Una vez aplicado un material, la esfera tiene un aspecto curvo cuando se representa. Esto es especialmente cierto si usa el sombreado Gouraud. Para obtener más información, vea [sombreado Gouraud](shading-modes.md).

![Ilustración de una esfera que se simula mediante triángulos](images/sphere3d.png)

Los dispositivos Direct3D pueden crear y manipular los siguientes tipos de primitivas.

-   [Listas de puntos](point-lists.md)
-   [Listas de líneas](line-lists.md)
-   [Bandas de líneas](line-strips.md)
-   [Listas de triángulos](triangle-lists.md)
-   [Bandas de triángulo](triangle-strips.md)
-   [Ventiladores de triángulo (Direct3D 9)](triangle-fans.md)

Puede representar tipos primitivos desde una aplicación de C++ con cualquiera de los métodos de representación de la interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
