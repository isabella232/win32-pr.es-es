---
title: Evitar LOS SRV del sombreador de píxeles NULL no deseados
description: En este tema se describe cómo evitar que el controlador que recibe vistas de recursos de sombreador (SRV) NULL, incluso cuando los SRV que no son NULL están enlazados a la fase del sombreador de píxeles.
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5021a197e4121603be374cd985a085a28faab8941316739a8985c0793004c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988305"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Evitar LOS SRV del sombreador de píxeles NULL no deseados

Las aplicaciones de Direct3D 11 que se ejecutan en el hardware gráfico  de Direct3D 9 podrían provocar accidentalmente que el controlador reciba vistas de recursos de sombreador (SRV) NULL incluso cuando las aplicaciones enlazan SRV que no son NULL a la fase del sombreador de píxeles. Esta situación solo puede producirse si las aplicaciones destruyen SRV mientras se ejecutan. En este tema se describe cómo  evitar que el controlador que recibe vistas de recursos de sombreador (SRV) NULL, incluso cuando los SRV que no son **NULL** están enlazados a la fase del sombreador de píxeles.

Para evitar que el controlador reciba SRV **NULL** no deseados, las aplicaciones deben llamar a [**ID3D11DeviceContext::P SSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) para anular todos los SRV antes de cada llamada a [**ID3D11DeviceContext::P SSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader). Sin embargo, si las aplicaciones no destruyen SRV hasta el final de la ejecución del código, no es necesario que desconjunte los SRV.

En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en los distintos niveles de características 10Level9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




