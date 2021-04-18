---
description: Prepara un dispositivo para dibujar sprites.
ms.assetid: ec9eb069-0a41-4dd5-bbd5-5a31133550b6
title: 'ID3DXSprite:: Begin (método) (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7670c3c516627283a466b3adbb369dc76bbe0d45
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718291"
---
# <a name="id3dxspritebegin-method"></a><span data-ttu-id="37c3b-103">ID3DXSprite:: Begin (método)</span><span class="sxs-lookup"><span data-stu-id="37c3b-103">ID3DXSprite::Begin method</span></span>

<span data-ttu-id="37c3b-104">Prepara un dispositivo para dibujar sprites.</span><span class="sxs-lookup"><span data-stu-id="37c3b-104">Prepares a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c3b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37c3b-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="37c3b-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37c3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37c3b-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="37c3b-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="37c3b-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="37c3b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="37c3b-109">Combinación de cero o más marcadores que describen las opciones de representación de Sprite.</span><span class="sxs-lookup"><span data-stu-id="37c3b-109">Combination of zero or more flags that describe sprite rendering options.</span></span> <span data-ttu-id="37c3b-110">Para este método, las marcas válidas son:</span><span class="sxs-lookup"><span data-stu-id="37c3b-110">For this method, the valid flags are:</span></span>

-   <span data-ttu-id="37c3b-111">D3DXSPRITE \_ ALPHABLEND</span><span class="sxs-lookup"><span data-stu-id="37c3b-111">D3DXSPRITE\_ALPHABLEND</span></span>
-   <span data-ttu-id="37c3b-112">D3DXSPRITE de la \_ \_ cartelera</span><span class="sxs-lookup"><span data-stu-id="37c3b-112">D3DXSPRITE\_\_BILLBOARD</span></span>
-   <span data-ttu-id="37c3b-113">D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE</span><span class="sxs-lookup"><span data-stu-id="37c3b-113">D3DXSPRITE\_DONOTMODIFY\_RENDERSTATE</span></span>
-   <span data-ttu-id="37c3b-114">D3DXSPRITE \_ DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="37c3b-114">D3DXSPRITE\_DONOTSAVESTATE</span></span>
-   <span data-ttu-id="37c3b-115">D3DXSPRITE \_ OBJECTSPACE</span><span class="sxs-lookup"><span data-stu-id="37c3b-115">D3DXSPRITE\_OBJECTSPACE</span></span>
-   <span data-ttu-id="37c3b-116">D3DXSPRITE \_ \_ profundidad de ordenación \_ \_ BACKTOFRONT</span><span class="sxs-lookup"><span data-stu-id="37c3b-116">D3DXSPRITE\_\_SORT\_DEPTH\_BACKTOFRONT</span></span>
-   <span data-ttu-id="37c3b-117">D3DXSPRITE \_ \_ profundidad de ordenación \_ \_ FRONTTOBACK</span><span class="sxs-lookup"><span data-stu-id="37c3b-117">D3DXSPRITE\_\_SORT\_DEPTH\_FRONTTOBACK</span></span>
-   <span data-ttu-id="37c3b-118">D3DXSPRITE \_ \_ ordenar \_ textura</span><span class="sxs-lookup"><span data-stu-id="37c3b-118">D3DXSPRITE\_\_SORT\_TEXTURE</span></span>

<span data-ttu-id="37c3b-119">Para obtener una descripción de las marcas y obtener información sobre cómo controlar la captura de estado de los dispositivos y las transformaciones de la vista de dispositivos, vea [D3DXSPRITE](d3dxsprite.md).</span><span class="sxs-lookup"><span data-stu-id="37c3b-119">For a description of the flags and for information on how to control device state capture and device view transforms, see [D3DXSPRITE](d3dxsprite.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37c3b-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37c3b-120">Return value</span></span>

<span data-ttu-id="37c3b-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="37c3b-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="37c3b-122">Si el método se ejecuta correctamente, el valor devuelto es S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="37c3b-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="37c3b-123">Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DERR \_ OUTOFVIDEOMEMORY, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="37c3b-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="37c3b-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37c3b-124">Remarks</span></span>

<span data-ttu-id="37c3b-125">Se debe llamar a este método desde dentro de [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="37c3b-125">This method must be called from inside a [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) .</span></span> <span data-ttu-id="37c3b-126">.</span><span class="sxs-lookup"><span data-stu-id="37c3b-126">.</span></span> <span data-ttu-id="37c3b-127">.</span><span class="sxs-lookup"><span data-stu-id="37c3b-127">.</span></span> <span data-ttu-id="37c3b-128">Secuencia [**IDirect3DDevice9:: EndScene**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="37c3b-128">[**IDirect3DDevice9::EndScene**](/windows/desktop/api) sequence.</span></span> <span data-ttu-id="37c3b-129">**ID3DXSprite:: Begin** no se puede usar como sustituto de **IDirect3DDevice9:: BeginScene** o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="37c3b-129">**ID3DXSprite::Begin** cannot be used as a substitute for either **IDirect3DDevice9::BeginScene** or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

<span data-ttu-id="37c3b-130">Este método establecerá los siguientes Estados en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="37c3b-130">This method will set the following states on the device.</span></span>

<span data-ttu-id="37c3b-131">Estados de representación:</span><span class="sxs-lookup"><span data-stu-id="37c3b-131">Render States:</span></span>



| <span data-ttu-id="37c3b-132">Tipo ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="37c3b-132">Type ([**D3DRENDERSTATETYPE**](./d3drenderstatetype.md))</span></span> | <span data-ttu-id="37c3b-133">Value</span><span class="sxs-lookup"><span data-stu-id="37c3b-133">Value</span></span>                                                                                                             |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c3b-134">D3DRS \_ ALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-134">D3DRS\_ALPHABLENDENABLE</span></span>                                       | <span data-ttu-id="37c3b-135">TRUE</span><span class="sxs-lookup"><span data-stu-id="37c3b-135">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="37c3b-136">D3DRS \_ ALPHAFUNC</span><span class="sxs-lookup"><span data-stu-id="37c3b-136">D3DRS\_ALPHAFUNC</span></span>                                              | <span data-ttu-id="37c3b-137">D3DCMP \_ mayor</span><span class="sxs-lookup"><span data-stu-id="37c3b-137">D3DCMP\_GREATER</span></span>                                                                                                   |
| <span data-ttu-id="37c3b-138">D3DRS \_ ALPHAREF</span><span class="sxs-lookup"><span data-stu-id="37c3b-138">D3DRS\_ALPHAREF</span></span>                                               | <span data-ttu-id="37c3b-139">0x00</span><span class="sxs-lookup"><span data-stu-id="37c3b-139">0x00</span></span>                                                                                                              |
| <span data-ttu-id="37c3b-140">D3DRS \_ ALPHATESTENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-140">D3DRS\_ALPHATESTENABLE</span></span>                                        | <span data-ttu-id="37c3b-141">AlphaCmpCaps</span><span class="sxs-lookup"><span data-stu-id="37c3b-141">AlphaCmpCaps</span></span>                                                                                                      |
| <span data-ttu-id="37c3b-142">D3DRS \_ BLENDOP</span><span class="sxs-lookup"><span data-stu-id="37c3b-142">D3DRS\_BLENDOP</span></span>                                                | <span data-ttu-id="37c3b-143">D3DBLENDOP \_ Agregar</span><span class="sxs-lookup"><span data-stu-id="37c3b-143">D3DBLENDOP\_ADD</span></span>                                                                                                   |
| <span data-ttu-id="37c3b-144">Recorte de D3DRS \_</span><span class="sxs-lookup"><span data-stu-id="37c3b-144">D3DRS\_CLIPPING</span></span>                                               | <span data-ttu-id="37c3b-145">TRUE</span><span class="sxs-lookup"><span data-stu-id="37c3b-145">TRUE</span></span>                                                                                                              |
| <span data-ttu-id="37c3b-146">D3DRS \_ CLIPPLANEENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-146">D3DRS\_CLIPPLANEENABLE</span></span>                                        | <span data-ttu-id="37c3b-147">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-147">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-148">D3DRS \_ COLORWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-148">D3DRS\_COLORWRITEENABLE</span></span>                                       | <span data-ttu-id="37c3b-149">D3DCOLORWRITEENABLE \_ alfa \| D3DCOLORWRITEENABLE \_ azul \| D3DCOLORWRITEENABLE \_ verde \| D3DCOLORWRITEENABLE \_ rojo</span><span class="sxs-lookup"><span data-stu-id="37c3b-149">D3DCOLORWRITEENABLE\_ALPHA \| D3DCOLORWRITEENABLE\_BLUE \| D3DCOLORWRITEENABLE\_GREEN \| D3DCOLORWRITEENABLE\_RED</span></span> |
| <span data-ttu-id="37c3b-150">D3DRS \_ CULLMODE</span><span class="sxs-lookup"><span data-stu-id="37c3b-150">D3DRS\_CULLMODE</span></span>                                               | <span data-ttu-id="37c3b-151">D3DCULL \_ ninguno</span><span class="sxs-lookup"><span data-stu-id="37c3b-151">D3DCULL\_NONE</span></span>                                                                                                     |
| <span data-ttu-id="37c3b-152">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="37c3b-152">D3DRS\_DESTBLEND</span></span>                                              | <span data-ttu-id="37c3b-153">D3DBLEND \_ INVSRCALPHA</span><span class="sxs-lookup"><span data-stu-id="37c3b-153">D3DBLEND\_INVSRCALPHA</span></span>                                                                                             |
| <span data-ttu-id="37c3b-154">D3DRS \_ DIFFUSEMATERIALSOURCE</span><span class="sxs-lookup"><span data-stu-id="37c3b-154">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>                                  | <span data-ttu-id="37c3b-155">D3DMCS \_ COLOR1</span><span class="sxs-lookup"><span data-stu-id="37c3b-155">D3DMCS\_COLOR1</span></span>                                                                                                    |
| <span data-ttu-id="37c3b-156">D3DRS \_ ENABLEADAPTIVETESSELLATION</span><span class="sxs-lookup"><span data-stu-id="37c3b-156">D3DRS\_ENABLEADAPTIVETESSELLATION</span></span>                             | <span data-ttu-id="37c3b-157">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-157">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-158">D3DRS \_ FILLMODE</span><span class="sxs-lookup"><span data-stu-id="37c3b-158">D3DRS\_FILLMODE</span></span>                                               | <span data-ttu-id="37c3b-159">D3DFILL \_ Solid</span><span class="sxs-lookup"><span data-stu-id="37c3b-159">D3DFILL\_SOLID</span></span>                                                                                                    |
| <span data-ttu-id="37c3b-160">D3DRS \_ FOGENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-160">D3DRS\_FOGENABLE</span></span>                                              | <span data-ttu-id="37c3b-161">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-161">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-162">D3DRS \_ INDEXEDVERTEXBLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-162">D3DRS\_INDEXEDVERTEXBLENDENABLE</span></span>                               | <span data-ttu-id="37c3b-163">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-163">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-164">\_Iluminación D3DRS</span><span class="sxs-lookup"><span data-stu-id="37c3b-164">D3DRS\_LIGHTING</span></span>                                               | <span data-ttu-id="37c3b-165">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-165">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-166">D3DRS \_ RANGEFOGENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-166">D3DRS\_RANGEFOGENABLE</span></span>                                         | <span data-ttu-id="37c3b-167">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-167">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-168">D3DRS \_ SEPARATEALPHABLENDENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-168">D3DRS\_SEPARATEALPHABLENDENABLE</span></span>                               | <span data-ttu-id="37c3b-169">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-169">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-170">D3DRS \_ SHADEMODE</span><span class="sxs-lookup"><span data-stu-id="37c3b-170">D3DRS\_SHADEMODE</span></span>                                              | <span data-ttu-id="37c3b-171">D3DSHADE \_ GOURAUD</span><span class="sxs-lookup"><span data-stu-id="37c3b-171">D3DSHADE\_GOURAUD</span></span>                                                                                                 |
| <span data-ttu-id="37c3b-172">D3DRS \_ SPECULARENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-172">D3DRS\_SPECULARENABLE</span></span>                                         | <span data-ttu-id="37c3b-173">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-173">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-174">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="37c3b-174">D3DRS\_SRCBLEND</span></span>                                               | <span data-ttu-id="37c3b-175">D3DBLEND \_ SRCALPHA</span><span class="sxs-lookup"><span data-stu-id="37c3b-175">D3DBLEND\_SRCALPHA</span></span>                                                                                                |
| <span data-ttu-id="37c3b-176">D3DRS \_ SRGBWRITEENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-176">D3DRS\_SRGBWRITEENABLE</span></span>                                        | <span data-ttu-id="37c3b-177">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-177">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-178">D3DRS \_ STENCILENABLE</span><span class="sxs-lookup"><span data-stu-id="37c3b-178">D3DRS\_STENCILENABLE</span></span>                                          | <span data-ttu-id="37c3b-179">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-179">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-180">D3DRS \_ VERTEXBLEND</span><span class="sxs-lookup"><span data-stu-id="37c3b-180">D3DRS\_VERTEXBLEND</span></span>                                            | <span data-ttu-id="37c3b-181">false</span><span class="sxs-lookup"><span data-stu-id="37c3b-181">FALSE</span></span>                                                                                                             |
| <span data-ttu-id="37c3b-182">D3DRS \_ WRAP0</span><span class="sxs-lookup"><span data-stu-id="37c3b-182">D3DRS\_WRAP0</span></span>                                                  | <span data-ttu-id="37c3b-183">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-183">0</span></span>                                                                                                                 |



 

<span data-ttu-id="37c3b-184">Estados de la fase de textura:</span><span class="sxs-lookup"><span data-stu-id="37c3b-184">Texture Stage States:</span></span>



| <span data-ttu-id="37c3b-185">Identificador de la fase</span><span class="sxs-lookup"><span data-stu-id="37c3b-185">Stage Identifier</span></span> | <span data-ttu-id="37c3b-186">Tipo ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span><span class="sxs-lookup"><span data-stu-id="37c3b-186">Type ([**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md))</span></span> | <span data-ttu-id="37c3b-187">Value</span><span class="sxs-lookup"><span data-stu-id="37c3b-187">Value</span></span>            |
|------------------|---------------------------------------------------------------------------|------------------|
| <span data-ttu-id="37c3b-188">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-188">0</span></span>                | <span data-ttu-id="37c3b-189">D3DTSS \_ ALPHAARG1</span><span class="sxs-lookup"><span data-stu-id="37c3b-189">D3DTSS\_ALPHAARG1</span></span>                                                         | <span data-ttu-id="37c3b-190">\_Textura D3DTA</span><span class="sxs-lookup"><span data-stu-id="37c3b-190">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="37c3b-191">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-191">0</span></span>                | <span data-ttu-id="37c3b-192">D3DTSS \_ ALPHAARG2</span><span class="sxs-lookup"><span data-stu-id="37c3b-192">D3DTSS\_ALPHAARG2</span></span>                                                         | <span data-ttu-id="37c3b-193">\_Difusión D3DTA</span><span class="sxs-lookup"><span data-stu-id="37c3b-193">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="37c3b-194">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-194">0</span></span>                | <span data-ttu-id="37c3b-195">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="37c3b-195">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="37c3b-196">D3DTOP \_ modular</span><span class="sxs-lookup"><span data-stu-id="37c3b-196">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="37c3b-197">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-197">0</span></span>                | <span data-ttu-id="37c3b-198">D3DTSS \_ COLORARG1</span><span class="sxs-lookup"><span data-stu-id="37c3b-198">D3DTSS\_COLORARG1</span></span>                                                         | <span data-ttu-id="37c3b-199">\_Textura D3DTA</span><span class="sxs-lookup"><span data-stu-id="37c3b-199">D3DTA\_TEXTURE</span></span>   |
| <span data-ttu-id="37c3b-200">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-200">0</span></span>                | <span data-ttu-id="37c3b-201">D3DTSS \_ COLORARG2</span><span class="sxs-lookup"><span data-stu-id="37c3b-201">D3DTSS\_COLORARG2</span></span>                                                         | <span data-ttu-id="37c3b-202">\_Difusión D3DTA</span><span class="sxs-lookup"><span data-stu-id="37c3b-202">D3DTA\_DIFFUSE</span></span>   |
| <span data-ttu-id="37c3b-203">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-203">0</span></span>                | <span data-ttu-id="37c3b-204">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="37c3b-204">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="37c3b-205">D3DTOP \_ modular</span><span class="sxs-lookup"><span data-stu-id="37c3b-205">D3DTOP\_MODULATE</span></span> |
| <span data-ttu-id="37c3b-206">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-206">0</span></span>                | <span data-ttu-id="37c3b-207">D3DTSS \_ TEXCOORDINDEX</span><span class="sxs-lookup"><span data-stu-id="37c3b-207">D3DTSS\_TEXCOORDINDEX</span></span>                                                     | <span data-ttu-id="37c3b-208">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-208">0</span></span>                |
| <span data-ttu-id="37c3b-209">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-209">0</span></span>                | <span data-ttu-id="37c3b-210">D3DTSS \_ TEXTURETRANSFORMFLAGS</span><span class="sxs-lookup"><span data-stu-id="37c3b-210">D3DTSS\_TEXTURETRANSFORMFLAGS</span></span>                                             | <span data-ttu-id="37c3b-211">Deshabilitación de D3DTTFF \_</span><span class="sxs-lookup"><span data-stu-id="37c3b-211">D3DTTFF\_DISABLE</span></span> |
| <span data-ttu-id="37c3b-212">1</span><span class="sxs-lookup"><span data-stu-id="37c3b-212">1</span></span>                | <span data-ttu-id="37c3b-213">D3DTSS \_ ALPHAOP</span><span class="sxs-lookup"><span data-stu-id="37c3b-213">D3DTSS\_ALPHAOP</span></span>                                                           | <span data-ttu-id="37c3b-214">Deshabilitación de D3DTOP \_</span><span class="sxs-lookup"><span data-stu-id="37c3b-214">D3DTOP\_DISABLE</span></span>  |
| <span data-ttu-id="37c3b-215">1</span><span class="sxs-lookup"><span data-stu-id="37c3b-215">1</span></span>                | <span data-ttu-id="37c3b-216">D3DTSS \_ COLOROP</span><span class="sxs-lookup"><span data-stu-id="37c3b-216">D3DTSS\_COLOROP</span></span>                                                           | <span data-ttu-id="37c3b-217">Deshabilitación de D3DTOP \_</span><span class="sxs-lookup"><span data-stu-id="37c3b-217">D3DTOP\_DISABLE</span></span>  |



 

<span data-ttu-id="37c3b-218">Estados de muestra:</span><span class="sxs-lookup"><span data-stu-id="37c3b-218">Sampler States:</span></span>



| <span data-ttu-id="37c3b-219">Índice de fase de muestra</span><span class="sxs-lookup"><span data-stu-id="37c3b-219">Sampler Stage Index</span></span> | <span data-ttu-id="37c3b-220">Tipo ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span><span class="sxs-lookup"><span data-stu-id="37c3b-220">Type ([**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md))</span></span> | <span data-ttu-id="37c3b-221">Value</span><span class="sxs-lookup"><span data-stu-id="37c3b-221">Value</span></span>                                                                                                          |
|---------------------|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c3b-222">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-222">0</span></span>                   | <span data-ttu-id="37c3b-223">D3DSAMP \_ ADDRESSU</span><span class="sxs-lookup"><span data-stu-id="37c3b-223">D3DSAMP\_ADDRESSU</span></span>                                               | <span data-ttu-id="37c3b-224">\_Abrazadera D3DTADDRESS</span><span class="sxs-lookup"><span data-stu-id="37c3b-224">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="37c3b-225">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-225">0</span></span>                   | <span data-ttu-id="37c3b-226">D3DSAMP \_ ADDRESSV</span><span class="sxs-lookup"><span data-stu-id="37c3b-226">D3DSAMP\_ADDRESSV</span></span>                                               | <span data-ttu-id="37c3b-227">\_Abrazadera D3DTADDRESS</span><span class="sxs-lookup"><span data-stu-id="37c3b-227">D3DTADDRESS\_CLAMP</span></span>                                                                                             |
| <span data-ttu-id="37c3b-228">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-228">0</span></span>                   | <span data-ttu-id="37c3b-229">D3DSAMP \_ MAGFILTER</span><span class="sxs-lookup"><span data-stu-id="37c3b-229">D3DSAMP\_MAGFILTER</span></span>                                              | <span data-ttu-id="37c3b-230">D3DTEXF \_ anisotrópico si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MAGFANISOTROPIC; de lo contrario D3DTEXF \_ lineal</span><span class="sxs-lookup"><span data-stu-id="37c3b-230">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MAGFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="37c3b-231">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-231">0</span></span>                   | <span data-ttu-id="37c3b-232">D3DSAMP \_ MAXMIPLEVEL</span><span class="sxs-lookup"><span data-stu-id="37c3b-232">D3DSAMP\_MAXMIPLEVEL</span></span>                                            | <span data-ttu-id="37c3b-233">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-233">0</span></span>                                                                                                              |
| <span data-ttu-id="37c3b-234">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-234">0</span></span>                   | <span data-ttu-id="37c3b-235">D3DSAMP \_ MAXANISOTROPY</span><span class="sxs-lookup"><span data-stu-id="37c3b-235">D3DSAMP\_MAXANISOTROPY</span></span>                                          | <span data-ttu-id="37c3b-236">MaxAnisotropy</span><span class="sxs-lookup"><span data-stu-id="37c3b-236">MaxAnisotropy</span></span>                                                                                                  |
| <span data-ttu-id="37c3b-237">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-237">0</span></span>                   | <span data-ttu-id="37c3b-238">D3DSAMP \_ MINFILTER</span><span class="sxs-lookup"><span data-stu-id="37c3b-238">D3DSAMP\_MINFILTER</span></span>                                              | <span data-ttu-id="37c3b-239">D3DTEXF \_ anisotrópico si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MINFANISOTROPIC; de lo contrario D3DTEXF \_ lineal</span><span class="sxs-lookup"><span data-stu-id="37c3b-239">D3DTEXF\_ANISOTROPIC if TextureFilterCaps includes D3DPTFILTERCAPS\_MINFANISOTROPIC; otherwise D3DTEXF\_LINEAR</span></span> |
| <span data-ttu-id="37c3b-240">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-240">0</span></span>                   | <span data-ttu-id="37c3b-241">D3DSAMP \_ MIPFILTER</span><span class="sxs-lookup"><span data-stu-id="37c3b-241">D3DSAMP\_MIPFILTER</span></span>                                              | <span data-ttu-id="37c3b-242">D3DTEXF \_ linear si TextureFilterCaps incluye D3DPTFILTERCAPS \_ MIPFLINEAR; de lo contrario D3DTEXF \_ Point</span><span class="sxs-lookup"><span data-stu-id="37c3b-242">D3DTEXF\_LINEAR if TextureFilterCaps includes D3DPTFILTERCAPS\_MIPFLINEAR; otherwise D3DTEXF\_POINT</span></span>            |
| <span data-ttu-id="37c3b-243">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-243">0</span></span>                   | <span data-ttu-id="37c3b-244">D3DSAMP \_ MIPMAPLODBIAS</span><span class="sxs-lookup"><span data-stu-id="37c3b-244">D3DSAMP\_MIPMAPLODBIAS</span></span>                                          | <span data-ttu-id="37c3b-245">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-245">0</span></span>                                                                                                              |
| <span data-ttu-id="37c3b-246">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-246">0</span></span>                   | <span data-ttu-id="37c3b-247">D3DSAMP \_ SRGBTEXTURE</span><span class="sxs-lookup"><span data-stu-id="37c3b-247">D3DSAMP\_SRGBTEXTURE</span></span>                                            | <span data-ttu-id="37c3b-248">0</span><span class="sxs-lookup"><span data-stu-id="37c3b-248">0</span></span>                                                                                                              |



 

> [!Note]  
> <span data-ttu-id="37c3b-249">Este método deshabilita N-patches.</span><span class="sxs-lookup"><span data-stu-id="37c3b-249">This method disables N-patches.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="37c3b-250">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c3b-250">Requirements</span></span>



| <span data-ttu-id="37c3b-251">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c3b-251">Requirement</span></span> | <span data-ttu-id="37c3b-252">Value</span><span class="sxs-lookup"><span data-stu-id="37c3b-252">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="37c3b-253">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37c3b-253">Header</span></span><br/>  | <dl> <span data-ttu-id="37c3b-254"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="37c3b-254"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="37c3b-255">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37c3b-255">Library</span></span><br/> | <dl> <span data-ttu-id="37c3b-256"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37c3b-256"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="37c3b-257">Vea también</span><span class="sxs-lookup"><span data-stu-id="37c3b-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c3b-258">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="37c3b-258">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="37c3b-259">D3DXSPRITE</span><span class="sxs-lookup"><span data-stu-id="37c3b-259">D3DXSPRITE</span></span>](d3dxsprite.md)
</dt> </dl>

 

 
