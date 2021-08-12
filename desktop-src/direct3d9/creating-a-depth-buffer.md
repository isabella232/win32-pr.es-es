---
description: Un búfer de profundidad es una propiedad del dispositivo. Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura PARAMETERS D3DPRESENT como se muestra \_ en el ejemplo de código siguiente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Crear un búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527927"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Crear un búfer de profundidad (Direct3D 9)

Un búfer de profundidad es una propiedad del dispositivo. Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura [**PARAMETERS D3DPRESENT \_**](d3dpresent-parameters.md) como se muestra en el ejemplo de código siguiente.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Al establecer el miembro EnableAutoDepthStencil en **TRUE,** se indica a Direct3D que administre los búferes de profundidad de la aplicación. Tenga en cuenta que AutoDepthStencilFormat debe establecerse en un formato de búfer de profundidad válido. La marca D3DFMT D16 especifica un búfer de profundidad de \_ 16 bits, si hay uno disponible.

La siguiente llamada al método [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo que, a continuación, crea un búfer de profundidad.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



El búfer de profundidad se establece automáticamente como destino de representación del dispositivo. Cuando se restablece el dispositivo, el búfer de profundidad se destruye automáticamente y se vuelve a crear en el nuevo tamaño.

Para crear una nueva superficie de búfer de profundidad, use el método [**IDirect3DDevice9::CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)

Para establecer una nueva superficie de búfer de profundidad para el dispositivo, use el método [**IDirect3DDevice9::SetDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface)

Para usar el búfer de profundidad en la aplicación, debe habilitar el búfer de profundidad. Para más información, consulte [Habilitación del almacenamiento en búfer de profundidad (Direct3D 9).](enabling-depth-buffering.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
