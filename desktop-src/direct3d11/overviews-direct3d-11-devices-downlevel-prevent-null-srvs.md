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
# <a name="preventing-unwanted-null-pixel-shader-srvs"></a><span data-ttu-id="505df-103">Prevención de SRVs de sombreador de píxeles NULOs no deseados</span><span class="sxs-lookup"><span data-stu-id="505df-103">Preventing Unwanted NULL Pixel Shader SRVs</span></span>

<span data-ttu-id="505df-104">Las aplicaciones de Direct3D 11 que se ejecutan en el hardware gráfico de Direct3D 9 podrían hacer que el controlador reciba involuntariamente vistas de recursos (SRVs) del sombreador **nulo** , incluso cuando las aplicaciones enlazan SRVs que no son **null** a la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="505df-104">Direct3D 11 applications that run on Direct3D 9 graphics hardware could inadvertently cause the driver to receive **NULL** shader-resource views (SRVs) even when the applications bind non-**NULL** SRVs to the pixel shader stage.</span></span> <span data-ttu-id="505df-105">Esta situación solo puede producirse si las aplicaciones destruyen SRVs mientras se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="505df-105">This situation can occur only if the applications destroy SRVs while they execute.</span></span> <span data-ttu-id="505df-106">En este tema se describe cómo solucionar el controlador que recibe el sombreador **nulo** : vistas de recursos (SRVs) incluso cuando se enlazan SRVs que no son **null** a la fase del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="505df-106">This topic discusses how to work around the driver receiving **NULL** shader-resource views (SRVs) even when non-**NULL** SRVs are bound to the pixel shader stage.</span></span>

<span data-ttu-id="505df-107">Para evitar que el controlador reciba SRVs **nulos** no deseados, las aplicaciones deben llamar a [**ID3D11DeviceContext::P ssetshaderresources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) para desactivar todos los SRVs antes de cada llamada a [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span><span class="sxs-lookup"><span data-stu-id="505df-107">To prevent the driver from receiving unwanted **NULL** SRVs, the applications must call [**ID3D11DeviceContext::PSSetShaderResources**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshaderresources) to unset all SRVs before each call to [**ID3D11DeviceContext::PSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader).</span></span> <span data-ttu-id="505df-108">Sin embargo, si las aplicaciones no destruyen SRVs hasta el final de la ejecución del código, no es necesario anular la SRVs.</span><span class="sxs-lookup"><span data-stu-id="505df-108">However, if the applications do not destroy SRVs until the end of their code execution, they do not need to unset the SRVs.</span></span>

<span data-ttu-id="505df-109">En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.</span><span class="sxs-lookup"><span data-stu-id="505df-109">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="505df-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="505df-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="505df-111">Direct3D 11 en hardware de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="505df-111">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 




