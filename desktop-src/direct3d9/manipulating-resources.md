---
description: La aplicación manipula los recursos para representar una escena.
ms.assetid: 4f0eea7d-b1e4-4d53-a136-f40df7a0fbb1
title: Manipulación de recursos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a0a9cf2ee85b2f8e86077eb525acffb914e60cba84082c9d610e10da9f5fa02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069055"
---
# <a name="manipulating-resources-direct3d-9"></a>Manipulación de recursos (Direct3D 9)

La aplicación manipula los recursos para representar una escena. En primer lugar, una aplicación debe crear un recurso de textura con uno de los métodos siguientes:

-   [**IDirect3DDevice9::CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)

En su lugar, se puede crear un recurso de textura con una de las funciones de texturing D3DXCreatexxx.

Los objetos de textura devueltos por los métodos de creación de textura son contenedores para superficies o volúmenes; Estos contenedores se conocen genéricamente como búferes. Los búferes que pertenecen al recurso heredan los usos, el formato y el grupo del recurso, pero tienen su propio tipo. Para obtener más información, [vea Propiedades de recursos (Direct3D 9).](resource-properties.md)

La aplicación obtiene acceso a las superficies contenidas, con el fin de cargar ilustraciones, llamando a los métodos siguientes. Para más información, consulte [Bloqueo de recursos (Direct3D 9).](locking-resources.md)

-   [**IDirect3DCubeTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
-   [**IDirect3DTexture9::LockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-lockrect)
-   [**IDirect3DVolumeTexture9::LockBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-lockbox)

Los métodos de bloqueo toman argumentos que indican la superficie contenida (por ejemplo, el subespacio mipmap o la cara del cubo de la textura) y devuelven punteros a los píxeles. La aplicación típica nunca usa un objeto de superficie directamente.

Cree recursos orientados a geometría llamando a [**IDirect3DDevice9::CreateIndexBuffer**](/windows/desktop/api) o [**IDirect3DDevice9::CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer).

Bloquee y rellene los recursos del búfer mediante una llamada a [**IDirect3DIndexBuffer9::Lock**](/windows/desktop/api) o [**IDirect3DVertexBuffer9::Lock,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock)según el recurso.

En el caso de los recursos de textura administrados, el proceso de creación de recursos finaliza aquí. En el caso de los recursos de textura no administrados, una aplicación promueve los recursos de memoria del sistema a recursos accesibles para dispositivos (para la aceleración de hardware) mediante una llamada a [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).

Para presentar imágenes que se representan a partir de recursos, la aplicación también necesita búferes de color y de galería de símbolos de profundidad. En el caso de las aplicaciones típicas, el búfer de color es propiedad de la cadena de intercambio del dispositivo, que es una colección de superficies de búfer de reserva, y se crea implícitamente con el dispositivo. Las superficies de galería de símbolos de profundidad se pueden crear implícitamente o crearse explícitamente mediante el método [**IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/desktop/api) La aplicación asocia un dispositivo y su búfer de profundidad y color a una llamada a [**IDirect3DDevice9::SetRenderTarget**](/windows/desktop/api) o [**IDirect3DDevice9::SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface).

Para obtener más información sobre cómo presentar la imagen final, consulte [Presentación de una escena (Direct3D 9).](presenting-a-scene.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos de Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
