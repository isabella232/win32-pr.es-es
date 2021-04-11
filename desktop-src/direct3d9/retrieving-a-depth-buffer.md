---
description: 'En el ejemplo de código siguiente se muestra cómo usar el método IDirect3DDevice9:: GetDepthStencilSurface para recuperar un puntero a la superficie del búfer de profundidad propiedad del dispositivo.'
ms.assetid: cd5c158a-d2c4-4ced-aa6f-cd8c0e426a74
title: Recuperar un búfer de profundidad (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae914b8506fd0c4169f0cfec0d78d7c3bd9b9d61
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152545"
---
# <a name="retrieving-a-depth-buffer-direct3d-9"></a>Recuperar un búfer de profundidad (Direct3D 9)

En el ejemplo de código siguiente se muestra cómo usar el método [**IDirect3DDevice9:: GetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdepthstencilsurface) para recuperar un puntero a la superficie del búfer de profundidad propiedad del dispositivo.


```
LPDIRECT3DSURFACE9 pZBuffer;

m_d3dDevice->GetDepthStencilSurface( &pZBuffer );
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Búferes de profundidad](depth-buffers.md)
</dt> </dl>

 

 
