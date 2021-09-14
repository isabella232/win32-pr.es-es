---
description: Los recursos de textura se implementan en la interfaz IDirect3DTexture9. Para obtener un puntero a una interfaz de textura, llame al método IDirect3DDevice9::CreateTexture o a cualquiera de las siguientes funciones D3DX.
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Recursos de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358864"
---
# <a name="texture-resources-direct3d-9"></a>Recursos de textura (Direct3D 9)

Los recursos de textura se implementan en la [**interfaz IDirect3DTexture9.**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) Para obtener un puntero a una interfaz de textura, llame al método [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o a cualquiera de las siguientes funciones D3DX.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

En el ejemplo de código siguiente se [**usa D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) para cargar una textura desde Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



El primer parámetro que [**acepta D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) es un puntero a una [**interfaz IDirect3DDevice9.**](/windows/desktop/api) El segundo parámetro indica a Direct3D el nombre del archivo desde el que se va a cargar la textura. El tercer parámetro toma la dirección de un puntero a una [**interfaz IDirect3DTexture9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) que representa el objeto de textura creado.

## <a name="rendering-with-texture-resources"></a>Representación con recursos de textura

Direct3D admite la mezcla de varias texturas a través del concepto de fases de textura. Cada fase de textura contiene una textura y operaciones que se pueden realizar en la textura. Las texturas de las fases de textura forman el conjunto de texturas actuales. Para obtener más información, vea [Mezcla de texturas (Direct3D 9).](texture-blending.md) El estado de cada textura se encapsula en su fase de textura.

En una aplicación de C++, el estado de cada textura debe establecerse con el [**método IDirect3DDevice9::SetTextureStageState.**](/windows/desktop/api) Pase el número de fase (0-7) como valor del primer parámetro. Establezca el valor del segundo parámetro en un miembro del tipo enumerado [**D3DTEXTURESTAGESTATETYPE.**](./d3dtexturestagestatetype.md) El parámetro final es el valor de estado para el estado de textura determinado.

Mediante punteros de interfaz de textura, la aplicación puede representar una mezcla de hasta ocho texturas. Establezca las texturas actuales invocando el [**método IDirect3DDevice9::SetTexture.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) Direct3D combina todas las texturas actuales con las primitivas que representa.

> [!Note]  
> El [**método IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa el recuento de referencias de la superficie de textura que se está asignando. Cuando la textura ya no sea necesaria, debe establecer la textura en la fase adecuada en **NULL.** Si no lo hace, la superficie no se liberará, lo que provocará una pérdida de memoria.

 

La aplicación puede establecer el estado de ajuste de textura para las texturas actuales llamando al [**método IDirect3DDevice9::SetRenderState.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) Pase un valor de D3DRS WRAP0 a D3DRS WRAP7 como valor del primer parámetro y use una combinación de las marcas \_ \_ D3DWRAPCOORD \_ 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD 2 y \_ D3DWRAPCOORD \_ 3 para habilitar el ajuste en las direcciones u, v o w.

La aplicación también puede establecer los estados de filtrado de textura y perspectiva de textura. Vea [Filtrado de texturas (Direct3D 9).](texture-filtering.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
