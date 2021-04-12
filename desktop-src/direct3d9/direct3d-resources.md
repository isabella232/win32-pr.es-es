---
description: Los recursos son las texturas y los búferes que se usan para representar una escena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Recursos de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7745318db3d880711ee962edb086996764455ec8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152328"
---
# <a name="direct3d-resources-direct3d-9"></a>Recursos de Direct3D (Direct3D 9)

Los recursos son las texturas y los búferes que se usan para representar una escena. Las aplicaciones necesitan crear, cargar, copiar y usar recursos. En esta sección se proporciona una breve introducción a los recursos y los pasos y métodos que usan las aplicaciones al trabajar con recursos.

Todos los recursos, incluidos los recursos de Geometry [**IDirect3DIndexBuffer9**](/windows/desktop/api) y [**IDirect3DVertexBuffer9**](/windows/desktop/api), se heredan de la interfaz [**IDirect3DResource9**](/windows/desktop/api) . Los recursos de textura, [**IDirect3DCubeTexture9**](/windows/desktop/api), [**IDirect3DTexture9**](/windows/desktop/api)y [**IDirect3DVolumeTexture9**](/windows/desktop/api), también heredan de la interfaz [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9) .

-   [Propiedades de recursos (Direct3D 9)](resource-properties.md)
-   [Manipular recursos (Direct3D 9)](manipulating-resources.md)
-   [Bloquear recursos (Direct3D 9)](locking-resources.md)
-   [Relaciones de recursos (Direct3D 9)](resource-relationships.md)
-   [Administrar recursos (Direct3D 9)](managing-resources.md)
-   [Recursos administrados por la aplicación y estrategias de asignación (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Búferes de índice (Direct3D 9)](index-buffers.md)
-   [Búferes de vértices (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
