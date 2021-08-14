---
description: El formato de archivo X hace referencia a los archivos con la extensión de nombre de archivo .x.
ms.assetid: 06b3dcb3-03fc-4d99-b8c3-32f56d8bf49e
title: Archivos X (heredados) (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7134decc9dc9de9b5610089a88a2c88b8b2fc58d238cd55c4e34db6ef594ed0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118518732"
---
# <a name="x-files-legacy-direct3d-9"></a>Archivos X (heredados) (Direct3D 9)

El formato de archivo X hace referencia a los archivos con la extensión de nombre de archivo .x. Los archivos X se introdujeron con DirectX 2.0. Posteriormente se publicó una versión binaria de este formato con DirectX 3.0, que también se describe en esta documentación. DirectX 6.0 introdujo interfaces y métodos que permiten leer y escribir en archivos .x.

Los archivos X proporcionan un formato controlado por plantillas que permite el almacenamiento de mallas, texturas, animaciones y objetos definibles por el usuario. La compatibilidad con conjuntos de animaciones permite almacenar rutas de acceso predefinidas para la reproducción en tiempo real. También se admiten la creación de instancias y jerarquías. La creación de instancias habilita varias referencias a un objeto, como una malla, mientras almacena sus datos una sola vez por archivo. Las jerarquías se usan para expresar relaciones entre registros de datos.

El formato de archivo .x proporciona primitivas de datos de bajo nivel en las que las aplicaciones definen primitivas de nivel superior a través de plantillas.

Los modelos tridimensionales creados en las aplicaciones Maya de 3ds max o Alias Wavefront se pueden convertir en archivos .x con las extensiones de DirectX para \| Alias Maya.

En esta sección se describe la estructura de los archivos .x y cómo usarlos en las aplicaciones. La información se divide en los temas siguientes.

-   [Cargar un archivo X (heredado) (Direct3D 9)](loading-an-x-file--legacy-.md)
-   [Guardar en un archivo X (heredado) (Direct3D 9)](saving-to-an-x-file--legacy-.md)
-   [Definir un cubo simple (Direct3D 9)](defining-a-simple-cube.md)
-   [Agregar texturas (Direct3D 9)](adding-textures.md)
-   [Agregar fotogramas y animaciones (Direct3D 9)](adding-frames-and-animations.md)

Para obtener más información sobre el formato de archivo .x, vea [X File Reference](dx9-graphics-reference-d3dx-x-file.md).

Para obtener más información sobre la API de archivo .x, vea [X File Reference (Legacy) [Referencia de archivo X (heredado)].](dx9-graphics-reference-x-file.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 



