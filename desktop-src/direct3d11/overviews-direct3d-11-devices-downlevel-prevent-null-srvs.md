---
title: Prevención de SRVs de sombreador de píxeles NULOs no deseados
description: 'En este tema se describe cómo solucionar el controlador que recibe el sombreador nulo: vistas de recursos (SRVs) incluso cuando se enlazan SRVs que no son NULL a la fase del sombreador de píxeles.'
ms.assetid: c832c199-59b8-4079-a159-45490a2f6a94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bacacf7704cffe12df44b9b0be667632307adb4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996800"
---
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a>Prevención de SRVs de sombreador de píxeles NULOs no deseados

Las aplicaciones de Direct3D 11 que se ejecutan en el hardware gráfico de Direct3D 9 podrían hacer que el controlador reciba involuntariamente vistas de recursos (SRVs) del sombreador **nulo** , incluso cuando las aplicaciones enlazan SRVs que no son **null** a la fase del sombreador de píxeles. Esta situación solo puede producirse si las aplicaciones destruyen SRVs mientras se ejecutan. En este tema se describe cómo solucionar el controlador que recibe el sombreador **nulo** : vistas de recursos (SRVs) incluso cuando se enlazan SRVs que no son **null** a la fase del sombreador de píxeles.

Para evitar que el controlador reciba SRVs **nulos** no deseados, las aplicaciones deben llamar a [**ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) para desactivar todos los SRVs antes de cada llamada a [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader). Sin embargo, si las aplicaciones no destruyen SRVs hasta el final de la ejecución del código, no es necesario anular la SRVs.

En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




