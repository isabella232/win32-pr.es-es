---
description: Al usar IDirect3DDevice9::UpdateSurface, pase un rectángulo en la superficie de origen o use NULL para especificar toda la superficie.
ms.assetid: 2219d037-8480-4c36-b04e-0c23406a2e7e
title: Copiar en superficies (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e28a8518f0792948af7aabda269fffe9679de2c6fc704ee93e2cf05381176b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989295"
---
# <a name="copying-to-surfaces-direct3d-9"></a>Copiar en superficies (Direct3D 9)

Al usar [**IDirect3DDevice9::UpdateSurface,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)pase un rectángulo en la superficie de origen o **use NULL** para especificar toda la superficie. También se pasa un punto en la superficie de destino en el que se copia la posición superior izquierda del rectángulo en la imagen de origen. Este método no admite el recorte. Se producirá un error en la operación a menos que el rectángulo de origen y el rectángulo de destino correspondiente estén completamente contenidos en las superficies de origen y destino, respectivamente. Este método no admite la combinación alfa, las claves de color ni la conversión de formato. Tenga en cuenta que las superficies de origen y de destino deben ser distintas.

Para otras restricciones al usar UpdateSurface, vea [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface).

Los métodos siguientes también están disponibles en C++/C para copiar imágenes en una superficie de Direct3D.

-   [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md)
-   [**D3DXLoadSurfaceFromFileInMemory**](d3dxloadsurfacefromfileinmemory.md)
-   [**D3DXLoadSurfaceFromMemory**](d3dxloadsurfacefrommemory.md)
-   [**D3DXLoadSurfaceFromResource**](d3dxloadsurfacefromresource.md)
-   [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)
-   [**IDirect3DDevice9::UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

## <a name="updatesurface-example"></a>Ejemplo de UpdateSurface

En el ejemplo siguiente se copian dos rectángulos de la superficie de origen a una superficie de destino. El primer rectángulo se copia de (0, 0, 50, 50) en la superficie de origen a la misma ubicación en la superficie de destino y el segundo rectángulo se copia de (50, 50, 100, 100) en la superficie de origen a (150, 150, 200, 200) en la superficie de destino.


```
//The following assumptions are made:
// -d3dDevice is a valid Direct3DDevice9 object.
// -pSource and pDest are valid IDirect3DSurface9 pointers.

RECT  rcSource[] = {  0,  0,  50,  50,
                     50, 50, 100, 100 };
POINT ptDest[]   = {  0,  0, 150, 150 };

d3dDevice->UpdateSurface( pSource, rcSource, 2, pDest, ptDest);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Superficies de Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> </dl>

 

 
