---
description: Los recursos son las texturas y búferes que se usan para representar una escena.
ms.assetid: 815a330c-9fd2-45ff-b7df-192fc197074f
title: Recursos de Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8acc40cc929f5cedbefaa0b652c67ea59e35212e4da81c4278e3a57f48ea7662
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523784"
---
# <a name="direct3d-resources-direct3d-9"></a>Recursos de Direct3D (Direct3D 9)

Los recursos son las texturas y búferes que se usan para representar una escena. Las aplicaciones deben crear, cargar, copiar y usar recursos. En esta sección se proporciona una breve introducción a los recursos y los pasos y métodos que usan las aplicaciones al trabajar con recursos.

Todos los recursos, incluidos los recursos de geometría [**IDirect3DIndexBuffer9**](/windows/desktop/api) [**e IDirect3DVertexBuffer9,**](/windows/desktop/api)heredan de la [**interfaz IDirect3DResource9.**](/windows/desktop/api) Los recursos de textura, [**IDirect3DCubeTexture9,**](/windows/desktop/api) [**IDirect3DTexture9**](/windows/desktop/api)e [**IDirect3DVolumeTexture9,**](/windows/desktop/api)también heredan de la interfaz [**IDirect3DBaseTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)

-   [Propiedades del recurso (Direct3D 9)](resource-properties.md)
-   [Manipulación de recursos (Direct3D 9)](manipulating-resources.md)
-   [Bloqueo de recursos (Direct3D 9)](locking-resources.md)
-   [Relaciones de recursos (Direct3D 9)](resource-relationships.md)
-   [Administración de recursos (Direct3D 9)](managing-resources.md)
-   [Recursos administrados por la aplicación y estrategias de asignación (Direct3D 9)](application-managed-resources-and-allocation-strategies.md)

<!-- -->

-   [Búferes de índice (Direct3D 9)](index-buffers.md)
-   [Búferes de vértices (Direct3D 9)](vertex-buffers.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Introducción](getting-started.md)
</dt> </dl>

 

 
