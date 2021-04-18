---
description: Los Estados de muestra definen operaciones de muestreo de textura como el direccionamiento de textura y el filtrado de textura.
ms.assetid: 03a6a5f1-5e4f-4ba8-be4a-74d78fbc85d0
title: Enumeración D3DSAMPLERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSAMPLERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3e12764db306e61422f8c06ef514f6fad59b3ed8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717690"
---
# <a name="d3dsamplerstatetype-enumeration"></a><span data-ttu-id="53fcc-103">Enumeración D3DSAMPLERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="53fcc-103">D3DSAMPLERSTATETYPE enumeration</span></span>

<span data-ttu-id="53fcc-104">Los Estados de muestra definen operaciones de muestreo de textura como el direccionamiento de textura y el filtrado de textura.</span><span class="sxs-lookup"><span data-stu-id="53fcc-104">Sampler states define texture sampling operations such as texture addressing and texture filtering.</span></span> <span data-ttu-id="53fcc-105">Algunos Estados muestreador establecen el procesamiento de vértices y algún procesamiento de píxeles de configuración.</span><span class="sxs-lookup"><span data-stu-id="53fcc-105">Some sampler states set-up vertex processing, and some set-up pixel processing.</span></span> <span data-ttu-id="53fcc-106">Los Estados de muestra se pueden guardar y restaurar mediante stateblocks (vea el [Estado de guardado y restauración de los bloques de estado (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="53fcc-106">Sampler states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="53fcc-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="53fcc-107">Syntax</span></span>


```C++
typedef enum D3DSAMPLERSTATETYPE { 
  D3DSAMP_ADDRESSU       = 1,
  D3DSAMP_ADDRESSV       = 2,
  D3DSAMP_ADDRESSW       = 3,
  D3DSAMP_BORDERCOLOR    = 4,
  D3DSAMP_MAGFILTER      = 5,
  D3DSAMP_MINFILTER      = 6,
  D3DSAMP_MIPFILTER      = 7,
  D3DSAMP_MIPMAPLODBIAS  = 8,
  D3DSAMP_MAXMIPLEVEL    = 9,
  D3DSAMP_MAXANISOTROPY  = 10,
  D3DSAMP_SRGBTEXTURE    = 11,
  D3DSAMP_ELEMENTINDEX   = 12,
  D3DSAMP_DMAPOFFSET     = 13,
  D3DSAMP_FORCE_DWORD    = 0x7fffffff
} D3DSAMPLERSTATETYPE, *LPD3DSAMPLERSTATETYPE;
```



## <a name="constants"></a><span data-ttu-id="53fcc-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="53fcc-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="53fcc-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP \_ ADDRESSU**</span><span class="sxs-lookup"><span data-stu-id="53fcc-109"><span id="D3DSAMP_ADDRESSU"></span><span id="d3dsamp_addressu"></span>**D3DSAMP\_ADDRESSU**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-110">Modo de dirección de textura para la coordenada u.</span><span class="sxs-lookup"><span data-stu-id="53fcc-110">Texture-address mode for the u coordinate.</span></span> <span data-ttu-id="53fcc-111">El valor predeterminado es D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="53fcc-111">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="53fcc-112">Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-112">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP \_ ADDRESSV**</span><span class="sxs-lookup"><span data-stu-id="53fcc-113"><span id="D3DSAMP_ADDRESSV"></span><span id="d3dsamp_addressv"></span>**D3DSAMP\_ADDRESSV**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-114">Modo de dirección de textura para la coordenada v.</span><span class="sxs-lookup"><span data-stu-id="53fcc-114">Texture-address mode for the v coordinate.</span></span> <span data-ttu-id="53fcc-115">El valor predeterminado es D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="53fcc-115">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="53fcc-116">Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-116">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP \_ ADDRESSW**</span><span class="sxs-lookup"><span data-stu-id="53fcc-117"><span id="D3DSAMP_ADDRESSW"></span><span id="d3dsamp_addressw"></span>**D3DSAMP\_ADDRESSW**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-118">Modo de dirección de textura para la coordenada w.</span><span class="sxs-lookup"><span data-stu-id="53fcc-118">Texture-address mode for the w coordinate.</span></span> <span data-ttu-id="53fcc-119">El valor predeterminado es D3DTADDRESS \_ Wrap.</span><span class="sxs-lookup"><span data-stu-id="53fcc-119">The default is D3DTADDRESS\_WRAP.</span></span> <span data-ttu-id="53fcc-120">Para obtener más información, vea [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-120">For more information, see [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md).</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP \_ BORDERCOLOR**</span><span class="sxs-lookup"><span data-stu-id="53fcc-121"><span id="D3DSAMP_BORDERCOLOR"></span><span id="d3dsamp_bordercolor"></span>**D3DSAMP\_BORDERCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-122">Color del borde o escriba [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-122">Border color or type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="53fcc-123">El color predeterminado es 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="53fcc-123">The default color is 0x00000000.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP \_ MAGFILTER**</span><span class="sxs-lookup"><span data-stu-id="53fcc-124"><span id="D3DSAMP_MAGFILTER"></span><span id="d3dsamp_magfilter"></span>**D3DSAMP\_MAGFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-125">Filtro de ampliación de tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-125">Magnification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="53fcc-126">El valor predeterminado es D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="53fcc-126">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP \_ MINFILTER**</span><span class="sxs-lookup"><span data-stu-id="53fcc-127"><span id="D3DSAMP_MINFILTER"></span><span id="d3dsamp_minfilter"></span>**D3DSAMP\_MINFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-128">Filtro de minificación de tipo [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-128">Minification filter of type [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="53fcc-129">El valor predeterminado es D3DTEXF \_ Point.</span><span class="sxs-lookup"><span data-stu-id="53fcc-129">The default value is D3DTEXF\_POINT.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP \_ MIPFILTER**</span><span class="sxs-lookup"><span data-stu-id="53fcc-130"><span id="D3DSAMP_MIPFILTER"></span><span id="d3dsamp_mipfilter"></span>**D3DSAMP\_MIPFILTER**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-131">Filtro de mipmap que se va a utilizar durante minificación.</span><span class="sxs-lookup"><span data-stu-id="53fcc-131">Mipmap filter to use during minification.</span></span> <span data-ttu-id="53fcc-132">Vea [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span><span class="sxs-lookup"><span data-stu-id="53fcc-132">See [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md).</span></span> <span data-ttu-id="53fcc-133">El valor predeterminado es D3DTEXF \_ None.</span><span class="sxs-lookup"><span data-stu-id="53fcc-133">The default value is D3DTEXF\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP \_ MIPMAPLODBIAS**</span><span class="sxs-lookup"><span data-stu-id="53fcc-134"><span id="D3DSAMP_MIPMAPLODBIAS"></span><span id="d3dsamp_mipmaplodbias"></span>**D3DSAMP\_MIPMAPLODBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-135">Sesgo de nivel de detalle del mipmap.</span><span class="sxs-lookup"><span data-stu-id="53fcc-135">Mipmap level-of-detail bias.</span></span> <span data-ttu-id="53fcc-136">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="53fcc-136">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP \_ MAXMIPLEVEL**</span><span class="sxs-lookup"><span data-stu-id="53fcc-137"><span id="D3DSAMP_MAXMIPLEVEL"></span><span id="d3dsamp_maxmiplevel"></span>**D3DSAMP\_MAXMIPLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-138">Índice de nivel de detalle del mapa más grande que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="53fcc-138">level-of-detail index of largest map to use.</span></span> <span data-ttu-id="53fcc-139">Los valores van de 0 a (n-1), donde 0 es el mayor.</span><span class="sxs-lookup"><span data-stu-id="53fcc-139">Values range from 0 to (n - 1) where 0 is the largest.</span></span> <span data-ttu-id="53fcc-140">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="53fcc-140">The default value is zero.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP \_ MAXANISOTROPY**</span><span class="sxs-lookup"><span data-stu-id="53fcc-141"><span id="D3DSAMP_MAXANISOTROPY"></span><span id="d3dsamp_maxanisotropy"></span>**D3DSAMP\_MAXANISOTROPY**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-142">DWORD máximo anisotropía.</span><span class="sxs-lookup"><span data-stu-id="53fcc-142">DWORD maximum anisotropy.</span></span> <span data-ttu-id="53fcc-143">Los valores van de 1 al valor que se especifica en el miembro **MaxAnisotropy** de la estructura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="53fcc-143">Values range from 1 to the value that is specified in the **MaxAnisotropy** member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure.</span></span> <span data-ttu-id="53fcc-144">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="53fcc-144">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP \_ SRGBTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="53fcc-145"><span id="D3DSAMP_SRGBTEXTURE"></span><span id="d3dsamp_srgbtexture"></span>**D3DSAMP\_SRGBTEXTURE**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-146">Valor de corrección gamma.</span><span class="sxs-lookup"><span data-stu-id="53fcc-146">Gamma correction value.</span></span> <span data-ttu-id="53fcc-147">El valor predeterminado es 0, lo que significa que gamma es 1,0 y no se requiere ninguna corrección.</span><span class="sxs-lookup"><span data-stu-id="53fcc-147">The default value is 0, which means gamma is 1.0 and no correction is required.</span></span> <span data-ttu-id="53fcc-148">De lo contrario, este valor significa que la muestra debe suponer un valor de gamma de 2,2 en el contenido y convertirla en lineal (gamma 1,0) antes de presentarla al sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="53fcc-148">Otherwise, this value means that the sampler should assume gamma of 2.2 on the content and convert it to linear (gamma 1.0) before presenting it to the pixel shader.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP \_ ELEMENTINDEX**</span><span class="sxs-lookup"><span data-stu-id="53fcc-149"><span id="D3DSAMP_ELEMENTINDEX"></span><span id="d3dsamp_elementindex"></span>**D3DSAMP\_ELEMENTINDEX**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-150">Cuando se asigna una textura de múltiples elementos a la muestra, indica el índice de elemento que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="53fcc-150">When a multielement texture is assigned to the sampler, this indicates which element index to use.</span></span> <span data-ttu-id="53fcc-151">El valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="53fcc-151">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP \_ DMAPOFFSET**</span><span class="sxs-lookup"><span data-stu-id="53fcc-152"><span id="D3DSAMP_DMAPOFFSET"></span><span id="d3dsamp_dmapoffset"></span>**D3DSAMP\_DMAPOFFSET**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-153">Desplazamiento de vértice en el mapa de desplazamiento premuestreado.</span><span class="sxs-lookup"><span data-stu-id="53fcc-153">Vertex offset in the presampled displacement map.</span></span> <span data-ttu-id="53fcc-154">Se trata de una constante usada por del teselador, su valor predeterminado es 0.</span><span class="sxs-lookup"><span data-stu-id="53fcc-154">This is a constant used by the tessellator, its default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="53fcc-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP \_ forzar \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="53fcc-155"><span id="D3DSAMP_FORCE_DWORD"></span><span id="d3dsamp_force_dword"></span>**D3DSAMP\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="53fcc-156">Obliga a esta enumeración a compilarse en 32 bits de tamaño.</span><span class="sxs-lookup"><span data-stu-id="53fcc-156">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="53fcc-157">Sin este valor, algunos compiladores permitirían que esta enumeración se compilara en un tamaño distinto de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="53fcc-157">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="53fcc-158">Este valor no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="53fcc-158">This value is not used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="53fcc-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53fcc-159">Requirements</span></span>



| <span data-ttu-id="53fcc-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="53fcc-160">Requirement</span></span> | <span data-ttu-id="53fcc-161">Value</span><span class="sxs-lookup"><span data-stu-id="53fcc-161">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53fcc-162">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53fcc-162">Header</span></span><br/> | <dl> <span data-ttu-id="53fcc-163"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="53fcc-163"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53fcc-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="53fcc-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53fcc-165">Enumeraciones de Direct3D</span><span class="sxs-lookup"><span data-stu-id="53fcc-165">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
