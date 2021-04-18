---
title: CD3DX12_STATIC_SAMPLER_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una \_ estructura de descripción de muestra estática de D3D12 \_ \_ .
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- Estructura de CD3DX12_STATIC_SAMPLER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717595"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a><span data-ttu-id="bb2fc-104">CD3DX12 \_ \_ estructura de DESC de muestra estática \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-104">CD3DX12\_STATIC\_SAMPLER\_DESC structure</span></span>

<span data-ttu-id="bb2fc-105">Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ \_ Descripción de muestra estática de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="bb2fc-105">A helper structure to enable easy initialization of a [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb2fc-106">Syntax</span></span>


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a><span data-ttu-id="bb2fc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb2fc-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb2fc-108">**Descripción de la \_ muestra estática CD3DX12 \_ \_ ()**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-108">**CD3DX12\_STATIC\_SAMPLER\_DESC()**</span></span>
</dt> <dd>

<span data-ttu-id="bb2fc-109">Crea una instancia nueva, no inicializada, de una descripción de la \_ muestra estática CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bb2fc-109">Creates a new, uninitialized, instance of a CD3DX12\_STATIC\_SAMPLER\_DESC.</span></span>

</dd> <dt>

<span data-ttu-id="bb2fc-110">**CD3DX12 explícito de la \_ muestra estática de la \_ \_ Descripción (const D3D12 \_ &de \_ muestra estática \_ )**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-110">**explicit CD3DX12\_STATIC\_SAMPLER\_DESC(const D3D12\_STATIC\_SAMPLER\_DESC &o)**</span></span>
</dt> <dd>

<span data-ttu-id="bb2fc-111">Crea una nueva instancia de una \_ Descripción de \_ muestra estática CD3DX12 \_ , inicializada con el contenido de otra estructura D3D12 de la [**\_ muestra estática de la \_ \_ muestra**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) .</span><span class="sxs-lookup"><span data-stu-id="bb2fc-111">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initialized with the contents of another [**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) structure.</span></span>

</dd> <dt>

<span data-ttu-id="bb2fc-112">**CD3DX12 \_ static \_ Sampler \_ DESC (uint shaderRegister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ anisotrópico, D3D12 \_ Texture \_ Address \_ mode addressU = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap, D3D12 \_ Texture \_ Address \_ mode addressV = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ de modo \_ de dirección de textura Wrap, Float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ color del borde estático \_ BorderColor = D3D12 el \_ \_ color del borde estático de la \_ \_ \_ visibilidad del sombreador minLOD = \_ \_ \_ \_ maxLOD \_ Visibility del sombreador \_ \_ All, uint D3D12 = 0)**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-112">**CD3DX12\_STATIC\_SAMPLER\_DESC(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="bb2fc-113">Crea una nueva instancia de una \_ Descripción de \_ la muestra estática CD3DX12 \_ , inicializando los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="bb2fc-113">Creates a new instance of a CD3DX12\_STATIC\_SAMPLER\_DESC, initializing the following parameters:</span></span>

<span data-ttu-id="bb2fc-114">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="bb2fc-114">UINT shaderRegister</span></span>

<span data-ttu-id="bb2fc-115">rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="bb2fc-115">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="bb2fc-116">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-116">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-117">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-117">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-118">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-118">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-119">rechace FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-119">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="bb2fc-120">rechace UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="bb2fc-120">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="bb2fc-121">rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="bb2fc-121">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="bb2fc-122">rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco</span><span class="sxs-lookup"><span data-stu-id="bb2fc-122">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="bb2fc-123">rechace FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="bb2fc-123">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="bb2fc-124">rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="bb2fc-124">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="bb2fc-125">rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-125">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="bb2fc-126">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-126">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="bb2fc-127">**Static inline init (D3D12 \_ static \_ sample \_ DESC &SamplerDesc, uint shaderRegister, D3D12 Filter \_ Filter = D3D12 \_ Filter \_ anisotrópico, D3D12 \_ Texture \_ Address \_ mode addressU = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap, D3D12 \_ Texture \_ Address \_ mode addressV = D3D12 \_ Texture Address Mode \_ \_ \_ Wrap D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ \_ de modo de dirección de textura Wrap, Float MIPLODBIAS = 0, uint maxAnisotropy = 16, D3D12 \_ Comparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ \_ color del borde estático BorderColor = D3D12 el \_ \_ \_ color del borde estático de la \_ \_ visibilidad del \_ sombreador minLOD = \_ \_ \_ maxLOD Visibility del \_ sombreador \_ \_ All, uint D3D12 = 0)**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-127">**static inline Init(D3D12\_STATIC\_SAMPLER\_DESC &samplerDesc, UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="bb2fc-128">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb2fc-128">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="bb2fc-129">[**D3D12 \_ \_ \_ Descripción de muestra estática**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span><span class="sxs-lookup"><span data-stu-id="bb2fc-129">[**D3D12\_STATIC\_SAMPLER\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc</span></span>

<span data-ttu-id="bb2fc-130">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="bb2fc-130">UINT shaderRegister</span></span>

<span data-ttu-id="bb2fc-131">rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="bb2fc-131">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="bb2fc-132">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-132">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-133">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-133">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-134">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-134">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-135">rechace FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-135">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="bb2fc-136">rechace UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="bb2fc-136">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="bb2fc-137">rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="bb2fc-137">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="bb2fc-138">rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco</span><span class="sxs-lookup"><span data-stu-id="bb2fc-138">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="bb2fc-139">rechace FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="bb2fc-139">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="bb2fc-140">rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="bb2fc-140">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="bb2fc-141">rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-141">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="bb2fc-142">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-142">(opt) UINT registerSpace = 0</span></span>

</dd> <dt>

<span data-ttu-id="bb2fc-143">**Init en línea (UINT shaderRegister, filtro de filtro de D3D12 \_ = D3D12 \_ filtro \_ anisotrópico, D3D12 \_ modo de dirección de textura \_ \_ addressU = D3D12 \_ ajuste del \_ \_ modo de dirección de textura \_ , D3D12 \_ modo de dirección de textura \_ \_ addressV = D3D12 \_ ajuste del \_ \_ modo de dirección de textura \_ , D3D12 \_ \_ \_ modo de dirección de textura addressW = D3D12 \_ \_ \_ \_ de modo de dirección de textura Wrap, Float mipLODBias = 0, uint maxAnisotropy = 16, D3D12 \_ COMparison \_ FUNC comparisonFunc = D3D12 \_ Comparison la \_ \_ función de comparación menos \_ igual, D3D12 el \_ \_ \_ color del borde estático BorderColor = D3D12 el \_ \_ \_ color del borde estático de la \_ \_ \_ visibilidad del sombreador minLOD = \_ \_ \_ maxLOD Visibility del \_ sombreador \_ \_ All, uint D3D12 = 0)**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-143">**inline Init(UINT shaderRegister, D3D12\_FILTER filter = D3D12\_FILTER\_ANISOTROPIC, D3D12\_TEXTURE\_ADDRESS\_MODE addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, D3D12\_TEXTURE\_ADDRESS\_MODE addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12\_COMPARISON\_FUNC comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL, D3D12\_STATIC\_BORDER\_COLOR borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12\_FLOAT32\_MAX, D3D12\_SHADER\_VISIBILITY shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL, UINT registerSpace = 0)**</span></span>
</dt> <dd>

<span data-ttu-id="bb2fc-144">Especifica una función que inicializa los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="bb2fc-144">Specifies a function that initializes the following parameters:</span></span>

<span data-ttu-id="bb2fc-145">UINT shaderRegister</span><span class="sxs-lookup"><span data-stu-id="bb2fc-145">UINT shaderRegister</span></span>

<span data-ttu-id="bb2fc-146">rechace [**D3D12 \_ Filtro filtro =**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) D3D12 \_ filtro \_ anisotrópico</span><span class="sxs-lookup"><span data-stu-id="bb2fc-146">(opt) [**D3D12\_FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12\_FILTER\_ANISOTROPIC</span></span>

<span data-ttu-id="bb2fc-147">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-147">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-148">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-148">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-149">rechace [**D3D12 \_ \_ \_ Modo de dirección de textura**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = \_ \_ \_ ajuste del modo de dirección de textura D3D12 \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-149">(opt) [**D3D12\_TEXTURE\_ADDRESS\_MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12\_TEXTURE\_ADDRESS\_MODE\_WRAP</span></span>

<span data-ttu-id="bb2fc-150">rechace FLOAT mipLODBias = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-150">(opt) FLOAT mipLODBias = 0</span></span>

<span data-ttu-id="bb2fc-151">rechace UINT maxAnisotropy = 16</span><span class="sxs-lookup"><span data-stu-id="bb2fc-151">(opt) UINT maxAnisotropy = 16</span></span>

<span data-ttu-id="bb2fc-152">rechace [**D3D12 \_ Comparison \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = función de comparación de D3D12 \_ \_ \_ menos \_ igual</span><span class="sxs-lookup"><span data-stu-id="bb2fc-152">(opt) [**D3D12\_COMPARISON\_FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonFunc = D3D12\_COMPARISON\_FUNC\_LESS\_EQUAL</span></span>

<span data-ttu-id="bb2fc-153">rechace [**D3D12 \_ \_ \_ Color de borde estático**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = \_ D3D12 \_ borde \_ estático \_ color \_ blanco opaco</span><span class="sxs-lookup"><span data-stu-id="bb2fc-153">(opt) [**D3D12\_STATIC\_BORDER\_COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12\_STATIC\_BORDER\_COLOR\_OPAQUE\_WHITE</span></span>

<span data-ttu-id="bb2fc-154">rechace FLOAT minLOD = 0. f</span><span class="sxs-lookup"><span data-stu-id="bb2fc-154">(opt) FLOAT minLOD = 0.f</span></span>

<span data-ttu-id="bb2fc-155">rechace FLOAT maxLOD = D3D12 \_ FLOAT32 \_ Max</span><span class="sxs-lookup"><span data-stu-id="bb2fc-155">(opt) FLOAT maxLOD = D3D12\_FLOAT32\_MAX</span></span>

<span data-ttu-id="bb2fc-156">rechace [**D3D12 \_ \_Visibilidad del sombreador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) SHADERVISIBILITY = D3D12 visibilidad del \_ sombreador \_ \_</span><span class="sxs-lookup"><span data-stu-id="bb2fc-156">(opt) [**D3D12\_SHADER\_VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12\_SHADER\_VISIBILITY\_ALL</span></span>

<span data-ttu-id="bb2fc-157">rechace UINT registerSpace = 0</span><span class="sxs-lookup"><span data-stu-id="bb2fc-157">(opt) UINT registerSpace = 0</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb2fc-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb2fc-158">Requirements</span></span>



| <span data-ttu-id="bb2fc-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb2fc-159">Requirement</span></span> | <span data-ttu-id="bb2fc-160">Value</span><span class="sxs-lookup"><span data-stu-id="bb2fc-160">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="bb2fc-161">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bb2fc-161">Header</span></span><br/> | <dl> <span data-ttu-id="bb2fc-162"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb2fc-162"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb2fc-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb2fc-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb2fc-164">**\_Descripción de \_ muestra \_ estática de D3D12**</span><span class="sxs-lookup"><span data-stu-id="bb2fc-164">**D3D12\_STATIC\_SAMPLER\_DESC**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[<span data-ttu-id="bb2fc-165">Estructuras auxiliares de D3D12</span><span class="sxs-lookup"><span data-stu-id="bb2fc-165">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





