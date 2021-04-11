---
description: 'Los recursos de textura se implementan en la interfaz IDirect3DTexture9. Para obtener un puntero a una interfaz de textura, llame al método IDirect3DDevice9:: CreateTexture o a cualquiera de las siguientes funciones de D3DX.'
ms.assetid: vs|directx_sdk|~\texture_resources.htm
title: Recursos de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14134ca53b7735426e3f01340308282858da5516
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104274781"
---
# <a name="texture-resources-direct3d-9"></a>Recursos de textura (Direct3D 9)

Los recursos de textura se implementan en la interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) . Para obtener un puntero a una interfaz de textura, llame al método [**IDirect3DDevice9:: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) o a cualquiera de las siguientes funciones de D3DX.

-   [**D3DXCreateTexture**](d3dxcreatetexture.md)
-   [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md)
-   [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md)
-   [**D3DXCreateTextureFromFileInMemory**](d3dxcreatetexturefromfileinmemory.md)
-   [**D3DXCreateTextureFromFileInMemoryEx**](d3dxcreatetexturefromfileinmemoryex.md)
-   [**D3DXCreateTextureFromResource**](d3dxcreatetexturefromresource.md)
-   [**D3DXCreateTextureFromResourceEx**](d3dxcreatetexturefromresourceex.md)

En el ejemplo de código siguiente se usa [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) para cargar una textura desde Tiger.bmp.


```
// The following code example assumes that D3dDevice
// is a valid pointer to an IDirect3DDevice9 interface.

LPDIRECT3DTEXTURE9 pTexture;

D3DXCreateTextureFromFile( d3dDevice, "tiger.bmp", &pTexture);
```



El primer parámetro que [**D3DXCreateTextureFromFile**](d3dxcreatetexturefromfile.md) acepta es un puntero a una interfaz [**IDirect3DDevice9**](/windows/desktop/api) . El segundo parámetro indica a Direct3D el nombre del archivo desde el que se va a cargar la textura. El tercer parámetro toma la dirección de un puntero a una interfaz [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , que representa el objeto de textura creado.

## <a name="rendering-with-texture-resources"></a>Representar con recursos de textura

Direct3D admite varias combinaciones de texturas mediante el concepto de fases de textura. Cada fase de textura contiene una textura y las operaciones que se pueden realizar en la textura. Las texturas de las fases de textura forman el conjunto de texturas actuales. Para obtener más información, vea [Texture blending (Direct3D 9)](texture-blending.md). El estado de cada textura se encapsula en su fase de textura.

En una aplicación de C++, el estado de cada textura debe establecerse con el método [**IDirect3DDevice9:: SetTextureStageState**](/windows/desktop/api) . Pase el número de fase (0-7) como valor del primer parámetro. Establezca el valor del segundo parámetro en un miembro del tipo enumerado [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) . El último parámetro es el valor de estado para el estado de textura determinado.

Mediante el uso de punteros de interfaz de textura, la aplicación puede presentar una mezcla de hasta ocho texturas. Establezca las texturas actuales invocando el método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) . Direct3D combina todas las texturas actuales con las primitivas que representa.

> [!Note]  
> El método [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) incrementa el recuento de referencias de la superficie de textura que se está asignando. Cuando ya no se necesite la textura, debe establecer la textura en la fase adecuada en **null**. Si no lo hace, la superficie no se liberará, lo que producirá una fuga de memoria.

 

La aplicación puede establecer el estado de ajuste de textura para las texturas actuales llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) . Pase un valor de D3DRS \_ WRAP0 a D3DRS \_ WRAP7 como valor del primer parámetro y use una combinación de las \_ marcas D3DWRAPCOORD 0, D3DWRAPCOORD \_ 1, D3DWRAPCOORD \_ 2 y D3DWRAPCOORD \_ 3 para habilitar el ajuste en las direcciones u, v o w.

La aplicación también puede establecer los Estados de la perspectiva de textura y del filtrado de textura. Vea [filtrado de textura (Direct3D 9)](texture-filtering.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Texturas de Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
