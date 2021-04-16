---
description: Direct3D permite seleccionar un modo de sombreado a la vez.
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: Establecer el modo de sombreado (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495316"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="62113-103">Establecer el modo de sombreado (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="62113-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="62113-104">Direct3D permite seleccionar un modo de sombreado a la vez.</span><span class="sxs-lookup"><span data-stu-id="62113-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="62113-105">De forma predeterminada, se selecciona sombreado Gouraud.</span><span class="sxs-lookup"><span data-stu-id="62113-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="62113-106">En C++, puede cambiar el modo de sombreado llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="62113-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="62113-107">Establezca el parámetro de *Estado* en D3DRS \_ SHADEMODE.</span><span class="sxs-lookup"><span data-stu-id="62113-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="62113-108">El parámetro *State* debe establecerse en un miembro de la enumeración [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="62113-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="62113-109">En los siguientes ejemplos de código de ejemplo se muestra cómo se puede establecer el modo de sombreado actual de una aplicación Direct3D en modo de sombreado plano o Gouraud.</span><span class="sxs-lookup"><span data-stu-id="62113-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="62113-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62113-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62113-111">Sombreado</span><span class="sxs-lookup"><span data-stu-id="62113-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
