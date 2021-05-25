---
description: Define el modo blend admitido.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumeración D3DBLEND (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343390"
---
# <a name="d3dblend-enumeration"></a><span data-ttu-id="0c285-103">D3DBLEND (enumeración)</span><span class="sxs-lookup"><span data-stu-id="0c285-103">D3DBLEND enumeration</span></span>

<span data-ttu-id="0c285-104">Define el modo blend admitido.</span><span class="sxs-lookup"><span data-stu-id="0c285-104">Defines the supported blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c285-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c285-105">Syntax</span></span>


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a><span data-ttu-id="0c285-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0c285-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0c285-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ ZERO**</span><span class="sxs-lookup"><span data-stu-id="0c285-107"><span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND\_ZERO**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-108">El factor blend es (0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="0c285-108">Blend factor is (0, 0, 0, 0).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ ONE**</span><span class="sxs-lookup"><span data-stu-id="0c285-109"><span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND\_ONE**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-110">El factor blend es (1, 1, 1, 1).</span><span class="sxs-lookup"><span data-stu-id="0c285-110">Blend factor is (1, 1, 1, 1).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ SRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-111"><span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND\_SRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-112">El factor blend es (Rs, Gs, Bs, As).</span><span class="sxs-lookup"><span data-stu-id="0c285-112">Blend factor is (Rₛ, Gₛ, Bₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ INVSRCCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-113"><span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND\_INVSRCCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-114">El factor blend es (1 - Rs, 1 - Gs, 1 - Bs, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="0c285-114">Blend factor is (1 - Rₛ, 1 - Gₛ, 1 - Bₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ SRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-115"><span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND\_SRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-116">El factor blend es (As, As, As, As).</span><span class="sxs-lookup"><span data-stu-id="0c285-116">Blend factor is (Aₛ, Aₛ, Aₛ, Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ INVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-117"><span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND\_INVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-118">El factor blend es ( 1 - As, 1 - As, 1 - As, 1 - As).</span><span class="sxs-lookup"><span data-stu-id="0c285-118">Blend factor is ( 1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ DESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-119"><span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND\_DESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-120">El factor de mezcla es (A<sub>d</sub> D<sub>D</sub> <sub>D</sub> <sub>D).</sub></span><span class="sxs-lookup"><span data-stu-id="0c285-120">Blend factor is (A<sub>d</sub> A<sub>d</sub> A<sub>d</sub> A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ INVDESTALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-121"><span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND\_INVDESTALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-122">El factor de mezcla es (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0c285-122">Blend factor is (1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub> 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ DESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-123"><span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND\_DESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-124">El factor blend es (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0c285-124">Blend factor is (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ INVDESTCOLOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-125"><span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND\_INVDESTCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-126">El factor blend es (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0c285-126">Blend factor is (1 - R<sub>d</sub>, 1 - G<sub>d</sub>, 1 - B<sub>d</sub>, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ SRCALPHASAT**</span><span class="sxs-lookup"><span data-stu-id="0c285-127"><span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND\_SRCALPHASAT**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-128">El factor blend es (f, f, f, 1); where f = min(As, 1 - A<sub>d</sub>).</span><span class="sxs-lookup"><span data-stu-id="0c285-128">Blend factor is (f, f, f, 1); where f = min(Aₛ, 1 - A<sub>d</sub>).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ BOTHSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-129"><span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND\_BOTHSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-130">**Obsoleto.**</span><span class="sxs-lookup"><span data-stu-id="0c285-130">**Obsolete**.</span></span> <span data-ttu-id="0c285-131">A partir de DirectX 6, puede lograr el mismo efecto estableciendo los factores de combinación de origen y destino en D3DBLEND \_ SRCALPHA y D3DBLEND \_ INVSRCALPHA en llamadas independientes.</span><span class="sxs-lookup"><span data-stu-id="0c285-131">Starting with DirectX 6, you can achieve the same effect by setting the source and destination blend factors to D3DBLEND\_SRCALPHA and D3DBLEND\_INVSRCALPHA in separate calls.</span></span>

</dd> <dt>

<span data-ttu-id="0c285-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ BOTHINVSRCALPHA**</span><span class="sxs-lookup"><span data-stu-id="0c285-132"><span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND\_BOTHINVSRCALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-133">**Obsoleto.**</span><span class="sxs-lookup"><span data-stu-id="0c285-133">**Obsolete**.</span></span> <span data-ttu-id="0c285-134">El factor de mezcla de origen es (1 - As, 1 - As, 1 - As, 1 - As) y el factor de mezcla de destino es (As, As, As, As); Se invalida la selección de combinación de destino.</span><span class="sxs-lookup"><span data-stu-id="0c285-134">Source blend factor is (1 - Aₛ, 1 - Aₛ, 1 - Aₛ, 1 - Aₛ), and destination blend factor is (Aₛ, Aₛ, Aₛ, Aₛ); the destination blend selection is overridden.</span></span> <span data-ttu-id="0c285-135">Este modo de mezcla solo se admite para el estado de representación D3DRS \_ SRCBLEND.</span><span class="sxs-lookup"><span data-stu-id="0c285-135">This blend mode is supported only for the D3DRS\_SRCBLEND render state.</span></span>

</dd> <dt>

<span data-ttu-id="0c285-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ BLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-136"><span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-137">Factor de mezcla de color constante utilizado por la mezcla de búfer de marco.</span><span class="sxs-lookup"><span data-stu-id="0c285-137">Constant color blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="0c285-138">Este modo blend solo se admite si D3DPBLENDCAPS BLENDFACTOR está establecido en los miembros \_ **SrcBlendCaps** o **DestBlendCaps** de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="0c285-138">This blend mode is supported only if D3DPBLENDCAPS\_BLENDFACTOR is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ INVBLENDFACTOR**</span><span class="sxs-lookup"><span data-stu-id="0c285-139"><span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND\_INVBLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-140">Factor de combinación de colores constante invertido usado por la mezcla de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0c285-140">Inverted constant color-blending factor used by the frame-buffer blender.</span></span> <span data-ttu-id="0c285-141">Este modo blend solo se admite si el bit BLENDFACTOR D3DPBLENDCAPS se establece en los miembros \_ **SrcBlendCaps** o **DestBlendCaps** de [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="0c285-141">This blend mode is supported only if the D3DPBLENDCAPS\_BLENDFACTOR bit is set in the **SrcBlendCaps** or **DestBlendCaps** members of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

</dd> <dt>

<span data-ttu-id="0c285-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="0c285-142"><span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND\_SRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-143">El factor blend es (PSOutColor \[ 1 \] <sub>r,</sub>PSOutColor \[ 1 \] <sub>g,</sub>PSOutColor \[ 1 \] <sub>b,</sub>no se usa).</span><span class="sxs-lookup"><span data-stu-id="0c285-143">Blend factor is (PSOutColor\[1\]<sub>r</sub>, PSOutColor\[1\]<sub>g</sub>, PSOutColor\[1\]<sub>b</sub>, not used).</span></span> <span data-ttu-id="0c285-144">Vea Render Target Blending (Combinación [de destinos de representación).](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="0c285-144">See [Render Target Blending](#render-target-blending).</span></span>

<span data-ttu-id="0c285-145">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0c285-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="0c285-146">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0c285-146">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="0c285-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**</span><span class="sxs-lookup"><span data-stu-id="0c285-147"><span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND\_INVSRCCOLOR2**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-148">El factor blend es (1 - PSOutColor \[ 1 \] <sub>r</sub>, 1 - PSOutColor \[ 1 \] <sub>g</sub>, 1 - PSOutColor \[ 1 \] <sub>b,</sub>no se usa)).</span><span class="sxs-lookup"><span data-stu-id="0c285-148">Blend factor is (1 - PSOutColor\[1\]<sub>r</sub>, 1 - PSOutColor\[1\]<sub>g</sub>, 1 - PSOutColor\[1\]<sub>b</sub>, not used)).</span></span> <span data-ttu-id="0c285-149">Vea Render Target Blending (Combinación [de destinos de representación).](#render-target-blending)</span><span class="sxs-lookup"><span data-stu-id="0c285-149">See [Render Target Blending](#render-target-blending).</span></span>


<span data-ttu-id="0c285-150">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="0c285-150">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="0c285-151">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="0c285-151">This flag is available in Direct3D 9Ex only.</span></span>



 

</dd> <dt>

<span data-ttu-id="0c285-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ FORCE \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0c285-152"><span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0c285-153">Fuerza esta enumeración a compilar hasta 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="0c285-153">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0c285-154">Sin este valor, algunos compiladores permitirían que esta enumeración se compilase a un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0c285-154">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0c285-155">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0c285-155">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c285-156">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0c285-156">Remarks</span></span>

<span data-ttu-id="0c285-157">En las descripciones de miembro anteriores, los subíndices s y d indican los valores RGBA del origen y el destino.</span><span class="sxs-lookup"><span data-stu-id="0c285-157">In the preceding member descriptions, the RGBA values of the source and destination are indicated by the s and d subscripts.</span></span>

<span data-ttu-id="0c285-158">Los siguientes estados de representación usan los valores de este tipo enumerado:</span><span class="sxs-lookup"><span data-stu-id="0c285-158">The values in this enumerated type are used by the following render states:</span></span>

-   <span data-ttu-id="0c285-159">D3DRS \_ DESTBLEND</span><span class="sxs-lookup"><span data-stu-id="0c285-159">D3DRS\_DESTBLEND</span></span>
-   <span data-ttu-id="0c285-160">D3DRS \_ SRCBLEND</span><span class="sxs-lookup"><span data-stu-id="0c285-160">D3DRS\_SRCBLEND</span></span>
-   <span data-ttu-id="0c285-161">D3DRS \_ DESTBLEPHA</span><span class="sxs-lookup"><span data-stu-id="0c285-161">D3DRS\_DESTBLENDALPHA</span></span>
-   <span data-ttu-id="0c285-162">D3DRS \_ SRCBLEPHA</span><span class="sxs-lookup"><span data-stu-id="0c285-162">D3DRS\_SRCBLENDALPHA</span></span>

<span data-ttu-id="0c285-163">Consulte [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span><span class="sxs-lookup"><span data-stu-id="0c285-163">See [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)</span></span>

### <a name="render-target-blending"></a><span data-ttu-id="0c285-164">Render Target Blending</span><span class="sxs-lookup"><span data-stu-id="0c285-164">Render Target Blending</span></span>

<span data-ttu-id="0c285-165">Direct3D 9Ex ha mejorado las funcionalidades de representación de texto.</span><span class="sxs-lookup"><span data-stu-id="0c285-165">Direct3D 9Ex has improved text rendering capabilities.</span></span> <span data-ttu-id="0c285-166">La representación de fuentes de tipo sin formato normalmente requeriría dos pases.</span><span class="sxs-lookup"><span data-stu-id="0c285-166">Rendering clear-type fonts would normally require two passes.</span></span> <span data-ttu-id="0c285-167">Para eliminar el segundo paso, se puede usar un sombreador de píxeles para generar dos colores, a los que podemos llamar PSOutColor 0 y \[ \] PSOutColor \[ \] 1.</span><span class="sxs-lookup"><span data-stu-id="0c285-167">To eliminate the second pass, a pixel shader can be used to output two colors, which we can call PSOutColor\[0\] and PSOutColor\[1\].</span></span> <span data-ttu-id="0c285-168">El primer color contendrá los 3 componentes de color estándar (RGB).</span><span class="sxs-lookup"><span data-stu-id="0c285-168">The first color would contain the standard 3 color components (RGB).</span></span> <span data-ttu-id="0c285-169">El segundo color contendrá 3 componentes alfa (uno para cada componente del primer color).</span><span class="sxs-lookup"><span data-stu-id="0c285-169">The second color would contain 3 alpha components (one for each component of the first color).</span></span>

<span data-ttu-id="0c285-170">Estos nuevos modos de combinación solo se usan para la representación de texto en el primer destino de representación.</span><span class="sxs-lookup"><span data-stu-id="0c285-170">These new blending modes are only used for text rendering on the first render target.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c285-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c285-171">Requirements</span></span>



| <span data-ttu-id="0c285-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c285-172">Requirement</span></span> | <span data-ttu-id="0c285-173">Value</span><span class="sxs-lookup"><span data-stu-id="0c285-173">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c285-174">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c285-174">Header</span></span><br/> | <dl> <span data-ttu-id="0c285-175"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="0c285-175"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c285-176">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c285-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c285-177">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0c285-177">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
