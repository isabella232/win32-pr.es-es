---
description: Un búfer de profundidad es una propiedad del dispositivo. Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura de \_ parámetros D3DPRESENT como se muestra en el ejemplo de código siguiente.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Crear un búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa30ccba6c44d3582201ea96017a16cc903fecce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152882"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Crear un búfer de profundidad (Direct3D 9)

Un búfer de profundidad es una propiedad del dispositivo. Para crear un búfer de profundidad administrado por Direct3D, establezca los miembros adecuados de la estructura [**de \_ parámetros D3DPRESENT**](d3dpresent-parameters.md) como se muestra en el ejemplo de código siguiente.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



Al establecer el miembro EnableAutoDepthStencil en **true**, se indica a Direct3D que administre los búferes de profundidad para la aplicación. Tenga en cuenta que AutoDepthStencilFormat debe establecerse en un formato de búfer de profundidad válido. La \_ marca D3DFMT D16 especifica un búfer de profundidad de 16 bits, si hay alguno disponible.

La siguiente llamada al método [**IDirect3D9:: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crea un dispositivo que después crea un búfer de profundidad.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



El búfer de profundidad se establece automáticamente como el destino de representación del dispositivo. Cuando se restablece el dispositivo, el búfer de profundidad se destruye automáticamente y se vuelve a crear con el nuevo tamaño.

Para crear una superficie de búfer de profundidad nueva, use el método [**IDirect3DDevice9:: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Para establecer una nueva superficie de búfer de profundidad para el dispositivo, use el método [**IDirect3DDevice9:: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .

Para usar el búfer de profundidad en la aplicación, debe habilitar el búfer de profundidad. Para obtener más información, vea [Habilitar el almacenamiento en búfer de profundidad (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
